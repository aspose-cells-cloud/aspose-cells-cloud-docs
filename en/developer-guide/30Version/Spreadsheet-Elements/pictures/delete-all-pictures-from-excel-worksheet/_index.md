---
title: "Delete all pictures in an Excel worksheet"
second_title: "Document"
linktitle: "Clear"
type: docs
url: /pictures/clear/
aliases: [/delete-all-pictures-from-excel-worksheet/]
keywords: "Aspose.Cells Cloud, Excel, delete all pictures, worksheet, REST API, clear pictures"
description: "Learn how to delete all pictures from an Excel worksheet using Aspose.Cells Cloud REST API with cURL and SDK examples."
weight: 60
ArticleTitle: "How to Delete All Pictures in an Excel Worksheet with Aspose.Cells Cloud"
---

This REST API deletes **all** pictures in a worksheet.

**Prerequisites**  
- An active Aspose.Cells Cloud account with a valid OAuth 2.0 access token.  
- API version 3.0 (or later) is required; earlier versions are deprecated.  
- The target Excel file must be stored in a supported storage location (default or custom).

**Version Compatibility**  
The endpoint follows the Cells Cloud 3.0 API specification. Ensure that your client libraries and request URLs target `api.aspose.cloud/v3.0`.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures
```

### **Request parameters**

| Parameter Name | Type   | Location | Description                                |
| -------------- | ------ | -------- | ------------------------------------------ |
| name           | string | Path     | Name of the Excel file.                    |
| sheetName      | string | Path     | Name of the worksheet containing pictures. |
| folder         | string | Query    | Folder where the file is stored.           |
| storageName    | string | Query    | Name of the storage service.               |

### Error Responses

| HTTP Code | Description                                                                    |
| --------- | ------------------------------------------------------------------------------ |
| 401       | Unauthorized – missing or invalid token.                                       |
| 404       | Not Found – the specified file, worksheet, or page‑break index does not exist. |
| 400       | Bad Request – malformed request syntax or invalid parameters.                  |
| 500       | Internal Server Error – an unexpected condition was encountered.               |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Pictures/DeleteWorksheetPictures) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to call the API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/pictures" \
  -X DELETE \
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

Using an SDK is the fastest way to develop. An SDK handles low‑level details so you can focus on your business logic. See the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetPictures.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetPictures.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetPictures.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetPictures.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetPictures.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetPictures.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetPictures.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetPictures.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Notes:** The DELETE operation does not support pagination and is subject to the standard Aspose.Cells Cloud API rate limits (default 100 requests per minute). Adjust your client logic accordingly.

**See also**:  
- [/pictures/delete/](../delete/) – Delete a specific picture from a worksheet.  
- [/pictures/add/](../add/) – Add a picture to a worksheet.  