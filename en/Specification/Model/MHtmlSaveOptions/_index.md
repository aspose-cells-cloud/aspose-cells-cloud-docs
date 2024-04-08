---
title: "MHtmlSaveOptions"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /mhtmlsaveoptions/
description: "Represents options of saving .mhtml file."
weight: 50
---

## **mHtmlSaveOptions**

Represents options of saving .mhtml file. 

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description | 
| :- | :- | :- |:- |  :- | :- |
| AttachedFilesDirectory | String | True |  False |  | The directory that the attached files will be saved to.  Only for saving to html stream. |  
| AttachedFilesUrlPrefix | String | True |  False |  | Specify the Url prefix of attached files such as image in the html file. Only for saving to html stream. |  
| Encoding | String | True |  False |  | If not set,use Encoding.UTF8 as default enconding type. |  
| ExportActiveWorksheetOnly | Boolean | True |  False |  | Indicates if exporting the whole workbook to html file. |  
| ExportChartImageFormat | String | True |  False |  | Get or set the format of chart image before exporting |  
| ExportImagesAsBase64 | Boolean | True |  False |  | Specifies whether images are saved in Base64 format to HTML, MHTML or EPUB. |  
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

