---  
title: "Convert Workbook Options"  
second_title: "Document"  
linktitle: "Convert Workbook Options"  
type: docs  
url: /convert-workbook-options/  
keywords: "Aspose.Cells Cloud, ConvertWorkbookOptions, Excel conversion API, REST API, Save Options, File formats, API reference"  
description: "Learn how to use the ConvertWorkbookOptions class in Aspose.Cells Cloud REST API. Detailed property list, defaults, and code examples for converting Excel workbooks to PDF, CSV, HTML, and more."  
weight: 79  
---  

# ConvertWorkbookOptions Properties  

**API version:** 23.12 (2024‑03)  

`ConvertWorkbookOptions` is the request model used by the Aspose.Cells Cloud conversion API to specify how an Excel workbook should be transformed into another format (PDF, CSV, HTML, etc.). It bundles the source‑file information, target format, page‑setup settings, and format‑specific save options.

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **DataSource** | **Object** | Data file source: `CloudFileSystem`, `RequestFiles`, or `HttpUri`. | |
| **[FileInfo](/cells/file-info/)** | **Object** | Describes the file name, size, and base‑64‑encoded content. | |
| **[PageSetup](/cells/page-setup/)** | **Object** | Page‑setup properties such as margins, orientation, and scaling. | |
| **SaveOptions** | **Object** | Container for format‑specific save‑option objects (e.g., `PdfSaveOptions`, `HtmlSaveOptions`). | |
| **ConvertFormat** | **string** | Target file format (e.g., **PDF**, **CSV**, **HTML**, **XLSX**, **TIFF**, etc.). | |
| **CheckExcelRestriction** | **boolean** | Gets or sets whether to enforce Excel‑specific restrictions (maximum rows, columns, sheet name length, etc.). | |

## FileSource Properties  

| Property Name | Property Type | Nullable | ReadOnly | Default Value | Description |
| ------------- | ------------- | -------- | -------- | ------------- | ----------- |
| FileSourceType | String | true | false |  | Indicates the source type (`CloudFileSystem`, `RequestFiles`, `HttpUri`). |
| FilePath | String | true | false |  | File path location. |

## DbfSaveOptions Properties  

| Property Name | Property Type | Nullable | ReadOnly | Default Value | Description |
| ------------- | ------------- | -------- | -------- | ------------- | ----------- |
| ExportAsString | Boolean | true | false |  | When **true**, exports numeric values as strings. |
| SaveFormat | String | true | false |  | The format identifier for DBF files. |
| CachedFileFolder | String | true | false |  | Folder used for temporary cached files. |
| ClearData | Boolean | true | false |  | Clears existing data before saving. |
| CreateDirectory | Boolean | true | false |  | Creates the target directory if it does not exist. |
| EnableHttpCompression | Boolean | true | false |  | Enables HTTP compression for the response. |
| RefreshChartCache | Boolean | true | false |  | Refreshes cached chart data before saving. |
| SortNames | Boolean | true | false |  | Sorts named ranges alphabetically. |
| ValidateMergedAreas | Boolean | true | false |  | Validates merged cells for consistency. |
| MergeAreas | Boolean | true | false |  | Merges adjacent cells when possible. |
| SortExternalNames | Boolean | true | false |  | Sorts external named references. |
| CheckExcelRestriction | Boolean | true | false |  | Enforces Excel‑specific limits during conversion. |
| UpdateSmartArt | Boolean | true | false |  | Updates SmartArt objects to the latest version. |
| EncryptDocumentProperties | Boolean | true | false |  | Encrypts document properties in the output file. |

## DifSaveOptions Properties  

| Property Name | Property Type | Nullable | ReadOnly | Default Value | Description |
| ------------- | ------------- | -------- | -------- | ------------- | ----------- |
| SaveFormat | String | true | false |  | The format identifier for DIF files. |
| CachedFileFolder | String | true | false |  | Folder used for temporary cached files. |
| ClearData | Boolean | true | false |  | Clears existing data before saving. |
| CreateDirectory | Boolean | true | false |  | Creates the target directory if it does not exist. |
| EnableHttpCompression | Boolean | true | false |  | Enables HTTP compression for the response. |
| RefreshChartCache | Boolean | true | false |  | Refreshes cached chart data before saving. |
| SortNames | Boolean | true | false |  | Sorts named ranges alphabetically. |
| ValidateMergedAreas | Boolean | true | false |  | Validates merged cells for consistency. |
| MergeAreas | Boolean | true | false |  | Merges adjacent cells when possible. |
| SortExternalNames | Boolean | true | false |  | Sorts external named references. |
| CheckExcelRestriction | Boolean | true | false |  | Enforces Excel‑specific limits during conversion. |
| UpdateSmartArt | Boolean | true | false |  | Updates SmartArt objects to the latest version. |
| EncryptDocumentProperties | Boolean | true | false |  | Encrypts document properties in the output file. |

## DocxSaveOptions Properties  

| Property Name | Property Type | Nullable | ReadOnly | Default Value | Description |
| ------------- | ------------- | -------- | -------- | ------------- | ----------- |
| DefaultFont | String | true | false |  | Font used when a source font is unavailable. |
| CheckWorkbookDefaultFont | Boolean | true | false |  | Checks whether the workbook default font is applied. |
| CheckFontCompatibility | Boolean | true | false |  | Validates font compatibility for the target format. |
| IsFontSubstitutionCharGranularity | Boolean | true | false |  | Controls character‑level font substitution. |
| OnePagePerSheet | Boolean | true | false |  | Forces each sheet onto a separate page. |
| AllColumnsInOnePagePerSheet | Boolean | true | false |  | Fits all columns of a sheet onto one page. |
| IgnoreError | Boolean | true | false |  | Ignores non‑critical errors during conversion. |
| OutputBlankPageWhenNothingToPrint | Boolean | true | false |  | Generates a blank page if there is nothing to render. |
| PageIndex | Integer | true | false |  | Index of the first page to export. |
| PageCount | Integer | true | false |  | Number of pages to export. |
| PrintingPageType | String | true | false |  | Specifies the page type for printing. |
| GridlineType | String | true | false |  | Determines how gridlines are rendered. |
| TextCrossType | String | true | false |  | Defines the cross‑type for text rendering. |
| DefaultEditLanguage | String | true | false |  | Default language for editing text. |
| EmfRenderSetting | String | true | false |  | Settings for EMF rendering. |
| MergeAreas | Boolean | true | false |  | Merges adjacent cells when possible. |
| SortExternalNames | Boolean | true | false |  | Sorts external named references. |
| UpdateSmartArt | Boolean | true | false |  | Updates SmartArt objects to the latest version. |
| SaveFormat | String | true | false |  | The format identifier for DOCX files. |
| CachedFileFolder | String | true | false |  | Folder used for temporary cached files. |
| ClearData | Boolean | true | false |  | Clears existing data before saving. |
| CreateDirectory | Boolean | true | false |  | Creates the target directory if it does not exist. |
| EnableHttpCompression | Boolean | true | false |  | Enables HTTP compression for the response. |
| RefreshChartCache | Boolean | true | false |  | Refreshes cached chart data before saving. |
| SortNames | Boolean | true | false |  | Sorts named ranges alphabetically. |
| ValidateMergedAreas | Boolean | true | false |  | Validates merged cells for consistency. |
| CheckExcelRestriction | Boolean | true | false |  | Enforces Excel‑specific limits during conversion. |
| EncryptDocumentProperties | Boolean | true | false |  | Encrypts document properties in the output file. |

## HtmlSaveOptions Properties  

| Property Name | Property Type | Nullable | ReadOnly | Default Value | Description |
| ------------- | ------------- | -------- | -------- | ------------- | ----------- |
| ExportPageHeaders | Boolean | true | false |  | Includes page headers in the HTML output. |
| ExportPageFooters | Boolean | true | false |  | Includes page footers in the HTML output. |
| ExportRowColumnHeadings | Boolean | true | false |  | Exports row and column headings. |
| ShowAllSheets | Boolean | true | false |  | Shows all worksheets in a single HTML file. |
| ImageOptions | Class | true | false |  | Settings that control image rendering. |
| SaveAsSingleFile | Boolean | true | false |  | Saves the entire workbook as one HTML file. |
| ExportHiddenWorksheet | Boolean | true | false |  | Includes hidden worksheets in the export. |
| ExportGridLines | Boolean | true | false |  | Renders grid lines in the HTML output. |
| PresentationPreference | Boolean | true | false |  | Optimizes HTML for presentation mode. |
| CellCssPrefix | String | true | false |  | Prefix added to generated CSS class names for cells. |
| TableCssId | String | true | false |  | ID attribute for the generated HTML table. |
| IsFullPathLink | Boolean | true | false |  | Generates full‑path hyperlinks for resources. |
| ExportWorksheetCSSSeparately | Boolean | true | false |  | Places each worksheet’s CSS in a separate file. |
| ExportSimilarBorderStyle | Boolean | true | false |  | Merges similar border styles to reduce CSS size. |
| MergeEmptyTdForcely | Boolean | true | false |  | Forces merging of empty `<td>` elements. |
| ExportCellCoordinate | Boolean | true | false |  | Includes cell coordinates (e.g., A1) in the HTML. |
| ExportExtraHeadings | Boolean | true | false |  | Adds extra heading rows/columns when required. |
| ExportHeadings | Boolean | true | false |  | Exports row and column headings. |
| ExportFormula | Boolean | true | false |  | Shows formulas instead of calculated values. |
| AddTooltipText | Boolean | true | false |  | Adds tool‑tips with cell comments. |
| ExportBogusRowData | Boolean | true | false |  | Includes placeholder rows for empty data. |
| ExcludeUnusedStyles | Boolean | true | false |  | Removes CSS styles that are not used. |
| ExportDocumentProperties | Boolean | true | false |  | Writes document‑level properties to HTML meta tags. |
| ExportWorksheetProperties | Boolean | true | false |  | Writes worksheet‑level properties to HTML. |
| ExportWorkbookProperties | Boolean | true | false |  | Writes workbook‑level properties to HTML. |
| ExportFrameScriptsAndProperties | Boolean | true | false |  | Includes scripts and properties for frames. |
| AttachedFilesDirectory | String | true | false |  | Directory path for attached files. |
| AttachedFilesUrlPrefix | String | true | false |  | URL prefix for attached files. |
| Encoding | String | true | false |  | Character encoding for the HTML file. |
| ExportActiveWorksheetOnly | Boolean | true | false |  | Exports only the active worksheet. |
| ExportChartImageFormat | String | true | false |  | Image format used for embedded charts. |
| ExportImagesAsBase64 | Boolean | true | false |  | Encodes images as Base64 strings. |
| HiddenColDisplayType | String | true | false |  | How hidden columns are displayed. |
| HiddenRowDisplayType | String | true | false |  | How hidden rows are displayed. |
| HtmlCrossStringType | String | true | false |  | Determines how cross‑string data is rendered. |
| IsExpImageToTempDir | Boolean | true | false |  | Exports images to a temporary directory. |
| PageTitle | String | true | false |  | Title used for the generated HTML page. |
| ParseHtmlTagInCell | Boolean | true | false |  | Parses HTML tags present in cell values. |
| CellNameAttribute | String | true | false |  | Attribute name that holds the cell reference. |
| SaveFormat | String | true | false |  | The format identifier for HTML files. |
| CachedFileFolder | String | true | false |  | Folder used for temporary cached files. |
| ClearData | Boolean | true | false |  | Clears existing data before saving. |
| CreateDirectory | Boolean | true | false |  | Creates the target directory if it does not exist. |
| EnableHttpCompression | Boolean | true | false |  | Enables HTTP compression for the response. |
| RefreshChartCache | Boolean | true | false |  | Refreshes cached chart data before saving. |
| SortNames | Boolean | true | false |  | Sorts named ranges alphabetically. |
| ValidateMergedAreas | Boolean | true | false |  | Validates merged cells for consistency. |
| MergeAreas | Boolean | true | false |  | Merges adjacent cells when possible. |
| SortExternalNames | Boolean | true | false |  | Sorts external named references. |
| CheckExcelRestriction | Boolean | true | false |  | Enforces Excel‑specific limits during conversion. |
| UpdateSmartArt | Boolean | true | false |  | Updates SmartArt objects to the latest version. |
| EncryptDocumentProperties | Boolean | true | false |  | Encrypts document properties in the output file. |

## ImageSaveOptions Properties  

| Property Name | Property Type | Nullable | ReadOnly | Default Value | Description |
| ------------- | ------------- | -------- | -------- | ------------- | ----------- |
| ChartImageType | String | true | false |  | Image format used for chart rendering. |
| EmbeddedImageNameInSvg | String | true | false |  | Name assigned to embedded images in SVG output. |
| HorizontalResolution | Integer | true | false |  | Horizontal DPI of the exported image. |
| ImageFormat | String | true | false |  | Target image format (PNG, JPG, etc.). |
| IsCellAutoFit | Boolean | true | false |  | Auto‑fits cell contents to the image size. |
| OnePagePerSheet | Boolean | true | false |  | Renders each worksheet on a separate page. |
| OnlyArea | Boolean | true | false |  | Exports only the defined area of the worksheet. |
| PrintingPage | String | true | false |  | Page layout used for printing. |
| PrintWithStatusDialog | Boolean | true | false |  | Shows a status dialog during printing. |
| Quality | Integer | true | false |  | Compression quality for JPEG images (0‑100). |
| TiffCompression | String | true | false |  | Compression type for TIFF images. |
| VerticalResolution | Integer | true | false |  | Vertical DPI of the exported image. |
| SaveFormat | String | true | false |  | The format identifier for image files. |
| CachedFileFolder | String | true | false |  | Folder used for temporary cached files. |
| ClearData | Boolean | true | false |  | Clears existing data before saving. |
| CreateDirectory | Boolean | true | false |  | Creates the target directory if it does not exist. |
| EnableHttpCompression | Boolean | true | false |  | Enables HTTP compression for the response. |
| RefreshChartCache | Boolean | true | false |  | Refreshes cached chart data before saving. |
| SortNames | Boolean | true | false |  | Sorts named ranges alphabetically. |
| ValidateMergedAreas | Boolean | true | false |  | Validates merged cells for consistency. |
| MergeAreas | Boolean | true | false |  | Merges adjacent cells when possible. |
| SortExternalNames | Boolean | true | false |  | Sorts external named references. |
| CheckExcelRestriction | Boolean | true | false |  | Enforces Excel‑specific limits during conversion. |
| UpdateSmartArt | Boolean | true | false |  | Updates SmartArt objects to the latest version. |
| EncryptDocumentProperties | Boolean | true | false |  | Encrypts document properties in the output file. |

## JsonSaveOptions Properties  

| Property Name | Property Type | Nullable | ReadOnly | Default Value | Description |
| ------------- | ------------- | -------- | -------- | ------------- | ----------- |
| ExportArea | Class | true | false |  | Defines the worksheet area to export. |
| HasHeaderRow | Boolean | true | false |  | Indicates whether the first row contains column headers. |
| ExportAsString | Boolean | true | false |  | Exports all values as strings. |
| Indent | String | true | false |  | String used for indentation (e.g., two spaces). |
| SaveFormat | String | true | false |  | The format identifier for JSON files. |
| CachedFileFolder | String | true | false |  | Folder used for temporary cached files. |
| ClearData | Boolean | true | false |  | Clears existing data before saving. |
| CreateDirectory | Boolean | true | false |  | Creates the target directory if it does not exist. |
| EnableHttpCompression | Boolean | true | false |  | Enables HTTP compression for the response. |
| RefreshChartCache | Boolean | true | false |  | Refreshes cached chart data before saving. |
| SortNames | Boolean | true | false |  | Sorts named ranges alphabetically. |
| ValidateMergedAreas | Boolean | true | false |  | Validates merged cells for consistency. |
| MergeAreas | Boolean | true | false |  | Merges adjacent cells when possible. |
| SortExternalNames | Boolean | true | false |  | Sorts external named references. |
| CheckExcelRestriction | Boolean | true | false |  | Enforces Excel‑specific limits during conversion. |
| UpdateSmartArt | Boolean | true | false |  | Updates SmartArt objects to the latest version. |
| EncryptDocumentProperties | Boolean | true | false |  | Encrypts document properties in the output file. |

## MarkdownSaveOptions Properties  

| Property Name | Property Type | Nullable | ReadOnly | Default Value | Description |
| ------------- | ------------- | -------- | -------- | ------------- | ----------- |
| Encoding | String | true | false |  | Character encoding for the markdown file. |
| FormatStrategy | String | true | false |  | Strategy used to format markdown (e.g., GitHub, CommonMark). |
| LineSeparator | String | true | false |  | Line‑break character(s) to use. |
| SaveFormat | String | true | false |  | The format identifier for markdown files. |
| CachedFileFolder | String | true | false |  | Folder used for temporary cached files. |
| ClearData | Boolean | true | false |  | Clears existing data before saving. |
| CreateDirectory | Boolean | true | false |  | Creates the target directory if it does not exist. |
| EnableHttpCompression | Boolean | true | false |  | Enables HTTP compression for the response. |
| RefreshChartCache | Boolean | true | false |  | Refreshes cached chart data before saving. |
| SortNames | Boolean | true | false |  | Sorts named ranges alphabetically. |
| ValidateMergedAreas | Boolean | true | false |  | Validates merged cells for consistency. |
| MergeAreas | Boolean | true | false |  | Merges adjacent cells when possible. |
| SortExternalNames | Boolean | true | false |  | Sorts external named references. |
| CheckExcelRestriction | Boolean | true | false |  | Enforces Excel‑specific limits during conversion. |
| UpdateSmartArt | Boolean | true | false |  | Updates SmartArt objects to the latest version. |
| EncryptDocumentProperties | Boolean | true | false |  | Encrypts document properties in the output file. |

## OoxmlSaveOptions Properties  

| Property Name | Property Type | Nullable | ReadOnly | Default Value | Description |
| ------------- | ------------- | -------- | -------- | ------------- | ----------- |
| ExportCellName | Boolean | true | false |  | Includes cell names in the exported file. |
| UpdateZoom | Boolean | true | false |  | Updates the zoom level in the output document. |
| EnableZip64 | Boolean | true | false |  | Enables ZIP64 extensions for large files. |
| EmbedOoxmlAsOleObject | Boolean | true | false |  | Embeds OOXML as an OLE object. |
| CompressionType | String | true | false |  | Type of compression applied (e.g., Normal, Maximum). |
| SaveFormat | String | true | false |  | The format identifier for OOXML files. |
| CachedFileFolder | String | true | false |  | Folder used for temporary cached files. |
| ClearData | Boolean | true | false |  | Clears existing data before saving. |
| CreateDirectory | Boolean | true | false |  | Creates the target directory if it does not exist. |
| EnableHttpCompression | Boolean | true | false |  | Enables HTTP compression for the response. |
| RefreshChartCache | Boolean | true | false |  | Refreshes cached chart data before saving. |
| SortNames | Boolean | true | false |  | Sorts named ranges alphabetically. |
| ValidateMergedAreas | Boolean | true | false |  | Validates merged cells for consistency. |
| MergeAreas | Boolean | true | false |  | Merges adjacent cells when possible. |
| SortExternalNames | Boolean | true | false |  | Sorts external named references. |
| CheckExcelRestriction | Boolean | true | false |  | Enforces Excel‑specific limits during conversion. |
| UpdateSmartArt | Boolean | true | false |  | Updates SmartArt objects to the latest version. |
| EncryptDocumentProperties | Boolean | true | false |  | Encrypts document properties in the output file. |

## PclSaveOptions Properties  

| Property Name | Property Type | Nullable | ReadOnly | Default Value | Description |
| ------------- | ------------- | -------- | -------- | ------------- | ----------- |
| fontFullName | String | true | false |  | Full name of the font to use. |
| fontPclName | String | true | false |  | PCL‑specific font name. |
| SaveFormat | String | true | false |  | The format identifier for PCL files. |
| CachedFileFolder | String | true | false |  | Folder used for temporary cached files. |
| ClearData | Boolean | true | false |  | Clears existing data before saving. |
| CreateDirectory | Boolean | true | false |  | Creates the target directory if it does not exist. |
| EnableHttpCompression | Boolean | true | false |  | Enables HTTP compression for the response. |
| RefreshChartCache | Boolean | true | false |  | Refreshes cached chart data before saving. |
| SortNames | Boolean | true | false |  | Sorts named ranges alphabetically. |
| ValidateMergedAreas | Boolean | true | false |  | Validates merged cells for consistency. |
| MergeAreas | Boolean | true | false |  | Merges adjacent cells when possible. |
| SortExternalNames | Boolean | true | false |  | Sorts external named references. |
| CheckExcelRestriction | Boolean | true | false |  | Enforces Excel‑specific limits during conversion. |
| UpdateSmartArt | Boolean | true | false |  | Updates SmartArt objects to the latest version. |
| EncryptDocumentProperties | Boolean | true | false |  | Encrypts document properties in the output file. |

## PDFSaveOptions Properties  

| Property Name | Property Type | Nullable | ReadOnly | Default Value | Description |
| ------------- | ------------- | -------- | -------- | ------------- | ----------- |
| DisplayDocTitle | Boolean | true | false |  | Uses the document title as the PDF title. |
| ExportDocumentStructure | Boolean | true | false |  | Preserves the logical structure of the document. |
| EmfRenderSetting | String | true | false |  | Settings for rendering EMF images. |
| CustomPropertiesExport | String | true | false |  | Controls export of custom document properties. |
| OptimizationType | String | true | false |  | Type of PDF optimization (e.g., Size, Speed). |
| Producer | String | true | false |  | Name of the PDF producer application. |
| PDFCompression | String | true | false |  | Compression algorithm for PDF streams. |
| FontEncoding | String | true | false |  | Encoding used for embedded fonts. |
| Watermark | Class | true | false |  | Watermark settings applied to the PDF. |
| CalculateFormula | Boolean | true | false |  | Calculates formulas before export. |
| CheckFontCompatibility | Boolean | true | false |  | Validates font compatibility for PDF rendering. |
| Compliance | String | true | false |  | PDF/A or PDF/X compliance level. |
| DefaultFont | String | true | false |  | Font used when a source font is unavailable. |
| OnePagePerSheet | Boolean | true | false |  | Places each worksheet on a separate PDF page. |
| PrintingPageType | String | true | false |  | Specifies the page type for printing. |
| SecurityOptions | Class | true | false |  | Security settings such as passwords and permissions. |
| desiredPPI | Integer | true | false |  | Desired pixels‑per‑inch resolution. |
| jpegQuality | Integer | true | false |  | JPEG image quality (0‑100). |
| ImageType | String | true | false |  | Image type used for rasterization. |
| SaveFormat | String | true | false |  | The format identifier for PDF files. |
| CachedFileFolder | String | true | false |  | Folder used for temporary cached files. |
| ClearData | Boolean | true | false |  | Clears existing data before saving. |
| CreateDirectory | Boolean | true | false |  | Creates the target directory if it does not exist. |
| EnableHttpCompression | Boolean | true | false |  | Enables HTTP compression for the response. |
| RefreshChartCache | Boolean | true | false |  | Refreshes cached chart data before saving. |
| SortNames | Boolean | true | false |  | Sorts named ranges alphabetically. |
| ValidateMergedAreas | Boolean | true | false |  | Validates merged cells for consistency. |
| MergeAreas | Boolean | true | false |  | Merges adjacent cells when possible. |
| SortExternalNames | Boolean | true | false |  | Sorts external named references. |
| CheckExcelRestriction | Boolean | true | false |  | Enforces Excel‑specific limits during conversion. |
| UpdateSmartArt | Boolean | true | false |  | Updates SmartArt objects to the latest version. |
| EncryptDocumentProperties | Boolean | true | false |  | Encrypts document properties in the output file. |

## PptxSaveOptions Properties  

| Property Name | Property Type | Nullable | ReadOnly | Default Value | Description |
| ------------- | ------------- | -------- | -------- | ------------- | ----------- |
| IgnoreHiddenRows | Boolean | true | false |  | Skips hidden rows during export. |
| AdjustFontSizeForRowType | String | true | false |  | Controls font‑size adjustment based on row type. |
| ExportViewType | String | true | false |  | Determines which view (slide, notes) to export. |
| DefaultFont | String | true | false |  | Font used when a source font is unavailable. |
| CheckWorkbookDefaultFont | Boolean | true | false |  | Checks whether the workbook default font is applied. |
| CheckFontCompatibility | Boolean | true | false |  | Validates font compatibility for the target format. |
| IsFontSubstitutionCharGranularity | Boolean | true | false |  | Controls character‑level font substitution. |
| OnePagePerSheet | Boolean | true | false |  | Places each worksheet on a separate slide. |
| AllColumnsInOnePagePerSheet | Boolean | true | false |  | Fits all columns of a sheet onto one slide. |
| IgnoreError | Boolean | true | false |  | Ignores non‑critical errors during conversion. |
| OutputBlankPageWhenNothingToPrint | Boolean | true | false |  | Generates a blank slide if there is nothing to render. |
| PageIndex | Integer | true | false |  | Index of the first slide to export. |
| PageCount | Integer | true | false |  | Number of slides to export. |
| PrintingPageType | String | true | false |  | Specifies the page type for printing. |
| GridlineType | String | true | false |  | Determines how gridlines are rendered. |
| TextCrossType | String | true | false |  | Defines the cross‑type for text rendering. |
| DefaultEditLanguage | String | true | false |  | Default language for editing text. |
| EmfRenderSetting | String | true | false |  | Settings for EMF rendering. |
| MergeAreas | Boolean | true | false |  | Merges adjacent cells when possible. |
| SortExternalNames | Boolean | true | false |  | Sorts external named references. |
| UpdateSmartArt | Boolean | true | false |  | Updates SmartArt objects to the latest version. |
| SaveFormat | String | true | false |  | The format identifier for PPTX files. |
| CachedFileFolder | String | true | false |  | Folder used for temporary cached files. |
| ClearData | Boolean | true | false |  | Clears existing data before saving. |
| CreateDirectory | Boolean | true | false |  | Creates the target directory if it does not exist. |
| EnableHttpCompression | Boolean | true | false |  | Enables HTTP compression for the response. |
| RefreshChartCache | Boolean | true | false |  | Refreshes cached chart data before saving. |
| SortNames | Boolean | true | false |  | Sorts named ranges alphabetically. |
| ValidateMergedAreas | Boolean | true | false |  | Validates merged cells for consistency. |
| CheckExcelRestriction | Boolean | true | false |  | Enforces Excel‑specific limits during conversion. |
| EncryptDocumentProperties | Boolean | true | false |  | Encrypts document properties in the output file. |

## SqlScriptSaveOptions Properties  

| Property Name | Property Type | Nullable | ReadOnly | Default Value | Description |
| ------------- | ------------- | -------- | -------- | ------------- | ----------- |
| CheckIfTableExists | Boolean | true | false |  | Checks whether the target table already exists. |
| ColumnTypeMap | String | true | false |  | Mapping of column names to SQL data types. |
| CheckAllDataForColumnType | Boolean | true | false |  | Scans all rows to infer column types. |
| AddBlankLineBetweenRows | Boolean | true | false |  | Inserts a blank line between generated rows. |
| Separator | String | true | false |  | String used to separate columns (e.g., comma, tab). |
| OperatorType | String | true | false |  | SQL operator used (INSERT, UPDATE, etc.). |
| PrimaryKey | Integer | true | false |  | Column index that acts as the primary key. |
| CreateTable | Boolean | true | false |  | Generates a CREATE TABLE statement. |
| IdName | String | true | false |  | Name of the identifier column. |
| StartId | Integer | true | false |  | Starting value for auto‑incremented IDs. |
| TableName | String | true | false |  | Name of the target database table. |
| ExportAsString | Boolean | true | false |  | Exports all values as strings. |
| ExportArea | Class | true | false |  | Defines the worksheet area to export. |
| HasHeaderRow | Boolean | true | false |  | Indicates whether the first row contains column headers. |
| SaveFormat | String | true | false |  | The format identifier for SQL script files. |
| CachedFileFolder | String | true | false |  | Folder used for temporary cached files. |
| ClearData | Boolean | true | false |  | Clears existing data before saving. |
| CreateDirectory | Boolean | true | false |  | Creates the target directory if it does not exist. |
| EnableHttpCompression | Boolean | true | false |  | Enables HTTP compression for the response. |
| RefreshChartCache | Boolean | true | false |  | Refreshes cached chart data before saving. |
| SortNames | Boolean | true | false |  | Sorts named ranges alphabetically. |
| ValidateMergedAreas | Boolean | true | false |  | Validates merged cells for consistency. |
| MergeAreas | Boolean | true | false |  | Merges adjacent cells when possible. |
| SortExternalNames | Boolean | true | false |  | Sorts external named references. |
| CheckExcelRestriction | Boolean | true | false |  | Enforces Excel‑specific limits during conversion. |
| UpdateSmartArt | Boolean | true | false |  | Updates SmartArt objects to the latest version. |
| EncryptDocumentProperties | Boolean | true | false |  | Encrypts document properties in the output file. |

## SvgSaveOptions Properties  

| Property Name | Property Type | Nullable | ReadOnly | Default Value | Description |
| ------------- | ------------- | -------- | -------- | ------------- | ----------- |
| SheetIndex | Integer | true | false |  | Index of the worksheet to export. |
| ChartImageType | String | true | false |  | Image format used for chart rendering. |
| EmbeddedImageNameInSvg | String | true | false |  | Name assigned to embedded images in SVG output. |
| HorizontalResolution | Integer | true | false |  | Horizontal DPI of the exported SVG. |
| ImageFormat | String | true | false |  | Target image format for raster elements. |
| IsCellAutoFit | Boolean | true | false |  | Auto‑fits cell contents to the SVG size. |
| OnePagePerSheet | Boolean | true | false |  | Renders each worksheet on a separate SVG page. |
| OnlyArea | Boolean | true | false |  | Exports only the defined area of the worksheet. |
| PrintingPage | String | true | false |  | Page layout used for printing. |
| PrintWithStatusDialog | Boolean | true | false |  | Shows a status dialog during printing. |
| Quality | Integer | true | false |  | Compression quality for raster images. |
| TiffCompression | String | true | false |  | Compression type for TIFF images embedded in SVG. |
| VerticalResolution | Integer | true | false |  | Vertical DPI of the exported SVG. |
| SaveFormat | String | true | false |  | The format identifier for SVG files. |
| CachedFileFolder | String | true | false |  | Folder used for temporary cached files. |
| ClearData | Boolean | true | false |  | Clears existing data before saving. |
| CreateDirectory | Boolean | true | false |  | Creates the target directory if it does not exist. |
| EnableHttpCompression | Boolean | true | false |  | Enables HTTP compression for the response. |
| RefreshChartCache | Boolean | true | false |  | Refreshes cached chart data before saving. |
| SortNames | Boolean | true | false |  | Sorts named ranges alphabetically. |
| ValidateMergedAreas | Boolean | true | false |  | Validates merged cells for consistency. |
| MergeAreas | Boolean | true | false |  | Merges adjacent cells when possible. |
| SortExternalNames | Boolean | true | false |  | Sorts external named references. |
| CheckExcelRestriction | Boolean | true | false |  | Enforces Excel‑specific limits during conversion. |
| UpdateSmartArt | Boolean | true | false |  | Updates SmartArt objects to the latest version. |
| EncryptDocumentProperties | Boolean | true | false |  | Encrypts document properties in the output file. |

## TxtSaveOptions Properties  

| Property Name | Property Type | Nullable | ReadOnly | Default Value | Description |
| ------------- | ------------- | -------- | -------- | ------------- | ----------- |
| QuoteType | String | true | false |  | Type of quoting used (e.g., double, single). |
| Separator | String | true | false |  | Column separator character (e.g., comma, tab). |
| SeparatorString | String | true | false |  | Full string used as a separator when more than one character is needed. |
| AlwaysQuoted | Boolean | true | false |  | Forces all fields to be quoted. |
| SaveFormat | String | true | false |  | The format identifier for TXT files. |
| CachedFileFolder | String | true | false |  | Folder used for temporary cached files. |
| ClearData | Boolean | true | false |  | Clears existing data before saving. |
| CreateDirectory | Boolean | true | false |  | Creates the target directory if it does not exist. |
| EnableHttpCompression | Boolean | true | false |  | Enables HTTP compression for the response. |
| RefreshChartCache | Boolean | true | false |  | Refreshes cached chart data before saving. |
| SortNames | Boolean | true | false |  | Sorts named ranges alphabetically. |
| ValidateMergedAreas | Boolean | true | false |  | Validates merged cells for consistency. |
| MergeAreas | Boolean | true | false |  | Merges adjacent cells when possible. |
| SortExternalNames | Boolean | true | false |  | Sorts external named references. |
| CheckExcelRestriction | Boolean | true | false |  | Enforces Excel‑specific limits during conversion. |
| UpdateSmartArt | Boolean | true | false |  | Updates SmartArt objects to the latest version. |
| EncryptDocumentProperties | Boolean | true | false |  | Encrypts document properties in the output file. |

## XlsSaveOptions & XlsbSaveOptions Properties  

| Property Name | Property Type | Nullable | ReadOnly | Default Value | Description |
| ------------- | ------------- | -------- | -------- | ------------- | ----------- |
| MatchColor | Boolean | true | false |  | Preserves exact cell colors during export. |
| WpsCompatibility | Boolean | true | false |  | Enables compatibility with WPS Office. |
| SaveFormat | String | true | false |  | The format identifier for XLS/XLSB files. |
| CachedFileFolder | String | true | false |  | Folder used for temporary cached files. |
| ClearData | Boolean | true | false |  | Clears existing data before saving. |
| CreateDirectory | Boolean | true | false |  | Creates the target directory if it does not exist. |
| EnableHttpCompression | Boolean | true | false |  | Enables HTTP compression for the response. |
| RefreshChartCache | Boolean | true | false |  | Refreshes cached chart data before saving. |
| SortNames | Boolean | true | false |  | Sorts named ranges alphabetically. |
| ValidateMergedAreas | Boolean | true | false |  | Validates merged cells for consistency. |
| MergeAreas | Boolean | true | false |  | Merges adjacent cells when possible. |
| SortExternalNames | Boolean | true | false |  | Sorts external named references. |
| CheckExcelRestriction | Boolean | true | false |  | Enforces Excel‑specific limits during conversion. |
| UpdateSmartArt | Boolean | true | false |  | Updates SmartArt objects to the latest version. |
| EncryptDocumentProperties | Boolean | true | false |  | Encrypts document properties in the output file. |

## XmlSaveOptions Properties  

| Property Name | Property Type | Nullable | ReadOnly | Default Value | Description |
| ------------- | ------------- | -------- | -------- | ------------- | ----------- |
| SheetIndexes | Array | true | false |  | List of worksheet indexes to include in the export. |
| ExportArea | Class | true | false |  | Defines the worksheet area to export. |
| HasHeaderRow | Boolean | true | false |  | Indicates whether the first row contains column headers. |
| XmlMapName | String | true | false |  | Name of the XML map applied to the worksheet. |
| SheetNameAsElementName | Boolean | true | false |  | Uses the sheet name as the XML element name. |
| DataAsAttribute | Boolean | true | false |  | Exports cell data as XML attributes instead of elements. |
| SaveFormat | String | true | false |  | The format identifier for XML files. |
| CachedFileFolder | String | true | false |  | Folder used for temporary cached files. |
| ClearData | Boolean | true | false |  | Clears existing data before saving. |
| CreateDirectory | String | true | false |  | Creates the target directory if it does not exist. |
| EnableHttpCompression | Boolean | true | false |  | Enables HTTP compression for the response. |
| RefreshChartCache | Boolean | true | false |  | Refreshes cached chart data before saving. |
| SortNames | Boolean | true | false |  | Sorts named ranges alphabetically. |
| ValidateMergedAreas | Boolean | true | false |  | Validates merged cells for consistency. |
| MergeAreas | Boolean | true | false |  | Merges adjacent cells when possible. |
| SortExternalNames | Boolean | true | false |  | Sorts external named references. |
| CheckExcelRestriction | Boolean | true | false |  | Enforces Excel‑specific limits during conversion. |
| UpdateSmartArt | Boolean | true | false |  | Updates SmartArt objects to the latest version. |
| EncryptDocumentProperties | Boolean | true | false |  | Encrypts document properties in the output file. |

## XpsSaveOptions Properties  

| Property Name | Property Type | Nullable | ReadOnly | Default Value | Description |
| ------------- | ------------- | -------- | -------- | ------------- | ----------- |
| DefaultFont | String | true | false |  | Font used when a source font is unavailable. |
| CheckWorkbookDefaultFont | Boolean | true | false |  | Checks whether the workbook default font is applied. |
| CheckFontCompatibility | Boolean | true | false |  | Validates font compatibility for the target format. |
| IsFontSubstitutionCharGranularity | Boolean | true | false |  | Controls character‑level font substitution. |
| OnePagePerSheet | Boolean | true | false |  | Places each worksheet on a separate XPS page. |
| AllColumnsInOnePagePerSheet | Boolean | true | false |  | Fits all columns of a sheet onto one page. |
| IgnoreError | Boolean | true | false |  | Ignores non‑critical errors during conversion. |
| OutputBlankPageWhenNothingToPrint | Boolean | true | false |  | Generates a blank page if there is nothing to render. |
| PageIndex | Integer | true | false |  | Index of the first page to export. |
| PageCount | Integer | true | false |  | Number of pages to export. |
| PrintingPageType | String | true | false |  | Specifies the page type for printing. |
| GridlineType | String | true | false |  | Determines how gridlines are rendered. |
| TextCrossType | String | true | false |  | Defines the cross‑type for text rendering. |
| DefaultEditLanguage | String | true | false |  | Default language for editing text. |
| EmfRenderSetting | String | true | false |  | Settings for EMF rendering. |
| MergeAreas | Boolean | true | false |  | Merges adjacent cells when possible. |
| SortExternalNames | Boolean | true | false |  | Sorts external named references. |
| UpdateSmartArt | Boolean | true | false |  | Updates SmartArt objects to the latest version. |
| SaveFormat | String | true | false |  | The format identifier for XPS files. |
| CachedFileFolder | String | true | false |  | Folder used for temporary cached files. |
| ClearData | Boolean | true | false |  | Clears existing data before saving. |
| CreateDirectory | Boolean | true | false |  | Creates the target directory if it does not exist. |
| EnableHttpCompression | Boolean | true | false |  | Enables HTTP compression for the response. |
| RefreshChartCache | Boolean | true | false |  | Refreshes cached chart data before saving. |
| SortNames | Boolean | true | false |  | Sorts named ranges alphabetically. |
| ValidateMergedAreas | Boolean | true | false |  | Validates merged cells for consistency. |
| CheckExcelRestriction | Boolean | true | false |  | Enforces Excel‑specific limits during conversion. |
| EncryptDocumentProperties | Boolean | true | false |  | Encrypts document properties in the output file. |  