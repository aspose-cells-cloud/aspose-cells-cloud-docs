---
title: "Migrating Data Processing to 4.0"
second_title: "Document"
ArticleTitle: "Migrating Data Processing APIs from 3.0 to 4.0: Why and How"
linktitle: "Data Processing Migration"
type: docs
weight: 100
keywords: "Aspose.Cells Cloud, Excel API, migration, spreadsheet conversion, merge Excel, split Excel, protect Excel, cloud spreadsheet SDK, REST API, Excel processing"
description: "How 13 Data Processing endpoints consolidate into 10 focused 4.0 endpoints, adding table-level split, remote folder merge and CSV import — with the full mapping and SDK examples."
url: /cells/migrating-data-processing/
type: docs
---
## Introduction

Aspose.Cells Cloud 4.0 reimagines the Data Processing API with a **cleaner architecture, remote file support, and new merge/split capabilities**. The 13 endpoints from version 3.0 are consolidated into 10 more focused endpoints that eliminate redundancy and add powerful new features like **table-level splitting** and **CSV data import**.

This guide provides a complete migration map, explains every improvement, and shows you exactly how to move your data processing workflows to 4.0.

---

## What's Changed at a Glance

| Aspect | 3.0 | 4.0 |
|--------|-----|-----|
| **Total Endpoints** | 13 | 10 |
| **HTTP Method** | POST | PUT |
| **Merge Operations** | 1 | 3 (local, remote folder, remote single) |
| **Split Operations** | 1 | 3 (workbook, table, remote workbook) |
| **Import Formats** | JSON, XML, generic data | JSON, XML, CSV, generic data |
| **Table-Level Split** | ❌ No | ✅ Yes |
| **Remote Folder Merge** | ❌ No | ✅ Yes (pattern matching) |
| **CSV Import** | ❌ No | ✅ Yes |
| **Base Path** | `/v3.0/cells` | `/v4.0/cells` |

---

## Endpoint Mapping: 3.0 → 4.0

### ✅ Directly Mappable Endpoints

| # | 3.0 Endpoint | 4.0 Endpoint | Change |
|---|-------------|-------------|--------|
| 1 | `POST /cells/{name}/importjson` | `PUT /cells/import/data/json` | Path restructured |
| 2 | `POST /cells/{name}/importxml` | `PUT /cells/import/data/xml` | Path restructured |
| 3 | `POST /cells/{name}/importdata` | `PUT /cells/import/data` | Path restructured |
| 4 | `POST /cells/{name}/datadeduplication` | `PUT /cells/remove/duplicates` | Moved to Transform controller |
| 5 | `POST /cells/datadeduplication` | `PUT /cells/remove/duplicates` | Moved to Transform controller |
| 6 | `POST /cells/{name}/datacleansing` | `PUT /cells/remove/duplicates` | Functionality merged |
| 7 | `POST /cells/datacleansing` | `PUT /cells/remove/duplicates` | Functionality merged |
| 8 | `POST /cells/deleteincompleterows` | `PUT /cells/remove/blank-rows` | Moved to Transform controller |

### ❌ Not Directly Mappable

| # | 3.0 Endpoint | 4.0 Status | Workaround |
|---|-------------|-----------|------------|
| 9 | `POST /cells/export` | ❌ No direct equivalent | Use Conversion API endpoints |
| 10 | `POST /cells/{name}/exportxml` | ❌ No direct equivalent | Use `GET /cells/{name}?format=xml` |
| 11 | `POST /cells/{name}/datafill` | ❌ Not supported | Implement custom logic using import + calculate |
| 12 | `POST /cells/datafill` | ❌ Not supported | Implement custom logic using import + calculate |
| 13 | `POST /cells/datatransformation` | ❌ Not supported | Use Transform API endpoints组合 |

### 🆕 4.0 Exclusive New Endpoints

| Endpoint | Description |
|----------|-------------|
| `PUT /cells/merge/spreadsheet` | Merge multiple local spreadsheets |
| `PUT /cells/merge/remote-spreadsheets` | Merge spreadsheets from remote folder (pattern matching) |
| `PUT /cells/{name}/merge/spreadsheet` | Merge one remote spreadsheet into another |
| `PUT /cells/split/spreadsheet` | Split spreadsheet by row range |
| `PUT /cells/split/table` | Split table by column value |
| `PUT /cells/{name}/split/spreadsheet` | Split remote spreadsheet by row range |
| `PUT /cells/import/data/csv` | Import CSV data into spreadsheet |

---

## Why Migrate to 4.0?

### 1. 🔀 Three-Level Merge Operations

3.0 had **no merge API** at all. 4.0 provides three distinct merge modes:

```bash
# Mode 1: Merge multiple local files into one
PUT /v4.0/cells/merge/spreadsheet?outFormat=xlsx&mergeInOneSheet=false
  -F "file1=@sheet1.xlsx"
  -F "file2=@sheet2.xlsx"
  -F "file3=@sheet3.xlsx"

# Mode 2: Merge all files matching a pattern in a remote folder
PUT /v4.0/cells/merge/remote-spreadsheets?folder=/reports&fileMatchExpression=Q[1-4]_*.xlsx&outFormat=xlsx

# Mode 3: Merge one remote file into another
PUT /v4.0/cells/report.xlsx/merge/spreadsheet?mergedSpreadsheet=appendix.xlsx&outFormat=xlsx
```

**Use cases:**
- Consolidating quarterly reports into annual summary
- Merging regional data files into master workbook
- Appending supplementary data to existing reports

### 2. 📊 Table-Level Splitting (NEW!)

3.0 could only split workbooks by sheets. 4.0 adds **table-level splitting** by column values:

```bash
# Split a table by the "Region" column
PUT /v4.0/cells/split/table?worksheet=Data&tableName=SalesTable&splitColumnName=Region&saveSplitColumn=true&toNewWorkbook=true
  -F "file=@sales.xlsx"
```

**Result:** One file per unique region value — `Sales_North.xlsx`, `Sales_South.xlsx`, etc.

**3.0 limitation:** Had to export entire workbook, then manually filter rows per region in client code.

### 3. 📁 Remote Folder Merge with Pattern Matching

This is a game-changer for batch operations:

```bash
# Merge all Q1-Q4 report files in the /reports folder
PUT /v4.0/cells/merge/remote-spreadsheets?folder=/reports&fileMatchExpression=Report_2024_Q[1-4].xlsx
```

No need to list and download files individually. The API handles everything server-side.

### 4. 📥 CSV Data Import

3.0 had no dedicated CSV import. 4.0 adds a specialized endpoint:

```bash
# Import CSV into Sheet1 starting at cell A1
PUT /v4.0/cells/import/data/csv?worksheet=Sheet1&startcell=A1&insert=true&convertNumericData=true&splitter=,
  -F "file=@data.csv"
```

**Features:**
- Auto-detect numeric data and convert appropriately
- Configurable delimiter (`splitter` parameter)
- Option to insert rows vs. overwrite

---

## Migration Examples

### Example 1: Import JSON Data

**3.0:**
```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/report.xlsx/importjson" \
  -H "Authorization: Bearer TOKEN" \
  -F "file=@data.json" \
  -d "worksheet=Sheet1&startCell=A1&insert=true"
```

**4.0:**
```bash
# Local file
curl -X PUT "https://api.aspose.cloud/v4.0/cells/import/data/json?worksheet=Sheet1&startcell=A1&insert=true" \
  -H "Authorization: Bearer TOKEN" \
  -F "file=@data.json"

# Remote file (NEW!)
curl -X PUT "https://api.aspose.cloud/v4.0/cells/report.xlsx/import/data/json?worksheet=Sheet1&startcell=A1&insert=true" \
  -H "Authorization: Bearer TOKEN" \
  -F "file=@data.json"
```

### Example 2: Import CSV Data (NEW in 4.0)

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/import/data/csv?worksheet=Sheet1&startcell=A1&convertNumericData=true&splitter=," \
  -H "Authorization: Bearer TOKEN" \
  -F "file=@data.csv"
```

### Example 3: Merge Multiple Files

**3.0:** ❌ Not possible — had to write custom code.

**4.0:**
```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/merge/spreadsheet?outFormat=xlsx&mergeInOneSheet=false" \
  -H "Authorization: Bearer TOKEN" \
  -F "file=@Q1.xlsx" \
  -F "file=@Q2.xlsx" \
  -F "file=@Q3.xlsx" \
  --output AnnualReport.xlsx
```

### Example 4: Split Table by Column Value (NEW!)

**3.0:** ❌ Not possible — had to export, filter manually, re-import.

**4.0:**
```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/split/table?worksheet=Data&tableName=SalesTable&splitColumnName=Region&saveSplitColumn=true&toMultipleFiles=true" \
  -H "Authorization: Bearer TOKEN" \
  -F "file=@sales.xlsx" \
  --output splits.zip
```

---

## C# SDK Migration

### 3.0 SDK
```csharp
var cellsApi = new CellsApi(clientId, clientSecret);

// Import JSON
using var jsonStream = File.OpenRead("data.json");
await cellsApi.PostWorkbookImportJson("report.xlsx", jsonStream, "Sheet1", "A1");
```

### 4.0 SDK
```csharp
var cellsApi = new CellsApi(clientId, clientSecret);

// Import JSON
using var jsonStream = File.OpenRead("data.json");
await cellsApi.ImportJsonDataIntoSpreadsheet(jsonStream, "Sheet1", "A1");

// Import CSV (NEW!)
using var csvStream = File.OpenRead("data.csv");
await cellsApi.ImportCsvDataIntoSpreadsheet(csvStream, "Sheet1", "A1", convertNumericData: true, splitter: ",");

// Merge files (NEW!)
var streams = new Dictionary<string, Stream>
{
    { "Q1.xlsx", File.OpenRead("Q1.xlsx") },
    { "Q2.xlsx", File.OpenRead("Q2.xlsx") }
};
await cellsApi.MergeSpreadsheets(streams, outFormat: "xlsx");

// Split table (NEW!)
using var workbook = File.OpenRead("sales.xlsx");
await cellsApi.SplitTable(workbook, "Data", "SalesTable", "Region", saveSplitColumn: true);
```

---

## Python SDK Migration

### 3.0 SDK
```python
cells_api = CellsApi(client_id, client_secret)

# Import JSON
with open("data.json", "rb") as f:
    cells_api.post_workbook_import_json("report.xlsx", f, "Sheet1", "A1")
```

### 4.0 SDK
```python
cells_api = CellsApi(client_id, client_secret)

# Import JSON
with open("data.json", "rb") as f:
    cells_api.import_json_data_into_spreadsheet(f, "Sheet1", "A1")

# Import CSV (NEW!)
with open("data.csv", "rb") as f:
    cells_api.import_csv_data_into_spreadsheet(f, "Sheet1", "A1", convert_numeric_data=True, splitter=",")

# Merge files (NEW!)
with open("Q1.xlsx", "rb") as f1, open("Q2.xlsx", "rb") as f2:
    files = {"Q1.xlsx": f1, "Q2.xlsx": f2}
    cells_api.merge_spreadsheets(files, out_format="xlsx")

# Split table (NEW!)
with open("sales.xlsx", "rb") as f:
    cells_api.split_table(f, "Data", "SalesTable", "Region", save_split_column=True)
```

---

## Summary: Migration Decision Matrix

| Scenario | Migrate to 4.0? | Reason |
|----------|----------------|--------|
| JSON/XML import | ✅ **Yes** | Direct mapping, cleaner URLs |
| Generic data import | ✅ **Yes** | Direct mapping |
| CSV import | ✅ **Yes, eagerly** | 4.0 exclusive — new feature |
| Data deduplication | ✅ **Yes** | Moved to Transform controller |
| Delete incomplete rows | ✅ **Yes** | Moved to Transform controller |
| Merge spreadsheets | ✅ **Yes, eagerly** | 4.0 exclusive — impossible in 3.0 |
| Split by column value | ✅ **Yes, eagerly** | 4.0 exclusive — table-level split |
| Export data | ⚠️ **Use Conversion API** | Redirect to Conversion endpoints |
| Data fill | ❌ **No** | Not in 4.0 — custom logic needed |
| Data transformation | ❌ **No** | Not in 4.0 — use Transform API组合 |

