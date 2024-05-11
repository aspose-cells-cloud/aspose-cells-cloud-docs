---
title: "PageSetup"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /specification/model/pagesetup/
description: "Aspose.Cells Cloud model specification : PageSetup. Effortlessly handle Excel and other spreadsheet documents with features like opening, generating, editing, splitting, merging, comparing, and converting."
weight: 50
---

## **pageSetup**

excel print page setting 

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description | 
| :- | :- | :- |:- |  :- | :- |
| BlackAndWhite | Boolean | True |  False |  | Represents if elements of the document will be printed in black and white. |  
| BottomMargin | Floating | True |  False |  | Represents the size of the bottom margin, in unit of centimeters. |  
| CenterHorizontally | Boolean | True |  False |  | Represent if the sheet is printed centered horizontally. |  
| CenterVertically | Boolean | True |  False |  | Represent if the sheet is printed centered vertically. |  
| FirstPageNumber | Integer | True |  False |  | Represents the first page number that will be used when this sheet is printed. |  
| FitToPagesTall | Integer | True |  False |  | Represents  the number of pages tall the worksheet will be scaled to when it's printed.                        The default value is 1. |  
| FitToPagesWide | Integer | True |  False |  | Represents the number of pages wide the worksheet will be scaled to when it's printed.                        The default value is 1. |  
| FooterMargin | Floating | True |  False |  | Represents the distance from the bottom of the page to the footer, in unit of centimeters. |  
| HeaderMargin | Floating | True |  False |  | Represents the distance from the top of the page to the header, in unit of centimeters. |  
| IsAutoFirstPageNumber | Boolean | True |  False |  | Indicates whether the first the page number is automatically assigned. |  
| IsHFAlignMargins | Boolean | True |  False |  | Indicates whether header and footer margins are aligned with the page margins.                        If this property is true, the left header and footer will be aligned with the left margin,                        and the right header and footer will be aligned with the right margin.                        This option is enabled by default. |  
| IsHFDiffFirst | Boolean | True |  False |  | True means that the header/footer of the first page is different with other pages. |  
| IsHFDiffOddEven | Boolean | True |  False |  | True means that the header/footer of the odd pages is different with odd pages. |  
| IsHFScaleWithDoc | Boolean | True |  False |  | Indicates whether header and footer are scaled with document scaling.                        Only applies for Excel 2007. |  
| IsPercentScale | Boolean | True |  False |  | If this property is False, the FitToPagesWide and FitToPagesTall properties control how the worksheet is scaled. |  
| LeftMargin | Floating | True |  False |  | Represents the size of the left margin, in unit of centimeters. |  
| Order | String | True |  False |  | Represents the order that Microsoft Excel uses to number pages when printing a large worksheet. |  
| Orientation | String | True |  False |  | Represents page print orientation. |  
| PaperSize | String | True |  False |  | Represents the size of the paper. |  
| PrintArea | String | True |  False |  | Represents the range to be printed. |  
| PrintComments | String | True |  False |  | Represents the way comments are printed with the sheet. |  
| PrintCopies | Integer | True |  False |  | Get and sets number of copies to print. |  
| PrintDraft | Boolean | True |  False |  | Represents if the sheet will be printed without graphics. |  
| PrintErrors | String | True |  False |  | Specifies the type of print error displayed. |  
| PrintGridlines | Boolean | True |  False |  | Represents if cell gridlines are printed on the page. |  
| PrintHeadings | Boolean | True |  False |  | Represents if row and column headings are printed with this page. |  
| PrintQuality | Integer | True |  False |  | Represents the print quality. |  
| PrintTitleColumns | String | True |  False |  | Represents the columns that contain the cells to be repeated on the left side of each page. |  
| PrintTitleRows | String | True |  False |  | Represents the rows that contain the cells to be repeated at the top of each page. |  
| RightMargin | Floating | True |  False |  | Represents the size of the right margin, in unit of centimeters. |  
| TopMargin | Floating | True |  False |  | Represents the size of the top margin, in unit of centimeters. |  
| Zoom | Integer | True |  False |  | Represents the scaling factor in percent. It should be between 10 and 400. |  
| Header | Container | True |  False |  | Represents the page header. |  
| Footer | Container | True |  False |  | Represents the page footor. |  
| link | Class:Link | True |  False |  |  |  

**Parent Name** : [LinkElement](linkelement)

