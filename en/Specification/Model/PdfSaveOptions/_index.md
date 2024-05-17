---
title: "PdfSaveOptions"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /specification/model/pdfsaveoptions/
description: "Aspose.Cells Cloud model specification : PdfSaveOptions. Effortlessly handle Excel and other spreadsheet documents with features like opening, generating, editing, splitting, merging, comparing, and converting."
kwords: Excel, Office, Spreadsheet, Cloud REST API, PdfSaveOptions
weight: 50
---

## **pdfSaveOptions**

Represents options of saving pdf file. 

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description | 
| :- | :- | :- |:- |  :- | :- |
| DisplayDocTitle | Boolean | True |  False |  | Indicates whether the window's title bar should display the document title. |  
| ExportDocumentStructure | Boolean | True |  False |  | Indicates whether to export document structure. |  
| EmfRenderSetting | String | True |  False |  | Setting for rendering Emf metafile. |  
| CustomPropertiesExport | String | True |  False |  | Specifies the way CustomDocumentPropertyCollection are exported to PDF file. |  
| OptimizationType | String | True |  False |  | Gets and sets pdf optimization type. |  
| Producer | String | True |  False |  | Gets and sets producer of generated pdf document. |  
| PdfCompression | String | True |  False |  | Indicate the compression algorithm. |  
| FontEncoding | String | True |  False |  | Gets or sets embedded font encoding in pdf. |  
| Watermark | Class:RenderingWatermark | True |  False |  | Gets or sets watermark to output. |  
| CalculateFormula | Boolean | True |  False |  | Indicates whether calculate formulas before saving pdf file.The default value is false. |  
| CheckFontCompatibility | Boolean | True |  False |  | Indicates whether check font compatibility for every character in text.                The default value is true.  Disable this property may give better performance.                 But when the default or specified font of text/character cannot be used                to render it, unreadable characters(such as block) maybe occur in the generated                pdf.  For such situation user should keep this property as true so that alternative                font can be searched and used to render the text instead; |  
| Compliance | String | True |  False |  | Workbook converts to pdf will according to PdfCompliance in this property. |  
| DefaultFont | String | True |  False |  | When characters in the Excel are unicode and not be set with correct font in cell style,              They may appear as block in pdf,image.  Set the DefaultFont such as MingLiu or MS Gothic to show these characters.               If this property is not set, Aspose.Cells will use system default font to show these unicode characters. |  
| OnePagePerSheet | Boolean | True |  False |  | If OnePagePerSheet is true , all content of one sheet will output to only            one page in result. The paper size of pagesetup will be invalid, and the               other settings of pagesetup will still take effect. |  
| PrintingPageType | String | True |  False |  | Indicates which pages will not be printed. |  
| SecurityOptions | Class:PdfSecurityOptions | True |  False |  | Set this options, when security is need in xls2pdf result. |  
| desiredPPI | Integer | True |  False |  | Set desired PPI(pixels per inch) of resample images and jpeg quality  All images will be converted to JPEG with the specified quality setting, and images that are greater than the specified PPI (pixels per inch) will be resampled.              Desired pixels per inch. 220 high quality. 150 screen quality. 96 email quality. |  
| jpegQuality | Integer | True |  False |  | Set desired PPI(pixels per inch) of resample images and jpeg quality  All images will be converted to JPEG with the specified quality setting, and images that are greater than the specified PPI (pixels per inch) will be resampled.              0 - 100% JPEG quality. |  
| ImageType | String | True |  False |  | Represents the image type when converting the chart and shape . |  
| SaveFormat | String | True |  False |  |  |  
| CachedFileFolder | String | True |  False |  |  |  
| ClearData | Boolean | True |  False |  |  |  
| CreateDirectory | Boolean | True |  False |  |  |  
| EnableHTTPCompression | Boolean | True |  False |  |  |  
| RefreshChartCache | Boolean | True |  False |  |  |  
| SortNames | Boolean | True |  False |  |  |  
| ValidateMergedAreas | Boolean | True |  False |  |  |  

**Parent Name** : [SaveOptions](/specification/model/saveoptions)

