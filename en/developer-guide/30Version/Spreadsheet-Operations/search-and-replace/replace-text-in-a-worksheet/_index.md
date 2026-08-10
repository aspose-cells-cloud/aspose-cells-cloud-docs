---
title: "Replace Text in an Excel Worksheet – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Replace in worksheet"
type: docs
url: /worksheets/replace-text/
aliases: [/replace-text-in-a-workbook/]
keywords: "Aspose.Cells, replace text, Excel, REST API, spreadsheet, worksheet"
description: "Learn how to replace text in an Excel worksheet using the Aspose.Cells Cloud API (v3.0). Includes prerequisites, authentication, request syntax, cURL example, SDK code samples, response details, and error handling."
ArticleTitle: "Replace Text in an Excel Worksheet – Aspose.Cells Cloud API"
weight: 70
---

This REST API replaces text in an Excel worksheet using the **Aspose.Cells replace text API**.

## Security and Authentication
The Aspose.Cells Cloud APIs are secure and require [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/replaceText
```

### Request Parameters

| Parameter Name  | Type   | Location | Description                        |
| --------------- | ------ | -------- | ---------------------------------- |
| **name**        | string | path     | The name of the Excel workbook.    |
| **sheetName**   | string | path     | The name of the worksheet.         |
| **oldValue**    | string | query    | The text to be replaced.           |
| **newValue**    | string | query    | The replacement text.              |
| **folder**      | string | query    | The folder that contains the file. |
| **storageName** | string | query    | The storage service name.          |

### **Response**

```json
{
    "Status":"OK",
    "Code":200,
      "Workbook": {
    "FileName": "test.xlsx",
    "Links": [
      {
        "Href": "/test.xlsx",
        "Rel": "self",
        "Title": null,
        "Type": null
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Download As CSV",
        "Type": "text/csv"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Download As HTML",
        "Type": "text/html"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Download As ODS",
        "Type": "application/vnd.oasis.opendocument.spreadsheet"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Download As PDF",
        "Type": "application/pdf"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Download As Table Delimited Text Format",
        "Type": "text/plain"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Download As TIFF",
        "Type": "image/tiff"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Download As Microsoft Excel 2003",
        "Type": "application/vnd.ms-excel"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Download As Microsoft Excel 2007",
        "Type": "application/vnd.openxmlformats-officedocument.spreadsheetml.sheet"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Download As XPS",
        "Type": "application/vnd.ms-xpsdocument"
      }
    ],
    "Worksheets": {
      "link": {
        "Href": "/worksheets",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "DefaultStyle": {
      "link": {
        "Href": "/defaultstyle",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "DocumentProperties": {
      "link": {
        "Href": "/documentproperties",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "Names": {
      "link": {
        "Href": "/names",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "Settings": {
      "link": {
        "Href": "/settings",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "IsWriteProtected": "False",
    "IsProtected": "False",
    "IsEncryption": "false",
    "Password": null
  }
}
```

**HTTP Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter applied successfully; response contains operation details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |
## How to Use the PostWorksheetTextReplace API with SDKs

### PostWorksheetTextReplace API Specification

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetTextReplace) defines this publicly accessible interface.

You can use the cURL command-line tool to call the service:

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/replaceText?oldValue=b&newValue=b11" \
     -H "accept: application/json" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Matches": 0,
  "Worksheet": {
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}


### Use Aspose.Cells Cloud SDKs

Using an SDK is the best way to speed up development. An SDK handles low‑level details, allowing you to focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetTextReplace.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetTextReplace.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetTextReplace.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetTextReplace.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetTextReplace.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetTextReplace.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetTextReplace.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetTextReplace.go" >}}

{{< /tab >}}

{{< /tabs >}}

