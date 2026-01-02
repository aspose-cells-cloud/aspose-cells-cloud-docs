---
title: "Aspose.Cells Cloud Web API - Convert a Spreadsheet to another format file."
second_title: "Document"
ArticleTitle: "Convert a Spreadsheet to another format file."
linktitle: "Convert Spreadsheet"
type: docs
url: /convert-spreadsheet/
keywords: "spreadsheet conversion, convert spreadsheet, cloud conversion, REST API, XLSX, PDF, CSV, JSON, Markdown, convert local files"
description: "Effortlessly converts a spreadsheet from a local drive to various specified formats using the Excel API."
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet Conversion, PDF, CSV, JSON, Markdown, Match all blank cells in an Excel worksheet
---

Convert a local spreadsheet/Excel file to other format file with the Aspose.Cells Cloud Web API.

|**Out Format**|**Description**|
| :- | :- |
|[XLS](https://docs.fileformat.com/spreadsheet/xls/)|Excel 95/5.0 - 2003 Workbook.|
|[XLSX](https://docs.fileformat.com/spreadsheet/xlsx/)|The Office Open XML SpreadsheetML File Format.|
|[XLSB](https://docs.fileformat.com/spreadsheet/xlsb/)|Excel Binary Workbook.|
|[XLSM](https://docs.fileformat.com/spreadsheet/xlsm/)|Excel Macro-Enabled Workbook.|
|[XLT](https://docs.fileformat.com/spreadsheet/xlt/)|Excel 97 - Excel 2003 Template.|
|[XLTX](https://docs.fileformat.com/spreadsheet/xltx/)|Excel Template.|
|[XLTM](https://docs.fileformat.com/spreadsheet/xltm/)|Excel Macro-Enabled Template.|
|[XLAM](https://docs.fileformat.com/spreadsheet/xlam/)|An Excel Macro-Enabled Add-In file that's used to add new functions to Excel.|
|[CSV](https://docs.fileformat.com/spreadsheet/csv/)|CSV (Comma Separated Value) file.|
|[TSV](https://docs.fileformat.com/spreadsheet/tsv/)|TSV (Tab-separated values) file.|
|[TXT](https://docs.fileformat.com/word-processing/txt/)|Delimited plain text file.|
|[HTML](https://docs.fileformat.com/web/html/)|HTML format.|
|[MHTML](https://docs.fileformat.com/web/mhtml/)|MHTML file.|
|[ODS](https://docs.fileformat.com/spreadsheet/ods/)|ODS (OpenDocument Spreadsheet).|
|SpreadsheetML|Excel 2003 XML file.|
|[Numbers](https://docs.fileformat.com/spreadsheet/numbers/)|The document is created by Apple's "Numbers" application which forms part of Apple's iWork office suite, a set of applications which run on the Mac OS X and iOS operating systems.|
|[JSON](https://docs.fileformat.com/web/json/)|JavaScript Object Notation|
|[DIF](https://docs.fileformat.com/spreadsheet/dif/)|Data Interchange Format.|
|[DBF](https://docs.fileformat.com/database/dbf/)|The file with .dbf extension is a database file used by a database management system application called dBASE.|
|[PDF](https://docs.fileformat.com/pdf/)|Adobe Portable Document Format.|
|[XPS](https://docs.fileformat.com/page-description-language/xps/)|XML Paper Specification Format.|
|[SVG](https://docs.fileformat.com/page-description-language/svg/)|Scalable Vector Graphics Format.|
|[TIFF](https://docs.fileformat.com/image/tiff/)|Tagged Image File Format|
|[PNG](https://docs.fileformat.com/image/png/)|Portable Network Graphics Format|
|[BMP](https://docs.fileformat.com/image/bmp/)|Bitmap Image Format|
|[EMF](https://docs.fileformat.com/image/emf/)|Enhanced metafile Format|
|[JPEG](https://docs.fileformat.com/image/jpeg/)|JPEG is a type of image format that is saved using the method of lossy compression.|
|[GIF](https://docs.fileformat.com/image/gif/)|Graphical Interchange Format|
|[MARKDOWN](https://docs.fileformat.com/word-processing/md/)|Represents a markdown document.|
|[SXC](https://docs.fileformat.com/spreadsheet/sxc/)|An XML based format used by OpenOffice and StarOffice|
|[FODS](https://docs.fileformat.com/spreadsheet/fods/)|This is an Open Document format stored as flat XML.|
|[DOCX](https://docs.fileformat.com/word-processing/docx/)|A well-known format for Microsoft Word documents that is a combination of XML and binary files.|
|[PPTX](https://docs.fileformat.com/presentation/pptx/)|The PPTX format is based on the Microsoft PowerPoint open XML presentation file format.|
|[SqlScript](https://docs.fileformat.com/database/sql/)|Structured Query Language.|
|[XHtml](https://docs.fileformat.com/web/xhtml/)|The XHTML is a text based file format with markup in the XML, using a reformulation of HTML 4.0.|
|[Epub](https://docs.fileformat.com/ebook/epub/)|Files with .epub extension are an e-book file format that provide a standard digital publication format for publishers and consumers.|
|[Xml](https://docs.fileformat.com/web/xml/)|XML stands for Extensible Markup Language that is similar to HTML but different in using tags for defining objects.|
|[Ots](https://docs.fileformat.com/spreadsheet/ots/)|Open Document Template Sheet(OTS) file.|
|[AZW3](https://docs.fileformat.com/ebook/azw3/)|AZW is a digital ebook file format developed by Amazon for its Kindle devices. AZW3, also known as Kindle Format 8 (KF8).|

## **Convert Spreadsheet API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/spreadsheet
```

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
|Spreadsheet|File|FormData|Upload the spreadsheet file to be converted.|
|format|String|Query|(Required) The desired output format (e.g., "Xlsx", "PDF", "CSV").|
|outPath|String|Query|(Optional) The folder path where the converted workbook will be stored. The default is null.|
|outStorageName|String|Query|Specify an output file storage name.|
|fontsLocation|String|Query|Use custom fonts for the spreadsheet.|
|region|String|Query|Specify the spreadsheet region setting.|
|password|String|Query|The password for opening the spreadsheet file if it is protected.|

### **Response**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
            "Identifier": "File",
            "Reference": "Stream"
        }
    }
]
```

### Error Codes

- **400 Bad Request**: Invalid Aspose.Cells Cloud API URI.
- **401 Unauthorized**: Invalid access token. Or invalid client id and secret.
- **404 Not Found**: The spreadsheet file not accessible.
- **500 Server Error**: The spreadsheet has encountered an anomaly in obtaining calculation data.

## Why should you use the Convert Spreadsheet API?

- No need for cloud storage, reducing the burden on cloud resources.
- Development can be quickly completed through the existing SDK.

## How to Use the Convert Spreadsheet API with SDKs?

### Convert Spreadsheet API Specification

The [Convert Spreadsheet API Specification](https://reference.aspose.cloud/cells/#/ConversionController/ConvertSpreadsheet) defines a publicly accessible programming interface, allowing you to perform REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low-level details, allowing you to convert a spreadsheet file to another format file with short code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to invoke Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorkbook.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorkbook.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorkbook.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorkbook.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorkbook.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorkbook.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorkbook.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorkbook.go" >}}
{{</tab>}}
{{< /tabs >}}
