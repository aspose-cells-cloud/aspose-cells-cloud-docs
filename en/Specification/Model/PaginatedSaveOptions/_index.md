---
title: "PaginatedSaveOptions"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /paginatedsaveoptions/
description: "Represents the options for pagination."
weight: 50
---

## **paginatedSaveOptions**

Represents the options for pagination. 

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description | 
| :- | :- | :- |:- |  :- | :- |
| DefaultFont | String | True |  False |  | When characters in the Excel are Unicode and not be set with correct font in cell style,They may appear as block in pdf,image.Set the DefaultFont such as MingLiu or MS Gothic to show these characters. If this property is not set, Aspose.Cells will use system default font to show these unicode characters. |  
| CheckWorkbookDefaultFont | Boolean | True |  False |  | When characters in the Excel are Unicode and not be set with correct font in cell style,They may appear as block in pdf,image.Set this to true to try to use workbook's default font to show these characters first. |  
| CheckFontCompatibility | Boolean | True |  False |  | Indicates whether to check font compatibility for every character in text. |  
| IsFontSubstitutionCharGranularity | Boolean | True |  False |  | Indicates whether to only substitute the font of character when the cell font is not compatibility for it. |  
| OnePagePerSheet | Boolean | True |  False |  | If OnePagePerSheet is true , all content of one sheet will output to only one page in result.The paper size of pagesetup will be invalid, and the other settings of pagesetup will still take effect. |  
| AllColumnsInOnePagePerSheet | Boolean | True |  False |  | If AllColumnsInOnePagePerSheet is true , all column content of one sheet will output to only one page in result.The width of paper size of pagesetup will be ignored, and the other settings of pagesetup will still take effect. |  
| IgnoreError | Boolean | True |  False |  | Indicates if you need to hide the error while rendering.The error can be error in shape, image, chart rendering, etc. |  
| OutputBlankPageWhenNothingToPrint | Boolean | True |  False |  | Indicates whether to output a blank page when there is nothing to print. |  
| PageIndex | Integer | True |  False |  | Gets or sets the 0-based index of the first page to save. |  
| PageCount | Integer | True |  False |  | Gets or sets the number of pages to save. |  
| PrintingPageType | String | True |  False |  | Indicates which pages will not be printed. |  
| GridlineType | String | True |  False |  | Gets or sets gridline type. |  
| TextCrossType | String | True |  False |  | Gets or sets displaying text type when the text width is larger than cell width. |  
| DefaultEditLanguage | String | True |  False |  | Gets or sets default edit language. |  
| EmfRenderSetting | String | True |  False |  |  |  
| MergeAreas | Boolean | True |  False |  |  |  
| SortExternalNames | Boolean | True |  False |  |  |  
| UpdateSmartArt | Boolean | True |  False |  |  |  
| SaveFormat | String | True |  False |  |  |  
| CachedFileFolder | String | True |  False |  |  |  
| ClearData | Boolean | True |  False |  |  |  
| CreateDirectory | Boolean | True |  False |  |  |  
| EnableHTTPCompression | Boolean | True |  False |  |  |  
| RefreshChartCache | Boolean | True |  False |  |  |  
| SortNames | Boolean | True |  False |  |  |  
| ValidateMergedAreas | Boolean | True |  False |  |  |  

**Parent Name** : (SaveOptions)[saveoptions]

**Children Name** : 
	-  [DocxSaveOptions](docxsaveoptions) 
	-  [PptxSaveOptions](pptxsaveoptions) 
	-  [XpsSaveOptions](xpssaveoptions) 
