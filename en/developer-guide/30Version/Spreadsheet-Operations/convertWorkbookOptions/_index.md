---
title: "Convert Workbook Options"
second_title: "Document"
linktitle: "Convert Workbook Options"
type: docs
url: /convert-workbook-options/
keywords: "ConvertWorkbookOptions."
description: "Aspose.Cells Cloud REST API support get excel files to kinds of format files. SDK support kinds of development languages. They include Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby, and swift."
weight: 79
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, JSON, Markdown, Convert Workbook Options
---



# ConvertWorkbookOptions Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DataSource** | **Object** | Data file soruce : CloudFileSystem ,RequestFiles , HttpUri. |
**[FileInfo](/cells/file-info/)** | **Object** |  File inforamtion description. include of filename, file size, and file content(base64 string). |
**[PageSetup](/cells/page-setup/)** | **Object** | Page setup properties. |
**SaveOptions** | **Object** | Save Options:  DbfSaveOptions, DifSaveOptions, DocxSaveOptions, HtmlSaveOptions, XlsSaveOptions, XlsxSaveOptions, XpsSaveOptions, PngSaveOptions, JpgSaveOptions, GifSaveOptions, EmfSaveOptions, BmpSaveOptions, MdSaveOptions, NumbersSaveOptions, WmfSaveOptions, SvgSaveOptions, TxtSaveOptions, TifSaveOptions, XlsbSaveOptions |
**ConvertFormat** | **string** | The file format: CSV, xls, HTML, mhtml, ods, pdf, xml, txt, tiff, xlsb, xlsm, xlsx, xltm, xltx, xps, png, jpg, gif, emf, bmp, md, Numbers, wmf, svg, and so on.  |
**CheckExcelRestriction** | **boolean** | Gets and sets the type of auto fitting wrapped text. |

## **fileSource Properties**

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description |
| :- | :- | :- |:- |  :- | :- |
|FileSourceType|String|true|false |  |A property named FileSourceType of type FileSourceType that can be accessed and modified.(CloudFileSystem/RequestFiles/HttpUri)|
|FilePath|String|true|false |  | The file position path.|

## **DbfSaveOptions Properties**

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description |
| :- | :- | :- |:- |  :- | :- |
|ExportAsString|Boolean|true|false |  ||
|SaveFormat|String|true|false |  ||
|CachedFileFolder|String|true|false |  ||
|ClearData|Boolean|true|false |  ||
|CreateDirectory|Boolean|true|false |  ||
|EnableHTTPCompression|Boolean|true|false |  ||
|RefreshChartCache|Boolean|true|false |  ||
|SortNames|Boolean|true|false |  ||
|ValidateMergedAreas|Boolean|true|false |  ||
|MergeAreas|Boolean|true|false |  ||
|SortExternalNames|Boolean|true|false |  ||
|CheckExcelRestriction|Boolean|true|false |  ||
|UpdateSmartArt|Boolean|true|false |  ||
|EncryptDocumentProperties|Boolean|true|false |  ||

## **DifSaveOptions Properties**

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description |
| :- | :- | :- |:- |  :- | :- |
|SaveFormat|String|true|false |  ||
|CachedFileFolder|String|true|false |  ||
|ClearData|Boolean|true|false |  ||
|CreateDirectory|Boolean|true|false |  ||
|EnableHTTPCompression|Boolean|true|false |  ||
|RefreshChartCache|Boolean|true|false |  ||
|SortNames|Boolean|true|false |  ||
|ValidateMergedAreas|Boolean|true|false |  ||
|MergeAreas|Boolean|true|false |  ||
|SortExternalNames|Boolean|true|false |  ||
|CheckExcelRestriction|Boolean|true|false |  ||
|UpdateSmartArt|Boolean|true|false |  ||
|EncryptDocumentProperties|Boolean|true|false |  ||

## **DocxSaveOptions Properties**

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description |
| :- | :- | :- |:- |  :- | :- |
|DefaultFont|String|true|false |  ||
|CheckWorkbookDefaultFont|Boolean|true|false |  ||
|CheckFontCompatibility|Boolean|true|false |  ||
|IsFontSubstitutionCharGranularity|Boolean|true|false |  ||
|OnePagePerSheet|Boolean|true|false |  ||
|AllColumnsInOnePagePerSheet|Boolean|true|false |  ||
|IgnoreError|Boolean|true|false |  ||
|OutputBlankPageWhenNothingToPrint|Boolean|true|false |  ||
|PageIndex|Integer|true|false |  ||
|PageCount|Integer|true|false |  ||
|PrintingPageType|String|true|false |  ||
|GridlineType|String|true|false |  ||
|TextCrossType|String|true|false |  ||
|DefaultEditLanguage|String|true|false |  ||
|EmfRenderSetting|String|true|false |  ||
|MergeAreas|Boolean|true|false |  ||
|SortExternalNames|Boolean|true|false |  ||
|UpdateSmartArt|Boolean|true|false |  ||
|SaveFormat|String|true|false |  ||
|CachedFileFolder|String|true|false |  ||
|ClearData|Boolean|true|false |  ||
|CreateDirectory|Boolean|true|false |  ||
|EnableHTTPCompression|Boolean|true|false |  ||
|RefreshChartCache|Boolean|true|false |  ||
|SortNames|Boolean|true|false |  ||
|ValidateMergedAreas|Boolean|true|false |  ||
|CheckExcelRestriction|Boolean|true|false |  ||
|EncryptDocumentProperties|Boolean|true|false |  ||

## **HtmlSaveOptions Properties**

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description |
| :- | :- | :- |:- |  :- | :- |
|ExportPageHeaders|Boolean|true|false |  ||
|ExportPageFooters|Boolean|true|false |  ||
|ExportRowColumnHeadings|Boolean|true|false |  ||
|ShowAllSheets|Boolean|true|false |  ||
|ImageOptions|Class|true|false |  ||
|SaveAsSingleFile|Boolean|true|false |  ||
|ExportHiddenWorksheet|Boolean|true|false |  ||
|ExportGridLines|Boolean|true|false |  ||
|PresentationPreference|Boolean|true|false |  ||
|CellCssPrefix|String|true|false |  ||
|TableCssId|String|true|false |  ||
|IsFullPathLink|Boolean|true|false |  ||
|ExportWorksheetCSSSeparately|Boolean|true|false |  ||
|ExportSimilarBorderStyle|Boolean|true|false |  ||
|MergeEmptyTdForcely|Boolean|true|false |  ||
|ExportCellCoordinate|Boolean|true|false |  ||
|ExportExtraHeadings|Boolean|true|false |  ||
|ExportHeadings|Boolean|true|false |  ||
|ExportFormula|Boolean|true|false |  ||
|AddTooltipText|Boolean|true|false |  ||
|ExportBogusRowData|Boolean|true|false |  ||
|ExcludeUnusedStyles|Boolean|true|false |  ||
|ExportDocumentProperties|Boolean|true|false |  ||
|ExportWorksheetProperties|Boolean|true|false |  ||
|ExportWorkbookProperties|Boolean|true|false |  ||
|ExportFrameScriptsAndProperties|Boolean|true|false |  ||
|AttachedFilesDirectory|String|true|false |  ||
|AttachedFilesUrlPrefix|String|true|false |  ||
|Encoding|String|true|false |  ||
|ExportActiveWorksheetOnly|Boolean|true|false |  ||
|ExportChartImageFormat|String|true|false |  ||
|ExportImagesAsBase64|Boolean|true|false |  ||
|HiddenColDisplayType|String|true|false |  ||
|HiddenRowDisplayType|String|true|false |  ||
|HtmlCrossStringType|String|true|false |  ||
|IsExpImageToTempDir|Boolean|true|false |  ||
|PageTitle|String|true|false |  ||
|ParseHtmlTagInCell|Boolean|true|false |  ||
|CellNameAttribute|String|true|false |  ||
|SaveFormat|String|true|false |  ||
|CachedFileFolder|String|true|false |  ||
|ClearData|Boolean|true|false |  ||
|CreateDirectory|Boolean|true|false |  ||
|EnableHTTPCompression|Boolean|true|false |  ||
|RefreshChartCache|Boolean|true|false |  ||
|SortNames|Boolean|true|false |  ||
|ValidateMergedAreas|Boolean|true|false |  ||
|MergeAreas|Boolean|true|false |  ||
|SortExternalNames|Boolean|true|false |  ||
|CheckExcelRestriction|Boolean|true|false |  ||
|UpdateSmartArt|Boolean|true|false |  ||
|EncryptDocumentProperties|Boolean|true|false |  ||

## **ImageSaveOptions Properties**

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description |
| :- | :- | :- |:- |  :- | :- |
|ChartImageType|String|true|false |  ||
|EmbededImageNameInSvg|String|true|false |  ||
|HorizontalResolution|Integer|true|false |  ||
|ImageFormat|String|true|false |  ||
|IsCellAutoFit|Boolean|true|false |  ||
|OnePagePerSheet|Boolean|true|false |  ||
|OnlyArea|Boolean|true|false |  ||
|PrintingPage|String|true|false |  ||
|PrintWithStatusDialog|Boolean|true|false |  ||
|Quality|Integer|true|false |  ||
|TiffCompression|String|true|false |  ||
|VerticalResolution|Integer|true|false |  ||
|SaveFormat|String|true|false |  ||
|CachedFileFolder|String|true|false |  ||
|ClearData|Boolean|true|false |  ||
|CreateDirectory|Boolean|true|false |  ||
|EnableHTTPCompression|Boolean|true|false |  ||
|RefreshChartCache|Boolean|true|false |  ||
|SortNames|Boolean|true|false |  ||
|ValidateMergedAreas|Boolean|true|false |  ||
|MergeAreas|Boolean|true|false |  ||
|SortExternalNames|Boolean|true|false |  ||
|CheckExcelRestriction|Boolean|true|false |  ||
|UpdateSmartArt|Boolean|true|false |  ||
|EncryptDocumentProperties|Boolean|true|false |  ||

## **JsonSaveOptions Properties**

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description |
| :- | :- | :- |:- |  :- | :- |
|ExportArea|Class|true|false |  ||
|HasHeaderRow|Boolean|true|false |  ||
|ExportAsString|Boolean|true|false |  ||
|Indent|String|true|false |  ||
|SaveFormat|String|true|false |  ||
|CachedFileFolder|String|true|false |  ||
|ClearData|Boolean|true|false |  ||
|CreateDirectory|Boolean|true|false |  ||
|EnableHTTPCompression|Boolean|true|false |  ||
|RefreshChartCache|Boolean|true|false |  ||
|SortNames|Boolean|true|false |  ||
|ValidateMergedAreas|Boolean|true|false |  ||
|MergeAreas|Boolean|true|false |  ||
|SortExternalNames|Boolean|true|false |  ||
|CheckExcelRestriction|Boolean|true|false |  ||
|UpdateSmartArt|Boolean|true|false |  ||
|EncryptDocumentProperties|Boolean|true|false |  ||

## **MarkdownSaveOptions Properties**

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description |
| :- | :- | :- |:- |  :- | :- |
|Encoding|String|true|false |  ||
|FormatStrategy|String|true|false |  ||
|LineSeparator|String|true|false |  ||
|SaveFormat|String|true|false |  ||
|CachedFileFolder|String|true|false |  ||
|ClearData|Boolean|true|false |  ||
|CreateDirectory|Boolean|true|false |  ||
|EnableHTTPCompression|Boolean|true|false |  ||
|RefreshChartCache|Boolean|true|false |  ||
|SortNames|Boolean|true|false |  ||
|ValidateMergedAreas|Boolean|true|false |  ||
|MergeAreas|Boolean|true|false |  ||
|SortExternalNames|Boolean|true|false |  ||
|CheckExcelRestriction|Boolean|true|false |  ||
|UpdateSmartArt|Boolean|true|false |  ||
|EncryptDocumentProperties|Boolean|true|false |  ||

## **OoxmlSaveOptions Properties**

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description |
| :- | :- | :- |:- |  :- | :- |
|ExportCellName|Boolean|true|false |  ||
|UpdateZoom|Boolean|true|false |  ||
|EnableZip64|Boolean|true|false |  ||
|EmbedOoxmlAsOleObject|Boolean|true|false |  ||
|CompressionType|String|true|false |  ||
|SaveFormat|String|true|false |  ||
|CachedFileFolder|String|true|false |  ||
|ClearData|Boolean|true|false |  ||
|CreateDirectory|Boolean|true|false |  ||
|EnableHTTPCompression|Boolean|true|false |  ||
|RefreshChartCache|Boolean|true|false |  ||
|SortNames|Boolean|true|false |  ||
|ValidateMergedAreas|Boolean|true|false |  ||
|MergeAreas|Boolean|true|false |  ||
|SortExternalNames|Boolean|true|false |  ||
|CheckExcelRestriction|Boolean|true|false |  ||
|UpdateSmartArt|Boolean|true|false |  ||
|EncryptDocumentProperties|Boolean|true|false |  ||

## **PclSaveOptions Properties**

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description |
| :- | :- | :- |:- |  :- | :- |
|fontFullName|String|true|false |  ||
|fontPclName|String|true|false |  ||
|SaveFormat|String|true|false |  ||
|CachedFileFolder|String|true|false |  ||
|ClearData|Boolean|true|false |  ||
|CreateDirectory|Boolean|true|false |  ||
|EnableHTTPCompression|Boolean|true|false |  ||
|RefreshChartCache|Boolean|true|false |  ||
|SortNames|Boolean|true|false |  ||
|ValidateMergedAreas|Boolean|true|false |  ||
|MergeAreas|Boolean|true|false |  ||
|SortExternalNames|Boolean|true|false |  ||
|CheckExcelRestriction|Boolean|true|false |  ||
|UpdateSmartArt|Boolean|true|false |  ||
|EncryptDocumentProperties|Boolean|true|false |  ||

## **PDFSaveOptions Properties**

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description |
| :- | :- | :- |:- |  :- | :- |
|DisplayDocTitle|Boolean|true|false |  ||
|ExportDocumentStructure|Boolean|true|false |  ||
|EmfRenderSetting|String|true|false |  ||
|CustomPropertiesExport|String|true|false |  ||
|OptimizationType|String|true|false |  ||
|Producer|String|true|false |  ||
|PDFCompression|String|true|false |  ||
|FontEncoding|String|true|false |  ||
|Watermark|Class|true|false |  ||
|CalculateFormula|Boolean|true|false |  ||
|CheckFontCompatibility|Boolean|true|false |  ||
|Compliance|String|true|false |  ||
|DefaultFont|String|true|false |  ||
|OnePagePerSheet|Boolean|true|false |  ||
|PrintingPageType|String|true|false |  ||
|SecurityOptions|Class|true|false |  ||
|desiredPPI|Integer|true|false |  ||
|jpegQuality|Integer|true|false |  ||
|ImageType|String|true|false |  ||
|SaveFormat|String|true|false |  ||
|CachedFileFolder|String|true|false |  ||
|ClearData|Boolean|true|false |  ||
|CreateDirectory|Boolean|true|false |  ||
|EnableHTTPCompression|Boolean|true|false |  ||
|RefreshChartCache|Boolean|true|false |  ||
|SortNames|Boolean|true|false |  ||
|ValidateMergedAreas|Boolean|true|false |  ||
|MergeAreas|Boolean|true|false |  ||
|SortExternalNames|Boolean|true|false |  ||
|CheckExcelRestriction|Boolean|true|false |  ||
|UpdateSmartArt|Boolean|true|false |  ||
|EncryptDocumentProperties|Boolean|true|false |  ||

## **PptxSaveOptions Properties**

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description |
| :- | :- | :- |:- |  :- | :- |
|IgnoreHiddenRows|Boolean|true|false |  ||
|AdjustFontSizeForRowType|String|true|false |  ||
|ExportViewType|String|true|false |  ||
|DefaultFont|String|true|false |  ||
|CheckWorkbookDefaultFont|Boolean|true|false |  ||
|CheckFontCompatibility|Boolean|true|false |  ||
|IsFontSubstitutionCharGranularity|Boolean|true|false |  ||
|OnePagePerSheet|Boolean|true|false |  ||
|AllColumnsInOnePagePerSheet|Boolean|true|false |  ||
|IgnoreError|Boolean|true|false |  ||
|OutputBlankPageWhenNothingToPrint|Boolean|true|false |  ||
|PageIndex|Integer|true|false |  ||
|PageCount|Integer|true|false |  ||
|PrintingPageType|String|true|false |  ||
|GridlineType|String|true|false |  ||
|TextCrossType|String|true|false |  ||
|DefaultEditLanguage|String|true|false |  ||
|EmfRenderSetting|String|true|false |  ||
|MergeAreas|Boolean|true|false |  ||
|SortExternalNames|Boolean|true|false |  ||
|UpdateSmartArt|Boolean|true|false |  ||
|SaveFormat|String|true|false |  ||
|CachedFileFolder|String|true|false |  ||
|ClearData|Boolean|true|false |  ||
|CreateDirectory|Boolean|true|false |  ||
|EnableHTTPCompression|Boolean|true|false |  ||
|RefreshChartCache|Boolean|true|false |  ||
|SortNames|Boolean|true|false |  ||
|ValidateMergedAreas|Boolean|true|false |  ||
|CheckExcelRestriction|Boolean|true|false |  ||
|EncryptDocumentProperties|Boolean|true|false |  ||

## **SqlScriptSaveOptions Properties**

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description |
| :- | :- | :- |:- |  :- | :- |
|CheckIfTableExists|Boolean|true|false |  ||
|ColumnTypeMap|String|true|false |  ||
|CheckAllDataForColumnType|Boolean|true|false |  ||
|AddBlankLineBetweenRows|Boolean|true|false |  ||
|Separator|String|true|false |  ||
|OperatorType|String|true|false |  ||
|PrimaryKey|Integer|true|false |  ||
|CreateTable|Boolean|true|false |  ||
|IdName|String|true|false |  ||
|StartId|Integer|true|false |  ||
|TableName|String|true|false |  ||
|ExportAsString|Boolean|true|false |  ||
|ExportArea|Class|true|false |  ||
|HasHeaderRow|Boolean|true|false |  ||
|SaveFormat|String|true|false |  ||
|CachedFileFolder|String|true|false |  ||
|ClearData|Boolean|true|false |  ||
|CreateDirectory|Boolean|true|false |  ||
|EnableHTTPCompression|Boolean|true|false |  ||
|RefreshChartCache|Boolean|true|false |  ||
|SortNames|Boolean|true|false |  ||
|ValidateMergedAreas|Boolean|true|false |  ||
|MergeAreas|Boolean|true|false |  ||
|SortExternalNames|Boolean|true|false |  ||
|CheckExcelRestriction|Boolean|true|false |  ||
|UpdateSmartArt|Boolean|true|false |  ||
|EncryptDocumentProperties|Boolean|true|false |  ||

## **SvgSaveOptions Properties**

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description |
| :- | :- | :- |:- |  :- | :- |
|SheetIndex|Integer|true|false |  ||
|ChartImageType|String|true|false |  ||
|EmbededImageNameInSvg|String|true|false |  ||
|HorizontalResolution|Integer|true|false |  ||
|ImageFormat|String|true|false |  ||
|IsCellAutoFit|Boolean|true|false |  ||
|OnePagePerSheet|Boolean|true|false |  ||
|OnlyArea|Boolean|true|false |  ||
|PrintingPage|String|true|false |  ||
|PrintWithStatusDialog|Boolean|true|false |  ||
|Quality|Integer|true|false |  ||
|TiffCompression|String|true|false |  ||
|VerticalResolution|Integer|true|false |  ||
|SaveFormat|String|true|false |  ||
|CachedFileFolder|String|true|false |  ||
|ClearData|Boolean|true|false |  ||
|CreateDirectory|Boolean|true|false |  ||
|EnableHTTPCompression|Boolean|true|false |  ||
|RefreshChartCache|Boolean|true|false |  ||
|SortNames|Boolean|true|false |  ||
|ValidateMergedAreas|Boolean|true|false |  ||
|MergeAreas|Boolean|true|false |  ||
|SortExternalNames|Boolean|true|false |  ||
|CheckExcelRestriction|Boolean|true|false |  ||
|UpdateSmartArt|Boolean|true|false |  ||
|EncryptDocumentProperties|Boolean|true|false |  ||

## **TxtSaveOptions Properties**

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description |
| :- | :- | :- |:- |  :- | :- |
|QuoteType|String|true|false |  ||
|Separator|String|true|false |  ||
|SeparatorString|String|true|false |  ||
|AlwaysQuoted|Boolean|true|false |  ||
|SaveFormat|String|true|false |  ||
|CachedFileFolder|String|true|false |  ||
|ClearData|Boolean|true|false |  ||
|CreateDirectory|Boolean|true|false |  ||
|EnableHTTPCompression|Boolean|true|false |  ||
|RefreshChartCache|Boolean|true|false |  ||
|SortNames|Boolean|true|false |  ||
|ValidateMergedAreas|Boolean|true|false |  ||
|MergeAreas|Boolean|true|false |  ||
|SortExternalNames|Boolean|true|false |  ||
|CheckExcelRestriction|Boolean|true|false |  ||
|UpdateSmartArt|Boolean|true|false |  ||
|EncryptDocumentProperties|Boolean|true|false |  ||

## **XlsSaveOptions&XlsbSaveOptions Properties**

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description |
| :- | :- | :- |:- |  :- | :- |
|MatchColor|Boolean|true|false |  ||
|WpsCompatibility|Boolean|true|false |  ||
|SaveFormat|String|true|false |  ||
|CachedFileFolder|String|true|false |  ||
|ClearData|Boolean|true|false |  ||
|CreateDirectory|Boolean|true|false |  ||
|EnableHTTPCompression|Boolean|true|false |  ||
|RefreshChartCache|Boolean|true|false |  ||
|SortNames|Boolean|true|false |  ||
|ValidateMergedAreas|Boolean|true|false |  ||
|MergeAreas|Boolean|true|false |  ||
|SortExternalNames|Boolean|true|false |  ||
|CheckExcelRestriction|Boolean|true|false |  ||
|UpdateSmartArt|Boolean|true|false |  ||
|EncryptDocumentProperties|Boolean|true|false |  ||

## **XmlSaveOptions Properties**

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description |
| :- | :- | :- |:- |  :- | :- |
|SheetIndexes|Array|true|false |  ||
|ExportArea|Class|true|false |  ||
|HasHeaderRow|Boolean|true|false |  ||
|XmlMapName|String|true|false |  ||
|SheetNameAsElementName|Boolean|true|false |  ||
|DataAsAttribute|Boolean|true|false |  ||
|SaveFormat|String|true|false |  ||
|CachedFileFolder|String|true|false |  ||
|ClearData|Boolean|true|false |  ||
|CreateDirectory|Boolean|true|false |  ||
|EnableHTTPCompression|Boolean|true|false |  ||
|RefreshChartCache|Boolean|true|false |  ||
|SortNames|Boolean|true|false |  ||
|ValidateMergedAreas|Boolean|true|false |  ||
|MergeAreas|Boolean|true|false |  ||
|SortExternalNames|Boolean|true|false |  ||
|CheckExcelRestriction|Boolean|true|false |  ||
|UpdateSmartArt|Boolean|true|false |  ||
|EncryptDocumentProperties|Boolean|true|false |  ||

## **XpsSaveOptions Properties**

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description |
| :- | :- | :- |:- |  :- | :- |
|DefaultFont|String|true|false |  ||
|CheckWorkbookDefaultFont|Boolean|true|false |  ||
|CheckFontCompatibility|Boolean|true|false |  ||
|IsFontSubstitutionCharGranularity|Boolean|true|false |  ||
|OnePagePerSheet|Boolean|true|false |  ||
|AllColumnsInOnePagePerSheet|Boolean|true|false |  ||
|IgnoreError|Boolean|true|false |  ||
|OutputBlankPageWhenNothingToPrint|Boolean|true|false |  ||
|PageIndex|Integer|true|false |  ||
|PageCount|Integer|true|false |  ||
|PrintingPageType|String|true|false |  ||
|GridlineType|String|true|false |  ||
|TextCrossType|String|true|false |  ||
|DefaultEditLanguage|String|true|false |  ||
|EmfRenderSetting|String|true|false |  ||
|MergeAreas|Boolean|true|false |  ||
|SortExternalNames|Boolean|true|false |  ||
|UpdateSmartArt|Boolean|true|false |  ||
|SaveFormat|String|true|false |  ||
|CachedFileFolder|String|true|false |  ||
|ClearData|Boolean|true|false |  ||
|CreateDirectory|Boolean|true|false |  ||
|EnableHTTPCompression|Boolean|true|false |  ||
|RefreshChartCache|Boolean|true|false |  ||
|SortNames|Boolean|true|false |  ||
|ValidateMergedAreas|Boolean|true|false |  ||
|CheckExcelRestriction|Boolean|true|false |  ||
|EncryptDocumentProperties|Boolean|true|false |  ||
