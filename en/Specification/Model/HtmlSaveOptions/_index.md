---
title: "HtmlSaveOptions"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /specification/model/htmlsaveoptions/
description: "Represents options of saving .html file."
weight: 50
---

## **htmlSaveOptions**

Represents options of saving .html file. 

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description | 
| :- | :- | :- |:- |  :- | :- |
| ExportPageHeaders | Boolean | True |  False |  |  |  
| ExportPageFooters | Boolean | True |  False |  |  |  
| ExportRowColumnHeadings | Boolean | True |  False |  |  |  
| ShowAllSheets | Boolean | True |  False |  |  |  
| ImageOptions | Class:ImageOrPrintOptions | True |  False |  |  |  
| SaveAsSingleFile | Boolean | True |  False |  | Indicates whether save the html as single file. The default value is false. |  
| ExportHiddenWorksheet | Boolean | True |  False |  | Indicates whether save the html as single file. The default value is false. |  
| ExportGridLines | Boolean | True |  False |  | Indicating whether exporting the gridlines.The default value is false. |  
| PresentationPreference | Boolean | True |  False |  | Indicating if html or mht file is presentation preference.The default value is             false.if you want to get more beautiful presentation,please set the value to                true. |  
| CellCssPrefix | String | True |  False |  | Gets and sets the prefix of the css name,the default value is "". |  
| TableCssId | String | True |  False |  | Gets and sets the prefix of the type css name such as tr,col,td and so on, they                are contained in the table element which has the specific TableCssId attribute.                The default value is "". |  
| IsFullPathLink | Boolean | True |  False |  | Indicating whether using full path link in sheet00x.htm,filelist.xml and tabstrip.htm.                The default value is false. |  
| ExportWorksheetCSSSeparately | Boolean | True |  False |  | Indicating whether export the worksheet css separately.The default value is false. |  
| ExportSimilarBorderStyle | Boolean | True |  False |  |  |  
| MergeEmptyTdForcely | Boolean | True |  False |  | Indicates whether merging empty TD element forcely when exporting file to html.                The size of html file will be reduced significantly after setting value to true.                The default value is false. If you want to import the html file to excel or export                perfect grid lines when saving file to html, please keep the default value. |  
| ExportCellCoordinate | Boolean | True |  False |  | Indicates whether exporting excel coordinate of nonblank cells when saving file                to html. The default value is false. If you want to import the output html to                excel, please keep the default value. |  
| ExportExtraHeadings | Boolean | True |  False |  | Indicates whether exporting extra headings when the length of text is longer                than max display column. The default value is false. If you want to import the                html file to excel, please keep the default value. |  
| ExportHeadings | Boolean | True |  False |  | Indicates whether exporting headings when saving file to html.The default value                is false. If you want to import the html file to excel, please keep the default                value. |  
| ExportFormula | Boolean | True |  False |  | Indicates whether exporting formula when saving file to html. The default value                is true. If you want to import the output html to excel, please keep the default                value |  
| AddTooltipText | Boolean | True |  False |  | Indicates whether adding tooltip text when the data can't be fully displayed. |  
| ExportBogusRowData | Boolean | True |  False |  | Indicating whether exporting bogus bottom row data. The default value is true.If you want to import the html or mht file to excel, please keep the default value. |  
| ExcludeUnusedStyles | Boolean | True |  False |  | Indicating whether excluding unused styles.The default value is false.If you  want to import the html or mht file to excel, please keep the default value. |  
| ExportDocumentProperties | Boolean | True |  False |  | Indicating whether exporting document properties.The default value is true.If  you want to import the html or mht file to excel, please keep the default value. |  
| ExportWorksheetProperties | Boolean | True |  False |  | Indicating whether exporting worksheet properties.The default value is true.If  you want to import the html or mht file to excel, please keep the default value. |  
| ExportWorkbookProperties | Boolean | True |  False |  | Indicating whether exporting workbook properties.The default value is true.If  you want to import the html or mht file to excel, please keep the default value. |  
| ExportFrameScriptsAndProperties | Boolean | True |  False |  | Indicating whether exporting frame scripts and document properties. The default  value is true.If you want to import the html or mht file to excel, please keep the default value. |  
| AttachedFilesDirectory | String | True |  False |  | The directory that the attached files will be saved to.  Only for saving to html stream. |  
| AttachedFilesUrlPrefix | String | True |  False |  | Specify the Url prefix of attached files such as image in the html file. Only for saving to html stream. |  
| Encoding | String | True |  False |  |  |  
| ExportActiveWorksheetOnly | Boolean | True |  False |  | Indicates if exporting the whole workbook to html file. |  
| ExportChartImageFormat | String | True |  False |  | Get or set the format of chart image before exporting |  
| ExportImagesAsBase64 | Boolean | True |  False |  |  |  
| HiddenColDisplayType | String | True |  False |  | Hidden column(the width of this column is 0) in excel,before save this into                html format, if HtmlHiddenColDisplayType is "Remove",the hidden column would               ont been output, if the value is "Hidden", the column would been output,but was hidden,the default value is "Hidden" |  
| HiddenRowDisplayType | String | True |  False |  | Hidden row(the height of this row is 0) in excel,before save this into html                format, if HtmlHiddenRowDisplayType is "Remove",the hidden row would ont               been output, if the value is "Hidden", the row would been output,but was               hidden,the default value is "Hidden" |  
| HtmlCrossStringType | String | True |  False |  | Indicates if a cross-cell string will be displayed in the same way as MS               Excel when saving an Excel file in html format.  By default the value is               Default, so, for cross-cell strings, there is little difference between the               html files created by Aspose.Cells and MS Excel. But the performance for               creating large html files,setting the value to Cross would be several times               faster than setting it to Default or Fit2Cell. |  
| IsExpImageToTempDir | Boolean | True |  False |  | Indicates if export image files to temp directory.  Only for saving to html  stream. |  
| PageTitle | String | True |  False |  | The title of the html page.  Only for saving to html stream. |  
| ParseHtmlTagInCell | Boolean | True |  False |  | Parse html tag in cell,like ,as cell value,or as html tag,default is true |  
| SaveFormat | String | True |  False |  |  |  
| CachedFileFolder | String | True |  False |  |  |  
| ClearData | Boolean | True |  False |  |  |  
| CreateDirectory | Boolean | True |  False |  |  |  
| EnableHTTPCompression | Boolean | True |  False |  |  |  
| RefreshChartCache | Boolean | True |  False |  |  |  
| SortNames | Boolean | True |  False |  |  |  
| ValidateMergedAreas | Boolean | True |  False |  |  |  

**Parent Name** : (SaveOptions)[saveoptions]

