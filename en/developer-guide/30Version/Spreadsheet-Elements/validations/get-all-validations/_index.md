---
title: "Get all worksheet validations from an Excel worksheet"
second_title: "Document"
linktitle: "Get all"
type: docs
url: /validations/get-all/
keywords: "Excel, worksheet validations, Aspose.Cells Cloud, REST API, Get all validations"
description: "Retrieve all worksheet validations from an Excel worksheet using the Aspose.Cells Cloud REST API. The service supports multiple SDKs (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go) for rapid integration."
weight: 10
---

This REST API retrieves all worksheet validations on an Excel worksheet.

## REST API

```bash
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations
```

**Request parameters**

| Parameter Name | Type   | Location | Description                                 |
|----------------|--------|----------|---------------------------------------------|
| name           | string | path     | Name of the Excel document.                 |
| sheetName      | string | path     | Name of the worksheet.                      |
| folder         | string | query    | Folder path where the document is stored.   |
| storageName    | string | query    | Name of the storage service.                |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/WorksheetValidations/GetWorksheetValidations) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The example below shows how to call the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.com/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```bash
# (Response example will be displayed here)
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetValidations.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetValidations.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetValidations.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetValidations.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetValidations.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetValidations.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetValidations.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetValidations.go" >}}

{{< /tab >}}

{{< /tabs >}}