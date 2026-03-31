---  
title: "Merge an Excel Workbook into Another Workbook"  
second_title: "Document"  
linktitle: "Merge an Excel workbook into another workbook"  
type: docs  
url: /merge-an-excel-file-into-the-excel-file/  
aliases: [/merge-excel-workbooks/, /workbook/merge/]  
keywords: "Excel workbook merge, Aspose.Cells Cloud, REST API, spreadsheet merging, cloud SDK, authentication, mergeWith, cURL example"  
description: "Learn how to merge one Excel workbook into another using the Aspose.Cells Cloud REST API (v3.0). Includes authentication details, the required `mergeWith` parameter, a cURL example, and SDK code samples for multiple languages."  
weight: 50  
---  

This REST API merges an Excel **workbook** into another workbook.

### Prerequisites  

Before calling the merge endpoint, ensure that both the target workbook (`{name}`) and the workbook to be merged (`mergeWith`) already exist in the specified storage folder. A valid access token is also required for authentication.

### Authentication  

All requests must include the `Authorization: Bearer <access‑token>` header.  
You can obtain an access token by following the OAuth guide in the Aspose.Cells Cloud documentation.

**Query Parameter**

| Parameter Name | Type   | Description                              |
|----------------|--------|------------------------------------------|
| folder         | string | Folder containing the original workbook. |
| storageName    | string | Name of the storage.                     |
| **mergeWith**  | string | Name of the workbook to be merged into the target workbook. |

## REST API  

| **API**                     | **Type** | **Description**      | **Swagger Link**                                                                 |
|-----------------------------|----------|----------------------|----------------------------------------------------------------------------------|
| /cells/{name}/merge         | POST     | Merge Excel workbooks | [PostWorkbooksMerge](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbooksMerge) |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbooksMerge) defines a publicly accessible programming interface and lets the API carry out REST interactions directly from a web browser.

### How to merge two workbooks (cURL)

You can use the **cURL** command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL, including the required authentication header.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
# Merge test2.xlsx into test.xlsx
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/merge?mergeWith=test2.xlsx" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access-token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
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
  },
  "Code": 200,
  "Status": "OK"
}
```

Response headers

{{< /tab >}}

{{< /tabs >}}

### Error Handling  

| HTTP Status | Description                              |
|-------------|------------------------------------------|
| 400         | Bad request – missing or invalid parameters. |
| 401         | Unauthorized – invalid or missing access token. |
| 404         | Not found – the specified workbook does not exist. |
| 500         | Internal server error – unexpected condition on the server. |

## Cloud SDK Family  

Using an SDK is the best way to speed up development. An SDK abstracts low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbooksMerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbooksMerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbooksMerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbooksMerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbooksMerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbooksMerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbooksMerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbooksMerge.go" >}}

{{< /tab >}}

{{< /tabs >}}