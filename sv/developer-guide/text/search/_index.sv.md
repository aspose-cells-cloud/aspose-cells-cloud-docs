---
title: Hitta text från filen Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Hitta utan att använda lagring
type: docs
url: /sv/search/
aliases: [/search-without-using-storage/,/search-without-storage/]
keywords: Find text from Microsoft Excel (XLS, XLSX, XLSM, XLSB) and Open Document Spreadsheet (ODS) files
description: Aspose.Cells Cloud REST API stöder att hitta text från Excel-filer. SDK stöder olika utvecklingsspråk. De inkluderar Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby och swift
weight: 50
---
Denna REST API indikerar till `search` text från Excel filer.
`## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/search
 
```
The request parameters are: 
 
| Parameter Name | Type | Path/Query String/HTTPBody | Description| 
| :- | :- | :- |:- | 
| file | file | formData | File to upload |
| text | string | query |   |
| password | string | query |   |
| sheetname | string | query |   |
 
The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/LiteCells/PostSearch) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.
 
You can use cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/search?text=1" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"\
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx'  
```
 
{{< /tab >}}
 
{{< tab tabNum="2" >}}
 
```bash
[{
	"Text": "12/31/1899 10:10:00 AM",
	"link": {
		"Href": "Book1.xlsx/worksheets/Sheet5",
		"Rel": "parent"
	}
}, {
	"Text": "12/31/1899 11:10:00 AM",
	"link": {
		"Href": "Book1.xlsx/worksheets/Sheet5",
		"Rel": "parent"
	}
}, {
	"Text": "12/31/1899 12:10:00 PM",
	"link": {
		"Href": "Book1.xlsx/worksheets/Sheet5",
		"Rel": "parent"
	}
}, {
	"Text": "12/31/1899 1:10:00 PM",
	"link": {
		"Href": "Book1.xlsx/worksheets/Sheet5",
		"Rel": "parent"
	}
}, {
	"Text": "12/31/1899 2:10:00 PM",
	"link": {
		"Href": "Book1.xlsx/worksheets/Sheet5",
		"Rel": "parent"
	}
}, {
	"Text": "12/31/1899 3:10:00 PM",
	"link": {
		"Href": "Book1.xlsx/worksheets/Sheet5",
		"Rel": "parent"
	}
}, {
	"Text": "12/31/1899 4:10:00 PM",
	"link": {
		"Href": "Book1.xlsx/worksheets/Sheet5",
		"Rel": "parent"
	}
}, {
	"Text": "12/31/1899 5:10:00 PM",
	"link": {
		"Href": "Book1.xlsx/worksheets/Sheet5",
		"Rel": "parent"
	}
}, {
	"Text": "12/31/1899 6:10:00 PM",
	"link": {
		"Href": "Book1.xlsx/worksheets/Sheet5",
		"Rel": "parent"
	}
}, {
	"Text": "12/31/1899 7:10:00 PM",
	"link": {
		"Href": "Book1.xlsx/worksheets/Sheet5",
		"Rel": "parent"
	}
}, {
	"Text": "12/31/1899 8:10:00 PM",
	"link": {
		"Href": "Book1.xlsx/worksheets/Sheet5",
		"Rel": "parent"
	}
}, {
	"Text": "12/31/1899 9:10:00 PM",
	"link": {
		"Href": "Book1.xlsx/worksheets/Sheet5",
		"Rel": "parent"
	}
}, {
	"Text": "12/31/1899 10:10:00 PM",
	"link": {
		"Href": "Book1.xlsx/worksheets/Sheet5",
		"Rel": "parent"
	}
}, {
	"Text": "12/31/1899 11:10:00 PM",
	"link": {
		"Href": "Book1.xlsx/worksheets/Sheet5",
		"Rel": "parent"
	}
}, {
	"Text": "18",
	"link": {
		"Href": "Book1.xlsx/worksheets/Sheet7",
		"Rel": "parent"
	}
}, {
	"Text": "18",
	"link": {
		"Href": "Book1.xlsx/worksheets/Sheet7",
		"Rel": "parent"
	}
}, {
	"Text": "18",
	"link": {
		"Href": "Book1.xlsx/worksheets/Sheet7",
		"Rel": "parent"
	}
}, {
	"Text": "18",
	"link": {
		"Href": "Book1.xlsx/worksheets/Sheet7",
		"Rel": "parent"
	}
}, {
	"Text": "18",
	"link": {
		"Href": "Book1.xlsx/worksheets/Sheet7",
		"Rel": "parent"
	}
}, {
	"Text": "18",
	"link": {
		"Href": "Book1.xlsx/worksheets/Sheet7",
		"Rel": "parent"
	}
}, {
	"Text": "18",
	"link": {
		"Href": "Book1.xlsx/worksheets/Sheet7",
		"Rel": "parent"
	}
}]
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Cloud SDK Family
 
Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.
 
The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:
 

{{< tabs tabTotal="9" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Search.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-Search.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-LiteCells-Search.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}


{{< /tab >}}

{{< tab tabNum="5" >}}


{{< /tab >}}

{{< tab tabNum="6" >}}


{{< /tab >}}

{{< tab tabNum="7" >}}


{{< /tab >}}

{{< tab tabNum="8" >}}


{{< /tab >}}
{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "LiteCellsSearch.py" >}}
{{< /tab >}}

{{< /tabs >}}
`