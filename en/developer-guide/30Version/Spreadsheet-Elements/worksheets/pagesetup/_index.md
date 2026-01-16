---  
title: "Worksheet page setup"  
second_title: "Document"  
linktitle: "Page setup"  
type: docs  
url: /page-setup/  
keywords: "Excel, worksheet, page setup, print settings, margins, orientation, paper size, header, footer, scaling"  
description: "Documentation for the **pageSetup** object in Aspose.Cells Cloud, detailing properties used to configure Excel worksheet print layout such as margins, orientation, scaling, headers, footers, and other print options."  
weight: 20  
---  

# **pageSetup**

Excel print page settings  

## **Properties**

| Property Name            | Property Type | Nullable | ReadOnly | DefaultValue | Description |
|--------------------------|---------------|----------|----------|--------------|-------------|
| BlackAndWhite            | Boolean       | true     | false    |              | Indicates whether the worksheet will be printed in black and white. |
| BottomMargin             | Floating      | true     | false    |              | Size of the bottom margin in centimeters. |
| CenterHorizontally       | Boolean       | true     | false    |              | Indicates whether the sheet is centered horizontally when printed. |
| CenterVertically         | Boolean       | true     | false    |              | Indicates whether the sheet is centered vertically when printed. |
| FirstPageNumber          | Integer       | true     | false    |              | The first page number used when the sheet is printed. |
| FitToPagesTall           | Integer       | true     | false    | 1            | Number of pages tall to which the worksheet will be scaled when printed. |
| FitToPagesWide           | Integer       | true     | false    | 1            | Number of pages wide to which the worksheet will be scaled when printed. |
| FooterMargin             | Floating      | true     | false    |              | Distance from the bottom of the page to the footer, in centimeters. |
| HeaderMargin             | Floating      | true     | false    |              | Distance from the top of the page to the header, in centimeters. |
| IsAutoFirstPageNumber   | Boolean       | true     | false    |              | Indicates whether the first page number is assigned automatically. |
| IsHFAlignMargins         | Boolean       | true     | false    |              | When true, header and footer margins align with the page margins (left with left, right with right). Enabled by default. |
| IsHFDiffFirst            | Boolean       | true     | false    |              | Indicates that the header/footer on the first page differs from other pages. |
| IsHFDiffOddEven          | Boolean       | true     | false    |              | Indicates that the header/footer on odd pages differs from even pages. |
| IsHFScaleWithDoc         | Boolean       | true     | false    |              | Determines whether the header and footer are scaled together with the document (applies to Excel 2007). |
| IsPercentScale           | Boolean       | true     | false    |              | When false, the `FitToPagesWide` and `FitToPagesTall` properties control worksheet scaling. |
| LeftMargin               | Floating      | true     | false    |              | Size of the left margin in centimeters. |
| Order                    | String        | true     | false    |              | The order Excel uses to number pages when printing a large worksheet. |
| Orientation              | String        | true     | false    |              | Page orientation: **Landscape** or **Portrait**. |
| PaperSize                | String        | true     | false    |              | Paper size used for printing. |
| PrintArea                | String        | true     | false    |              | Range of cells to be printed. |
| PrintComments            | String        | true     | false    |              | How comments are printed with the sheet. |
| PrintCopies              | Integer       | true     | false    |              | Number of copies to print. |
| PrintDraft               | Boolean       | true     | false    |              | Indicates whether the sheet is printed without graphics (draft mode). |
| PrintErrors              | String        | true     | false    |              | Type of print error displayed. |
| PrintGridlines           | Boolean       | true     | false    |              | Indicates whether cell gridlines are printed. |
| PrintHeadings            | Boolean       | true     | false    |              | Indicates whether row and column headings are printed. |
| PrintQuality             | Integer       | true     | false    |              | Print quality setting. |
| PrintTitleColumns        | String        | true     | false    |              | Columns to repeat on the left side of each printed page. |
| PrintTitleRows           | String        | true     | false    |              | Rows to repeat at the top of each printed page. |
| RightMargin              | Floating      | true     | false    |              | Size of the right margin in centimeters. |
| TopMargin                | Floating      | true     | false    |              | Size of the top margin in centimeters. |
| Zoom                     | Integer       | true     | false    |              | Scaling factor in percent (10–400%). |
| Header                   | Container     | true     | false    |              | Page header configuration. |
| Footer                   | Container     | true     | false    |              | Page footer configuration. |