---
title: "Migrating Conversion APIs from 3.0 to 4.0: Feature Map, Replacement Guide, and Real Gaps"
second_title: "Document"
ArticleTitle: "Migrating Conversion APIs from 3.0 to 4.0: Feature Map, Replacement Guide, and Real Gaps"
linktitle: "Conversion Migration"
type: docs
weight: 100
keywords: "Aspose.Cells Cloud, Excel API, migration, spreadsheet conversion, merge Excel, split Excel, protect Excel, cloud spreadsheet SDK, REST API, Excel processing"
description: "A verified mapping of all 14 conversion endpoints in 3.0 to their 28 counterparts in 4.0, with parameter-level changes, working replacement recipes, the formats that are genuinely missing, and a phased development plan."
url: /cells/migrating-conversion/
type: docs
---

## Introduction

This report compares the format-conversion surface of Aspose.Cells Cloud 3.0 and 4.0, shows how to replace every 3.0 call, and separates capabilities that are genuinely absent from capabilities that merely lost a dedicated route.

The analysis is based on two sources rather than on endpoint names alone:

- the published specifications — **356 operations / 469 models in 3.0** and **124 operations / 72 models in 4.0**;
- the 4.0 implementation — `ConversionController`, the `ExportData` format registry, and the `Workbook.Convert` / `Worksheet.Convert` extension methods that actually execute a conversion.

That second source matters. A route-level comparison suggests that Markdown, SQL, DOCX and PPTX "disappeared", because 3.0 had `POST /cells/convert/markdown` and 4.0 does not. At the engine level all four formats are still registered and still convert correctly through the generic route. **The migration problem is therefore mostly a request-shape problem, not a format-coverage problem.**

The biggest real regression is `PageSetup`, which 3.0 accepted as a 34-property object on two endpoints and 4.0 does not accept at all ([Gap G1](#g1-pagesetup-has-no-equivalent)). Two narrower paths also lost their direct equivalent: PDF→Excel table extraction and custom image options on a stored worksheet.

---

## What's Changed at a Glance

| Aspect | 3.0 | 4.0 |
|--------|-----|-----|
| **Total conversion endpoints** | 14 | 28 |
| **Granularity** | Workbook only | Workbook / worksheet / table / range / chart |
| **HTTP methods** | GET + POST | GET + PUT |
| **Remote export** | `GET /cells/{name}?format=X` | Same, plus 4 granular GET routes |
| **Local upload execution** | `PUT /cells/convert` + 9 POST routes | `PUT /cells/convert/*` (22 routes) |
| **Save to storage** | `POST /cells/{name}/SaveAs` | `PUT /cells/{name}/saveas` |
| **Request body for conversion** | JSON options object on 2 endpoints | None — query parameters + multipart file |
| **Format registry** | Implicit in each method | One registry (`ExportData`, ~45 keys) |
| **Image/print options** | JSON object (`ImageOrPrintOptions`) | 25 flat query parameters |
| **Page setup** | 34-property object | Not accepted |

---

## 3.0 Feature Inventory — 14 Endpoints

| # | Method and path | Operation | Input | Output |
|---|-----------------|-----------|-------|--------|
| 1 | `GET /cells/{name}` | `GetWorkbook` | Cloud-stored file | Any registered format |
| 2 | `PUT /cells/convert` | `PutConvertWorkbook` | Multipart `File` | Any registered format |
| 3 | `POST /cells/{name}/SaveAs` | `PostWorkbookSaveAs` | Cloud-stored file + `saveOptions` object | Saved to storage |
| 4 | `POST /cells/convert/pdf` | `PostConvertWorkbookToPDF` | Multipart `File` | PDF |
| 5 | `POST /cells/convert/png` | `PostConvertWorkbookToPNG` | Multipart `File` | PNG |
| 6 | `POST /cells/convert/docx` | `PostConvertWorkbookToDocx` | Multipart `File` | DOCX |
| 7 | `POST /cells/convert/pptx` | `PostConvertWorkbookToPptx` | Multipart `File` | PPTX |
| 8 | `POST /cells/convert/html` | `PostConvertWorkbookToHtml` | Multipart `File` | HTML |
| 9 | `POST /cells/convert/markdown` | `PostConvertWorkbookToMarkdown` | Multipart `File` | Markdown |
| 10 | `POST /cells/convert/json` | `PostConvertWorkbookToJson` | Multipart `File` | JSON |
| 11 | `POST /cells/convert/sql` | `PostConvertWorkbookToSQL` | Multipart `File` | SQL script |
| 12 | `POST /cells/convert/csv` | `PostConvertWorkbookToCSV` | Multipart `File` | CSV |
| 13 | `POST /cells/convertWorksheetToImage` | `PostConvertWorksheetToImage` | JSON `ConvertWorksheetOptions` | Image |
| 14 | `POST /cells/convertWorkbook` | `PostConvertWorkbook` | JSON `ConvertWorkbookOptions` | Any format |

Two properties of 3.0 are easy to miss:

- **Only endpoints 1–3 could be told which file to use by name.** Endpoints 4–12 always took an upload, and 13–14 took a JSON descriptor (`Name`, `DataSource`, `FileInfo`).
- **Only endpoints 13–14 accepted `PageSetup`.** That is the only place the lost capability existed.

---

## 4.0 Feature Inventory — 28 Endpoints

### Remote files (5 GET routes)

| Method and path | Level | Formats |
|-----------------|-------|---------|
| `GET /cells/{name}` | Workbook | Any registry key |
| `GET /cells/{name}/worksheets/{worksheet}` | Worksheet | Any registry key |
| `GET /cells/{name}/worksheets/{worksheet}/charts/{chartIndex}` | Chart | PDF or image |
| `GET /cells/{name}/worksheets/{worksheet}/tables/{tableName}` | Table | Any registry key |
| `GET /cells/{name}/worksheets/{worksheet}/ranges/{range}` | Range | Any registry key |

### Local uploads (22 PUT routes)

| Level | Routes |
|-------|--------|
| Workbook | `/convert/spreadsheet` (any format), `/convert/spreadsheet/pdf`, `/convert/spreadsheet/json`, `/convert/spreadsheet/csv` |
| Worksheet | `/convert/worksheet/image`, `/pdf`, `/json`, `/csv`, `/html`, `/html-table` |
| Table | `/convert/table/image`, `/pdf`, `/csv`, `/html`, `/json` |
| Range | `/convert/range/image`, `/pdf`, `/csv`, `/html`, `/json` |
| Chart | `/convert/chart/image`, `/convert/chart/pdf` |

### Storage (1 PUT route)

| Method and path | Behaviour |
|-----------------|-----------|
| `PUT /cells/{name}/saveas` | Converts a stored workbook and uploads the result |

All local routes share three conventions: the file arrives in the multipart field **`Spreadsheet`**, the input format is auto-detected, and the response is a file stream unless `outPath` is supplied.

---

## Capability Matrix

`✅` supported · `⚠️` supported with a caveat · `—` not available at that level.

| Output | 3.0 workbook | 4.0 workbook | 4.0 worksheet | 4.0 table / range | 4.0 chart |
|--------|--------------|--------------|---------------|-------------------|-----------|
| PDF | ✅ | ✅ | ✅ | ✅ | ✅ |
| Raster image (PNG/JPG/GIF/BMP/EMF) | ✅ | ✅ | ✅ | ✅ | ✅ |
| TIFF / SVG | ✅ | ✅ | ⚠️ image route | ⚠️ image route | ⚠️ image route |
| HTML | ✅ | ✅ | ✅ (`/html`) | ✅ | — |
| HTML table fragment | — | — | ✅ (`/html-table`) | — | — |
| JSON | ✅ | ✅ | ✅ | ✅ | — |
| CSV / TSV / TXT | ✅ | ✅ | ✅ | ✅ | — |
| Markdown | ✅ | ✅ | — | — | — |
| SQL script | ✅ | ✅ | — | — | — |
| DOCX | ✅ | ✅ | — | — | — |
| PPTX | ✅ | ✅ | — | — | — |
| XLSX / XLS / XLSB / ODS / XML family | ✅ | ✅ | ✅ | ✅ | — |
| PageSetup-controlled output | ✅ endpoints 13–14 | ❌ | ❌ | ❌ | ❌ |

---

## Endpoint-by-Endpoint Mapping

### Direct replacements

| 3.0 | 4.0 | What changes |
|-----|-----|--------------|
| `GET /cells/{name}?format=X` | `GET /cells/{name}?format=X` | Path unchanged. Registry is larger. `isAutoFit` → `AutoRowsFit` + `AutoColumnsFit`. |
| `PUT /cells/convert` | `PUT /cells/convert/spreadsheet` | `File` → `Spreadsheet`; `streamFormat` removed. |
| `POST /cells/{name}/SaveAs` | `PUT /cells/{name}/saveas` | POST → PUT; `newfilename` + `saveOptions` move into a `SaveOptionsData` body. |
| `POST /cells/convert/pdf` | `PUT /cells/convert/spreadsheet/pdf` | POST → PUT; `File` → `Spreadsheet`. |
| `POST /cells/convert/json` | `PUT /cells/convert/spreadsheet/json` | POST → PUT. |
| `POST /cells/convert/csv` | `PUT /cells/convert/spreadsheet/csv` | POST → PUT. |
| `POST /cells/convert/html` | `PUT /cells/convert/spreadsheet?format=html` | No dedicated spreadsheet-level route; the generic route covers it. |
| `POST /cells/convert/png` | `PUT /cells/convert/spreadsheet?format=png` | No dedicated route. |
| `POST /cells/convert/docx` | `PUT /cells/convert/spreadsheet?format=docx` | No dedicated route; format still supported. |
| `POST /cells/convert/pptx` | `PUT /cells/convert/spreadsheet?format=pptx` | No dedicated route; format still supported. |
| `POST /cells/convert/markdown` | `PUT /cells/convert/spreadsheet?format=markdown` | No dedicated route; format still supported. |
| `POST /cells/convert/sql` | `PUT /cells/convert/spreadsheet?format=sql` | No dedicated route; format still supported. |
| `POST /cells/convertWorksheetToImage` | `PUT /cells/convert/worksheet/image?worksheet=…&format=…` | JSON body → multipart + query. `ImageOrPrintOptions` flattens to query parameters. |
| `POST /cells/convertWorkbook` | `GET /cells/{name}?format=X` | Body descriptor → path + query. `PageSetup` is lost. |

### New capabilities with no 3.0 ancestor

| 4.0 endpoint | Why it matters |
|--------------|----------------|
| `GET /cells/{name}/worksheets/{worksheet}` | Export one sheet without downloading the workbook output |
| `GET /cells/{name}/worksheets/{worksheet}/tables/{tableName}` | Replaces `onlySaveTable` |
| `GET /cells/{name}/worksheets/{worksheet}/ranges/{range}` | Arbitrary rectangle, any format |
| `GET /cells/{name}/worksheets/{worksheet}/charts/{chartIndex}` | Chart export, which 3.0 could not do at all |
| 22 local PUT routes | Table/range/chart conversion from an upload, not just a stored file |

---

## Parameter-Level Mapping

This is where most migrations break, because several 3.0 parameters are accepted without error but silently ignored in 4.0.

| 3.0 parameter | 4.0 equivalent | Status | Notes |
|---------------|----------------|--------|-------|
| `File` | `Spreadsheet` | Renamed | Multipart field name changed |
| `format` | `format` | Same | Must be a registry key |
| `password` | `password` | Same | |
| `folder`, `storageName` | Same | Same | |
| `outPath`, `outStorageName` | Same | Same | Honoured by file-result routes only; ignored by `saveas` |
| `newfilename` | `saveOptionsData.Filename` | Moved to body | Include the extension |
| `saveOptions` | `saveOptionsData.SaveOptions` | Moved to body | Binds to the base type; prefer flat query parameters for format-specific options |
| `isAutoFit` | `AutoRowsFit` + `AutoColumnsFit` | Split | Two booleans now |
| `isAutoFitRows` | `AutoRowsFit` | Renamed | |
| `isAutoFitColumns` | `AutoColumnsFit` | Renamed | |
| `sheetName` | `worksheet` path segment | Moved to route | **Ignored** on workbook routes |
| `pageIndex` | `pageIndex` | Still read | Only honoured on worksheet-level routes |
| `onePagePerSheet` | `onePagePerSheet` | Works | Applied through save options |
| `checkExcelRestriction` | `checkExcelRestriction` | Works | Applied through save options |
| `pageWideFitOnPerSheet` | Same | Works | Sets `FitToPagesWide` |
| `pageTallFitOnPerSheet` | Same | Works | Sets `FitToPagesTall` |
| `region` | `region` | Works | |
| `FontsLocation` | `fontsLocation` | Renamed | Casing changed; names are case-insensitive |
| `onlySaveTable` | — | Removed | 3.0 used it for PDF→Excel table extraction; 4.0 has no PDF table-import path |
| `onlyAutofitTable` | — | Removed | Same PDF→Excel scope; no equivalent |
| `streamFormat` | — | Removed | Input format is auto-detected |
| `ImageOrPrintOptions.*` (25 fields) | Same names as query parameters | Flattened | Honoured only by `/worksheet/image`, `/chart/image` and the remote chart route; absent from the 4.0 spec |
| `PageSetup.*` (34 fields) | — | Removed | Only the fit-to-page booleans survive |
| `DataSource`, `FileInfo` | — | Removed | Use `name` + `folder` + `storageName` |

---

## Replacement Recipes

### 1. Local upload to PDF

```bash
# 3.0
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/pdf" \
  -H "Authorization: Bearer $TOKEN" \
  -F "File=@Book1.xlsx" -o Book1.pdf

# 4.0 — dedicated route
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/pdf" \
  -H "Authorization: Bearer $TOKEN" \
  -F "Spreadsheet=@Book1.xlsx" -o Book1.pdf
```

### 2. Local upload to a format without a dedicated route

```bash
# 3.0
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/markdown" \
  -H "Authorization: Bearer $TOKEN" \
  -F "File=@Book1.xlsx" -o Book1.md

# 4.0 — generic route, same capability
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet?format=markdown" \
  -H "Authorization: Bearer $TOKEN" \
  -F "Spreadsheet=@Book1.xlsx" -o Book1.md
```

The same shape works for `format=sql`, `format=docx`, `format=pptx`, `format=png`, `format=svg` and every other registry key.

### 3. Remote file export

```bash
# 3.0
curl -X GET "https://api.aspose.cloud/v3.0/cells/Book1.xlsx?format=pdf&isAutoFit=true" \
  -H "Authorization: Bearer $TOKEN" -o Book1.pdf

# 4.0
curl -X GET "https://api.aspose.cloud/v4.0/cells/Book1.xlsx?format=pdf&AutoRowsFit=true&AutoColumnsFit=true" \
  -H "Authorization: Bearer $TOKEN" -o Book1.pdf
```

### 4. SaveAs

```bash
# 3.0
curl -X POST "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/SaveAs?newfilename=out/Book1.pdf&isAutoFitRows=true" \
  -H "Authorization: Bearer $TOKEN" \
  -H "Content-Type: application/json" \
  -d '{"SaveFormat":"Pdf"}'

# 4.0
curl -X PUT "https://api.aspose.cloud/v4.0/cells/Book1.xlsx/saveas?format=pdf&AutoRowsFit=true&OnePagePerSheet=true" \
  -H "Authorization: Bearer $TOKEN" \
  -H "Content-Type: application/json" \
  -d '{
        "Filename": "out/Book1.pdf",
        "StorageName": "MyStorage"
      }'
```

`StorageName` in the body is the output storage. The `outStorageName` query parameter is advertised by the route but not read by this method — see [Gap G7](#g7-outpath-and-outstoragename-are-ignored-by-saveas).

Keep format-specific options in the query string, as `OnePagePerSheet` is here. A `SaveOptions` object in the body binds to the base DTO type, so its format-specific properties are not applied reliably (G11).

### 5. One worksheet, not the whole workbook

```bash
# 3.0 — POST /cells/convert with sheetName
curl -X PUT "https://api.aspose.cloud/v3.0/cells/convert?format=pdf&sheetName=Q1" \
  -H "Authorization: Bearer $TOKEN" \
  -F "File=@Book1.xlsx" -o Q1.pdf

# 4.0 — the worksheet moves into the route
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf?worksheet=Q1" \
  -H "Authorization: Bearer $TOKEN" \
  -F "Spreadsheet=@Book1.xlsx" -o Q1.pdf

# 4.0 — or, for a stored file
curl -X GET "https://api.aspose.cloud/v4.0/cells/Book1.xlsx/worksheets/Q1?format=pdf" \
  -H "Authorization: Bearer $TOKEN" -o Q1.pdf
```

Passing `sheetName=Q1` to `/cells/convert/spreadsheet` returns the whole workbook, without an error. That silent fallback is the single most likely migration bug.

### 6. One page of one worksheet

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf?worksheet=Q1&pageIndex=2" \
  -H "Authorization: Bearer $TOKEN" \
  -F "Spreadsheet=@Book1.xlsx" -o Q1-page3.pdf
```

`pageIndex` is still read, but only by worksheet-level routes. It is not part of the 4.0 specification, so SDKs do not expose it.

### 7. Export a single table (new in 4.0)

This is not a replacement for `onlySaveTable`, which extracted tables from a PDF. It addresses a table that already exists in the workbook:

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/json?worksheet=Sales&tableName=SalesData" \
  -H "Authorization: Bearer $TOKEN" \
  -F "Spreadsheet=@Book1.xlsx" -o SalesData.json
```

### 8. Replace `ImageOrPrintOptions`

```bash
# 3.0 — JSON body
curl -X POST "https://api.aspose.cloud/v3.0/cells/convertWorksheetToImage" \
  -H "Authorization: Bearer $TOKEN" -H "Content-Type: application/json" \
  -d '{
        "Name": "Book1.xlsx",
        "WorksheetName": "Dashboard",
        "ConvertFormat": "png",
        "ImageOrPrintOptions": { "Quality": 90, "HorizontalResolution": 200 }
      }'

# 4.0 — same options as flat query parameters on the local image route
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/image?worksheet=Dashboard&format=png&Quality=90&HorizontalResolution=200" \
  -H "Authorization: Bearer $TOKEN" \
  -F "Spreadsheet=@Book1.xlsx" -o Dashboard.png
```

All 25 fields of the 3.0 `ImageOrPrintOptions` model are read as query parameters, including `Quality`, `HorizontalResolution`, `VerticalResolution`, `OnePagePerSheet`, `OnlyArea`, `Transparent`, `SVGFitToViewPort`, `GridlineType`, `TextCrossType`, `PrintingPage`, `TiffCompression`, `TiffColorDepth` and `TiffBinarizationMethod`. Only three paths pass them to the renderer: `PUT /cells/convert/worksheet/image`, `PUT /cells/convert/chart/image` and the remote chart route. Workbook, worksheet, table and range exports render with fixed options. For a stored workbook there is no 4.0 route that renders a worksheet image with custom options — see [G9](#g9-image-options-are-only-honoured-on-three-routes-and-none-of-them-are-documented).

---

## Formats 4.0 Actually Accepts

The `format` value is resolved against one registry. These keys are accepted by the remote workbook, worksheet, table and range routes, and by the local workbook and worksheet routes:

| Family | Keys |
|--------|------|
| Documents | `PDF`, `DOCX`, `PPTX`, `HTML`, `HTM`, `MHTML`, `XPS`, `EPUB`, `AZW3` |
| Images | `PNG`, `JPG`, `JPEG`, `GIF`, `BMP`, `EMF`, `WMF`, `TIFF`, `TIF`, `SVG` |
| Data | `JSON`, `CSV`, `TSV`, `TXT`, `SQL`, `SQLSCRIPT`, `XML`, `SPREADSHEETML`, `DIF`, `DBF`, `XHTML` |
| Spreadsheets | `XLSX`, `XLSM`, `XLSB`, `XLS`, `EXCEL97TO2003`, `XLT`, `XLTX`, `XLTM`, `XLAM`, `ODS`, `FODS`, `OTS`, `SXC`, `NUMBERS` |
| Print / other | `PCL`, `AUTO` |

Route-specific restrictions:

- `worksheet/image` and `chart/image` require an image key and reject everything else.
- `chart/pdf` is PDF only; the remote chart route accepts PDF or image and throws for anything else.
- `worksheet/html-table` takes no `format` at all.
- `table/image` and `range/image` do not validate the key before rendering; a non-image key produces a `NullReferenceException` (HTTP 500) instead of a 400 ([G13](#g13-validation-defects)).

---

## What 4.0 Does Not Support

The following list was verified against the implementation. It distinguishes real gaps from formats that only lost a route.

### G1. `PageSetup` has no equivalent

3.0 accepted a 34-property `PageSetup` object on `POST /cells/convertWorkbook` and `POST /cells/convertWorksheetToImage`. 4.0 has no `PageSetup` model and no conversion request body.

| Preserved | Lost |
|-----------|------|
| `pageWideFitOnPerSheet` (`FitToPagesWide = 1`) | Orientation, paper size, margins |
| `pageTallFitOnPerSheet` (`FitToPagesTall = 1`) | Print area, print titles, print order |
| `onePagePerSheet` (PDF) | Zoom, scale, first page number |
| `printHeadings` (range image route only) | Headers, footers, centring, black-and-white, draft, copies, gridlines, comments, errors |

**Impact:** high. Any job that depends on paper size, orientation or margins cannot be reproduced from a local upload.

**Workaround:** for stored files, call the PageSetup API to persist the settings on the workbook before exporting. For uploads, there is no workaround today; this is the top item in the development plan.

### G2. `onlyAutofitTable` has no equivalent

This flag belongs to the same PDF→Excel path as `onlySaveTable` (G6) and has no 4.0 counterpart. For a table that already exists in a workbook, a table route with `AutoRowsFit=true` and `AutoColumnsFit=true` scopes the autofit to the extracted table, but that is a different scenario.

### G3. Workbook-level `sheetName` and `pageIndex` are silent no-ops

`sheetName` is read from the query string, stored in `ConvertRequestParameters`, and never applied. `pageIndex` is applied only by `Worksheet.Convert`. On `/cells/convert/spreadsheet` and `GET /cells/{name}` both parameters are accepted and ignored.

**Workaround:** move to a worksheet route. Do not rely on the parameter being rejected.

### G4. `streamFormat` is gone

4.0 detects the input format from content and filename. A stream with no filename and an unusual container can be misdetected. Upload with a filename that carries the correct extension.

### G5. No request body that describes a data source

3.0's `ConvertWorkbookOptions` and `ConvertWorksheetOptions` accepted `DataSource` (`DataSourceType`, `DataPath`) and `FileInfo`. 4.0's remote routes accept only `name` + `folder` + `storageName`. If a 3.0 integration used `DataSource` to point at something other than Cells Cloud storage, there is no 4.0 equivalent.

### G6. `onlySaveTable` and `onlyAutofitTable` have no equivalent

The 3.0 specification describes `onlySaveTable` as a PDF→Excel option that saves table data only; `onlyAutofitTable` is its autofit companion. 4.0 has no PDF table-import path, and its table routes operate on tables that already exist in a spreadsheet. A client that used these flags to extract tables from a PDF must keep using 3.0 or pre-convert the PDF outside the API.

### G7. `outPath` and `outStorageName` are ignored by `saveas`

Both parameters are advertised on `PUT /cells/{name}/saveas`, and both are ignored. The method takes the output path from `saveOptionsData.Filename` and the output storage from `saveOptionsData.StorageName`, falling back to the input `storageName`.

**Workaround:** put both values in the body.

### G8. Dedicated routes were dropped for six formats

`png`, `docx`, `pptx`, `html`, `markdown` and `sql` have no workbook-level dedicated route. All six still convert through `format=`. This is a contract and discoverability problem, not a capability problem, and it is cheap to fix.

### G9. Image options are only honoured on three routes, and none of them are documented

The 25 `ImageOrPrintOptions` fields are read from the query string, but only `PUT /cells/convert/worksheet/image`, `PUT /cells/convert/chart/image` and the remote chart route pass them to the renderer. Workbook, worksheet, table and range exports use fixed options, and the workbook image path forces `OnePagePerSheet = true`. A 3.0 job that rendered a **stored** worksheet with `Quality`, `HorizontalResolution` or `OnlyArea` therefore has no 4.0 equivalent.

The same options, plus working save options (`onePagePerSheet`, `checkExcelRestriction`, `pageIndex`, `cellArea`, `range`), are also absent from the 4.0 specification, so Swagger and generated SDKs cannot discover them.

### G10. Chart export accepts only PDF and image

A chart can be exported as PDF or as a raster/vector image. It cannot be exported as DOCX, PPTX, HTML or JSON. This is not a regression — 3.0 had no chart export — but it caps the new capability.

### G11. Registry and metadata defects

| Defect | Effect |
|--------|--------|
| `PPTX` is registered with the DOCX content type | Clients receive `application/vnd.openxmlformats-officedocument.wordprocessingml.document` for a `.pptx` response |
| `WMF` maps to `SaveFormat.Emf` in the general registry | WMF output may actually be EMF |
| `TXT` maps to `SaveFormat.Tsv` | "TXT" output is tab-separated, not plain text |
| Markdown extensions are `"Markdown"` and `"MD"` | Output filenames use inconsistent casing |
| `SaveOptionsData.SaveOptions` binds to the base type | `SaveOptionsConverter` is registered on the MVC serializer, but `JToken.ToObject<SaveOptions>()` inside `SaveOptionsDataConverter` uses a default serializer, and the aliases `md` and `sqlscript` are missing. Format-specific body options are unreliable — use flat query parameters |
| `SQL` with no valid cell data falls back to TSV | A SQL request can return tab-separated data instead of an error |

### G12. `worksheet/html-table` breaks the response contract

`PUT /cells/convert/worksheet/html-table` returns a `Stream` directly. It has no `[FileResult]`, no `ToResult`, no `Content-Type`, and ignores `outPath`. Every other converter follows the standard envelope.

### G13. Validation defects

| Location | Defect |
|----------|--------|
| `table/image`, `range/image` | Non-image `format` triggers a `NullReferenceException` (HTTP 500) instead of 400 |
| `worksheet/image`, `table/image`, `range/image` | `ArgumentNullException(nameof(format))` is thrown for a missing `worksheet` |
| `chart/image`, `chart/pdf`, remote chart route | Bounds check is `charts.Count >= chartIndex`; `chartIndex == Count` reaches the indexer and throws `ArgumentOutOfRangeException` |

### Not a gap: Markdown, SQL, DOCX and PPTX

These four are the most commonly misreported losses. They work. A migration that depends on them should proceed now, using the generic route, and switch to dedicated routes later if and when those are added.

---

## Development Plan

The plan closes the gaps above in four phases, ordered by user impact per unit of work.

| Phase | Scope | Effort | Exit criteria |
|-------|-------|--------|---------------|
| **0 — Contract** | Publish the format registry; add the missing query parameters to the specification | 2 days | Every accepted parameter appears in the 4.0 spec and in regenerated SDKs |
| **1 — Coverage** | Dedicated routes for `docx`, `pptx`, `html`, `markdown`, `sql`, `png`; format discovery endpoint | 3 days | Each dedicated route returns byte-identical output to the generic route |
| **2 — Parity** | `PageSetup` support; `sheetName` on workbook routes; `printHeadings`; `saveas` output path; image options on workbook and worksheet routes | 6 days | The 3.0 `ConvertWorkbookOptions` and `ConvertWorksheetOptions` scenarios can be reproduced |
| **3 — Correctness** | Registry metadata, validation, chart bounds, `html-table` contract | 3 days | The defect table is empty; contract tests pass |
| **4 — Verification** | Golden-file matrix, SDK regeneration, deprecation window | 4 days | 80-case matrix green; v3 endpoints retired only after the published window |

### Phase 0 — Contract (2 days)

1. Add attributes so the specification generator emits `pageIndex`, `cellArea` / `range`, `onePagePerSheet`, `checkExcelRestriction`, `printHeadings` and the 25 `ImageOrPrintOptions` fields on the routes that read them.
2. Add `GET /cells/convert/formats` returning `{ key, extension, contentType, levels[] }` from `ExportData`.
3. Correct this guide and the FAQ entries that claimed Markdown and SQL were unsupported.

**Why first:** it costs two days, it removes the largest source of migration uncertainty, and it requires no behavioural change.

### Phase 1 — Coverage (3 days)

Add thin wrappers, each one line of routing over the existing generic implementation:

```csharp
[HttpPut, Route("convert/spreadsheet/docx"), OnlineOperation, FileResult, CanOutFileToRemote, CanUseCustomFonts, CanAutoFits]
public IActionResult ConvertSpreadsheetToDocx() => ConvertSpreadsheet("docx");
```

Same for `pptx`, `html`, `markdown`, `sql`, `png`. Add worksheet-level `markdown`, `sql`, `docx` and `pptx` routes that delegate to `worksheet.Convert(...)`.

**Acceptance:** for a fixed set of workbooks, each dedicated route and the generic route produce the same SHA-256 hash.

### Phase 2 — Parity (6 days)

1. **`PageSetup`**: add an optional `pageSetup` object to a new `ConvertOptionsData` body, or accept flat `PageSetup.*` query parameters. Apply to each worksheet before conversion. Cover all 34 properties.
2. **`sheetName`**: on workbook routes, either convert only the named sheet or reject the request with 400. Silent fallback must go.
3. **`printHeadings`**: wire `ConvertRequestParameters.PrintHeadings` into the image and PDF paths.
4. **`saveas`**: honour `outPath` and `outStorageName`, matching the file-result routes.
5. **`streamFormat`**: optionally accept it as a load-format hint; otherwise document auto-detection.
6. **Image options**: pass `ConvertRequestParameters.ImageOrPrintOptions` into `Workbook.Convert` and `Worksheet.Convert` so the workbook and worksheet routes honour `Quality`, `HorizontalResolution` and the other renderer fields.

**Why 6 days:** `PageSetup` and image-option plumbing are the only items that need new request paths and rendering tests; the rest are small.

### Phase 3 — Correctness (3 days)

1. Fix the PPTX content type, the WMF and TXT mappings, and the Markdown extension casing.
2. Add `md` and `sqlscript` to `SaveOptionsConverter`.
3. Replace `charts.Count >= chartIndex` with a proper bound check (`chartIndex >= 0 && chartIndex < charts.Count`); return the intended message for an out-of-range index.
4. Validate image keys on `table/image` and `range/image`; fix `nameof` arguments.
5. Move `html-table` onto `ToResult` with `[FileResult]`.
6. Make the SQL fallback explicit: return an error, or add `SqlScriptSaveOptions.ExportArea` handling instead of switching to TSV.
7. Make `SaveOptionsData` bind the body with the configured serializer, or build the save-options DTO from `format` explicitly, so `saveas` can accept format-specific save options.

### Phase 4 — Verification and rollout (4 days)

Build a golden-file matrix: **8 output formats × 5 levels × 2 sources = 80 cases**, run against both versions where the 3.0 baseline exists.

- Hash comparison for deterministic outputs (CSV, JSON, SQL, Markdown, XLSX).
- Pixel diff for images; text extraction diff for PDF and DOCX.
- Contract tests that every registry key claimed by `GET /cells/convert/formats` is accepted by every route that lists it.
- Regenerate SDKs after Phase 0, not after Phase 3, so client code can be updated in parallel.
- Keep 3.0 conversion endpoints running for a published deprecation window; return `Deprecation` and `Sunset` headers with the migration link.

### Priority matrix

| Item | Impact | Effort | Priority |
|------|--------|--------|----------|
| Spec exposure of working parameters | High | Low | P0 |
| Dedicated routes for 6 formats | Medium | Low | P1 |
| `PageSetup` parity | High | Medium | P1 |
| Image options on workbook and worksheet routes | High | Medium | P1 |
| `sheetName` correctness | High | Low | P1 |
| `saveas` output path | Medium | Low | P1 |
| `saveas` body save options | High | Medium | P1 |
| Registry metadata fixes | Medium | Low | P2 |
| Validation and bounds fixes | Medium | Low | P2 |
| Golden-file matrix | High | Medium | P2 |

---

## Migration Checklist

1. Replace `/v3.0/cells` with `/v4.0/cells`.
2. Change `POST` format converters to `PUT`; rename the multipart field `File` to `Spreadsheet`.
3. Replace `isAutoFit` with `AutoRowsFit` and `AutoColumnsFit`; rename `isAutoFitRows` / `isAutoFitColumns`.
4. Move `sheetName` selection into a worksheet route; keep `pageIndex` only there.
5. If you relied on `onlySaveTable` or `onlyAutofitTable` for PDF→Excel extraction, keep the 3.0 endpoint or pre-convert the PDF outside the API.
6. Convert `SaveAs` to `PUT` and move `newfilename` into `SaveOptionsData.Filename`; keep format-specific options in query parameters.
7. Move output location into `SaveOptionsData.Filename` and `SaveOptionsData.StorageName`.
8. Audit every job that used `PageSetup`; move stored-file jobs to the PageSetup API and flag upload jobs.
9. Remove `streamFormat`; ensure uploaded filenames carry the correct extension.
10. Re-run golden outputs, comparing bytes for data formats and pixels for images.

