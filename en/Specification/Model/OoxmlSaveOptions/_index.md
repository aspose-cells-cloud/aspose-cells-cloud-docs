---
title: "OoxmlSaveOptions"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /specification/model/ooxmlsaveoptions/
description: "Aspose.Cells Cloud model specification : OoxmlSaveOptions. Effortlessly handle Excel and other spreadsheet documents with features like opening, generating, editing, splitting, merging, comparing, and converting."
kwords: Excel, Office, Spreadsheet, Cloud REST API, OoxmlSaveOptions
weight: 50
---

## **ooxmlSaveOptions**

Represents options of saving ooxml file. 

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description | 
| :- | :- | :- |:- |  :- | :- |
| ExportCellName | Boolean | True |  False |  | Indicates if export cell name to Excel2007 .xlsx (.xlsm, .xltx, .xltm) file.               If the output file may be accessed by SQL Server DTS, this value must be               true.  Setting the value to false will highly increase the performance and               reduce the file size when creating large file.  Default value is false. |  
| UpdateZoom | Boolean | True |  False |  | Indicates whether update scaling factor before saving the file if the PageSetup.FitToPagesWide and PageSetup.FitToPagesTall properties control how the worksheet is scaled. |  
| EnableZip64 | Boolean | True |  False |  | Always use ZIP64 extensions when writing zip archives, even when unnecessary. |  
| EmbedOoxmlAsOleObject | Boolean | True |  False |  | Indicates whether embedding Ooxml files of OleObject as ole object. |  
| CompressionType | String | True |  False |  | Gets and sets the compression type for ooxml file. |  
| SaveFormat | String | True |  False |  |  |  
| CachedFileFolder | String | True |  False |  |  |  
| ClearData | Boolean | True |  False |  |  |  
| CreateDirectory | Boolean | True |  False |  |  |  
| EnableHTTPCompression | Boolean | True |  False |  |  |  
| RefreshChartCache | Boolean | True |  False |  |  |  
| SortNames | Boolean | True |  False |  |  |  
| ValidateMergedAreas | Boolean | True |  False |  |  |  

**Parent Name** : [SaveOptions](/specification/model/saveoptions)

