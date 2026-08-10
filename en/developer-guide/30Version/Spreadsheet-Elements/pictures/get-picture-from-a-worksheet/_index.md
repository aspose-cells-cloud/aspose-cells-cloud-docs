---
title: "Get all pictures in an Excel worksheet"
second_title: "Document"
linktitle: "Get all"
type: docs
url: /pictures/get-all/
aliases: [/get-picture-from-a-worksheet/]
keywords: "Aspose.Cells Cloud, Excel worksheet, pictures API, get all pictures, REST API, SDK"
description: "Retrieve all picture objects from an Excel worksheet via Aspose.Cells Cloud REST API."
ArticleTitle: "Get all pictures in an Excel worksheet - Aspose.Cells Cloud API"
weight: 10
---

This REST API retrieves all picture information from an Excel worksheet.

**Prerequisites**  
Before calling this endpoint, ensure you have:

- A valid Aspose Cloud JWT access token.  
- The target Excel file uploaded to the selected storage.  
- The correct storage name (if using a custom storage).  
- The worksheet name that contains the pictures.

## GetWorksheetPictures API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures
```

**Note:** Use HTTPS (TLS 1.2 or higher) when calling the API and include a valid JWT token in the `Authorization` header.

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### **Request parameters**

| Parameter Name | Type   | Location | Description                                    |
| -------------- | ------ | -------- | ---------------------------------------------- |
| name           | string | path     | The name of the Excel file.                    |
| sheetName      | string | path     | The name of the worksheet containing pictures. |
| folder         | string | query    | The folder path where the file is stored.      |
| storageName    | string | query    | The name of the storage service.               |

### Error Responses

| HTTP Code | Description                                                                    |
| --------- | ------------------------------------------------------------------------------ |
| 401       | Unauthorized – missing or invalid token.                                       |
| 404       | Not Found – the specified file, worksheet, or page‑break index does not exist. |
| 400       | Bad Request – malformed request syntax or invalid parameters.                  |
| 500       | Internal Server Error – an unexpected condition was encountered.               |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Pictures/GetWorksheetPictures) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Pictures": {
    "PictureList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/1",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/2",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      }
    ],
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet2/pictures",
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

**Success Response** – A successful call returns HTTP 200 with a JSON payload containing a `Pictures` object that lists each picture’s resource link.

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

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

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetPictureWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetPictureWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetPictureWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetPictureWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetPictureWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}

You can download the SDKs directly from their respective package managers (e.g., NuGet for .NET, Maven Central for Java, Composer for PHP, npm for Node.js, PyPI for Python, CPAN for Perl, and Go modules for Go).  

*See also:* Add a picture, Delete a picture, Update picture properties.