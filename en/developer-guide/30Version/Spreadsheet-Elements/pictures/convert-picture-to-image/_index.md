---  
title: "Aspose.Cells Cloud API – Get Picture from Worksheet"  
second_title: "Document"  
linktitle: "Get"  
type: docs  
url: /pictures/get/  
aliases: [/convert-picture-to-image/]  
keywords: "Aspose.Cells Get Picture API, Excel picture API, Cells Cloud picture, Aspose.Cells Cloud, REST API"  
description: "Retrieve a specific picture from an Excel worksheet using Aspose.Cells Cloud REST API. Includes endpoint, parameters, authentication steps, response codes, and code examples."  
weight: 10  
---  

**Version:** `v3.0`  
**Last updated:** 2024‑06‑30  

This REST API retrieves a picture by its zero‑based index from an Excel worksheet.

**Prerequisites:** Create an Aspose Cloud account, obtain a *client‑id* and *client‑secret*, generate a JWT token, and upload the workbook to your storage location.  

**Authentication:** Request a JWT token via the OAuth 2.0 `/connect/token` endpoint and supply it in the request header as `Authorization: Bearer <jwt token>`.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/{pictureIndex}
```

The request parameters are:

| Parameter Name | Type    | Location | Description                              |
|----------------|---------|----------|------------------------------------------|
| name           | string  | path     | Name of the Excel document.              |
| sheetName      | string  | path     | Name of the worksheet.                   |
| pictureIndex   | integer | path     | Zero‑based index of the picture.         |
| format         | string  | query    | Desired export format (e.g., png, jpg, bmp, gif, tiff). If omitted, the picture is returned in its original format. |
| folder         | string  | query    | Folder that contains the document.       |
| storageName    | string  | query    | Name of the storage location.            |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Pictures/GetWorksheetPicture) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to call the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures/1?format=png" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```bash
<IMAGE DATA>
```

*Successful response:* HTTP **200 OK** with `Content‑Type: image/png` (or the appropriate image MIME type).  

*Possible error codes:*  

- **401 Unauthorized** – missing or invalid JWT token.  
- **404 Not Found** – workbook, worksheet, or picture index does not exist.  
- **500 Internal Server Error** – server‑side problem.

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the fastest way to develop. An SDK handles low‑level details so you can focus on your project. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetPictureWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetPictureWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetPictureWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "ExampleGetWorksheetPictureWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "ExampleGetWorksheetPictureWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ExampleGetWorksheetPictureWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "ExampleGetWorksheetPictureWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "ExampleGetWorksheetPictureWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}