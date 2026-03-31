---
title: "Delete Background on an Excel Workbook"
second_title: "Document"
linktitle: "Delete"
type: docs
url: /delete-background-in-excel-file/
aliases:
  - /delete-background-in-workbook/
  - /workbook/delete-background/
  - /workbook/background/delete/
keywords: "Aspose Cells delete background, Excel API delete background, Aspose.Cells Cloud, DELETE /cells background"
description: "Remove a background image from an Excel workbook using Aspose.Cells Cloud API. Learn the DELETE endpoint, required parameters, cURL example, and SDK code in C#, Java, Python, and more."
weight: 170
---

This REST API deletes the background image of an Excel workbook.

**Prerequisites**  
To use this endpoint you must:

* Include a valid **Authorization** header (`Authorization: Bearer <access_token>`).  
* Provide the workbook name in the path (`{name}`), e.g., `Book1.xlsx`.  
* (Optional) Specify the storage folder (`folder`) and storage service (`storageName`) when the file is not stored in the root folder.

**Query Parameter**

| Parameter Name | Type   | Description                              | Required |
|----------------|--------|------------------------------------------|----------|
| folder         | string | Folder that contains the original workbook. | No |
| storageName    | string | Name of the storage service to use.       | No |

## REST API

| **API**                     | **Type** | **Description**                | **Resource Link** |
|-----------------------------|----------|--------------------------------|-------------------|
| /cells/{name}/background    | DELETE   | Delete background in an Excel file | [DeleteWorkbookBackground](https://apireference.aspose.cloud/cells/#/Workbook/DeleteWorkbookBackground) |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/DeleteWorkbookBackground) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the **cURL** command‑line tool (a utility for transferring data with URLs) to access Aspose.Cells web services easily. The following example demonstrates how to call the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/background?folder=DotnetFiles" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -H "x-aspose-client: Containerize.Swagger"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4"
   tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby"
   tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}

*Updated: 2024‑10‑15*