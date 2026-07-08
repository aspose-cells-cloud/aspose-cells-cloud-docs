---
title: "Find Text in Excel Files"
second_title: "Document"
linktitle: "Find Without Using Storage"
type: docs
url: /search/
aliases: [/search-without-using-storage/, /search-without-storage/]
keywords: "Aspose.Cells, Excel, search, API, REST"
description: "Search for specific text in Excel (XLS, XLSX, XLSM, XLSB) and ODS files using Aspose.Cells Cloud API. Includes cURL and SDK examples."
weight: 50
ArticleTitle: "Find Text in Excel Files – Aspose.Cells Cloud API"
---

This REST API searches for text within Excel files.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/search
```

### Request parameters

| Parameter Name | Type   | Location                | Description                                                    |
| -------------- | ------ | ----------------------- | -------------------------------------------------------------- |
| file           | file   | formData (multipart)    | The spreadsheet file to upload.                                |
| text           | string | query string            | The text string to search for.                                 |
| password       | string | query string (optional) | Password for opening a protected workbook, if required.        |
| sheetname      | string | query string (optional) | Name of the worksheet to limit the search to a specific sheet. |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/LightCells/PostSearch) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL. **Make sure you replace `<jwt token>` with a valid JWT token that has the required scope for the Cells API.**

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/search?text=1" \
  -X POST \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F "file=@book1.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
[
  {
    "Text": "12/31/1899 10:10:00 AM",
    "link": {
      "Href": "Book1.xlsx/worksheets/Sheet5",
      "Rel": "parent"
    }
  },
  {
    "Text": "12/31/1899 11:10:00 AM",
    "link": {
      "Href": "Book1.xlsx/worksheets/Sheet5",
      "Rel": "parent"
    }
  },
  {
    "Text": "12/31/1899 12:10:00 PM",
    "link": {
      "Href": "Book1.xlsx/worksheets/Sheet5",
      "Rel": "parent"
    }
  },
  {
    "Text": "12/31/1899 1:10:00 PM",
    "link": {
      "Href": "Book1.xlsx/worksheets/Sheet5",
      "Rel": "parent"
    }
  },
  {
    "Text": "12/31/1899 2:10:00 PM",
    "link": {
      "Href": "Book1.xlsx/worksheets/Sheet5",
      "Rel": "parent"
    }
  },
  {
    "Text": "12/31/1899 3:10:00 PM",
    "link": {
      "Href": "Book1.xlsx/worksheets/Sheet5",
      "Rel": "parent"
    }
  },
  {
    "Text": "12/31/1899 4:10:00 PM",
    "link": {
      "Href": "Book1.xlsx/worksheets/Sheet5",
      "Rel": "parent"
    }
  },
  {
    "Text": "12/31/1899 5:10:00 PM",
    "link": {
      "Href": "Book1.xlsx/worksheets/Sheet5",
      "Rel": "parent"
    }
  },
  {
    "Text": "12/31/1899 6:10:00 PM",
    "link": {
      "Href": "Book1.xlsx/worksheets/Sheet5",
      "Rel": "parent"
    }
  },
  {
    "Text": "12/31/1899 7:10:00 PM",
    "link": {
      "Href": "Book1.xlsx/worksheets/Sheet5",
      "Rel": "parent"
    }
  },
  {
    "Text": "12/31/1899 8:10:00 PM",
    "link": {
      "Href": "Book1.xlsx/worksheets/Sheet5",
      "Rel": "parent"
    }
  },
  {
    "Text": "12/31/1899 9:10:00 PM",
    "link": {
      "Href": "Book1.xlsx/worksheets/Sheet5",
      "Rel": "parent"
    }
  },
  {
    "Text": "12/31/1899 10:10:00 PM",
    "link": {
      "Href": "Book1.xlsx/worksheets/Sheet5",
      "Rel": "parent"
    }
  },
  {
    "Text": "12/31/1899 11:10:00 PM",
    "link": {
      "Href": "Book1.xlsx/worksheets/Sheet5",
      "Rel": "parent"
    }
  },
  {
    "Text": "18",
    "link": {
      "Href": "Book1.xlsx/worksheets/Sheet7",
      "Rel": "parent"
    }
  }
]
```

**Response status codes**

- **200 OK** – Successful search; returns a JSON array of matching cells (as shown above).  
- **400 Bad Request** – Missing required parameters or invalid query values.  
- **401 Unauthorized** – Invalid or missing JWT token.  
- **403 Forbidden** – Insufficient permissions to access the workbook.  
- **404 Not Found** – The specified file or worksheet does not exist.  
- **500 Internal Server Error** – Unexpected server error.

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the most efficient way to accelerate development. An SDK abstracts low‑level details, allowing you to focus on your business logic. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostSearch.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostSearch.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostSearch.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostSearch.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostSearch.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostSearch.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostSearch.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostSearch.go" >}}

{{< /tab >}}

{{< /tabs >}}