---
title: "Migrating Search & Replace to 4.0"
second_title: "Document"
ArticleTitle: "Migrating Search & Replace APIs from 3.0 to 4.0: Why and How"
linktitle: "Search & Replace Migration"
type: docs
weight: 100
keywords: "Aspose.Cells Cloud, Excel API, migration, spreadsheet conversion, merge Excel, split Excel, protect Excel, cloud spreadsheet SDK, REST API, Excel processing"
description: "How 4 basic 3.0 search and replace endpoints expand into 14 in 4.0, adding worksheet and range scope, broken-link detection and remote file support."
url: /cells/migrating-search-and-replace/
---

## Introduction

Aspose.Cells Cloud 4.0 transforms the search and replace capabilities from 4 basic endpoints in version 3.0 into a **comprehensive 14-endpoint search system**. The new API introduces **worksheet-level search**, **cell-range-scoped search**, **broken link detection**, and **full remote file support** — turning a simple find-and-replace tool into a powerful spreadsheet auditing engine.

This guide maps every 3.0 search endpoint to its 4.0 replacement and demonstrates why the upgrade delivers dramatically more value.

---

## What's Changed at a Glance

| Aspect | 3.0 | 4.0 |
|--------|-----|-----|
| **Total Endpoints** | 4 | 14 |
| **HTTP Method** | POST | PUT |
| **Search Scope** | Workbook only | Workbook / Worksheet / Range |
| **Broken Link Detection** | ❌ No | ✅ Yes (4 endpoints) |
| **Remote File Support** | ❌ No | ✅ Yes (per-endpoint) |
| **All Text Items Search** | ❌ No | ✅ Yes |
| **Range-Scoped Replace** | ❌ No | ✅ Yes |
| **Base Path** | `/v3.0/cells` | `/v4.0/cells` |

---

## Endpoint Mapping: 3.0 → 4.0

### Complete Mapping Table

| # | 3.0 Endpoint | 4.0 Endpoint | Change |
|---|-------------|-------------|--------|
| 1 | `POST /cells/{name}/findText` | `PUT /cells/{name}/search/content` | Renamed + enhanced |
| 2 | `POST /cells/{name}/replaceText` | `PUT /cells/{name}/replace/content` | Renamed + enhanced |
| 3 | `POST /cells/{name}/worksheets/{sheetName}/findText` | `PUT /cells/{name}/worksheets/{worksheet}/search/content` | Path adjusted |
| 4 | `POST /cells/{name}/worksheets/{sheetName}/replaceText` | `PUT /cells/{name}/worksheets/{worksheet}/replace/content` | Path adjusted |

### 4.0 Exclusive New Endpoints

| Endpoint | Description |
|----------|-------------|
| `PUT /cells/search/content` | Search local spreadsheet content |
| `PUT /cells/replace/content` | Replace local spreadsheet content |
| `PUT /cells/search/content/all-textitems` | Search all text items in local spreadsheet |
| `PUT /cells/{name}/search/content/all-textitems` | Search all text items in remote spreadsheet |
| `PUT /cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/search/content` | Search within a specific cell range |
| `PUT /cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/replace/content` | Replace within a specific cell range |
| `PUT /cells/search/broken-links` | Find broken hyperlinks in local spreadsheet |
| `PUT /cells/{name}/search/broken-links` | Find broken hyperlinks in remote spreadsheet |
| `PUT /cells/{name}/worksheets/{worksheet}/search/broken-links` | Find broken links in specific worksheet |
| `PUT /cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/search/broken-links` | Find broken links in specific range |

---

## Why Migrate to 4.0?

### 1. 🔍 Three-Level Search Granularity

3.0 offered only two search levels: whole workbook or one worksheet. 4.0 adds a third level — **cell range** — letting you search precisely where it matters.

```bash
# Level 1: Entire workbook (local file)
PUT /v4.0/cells/search/content?searchText=revenue

# Level 2: Single worksheet (remote file)
PUT /v4.0/cells/report.xlsx/worksheets/Q1/search/content?searchText=revenue

# Level 3: Specific cell range (remote file)
PUT /v4.0/cells/report.xlsx/worksheets/Q1/ranges/A1:D50/search/content?searchText=revenue
```

**Use case:** In a 50-sheet workbook with 100K cells, narrowing your search to `A1:D50` in one sheet reduces processing time by over 95%.

### 2. 🔗 Broken Link Detection — 3.0 Had Nothing

One of the most requested features in spreadsheet management is finding **broken hyperlinks**. 3.0 had zero support for this. 4.0 provides **4 dedicated endpoints**:

```bash
# Find all broken links in a local file
PUT /v4.0/cells/search/broken-links \
  -F "file=@workbook.xlsx"

# Find broken links in a remote file
PUT /v4.0/cells/report.xlsx/search/broken-links

# Find broken links in a specific worksheet
PUT /v4.0/cells/report.xlsx/worksheets/Sheet1/search/broken-links

# Find broken links in a specific range
PUT /v4.0/cells/report.xlsx/worksheets/Sheet1/ranges/A1:Z100/search/broken-links
```

**Response example:**
```json
{
  "Code": 200,
  "Status": "OK",
  "BrokenLinks": [
    {
      "Worksheet": "Sheet1",
      "Cell": "B15",
      "Address": "https://old-server.com/report/2024",
      "Type": "ExternalHyperlink"
    },
    {
      "Worksheet": "Sheet1",
      "Cell": "D22",
      "Address": "../shared/data.xlsx",
      "Type": "ExternalHyperlink"
    }
  ]
}
```

**Impact:** Eliminates hours of manual link auditing. Critical for compliance, data integrity, and migration projects.

### 3. 📋 All Text Items Search

4.0 introduces a dedicated endpoint to retrieve **every text item** in a spreadsheet at once — much more efficient than searching for specific strings when you need a full inventory.

```bash
# Get all text items from a local file
PUT /v4.0/cells/search/content/all-textitems \
  -F "file=@workbook.xlsx"

# Get all text items from a remote file
PUT /v4.0/cells/report.xlsx/search/content/all-textitems
```

**Use cases:**
- Full-text indexing for search engines
- Content audit before migration
- Extracting all unique strings for translation
- Building a spreadsheet's text inventory

### 4. 📍 Range-Scoped Replace

3.0 could only replace text across an entire workbook or worksheet. 4.0 lets you **target a specific cell range**:

```bash
# Replace in entire workbook
PUT /v4.0/cells/replace/content?searchText=2024&replaceText=2025 \
  -F "file=@report.xlsx"

# Replace in a specific range
PUT /v4.0/cells/report.xlsx/worksheets/Q1/ranges/A1:D50/replace/content?searchText=2024&replaceText=2025
```

**Impact:** Prevents accidental replacements in cells outside your target area. Essential for templates and shared workbooks.

### 5. 🌐 Remote File Support — Every Endpoint

Every search and replace endpoint in 4.0 has a **remote file variant** that operates directly on files in your cloud storage:

| Operation | Local File | Remote File |
|-----------|-----------|-------------|
| Search content | `PUT /cells/search/content` | `PUT /cells/{name}/search/content` |
| Replace content | `PUT /cells/replace/content` | `PUT /cells/{name}/replace/content` |
| All text items | `PUT /cells/search/content/all-textitems` | `PUT /cells/{name}/search/content/all-textitems` |
| Broken links | `PUT /cells/search/broken-links` | `PUT /cells/{name}/search/broken-links` |

**3.0 limitation:** All search/replace operations required uploading the file first. No remote file support at all.

---

## Migration Examples

### Example 1: Search Text

**3.0:**
```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/report.xlsx/findText" \
  -H "Authorization: Bearer TOKEN" \
  -d "searchText=revenue"
```

**4.0:**
```bash
# Search entire remote workbook
curl -X PUT "https://api.aspose.cloud/v4.0/cells/report.xlsx/search/content?searchText=revenue" \
  -H "Authorization: Bearer TOKEN"

# Search specific worksheet
curl -X PUT "https://api.aspose.cloud/v4.0/cells/report.xlsx/worksheets/Q1/search/content?searchText=revenue" \
  -H "Authorization: Bearer TOKEN"

# Search specific range
curl -X PUT "https://api.aspose.cloud/v4.0/cells/report.xlsx/worksheets/Q1/ranges/A1:D50/search/content?searchText=revenue" \
  -H "Authorization: Bearer TOKEN"
```

### Example 2: Replace Text

**3.0:**
```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/report.xlsx/replaceText" \
  -H "Authorization: Bearer TOKEN" \
  -d "searchText=2024&replaceText=2025"
```

**4.0:**
```bash
# Replace in entire workbook
curl -X PUT "https://api.aspose.cloud/v4.0/cells/report.xlsx/replace/content?searchText=2024&replaceText=2025" \
  -H "Authorization: Bearer TOKEN"

# Replace in specific range only
curl -X PUT "https://api.aspose.cloud/v4.0/cells/report.xlsx/worksheets/Q1/ranges/A1:D50/replace/content?searchText=2024&replaceText=2025" \
  -H "Authorization: Bearer TOKEN"
```

### Example 3: Find Broken Links (NEW — No 3.0 Equivalent)

```bash
# Scan entire workbook for broken links
curl -X PUT "https://api.aspose.cloud/v4.0/cells/report.xlsx/search/broken-links" \
  -H "Authorization: Bearer TOKEN"

# Scan specific worksheet
curl -X PUT "https://api.aspose.cloud/v4.0/cells/report.xlsx/worksheets/References/search/broken-links" \
  -H "Authorization: Bearer TOKEN"
```

### Example 4: Get All Text Items (NEW — No 3.0 Equivalent)

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/report.xlsx/search/content/all-textitems" \
  -H "Authorization: Bearer TOKEN"
```

---

## C# SDK Migration

### 3.0 SDK
```csharp
var cellsApi = new CellsApi(clientId, clientSecret);

// Search
var results = await cellsApi.PostWorkbooksTextSearch("report.xlsx", "revenue");

// Replace
var response = await cellsApi.PostWorkbookTextReplace("report.xlsx", "2024", "2025");
```

### 4.0 SDK
```csharp
var cellsApi = new CellsApi(clientId, clientSecret);

// Search — workbook level
var results = await cellsApi.SearchContentInRemoteSpreadsheet("report.xlsx", "revenue");

// Search — worksheet level
var results = await cellsApi.SearchContentInRemoteWorksheet("report.xlsx", "Q1", "revenue");

// Search — range level (NEW!)
var results = await cellsApi.SearchContentInRemoteRange("report.xlsx", "Q1", "A1:D50", "revenue");

// Replace — range level (NEW!)
var response = await cellsApi.ReplaceContentInRemoteRange("report.xlsx", "Q1", "A1:D50", "2024", "2025");

// Broken links (NEW!)
var brokenLinks = await cellsApi.SearchBrokenLinksInRemoteSpreadsheet("report.xlsx");

// All text items (NEW!)
var allText = await cellsApi.SearchAllTextItemsInRemoteSpreadsheet("report.xlsx");
```

---

## Python SDK Migration

### 3.0 SDK
```python
cells_api = CellsApi(client_id, client_secret)

# Search
results = cells_api.post_workbooks_text_search("report.xlsx", "revenue")

# Replace
response = cells_api.post_workbook_text_replace("report.xlsx", "2024", "2025")
```

### 4.0 SDK
```python
cells_api = CellsApi(client_id, client_secret)

# Search — workbook level
results = cells_api.search_content_in_remote_spreadsheet("report.xlsx", "revenue")

# Search — worksheet level
results = cells_api.search_content_in_remote_worksheet("report.xlsx", "Q1", "revenue")

# Search — range level (NEW!)
results = cells_api.search_content_in_remote_range("report.xlsx", "Q1", "A1:D50", "revenue")

# Replace — range level (NEW!)
response = cells_api.replace_content_in_remote_range("report.xlsx", "Q1", "A1:D50", "2024", "2025")

# Broken links (NEW!)
broken_links = cells_api.search_broken_links_in_remote_spreadsheet("report.xlsx")

# All text items (NEW!)
all_text = cells_api.search_all_text_items_in_remote_spreadsheet("report.xlsx")
```

---

## Real-World Scenarios

### Scenario 1: Year-End Report Update

**Task:** Update all "FY2024" references to "FY2025" across 50 regional reports.

**3.0 approach:**
```python
for filename in report_files:
    # Must download, process, upload for each file
    cells_api.post_workbook_text_replace(filename, "FY2024", "FY2025")
```

**4.0 approach:**
```python
for filename in report_files:
    # Direct remote operation — no download/upload needed
    cells_api.replace_content_in_remote_spreadsheet(filename, "FY2024", "FY2025")
```

**Time saved:** ~60% reduction in total processing time (eliminates download/upload cycles).

### Scenario 2: Pre-Migration Link Audit

**Task:** Before migrating to a new server, identify all broken hyperlinks.

**3.0:** ❌ Not possible. Would require custom code to parse each cell.

**4.0:**
```bash
# One API call per file
PUT /v4.0/cells/report.xlsx/search/broken-links
```

**Time saved:** Hours of manual work reduced to seconds.

### Scenario 3: Targeted Data Correction

**Task:** Fix a data entry error, but only in the "Q1" sheet, columns A-D.

**3.0:**
```bash
# Must replace across the entire workbook — risky!
POST /cells/report.xlsx/replaceText?searchText=wrong_value&replaceText=correct_value
```
⚠️ This might replace values in other sheets where "wrong_value" is intentional.

**4.0:**
```bash
# Replace only in the exact range
PUT /v4.0/cells/report.xlsx/worksheets/Q1/ranges/A1:D1000/replace/content?searchText=wrong_value&replaceText=correct_value
```
✅ Safe, precise, no risk of collateral changes.

---

## Migration Checklist

| Step | Action | Risk |
|------|--------|------|
| 1 | Update base URL from `v3.0` to `v4.0` | 🟢 Low |
| 2 | Change HTTP method from `POST` to `PUT` | 🟢 Low |
| 3 | Update endpoint paths (see mapping table) | 🟢 Low |
| 4 | Rename `findText` → `search/content` | 🟢 Low |
| 5 | Rename `replaceText` → `replace/content` | 🟢 Low |
| 6 | Add worksheet parameter to worksheet-level calls | 🟢 Low |
| 7 | Adopt remote file variants where applicable | 🟢 Low |
| 8 | Enable broken link scanning in audit workflows | 🟢 Low |
| 9 | Use range-level targeting for precision operations | 🟢 Low |
| 10 | Replace full-text searches with all-textitems where appropriate | 🟢 Low |

---

## Summary: Why Migrate?

| Benefit | Impact |
|---------|--------|
| **Range-level targeting** | 95%+ faster searches in large workbooks |
| **Broken link detection** | Hours of manual auditing → seconds |
| **All text items search** | Full content inventory in one call |
| **Remote file support** | Eliminates download/upload cycles (~60% faster) |
| **Range-scoped replace** | Prevents accidental collateral changes |
| **Consistent URL structure** | Self-documenting, easier to discover |
| **Same core functionality** | All 4 original operations preserved |

**Bottom line:** The 4.0 Search & Replace API is not just an upgrade — it's a **category expansion**. What was a simple find-and-replace tool in 3.0 becomes a comprehensive spreadsheet auditing and content management system in 4.0. The migration is trivial (URL + method change), but the capabilities you gain are transformative.
