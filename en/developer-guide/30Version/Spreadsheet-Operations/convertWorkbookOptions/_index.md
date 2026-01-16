---
title: "Convert Workbook Options"
second_title: "Document"
linktitle: "Convert Workbook Options"
type: docs
url: /convert-workbook-options/
keywords: "Aspose Cells, Convert Workbook Options, Excel conversion, REST API, Save Options, File formats"
description: "Documentation for the ConvertWorkbookOptions class in Aspose.Cells Cloud REST API, detailing its properties and associated save‑option configurations for converting Excel workbooks to various formats."
weight: 79
---

# ConvertWorkbookOptions Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **DataSource** | **Object** | Data file source: `CloudFileSystem`, `RequestFiles`, `HttpUri`. | |
| **[FileInfo](/cells/file-info/)** | **Object** | File information description, including filename, file size, and file content (base64 string). | |
| **[PageSetup](/cells/page-setup/)** | **Object** | Page‑setup properties. | |
| **SaveOptions** | **Object** | Save options such as `DbfSaveOptions`, `DifSaveOptions`, `DocxSaveOptions`, `HtmlSaveOptions`, `XlsSaveOptions`, `XlsxSaveOptions`, `XpsSaveOptions`, `PngSaveOptions`, `JpgSaveOptions`, `GifSaveOptions`, `EmfSaveOptions`, `BmpSaveOptions`, `MdSaveOptions`, `NumbersSaveOptions`, `WmfSaveOptions`, `SvgSaveOptions`, `TxtSaveOptions`, `TifSaveOptions`, `XlsbSaveOptions`. | |
| **ConvertFormat** | **string** | Target file format (e.g., CSV, XLS, HTML, MHTML, ODS, PDF, XML, TXT, TIFF, XLSB, XLSM, XLSX, XLTM, XLTX, XPS, PNG, JPG, GIF, EMF, BMP, MD, Numbers, WMF, SVG, etc.). | |
| **CheckExcelRestriction** | **boolean** | Gets or sets the type of auto‑fitting wrapped text. | |

## FileSource Properties

| Property Name | Property Type | Nullable | ReadOnly | Default Value | Description |
| ------------- | ------------- | -------- | -------- | ------------- | ----------- |
| FileSourceType | String | true | false |  | Indicates the source type (`CloudFileSystem`, `RequestFiles`, `HttpUri`). |
| FilePath | String | true | false |  | File path location. |

## DbfSaveOptions Properties

| Property Name | Property Type | Nullable | ReadOnly | Default Value | Description |
| ------------- | ------------- | -------- | -------- | ------------- | ----------- |
| ExportAsString | Boolean | true | false |  |  |
| SaveFormat | String | true | false |  |  |
| CachedFileFolder | String | true | false |  |  |
| ClearData | Boolean | true | false |  |  |
| CreateDirectory | Boolean | true | false |  |  |
| EnableHTTPCompression | Boolean | true | false |  |  |
| RefreshChartCache | Boolean | true | false |  |  |
| SortNames | Boolean | true | false |  |  |
| ValidateMergedAreas | Boolean | true | false |  |  |
| MergeAreas | Boolean | true | false |  |  |
| SortExternalNames | Boolean | true | false |  |  |
| CheckExcelRestriction | Boolean | true | false |  |  |
| UpdateSmartArt | Boolean | true | false |  |  |
| EncryptDocumentProperties | Boolean | true | false |  |  |

## DifSaveOptions Properties

| Property Name | Property Type | Nullable | ReadOnly | Default Value | Description |
| ------------- | ------------- | -------- | -------- | ------------- | ----------- |
| SaveFormat | String | true | false |  |  |
| CachedFileFolder | String | true | false |  |  |
| ClearData | Boolean | true | false |  |  |
| CreateDirectory | Boolean | true | false |  |  |
| EnableHTTPCompression | Boolean | true | false |  |  |
| RefreshChartCache | Boolean | true | false |  |  |
| SortNames | Boolean | true | false |  |  |
| ValidateMergedAreas | Boolean | true | false |  |  |
| MergeAreas | Boolean | true | false |  |  |
| SortExternalNames | Boolean | true | false |  |  |
| CheckExcelRestriction | Boolean | true | false |  |  |
| UpdateSmartArt | Boolean | true | false |  |  |
| EncryptDocumentProperties | Boolean | true | false |  |  |

## DocxSaveOptions Properties

| Property Name | Property Type | Nullable | ReadOnly | Default Value | Description |
| ------------- | ------------- | -------- | -------- | ------------- | ----------- |
| DefaultFont | String | true | false |  |  |
| CheckWorkbookDefaultFont | Boolean | true | false |  |  |
| CheckFontCompatibility | Boolean | true | false |  |  |
| IsFontSubstitutionCharGranularity | Boolean | true | false |  |  |
| OnePagePerSheet | Boolean | true | false |  |  |
| AllColumnsInOnePagePerSheet | Boolean | true | false |  |  |
| IgnoreError | Boolean | true | false |  |  |
| OutputBlankPageWhenNothingToPrint | Boolean | true | false |  |  |
| PageIndex | Integer | true | false |  |  |
| PageCount | Integer | true | false |  |  |
| PrintingPageType | String | true | false |  |  |
| GridlineType | String | true | false |  |  |
| TextCrossType | String | true | false |  |  |
| DefaultEditLanguage | String | true | false |  |  |
| EmfRenderSetting | String | true | false |  |  |
| MergeAreas | Boolean | true | false |  |  |
| SortExternalNames | Boolean | true | false |  |  |
| UpdateSmartArt | Boolean | true | false |  |  |
| SaveFormat | String | true | false |  |  |
| CachedFileFolder | String | true | false |  |  |
| ClearData | Boolean | true | false |  |  |
| CreateDirectory | Boolean | true | false |  |  |
| EnableHTTPCompression | Boolean | true | false |  |  |
| RefreshChartCache | Boolean | true | false |  |  |
| SortNames | Boolean | true | false |  |  |
| ValidateMergedAreas | Boolean | true | false |  |  |
| CheckExcelRestriction | Boolean | true | false |  |  |
| EncryptDocumentProperties | Boolean | true | false |  |  |

## HtmlSaveOptions Properties

| Property Name | Property Type | Nullable | ReadOnly | Default Value | Description |
| ------------- | ------------- | -------- | -------- | ------------- | ----------- |
| ExportPageHeaders | Boolean | true | false |  |  |
| ExportPageFooters | Boolean | true | false |  |  |
| ExportRowColumnHeadings | Boolean | true | false |  |  |
| ShowAllSheets | Boolean | true | false |  |  |
| ImageOptions | Class | true | false |  |  |
| SaveAsSingleFile | Boolean | true | false |  |  |
| ExportHiddenWorksheet | Boolean | true | false |  |  |
| ExportGridLines | Boolean | true | false |  |  |
| PresentationPreference | Boolean | true | false |  |  |
| CellCssPrefix | String | true | false |  |  |
| TableCssId | String | true | false |  |  |
| IsFullPathLink | Boolean | true | false |  |  |
| ExportWorksheetCSSSeparately | Boolean | true | false |  |  |
| ExportSimilarBorderStyle | Boolean | true | false |  |  |
| MergeEmptyTdForcely | Boolean | true | false |  |  |
| ExportCellCoordinate | Boolean | true | false |  |  |
| ExportExtraHeadings | Boolean | true | false |  |  |
| ExportHeadings | Boolean | true | false |  |  |
| ExportFormula | Boolean | true | false |  |  |
| AddTooltipText | Boolean | true | false |  |  |
| ExportBogusRowData | Boolean | true | false |  |  |
| ExcludeUnusedStyles | Boolean | true | false |  |  |
| ExportDocumentProperties | Boolean | true | false |  |  |
| ExportWorksheetProperties | Boolean | true | false |  |  |
| ExportWorkbookProperties | Boolean | true | false |  |  |
| ExportFrameScriptsAndProperties | Boolean | true | false |  |  |
| AttachedFilesDirectory | String | true | false |  |  |
| AttachedFilesUrlPrefix | String | true | false |  |  |
| Encoding | String | true | false |  |  |
| ExportActiveWorksheetOnly | Boolean | true | false |  |  |
| ExportChartImageFormat | String | true | false |  |  |
| ExportImagesAsBase64 | Boolean | true | false |  |  |
| HiddenColDisplayType | String | true | false |  |  |
| HiddenRowDisplayType | String | true | false |  |  |
| HtmlCrossStringType | String | true | false |  |  |
| IsExpImageToTempDir | Boolean | true | false |  |  |
| PageTitle | String | true | false |  |  |
| ParseHtmlTagInCell | Boolean | true | false |  |  |
| CellNameAttribute | String | true | false |  |  |
| SaveFormat | String | true | false |  |  |
| CachedFileFolder | String | true | false |  |  |
| ClearData | Boolean | true | false |  |  |
| CreateDirectory | Boolean | true | false |  |  |
| EnableHTTPCompression | Boolean | true | false |  |  |
| RefreshChartCache | Boolean | true | false |  |  |
| SortNames | Boolean | true | false |  |  |
| ValidateMergedAreas | Boolean | true | false |  |  |
| MergeAreas | Boolean | true | false |  |  |
| SortExternalNames | Boolean | true | false |  |  |
| CheckExcelRestriction | Boolean | true | false |  |  |
| UpdateSmartArt | Boolean | true | false |  |  |
| EncryptDocumentProperties | Boolean | true | false |  |  |

## ImageSaveOptions Properties

| Property Name | Property Type | Nullable | ReadOnly | Default Value | Description |
| ------------- | ------------- | -------- | -------- | ------------- | ----------- |
| ChartImageType | String | true | false |  |  |
| EmbeddedImageNameInSvg | String | true | false |  |  |
| HorizontalResolution | Integer | true | false |  |  |
| ImageFormat | String | true | false |  |  |
| IsCellAutoFit | Boolean | true | false |  |  |
| OnePagePerSheet | Boolean | true | false |  |  |
| OnlyArea | Boolean | true | false |  |  |
| PrintingPage | String | true | false |  |  |
| PrintWithStatusDialog | Boolean | true | false |  |  |
| Quality | Integer | true | false |  |  |
| TiffCompression | String | true | false |  |  |
| VerticalResolution | Integer | true | false |  |  |
| SaveFormat | String | true | false |  |  |
| CachedFileFolder | String | true | false |  |  |
| ClearData | Boolean | true | false |  |  |
| CreateDirectory | Boolean | true | false |  |  |
| EnableHTTPCompression | Boolean | true | false |  |  |
| RefreshChartCache | Boolean | true | false |  |  |
| SortNames | Boolean | true | false |  |  |
| ValidateMergedAreas | Boolean | true | false |  |  |
| MergeAreas | Boolean | true | false |  |  |
| SortExternalNames | Boolean | true | false |  |  |
| CheckExcelRestriction | Boolean | true | false |  |  |
| UpdateSmartArt | Boolean | true | false |  |  |
| EncryptDocumentProperties | Boolean | true | false |  |  |

## JsonSaveOptions Properties

| Property Name | Property Type | Nullable | ReadOnly | Default Value | Description |
| ------------- | ------------- | -------- | -------- | ------------- | ----------- |
| ExportArea | Class | true | false |  |  |
| HasHeaderRow | Boolean | true | false |  |  |
| ExportAsString | Boolean | true | false |  |  |
| Indent | String | true | false |  |  |
| SaveFormat | String | true | false |  |  |
| CachedFileFolder | String | true | false |  |  |
| ClearData | Boolean | true | false |  |  |
| CreateDirectory | Boolean | true | false |  |  |
| EnableHTTPCompression | Boolean | true | false |  |  |
| RefreshChartCache | Boolean | true | false |  |  |
| SortNames | Boolean | true | false |  |  |
| ValidateMergedAreas | Boolean | true | false |  |  |
| MergeAreas | Boolean | true | false |  |  |
| SortExternalNames | Boolean | true | false |  |  |
| CheckExcelRestriction | Boolean | true | false |  |  |
| UpdateSmartArt | Boolean | true | false |  |  |
| EncryptDocumentProperties | Boolean | true | false |  |  |

## MarkdownSaveOptions Properties

| Property Name | Property Type | Nullable | ReadOnly | Default Value | Description |
| ------------- | ------------- | -------- | -------- | ------------- | ----------- |
| Encoding | String | true | false |  |  |
| FormatStrategy | String | true | false |  |  |
| LineSeparator | String | true | false |  |  |
| SaveFormat | String | true | false |  |  |
| CachedFileFolder | String | true | false |  |  |
| ClearData | Boolean | true | false |  |  |
| CreateDirectory | Boolean | true | false |  |  |
| EnableHTTPCompression | Boolean | true | false |  |  |
| RefreshChartCache | Boolean | true | false |  |  |
| SortNames | Boolean | true | false |  |  |
| ValidateMergedAreas | Boolean | true | false |  |  |
| MergeAreas | Boolean | true | false |  |  |
| SortExternalNames | Boolean | true | false |  |  |
| CheckExcelRestriction | Boolean | true | false |  |  |
| UpdateSmartArt | Boolean | true | false |  |  |
| EncryptDocumentProperties | Boolean | true | false |  |  |

## OoxmlSaveOptions Properties

| Property Name | Property Type | Nullable | ReadOnly | Default Value | Description |
| ------------- | ------------- | -------- | -------- | ------------- | ----------- |
| ExportCellName | Boolean | true | false |  |  |
| UpdateZoom | Boolean | true | false |  |  |
| EnableZip64 | Boolean | true | false |  |  |
| EmbedOoxmlAsOleObject | Boolean | true | false |  |  |
| CompressionType | String | true | false |  |  |
| SaveFormat | String | true | false |  |  |
| CachedFileFolder | String | true | false |  |  |
| ClearData | Boolean | true | false |  |  |
| CreateDirectory | Boolean | true | false |  |  |
| EnableHTTPCompression | Boolean | true | false |  |  |
| RefreshChartCache | Boolean | true | false |  |  |
| SortNames | Boolean | true | false |  |  |
| ValidateMergedAreas | Boolean | true | false |  |  |
| MergeAreas | Boolean | true | false |  |  |
| SortExternalNames | Boolean | true | false |  |  |
| CheckExcelRestriction | Boolean | true | false |  |  |
| UpdateSmartArt | Boolean | true | false |  |  |
| EncryptDocumentProperties | Boolean | true | false |  |  |

## PclSaveOptions Properties

| Property Name | Property Type | Nullable | ReadOnly | Default Value | Description |
| ------------- | ------------- | -------- | -------- | ------------- | ----------- |
| fontFullName | String | true | false |  |  |
| fontPclName | String | true | false |  |  |
| SaveFormat | String | true | false |  |  |
| CachedFileFolder | String | true | false |  |  |
| ClearData | Boolean | true | false |  |  |
| CreateDirectory | Boolean | true | false |  |  |
| EnableHTTPCompression | Boolean | true | false |  |  |
| RefreshChartCache | Boolean | true | false |  |  |
| SortNames | Boolean | true | false |  |  |
| ValidateMergedAreas | Boolean | true | false |  |  |
| MergeAreas | Boolean | true | false |  |  |
| SortExternalNames | Boolean | true | false |  |  |
| CheckExcelRestriction | Boolean | true | false |  |  |
| UpdateSmartArt | Boolean | true | false |  |  |
| EncryptDocumentProperties | Boolean | true | false |  |  |

## PDFSaveOptions Properties

| Property Name | Property Type | Nullable | ReadOnly | Default Value | Description |
| ------------- | ------------- | -------- | -------- | ------------- | ----------- |
| DisplayDocTitle | Boolean | true | false |  |  |
| ExportDocumentStructure | Boolean | true | false |  |  |
| EmfRenderSetting | String | true | false |  |  |
| CustomPropertiesExport | String | true | false |  |  |
| OptimizationType | String | true | false |  |  |
| Producer | String | true | false |  |  |
| PDFCompression | String | true | false |  |  |
| FontEncoding | String | true | false |  |  |
| Watermark | Class | true | false |  |  |
| CalculateFormula | Boolean | true | false |  |  |
| CheckFontCompatibility | Boolean | true | false |  |  |
| Compliance | String | true | false |  |  |
| DefaultFont | String | true | false |  |  |
| OnePagePerSheet | Boolean | true | false |  |  |
| PrintingPageType | String | true | false |  |  |
| SecurityOptions | Class | true | false |  |  |
| desiredPPI | Integer | true | false |  |  |
| jpegQuality | Integer | true | false |  |  |
| ImageType | String | true | false |  |  |
| SaveFormat | String | true | false |  |  |
| CachedFileFolder | String | true | false |  |  |
| ClearData | Boolean | true | false |  |  |
| CreateDirectory | Boolean | true | false |  |  |
| EnableHTTPCompression | Boolean | true | false |  |  |
| RefreshChartCache | Boolean | true | false |  |  |
| SortNames | Boolean | true | false |  |  |
| ValidateMergedAreas | Boolean | true | false |  |  |
| MergeAreas | Boolean | true | false |  |  |
| SortExternalNames | Boolean | true | false |  |  |
| CheckExcelRestriction | Boolean | true | false |  |  |
| UpdateSmartArt | Boolean | true | false |  |  |
| EncryptDocumentProperties | Boolean | true | false |  |  |

## PptxSaveOptions Properties

| Property Name | Property Type | Nullable | ReadOnly | Default Value | Description |
| ------------- | ------------- | -------- | -------- | ------------- | ----------- |
| IgnoreHiddenRows | Boolean | true | false |  |  |
| AdjustFontSizeForRowType | String | true | false |  |  |
| ExportViewType | String | true | false |  |  |
| DefaultFont | String | true | false |  |  |
| CheckWorkbookDefaultFont | Boolean | true | false |  |  |
| CheckFontCompatibility | Boolean | true | false |  |  |
| IsFontSubstitutionCharGranularity | Boolean | true | false |  |  |
| OnePagePerSheet | Boolean | true | false |  |  |
| AllColumnsInOnePagePerSheet | Boolean | true | false |  |  |
| IgnoreError | Boolean | true | false |  |  |
| OutputBlankPageWhenNothingToPrint | Boolean | true | false |  |  |
| PageIndex | Integer | true | false |  |  |
| PageCount | Integer | true | false |  |  |
| PrintingPageType | String | true | false |  |  |
| GridlineType | String | true | false |  |  |
| TextCrossType | String | true | false |  |  |
| DefaultEditLanguage | String | true | false |  |  |
| EmfRenderSetting | String | true | false |  |  |
| MergeAreas | Boolean | true | false |  |  |
| SortExternalNames | Boolean | true | false |  |  |
| UpdateSmartArt | Boolean | true | false |  |  |
| SaveFormat | String | true | false |  |  |
| CachedFileFolder | String | true | false |  |  |
| ClearData | Boolean | true | false |  |  |
| CreateDirectory | Boolean | true | false |  |  |
| EnableHTTPCompression | Boolean | true | false |  |  |
| RefreshChartCache | Boolean | true | false |  |  |
| SortNames | Boolean | true | false |  |  |
| ValidateMergedAreas | Boolean | true | false |  |  |
| CheckExcelRestriction | Boolean | true | false |  |  |
| EncryptDocumentProperties | Boolean | true | false |  |  |

## SqlScriptSaveOptions Properties

| Property Name | Property Type | Nullable | ReadOnly | Default Value | Description |
| ------------- | ------------- | -------- | -------- | ------------- | ----------- |
| CheckIfTableExists | Boolean | true | false |  |  |
| ColumnTypeMap | String | true | false |  |  |
| CheckAllDataForColumnType | Boolean | true | false |  |  |
| AddBlankLineBetweenRows | Boolean | true | false |  |  |
| Separator | String | true | false |  |  |
| OperatorType | String | true | false |  |  |
| PrimaryKey | Integer | true | false |  |  |
| CreateTable | Boolean | true | false |  |  |
| IdName | String | true | false |  |  |
| StartId | Integer | true | false |  |  |
| TableName | String | true | false |  |  |
| ExportAsString | Boolean | true | false |  |  |
| ExportArea | Class | true | false |  |  |
| HasHeaderRow | Boolean | true | false |  |  |
| SaveFormat | String | true | false |  |  |
| CachedFileFolder | String | true | false |  |  |
| ClearData | Boolean | true | false |  |  |
| CreateDirectory | Boolean | true | false |  |  |
| EnableHTTPCompression | Boolean | true | false |  |  |
| RefreshChartCache | Boolean | true | false |  |  |
| SortNames | Boolean | true | false |  |  |
| ValidateMergedAreas | Boolean | true | false |  |  |
| MergeAreas | Boolean | true | false |  |  |
| SortExternalNames | Boolean | true | false |  |  |
| CheckExcelRestriction | Boolean | true | false |  |  |
| UpdateSmartArt | Boolean | true | false |  |  |
| EncryptDocumentProperties | Boolean | true | false |  |  |

## SvgSaveOptions Properties

| Property Name | Property Type | Nullable | ReadOnly | Default Value | Description |
| ------------- | ------------- | -------- | -------- | ------------- | ----------- |
| SheetIndex | Integer | true | false |  |  |
| ChartImageType | String | true | false |  |  |
| EmbeddedImageNameInSvg | String | true | false |  |  |
| HorizontalResolution | Integer | true | false |  |  |
| ImageFormat | String | true | false |  |  |
| IsCellAutoFit | Boolean | true | false |  |  |
| OnePagePerSheet | Boolean | true | false |  |  |
| OnlyArea | Boolean | true | false |  |  |
| PrintingPage | String | true | false |  |  |
| PrintWithStatusDialog | Boolean | true | false |  |  |
| Quality | Integer | true | false |  |  |
| TiffCompression | String | true | false |  |  |
| VerticalResolution | Integer | true | false |  |  |
| SaveFormat | String | true | false |  |  |
| CachedFileFolder | String | true | false |  |  |
| ClearData | Boolean | true | false |  |  |
| CreateDirectory | Boolean | true | false |  |  |
| EnableHTTPCompression | Boolean | true | false |  |  |
| RefreshChartCache | Boolean | true | false |  |  |
| SortNames | Boolean | true | false |  |  |
| ValidateMergedAreas | Boolean | true | false |  |  |
| MergeAreas | Boolean | true | false |  |  |
| SortExternalNames | Boolean | true | false |  |  |
| CheckExcelRestriction | Boolean | true | false |  |  |
| UpdateSmartArt | Boolean | true | false |  |  |
| EncryptDocumentProperties | Boolean | true | false |  |  |

## TxtSaveOptions Properties

| Property Name | Property Type | Nullable | ReadOnly | Default Value | Description |
| ------------- | ------------- | -------- | -------- | ------------- | ----------- |
| QuoteType | String | true | false |  |  |
| Separator | String | true | false |  |  |
| SeparatorString | String | true | false |  |  |
| AlwaysQuoted | Boolean | true | false |  |  |
| SaveFormat | String | true | false |  |  |
| CachedFileFolder | String | true | false |  |  |
| ClearData | Boolean | true | false |  |  |
| CreateDirectory | Boolean | true | false |  |  |
| EnableHTTPCompression | Boolean | true | false |  |  |
| RefreshChartCache | Boolean | true | false |  |  |
| SortNames | Boolean | true | false |  |  |
| ValidateMergedAreas | Boolean | true | false |  |  |
| MergeAreas | Boolean | true | false |  |  |
| SortExternalNames | Boolean | true | false |  |  |
| CheckExcelRestriction | Boolean | true | false |  |  |
| UpdateSmartArt | Boolean | true | false |  |  |
| EncryptDocumentProperties | Boolean | true | false |  |  |

## XlsSaveOptions & XlsbSaveOptions Properties

| Property Name | Property Type | Nullable | ReadOnly | Default Value | Description |
| ------------- | ------------- | -------- | -------- | ------------- | ----------- |
| MatchColor | Boolean | true | false |  |  |
| WpsCompatibility | Boolean | true | false |  |  |
| SaveFormat | String | true | false |  |  |
| CachedFileFolder | String | true | false |  |  |
| ClearData | Boolean | true | false |  |  |
| CreateDirectory | Boolean | true | false |  |  |
| EnableHTTPCompression | Boolean | true | false |  |  |
| RefreshChartCache | Boolean | true | false |  |  |
| SortNames | Boolean | true | false |  |  |
| ValidateMergedAreas | Boolean | true | false |  |  |
| MergeAreas | Boolean | true | false |  |  |
| SortExternalNames | Boolean | true | false |  |  |
| CheckExcelRestriction | Boolean | true | false |  |  |
| UpdateSmartArt | Boolean | true | false |  |  |
| EncryptDocumentProperties | Boolean | true | false |  |  |

## XmlSaveOptions Properties

| Property Name | Property Type | Nullable | ReadOnly | Default Value | Description |
| ------------- | ------------- | -------- | -------- | ------------- | ----------- |
| SheetIndexes | Array | true | false |  |  |
| ExportArea | Class | true | false |  |  |
| HasHeaderRow | Boolean | true | false |  |  |
| XmlMapName | String | true | false |  |  |
| SheetNameAsElementName | Boolean | true | false |  |  |
| DataAsAttribute | Boolean | true | false |  |  |
| SaveFormat | String | true | false |  |  |
| CachedFileFolder | String | true | false |  |  |
| ClearData | Boolean | true | false |  |  |
| CreateDirectory | Boolean | true | false |  |  |
| EnableHTTPCompression | Boolean | true | false |  |  |
| RefreshChartCache | Boolean | true | false |  |  |
| SortNames | Boolean | true | false |  |  |
| ValidateMergedAreas | Boolean | true | false |  |  |
| MergeAreas | Boolean | true | false |  |  |
| SortExternalNames | Boolean | true | false |  |  |
| CheckExcelRestriction | Boolean | true | false |  |  |
| UpdateSmartArt | Boolean | true | false |  |  |
| EncryptDocumentProperties | Boolean | true | false |  |  |

## XpsSaveOptions Properties

| Property Name | Property Type | Nullable | ReadOnly | Default Value | Description |
| ------------- | ------------- | -------- | -------- | ------------- | ----------- |
| DefaultFont | String | true | false |  |  |
| CheckWorkbookDefaultFont | Boolean | true | false |  |  |
| CheckFontCompatibility | Boolean | true | false |  |  |
| IsFontSubstitutionCharGranularity | Boolean | true | false |  |  |
| OnePagePerSheet | Boolean | true | false |  |  |
| AllColumnsInOnePagePerSheet | Boolean | true | false |  |  |
| IgnoreError | Boolean | true | false |  |  |
| OutputBlankPageWhenNothingToPrint | Boolean | true | false |  |  |
| PageIndex | Integer | true | false |  |  |
| PageCount | Integer | true | false |  |  |
| PrintingPageType | String | true | false |  |  |
| GridlineType | String | true | false |  |  |
| TextCrossType | String | true | false |  |  |
| DefaultEditLanguage | String | true | false |  |  |
| EmfRenderSetting | String | true | false |  |  |
| MergeAreas | Boolean | true | false |  |  |
| SortExternalNames | Boolean | true | false |  |  |
| UpdateSmartArt | Boolean | true | false |  |  |
| SaveFormat | String | true | false |  |  |
| CachedFileFolder | String | true | false |  |  |
| ClearData | Boolean | true | false |  |  |
| CreateDirectory | Boolean | true | false |  |  |
| EnableHTTPCompression | Boolean | true | false |  |  |
| RefreshChartCache | Boolean | true | false |  |  |
| SortNames | Boolean | true | false |  |  |
| ValidateMergedAreas | Boolean | true | false |  |  |
| CheckExcelRestriction | Boolean | true | false |  |  |
| EncryptDocumentProperties | Boolean | true | false |  |  |