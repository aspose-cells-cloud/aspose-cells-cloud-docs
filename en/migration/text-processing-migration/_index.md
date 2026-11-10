---
title: "Migrating Text Processing to 4.0"
second_title: "Document"
ArticleTitle: "Migrating Text Processing APIs from 3.0 to 4.0: Why and How"
linktitle: "Text Processing Migration"
type: docs
weight: 100
keywords: "Aspose.Cells Cloud, Excel API, migration, spreadsheet conversion, merge Excel, split Excel, protect Excel, cloud spreadsheet SDK, REST API, Excel processing"
description: "How 8 flat 3.0 text endpoints become 16 hierarchical 4.0 routes, adding remote file support, position-based removal and in-cell duplicate removal — with the full mapping."
url: /cells/migrating-text-processing/
---

## Introduction

Aspose.Cells Cloud 4.0 introduces a **completely redesigned Text Processing API** that replaces the 8 endpoints from version 3.0 with 16 more powerful, flexible endpoints. The new API not only preserves all existing text manipulation capabilities but also adds **remote file support**, **position-based character removal**, and **duplicate substring removal** — all while using a cleaner, more consistent URL structure.

In this guide, we'll walk through every 3.0 text processing endpoint, show you its 4.0 replacement, and explain **why migrating is worth your time**.

---

## What's Changed at a Glance

| Aspect | 3.0 | 4.0 |
|--------|-----|-----|
| **Total Endpoints** | 8 | 16 |
| **HTTP Method** | POST | PUT |
| **Remote File Support** | ❌ No | ✅ Yes (per-endpoint) |
| **Position-Based Removal** | ❌ No | ✅ Yes |
| **Duplicate Substring Removal** | ❌ No | ✅ Yes |
| **Range-Level Targeting** | ❌ No | ✅ Yes (via `{range}` parameter) |
| **Worksheet-Level Targeting** | ❌ No | ✅ Yes (via `{worksheet}` parameter) |
| **Base Path** | `/v3.0/cells` | `/v4.0/cells` |

---

## Endpoint Mapping: 3.0 → 4.0

### Complete Mapping Table

| # | 3.0 Endpoint | 4.0 Endpoint | Change |
|---|-------------|-------------|--------|
| 1 | `POST /cells/addtext` | `PUT /cells/content/add/text` | Path restructured |
| 2 | `POST /cells/trimcontent` | `PUT /cells/content/trim` | Path restructured |
| 3 | `POST /cells/updatewordcase` | `PUT /cells/content/wordcase` | Path restructured |
| 4 | `POST /cells/removecharacters` | `PUT /cells/content/remove/characters` | Path restructured |
| 5 | `POST /cells/converttext` | `PUT /cells/content/convert/text` | Path restructured |
| 6 | `POST /cells/removeduplicates` | `PUT /cells/content/remove/duplicate-substrings` | Renamed + enhanced |
| 7 | `POST /cells/extracttext` | `PUT /cells/content/extract/text` | Path restructured |
| 8 | `POST /cells/splittext` | `PUT /cells/content/split/text` | Path restructured |

### 4.0 Exclusive New Endpoints

| Endpoint | Description |
|----------|-------------|
| `PUT /cells/content/remove/characters-by-position` | Remove characters by position (first N, last N, before/after text) |
| `PUT /cells/{name}/worksheets/{worksheet}/range/{range}/content/*` | All 8 operations available at worksheet+range level for remote files |

---

## Why Migrate to 4.0?

### 1. 🎯 Remote File Support — No More Download-Process-Upload

In 3.0, every text processing operation required you to **upload the file first**, process it, then download the result. In 4.0, each text processing endpoint has a **remote file variant** that operates directly on files stored in your cloud storage.

**3.0 workflow (5 steps):**
```
1. Download file from storage
2. Upload file to API
3. Process text
4. Download result
5. Upload result back to storage
```

**4.0 workflow (1 step):**
```
1. PUT /cells/{name}/worksheets/{worksheet}/range/{range}/content/trim
   → Operates directly on the remote file
```

**Impact:** Reduces network round-trips by up to 80% and eliminates temporary file management.

### 2. 📍 Granular Targeting — Worksheet + Range Level

4.0 allows you to target text operations at three levels:
- **Workbook level** — Process all worksheets
- **Worksheet level** — Process a specific worksheet
- **Range level** — Process only a specific cell range (e.g., `A1:D100`)

```bash
# Workbook level — trim all cells in all worksheets
PUT /v4.0/cells/content/trim

# Worksheet level — trim only Sheet1
PUT /v4.0/cells/content/trim?worksheet=Sheet1

# Range level — trim only A1:D100 in Sheet1 of a remote file
PUT /v4.0/cells/myfile.xlsx/worksheets/Sheet1/range/A1:D100/content/trim
```

**3.0 limitation:** Could only process the entire workbook. No way to target specific worksheets or ranges.

### 3. 🔢 Position-Based Character Removal

4.0 adds a powerful new endpoint for removing characters by position:

```bash
# Remove first 3 characters from all cells
PUT /v4.0/cells/content/remove/characters-by-position?theFirstNCharacters=3

# Remove last 5 characters
PUT /v4.0/cells/content/remove/characters-by-position?theLastNCharacters=5

# Remove everything before a specific text marker
PUT /v4.0/cells/content/remove/characters-by-position?allCharactersBeforeText=ID:

# Remove everything after a specific text marker
PUT /v4.0/cells/content/remove/characters-by-position?allCharactersAfterText=END
```

This is ideal for cleaning up imported data with fixed-width fields, log files, or data with known prefixes/suffixes.

### 4. 🧹 Duplicate Substring Removal Within Cells

3.0's `removeduplicates` endpoint operated on **rows** (removing duplicate rows). 4.0's `remove/duplicate-substrings` operates **within each cell**, removing repeated substrings:

```bash
# Remove duplicate words separated by spaces
PUT /v4.0/cells/content/remove/duplicate-substrings?delimiters=

# Remove duplicate values separated by commas, treating consecutive delimiters as one
PUT /v4.0/cells/content/remove/duplicate-substrings?delimiters=,&treatConsecutiveDelimitersAsOne=true
```

**Use case:** Cleaning up tag lists like `"red,blue,red,green,blue"` → `"red,blue,green"`.

### 5. 🔧 Consistent URL Structure

4.0 uses a **hierarchical, RESTful URL structure** that makes the API self-documenting:

```
/v4.0/cells/content/{operation}/{sub-operation}
```

Compare with 3.0's flat structure:
```
/v3.0/cells/{operationName}
```

The 4.0 structure:
- Groups related operations under `/content/`
- Uses nouns, not verbs (`/trim` instead of `/trimcontent`)
- Makes it easy to discover related endpoints

---

## Migration Examples

### Example 1: Trim Whitespace

**3.0:**
```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/trimcontent" \
  -H "Authorization: Bearer TOKEN" \
  -F "file=@data.xlsx" \
  -d "trimContent= "
```

**4.0 (local file):**
```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/content/trim?trimContent= " \
  -H "Authorization: Bearer TOKEN" \
  -F "file=@data.xlsx"
```

**4.0 (remote file — no upload needed!):**
```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/data.xlsx/worksheets/Sheet1/range/A1:Z1000/content/trim?trimContent= " \
  -H "Authorization: Bearer TOKEN"
```

### Example 2: Change Text Case

**3.0:**
```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/updatewordcase" \
  -H "Authorization: Bearer TOKEN" \
  -F "file=@data.xlsx" \
  -d "wordCaseType=UpperCase"
```

**4.0:**
```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/content/wordcase?wordCaseType=UpperCase" \
  -H "Authorization: Bearer TOKEN" \
  -F "file=@data.xlsx"
```

Available `wordCaseType` values: `UpperCase`, `LowerCase`, `ProperCase`, `SentenceCase`.

### Example 3: Remove Characters

**3.0:**
```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/removecharacters" \
  -H "Authorization: Bearer TOKEN" \
  -F "file=@data.xlsx" \
  -d "removeTextMethod=CustomChars&removeCustomValue=@#$"
```

**4.0:**
```bash
# By custom characters
curl -X PUT "https://api.aspose.cloud/v4.0/cells/content/remove/characters?removeTextMethod=CustomChars&removeCustomValue=@#$" \
  -H "Authorization: Bearer TOKEN" \
  -F "file=@data.xlsx"

# By character set (NEW in 4.0!)
curl -X PUT "https://api.aspose.cloud/v4.0/cells/content/remove/characters?removeTextMethod=CharacterSet&characterSets=NonPrintingCharacters" \
  -H "Authorization: Bearer TOKEN" \
  -F "file=@data.xlsx"

# By position (NEW in 4.0!)
curl -X PUT "https://api.aspose.cloud/v4.0/cells/content/remove/characters-by-position?theFirstNCharacters=3" \
  -H "Authorization: Bearer TOKEN" \
  -F "file=@data.xlsx"
```

### Example 4: Extract Text

**3.0:**
```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/extracttext" \
  -H "Authorization: Bearer TOKEN" \
  -F "file=@data.xlsx" \
  -d "extractTextType=BeforeText&beforeText=@&outPositionRange=0"
```

**4.0:**
```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/content/extract/text?extractTextType=BeforeText&beforeText=@&outPositionRange=0" \
  -H "Authorization: Bearer TOKEN" \
  -F "file=@data.xlsx"
```

---

## C# SDK Migration

### 3.0 SDK
```csharp
var cellsApi = new CellsApi(clientId, clientSecret);
using var stream = File.OpenRead("data.xlsx");
var response = await cellsApi.TrimContent(stream, " ");
```

### 4.0 SDK
```csharp
var cellsApi = new CellsApi(clientId, clientSecret);

// Local file
using var stream = File.OpenRead("data.xlsx");
var response = await cellsApi.TrimCharacter(stream, trimContent: ' ');

// Remote file (NEW!)
var response = await cellsApi.TrimCharacterInRemoteSpreadsheet(
    name: "data.xlsx",
    worksheet: "Sheet1",
    range: "A1:Z1000",
    trimContent: ' ');
```

---

## Python SDK Migration

### 3.0 SDK
```python
cells_api = CellsApi(client_id, client_secret)
with open("data.xlsx", "rb") as f:
    response = cells_api.trim_content(f, trim_content=" ")
```

### 4.0 SDK
```python
cells_api = CellsApi(client_id, client_secret)

# Local file
with open("data.xlsx", "rb") as f:
    response = cells_api.trim_character(f, trim_content=" ")

# Remote file (NEW!)
response = cells_api.trim_character_in_remote_spreadsheet(
    name="data.xlsx",
    worksheet="Sheet1",
    range="A1:Z1000",
    trim_content=" "
)
```

---

## Migration Checklist

| Step | Action | Risk |
|------|--------|------|
| 1 | Update base URL from `v3.0` to `v4.0` | 🟢 Low |
| 2 | Change HTTP method from `POST` to `PUT` | 🟢 Low |
| 3 | Update endpoint paths (see mapping table) | 🟢 Low |
| 4 | Test each text processing operation | 🟡 Medium |
| 5 | Enable remote file mode where applicable | 🟢 Low |
| 6 | Take advantage of new range-level targeting | 🟢 Low |
| 7 | Try new position-based removal for cleanup tasks | 🟢 Low |

---

## Summary: Why Migrate?

| Benefit | Impact |
|---------|--------|
| **Remote file support** | Eliminates 4 network round-trips per operation |
| **Range-level targeting** | Process only what you need, faster results |
| **Position-based removal** | Handle fixed-width and prefixed data without custom code |
| **Duplicate substring removal** | Clean up tag lists, CSV values within cells |
| **Cleaner API structure** | Self-documenting URLs, easier to discover features |
| **Same core functionality** | All 8 original operations preserved, just better |

**Bottom line:** The 4.0 Text Processing API is a superset of 3.0. Every operation you could do in 3.0, you can do in 4.0 — plus remote file support, granular targeting, and two brand-new operations. The migration is straightforward: update the URL, change POST to PUT, and you're done.
