---
title: "Add Picture in an Excel file"
second_title: "Document"
linktitle: "Add"
type: docs
url: /pictures/add/
aliases: [/add-pictures-to-excel-worksheet/]
keywords: "Aspose Cells, Excel, Add Picture, REST API, Cloud SDK, Spreadsheet"
description: "Use Aspose.Cells Cloud REST API to add a picture to an Excel worksheet. SDKs for Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby, and Swift simplify integration across platforms."
weight: 20
---

This REST API adds a new picture to an Excel worksheet.

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures
```

The request parameters are:

| Parameter Name      | Type   | Location                     | Description                                                                                 |
|---------------------|--------|------------------------------|---------------------------------------------------------------------------------------------|
| name                | string | path                         | The workbook name.                                                                          |
| sheetName           | string | path                         | The worksheet name.                                                                         |
| picture             | object | body                         | Picture object (binary data).                                                               |
| upperLeftRow        | integer| query                        | Zero‑based index of the upper‑left row where the picture will be placed.                    |
| upperLeftColumn     | integer| query                        | Zero‑based index of the upper‑left column where the picture will be placed.                 |
| lowerRightRow       | integer| query                        | Zero‑based index of the lower‑right row of the picture area.                               |
| lowerRightColumn    | integer| query                        | Zero‑based index of the lower‑right column of the picture area.                            |
| picturePath         | string | query                        | Path to the picture file; if omitted, the picture data must be supplied in the request body.|
| folder              | string | query                        | The folder that contains the workbook.                                                      |
| storageName         | string | query                        | The name of the storage service.                                                            |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Pictures/PutWorksheetAddPicture) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.com/v1.1/cells/Sample_Test_Book.xls/worksheets/Sheet6/pictures?picturePath=aspose-cloud.png" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetAddPicture.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetAddPicture.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetAddPicture.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetAddPicture.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetAddPicture.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetAddPicture.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetAddPicture.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetAddPicture.go" >}}

{{< /tab >}}

{{< /tabs >}}