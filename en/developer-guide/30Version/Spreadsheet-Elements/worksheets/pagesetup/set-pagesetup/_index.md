---
title: "Set page setup for a worksheet"
second_title: "Developer Guide"
linktitle: "Set page setup"
type: docs
url: /set-page-setup/
keywords: "Aspose.Cells, Excel, page setup, REST API, worksheet, cloud SDK"
description: "Configure Excel page setup via Aspose.Cells Cloud API: POST /cells/{name}/worksheets/{sheetName}/pagesetup with JWT auth"
weight: 100
ArticleTitle: "Set page setup for a worksheet – Aspose.Cells Cloud API Guide"
---
The **PostPageSetup** API (`POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pagesetup`) updates page setup configurations for a specified worksheet in a workbook stored in Aspose.Cells Cloud, allowing precise control over print settings such as margins, orientation, and paper size. To call this API, you must provide a valid JWT (OAuth) token in the `Authorization` header, ensure the workbook resides in an Aspose Cloud storage location where you have read/write permissions, and include the required path parameters `{name}` and `{sheetName}` along with a `pageSetup` object in the request body describing the desired settings.

This REST API sets the page setup for an Excel worksheet.

## The Post Page Setup Web API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pagesetup
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### **Request parameters**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| sheetName | String | Path | The worksheet name. |
| pageSetup | class:pagesetup | HTTPBody | PageSetup Page Setup description. |
| folder | String | Query | The folder where the file is situated. |
| storageName | String | Query | The storage name where the file is situated. |

**Example JSON payload for the `pageSetup` object**

```json
{
  "pageSetup": {
    "orientation": "Portrait",
    "paperSize": "A4",
    "fitToPagesTall": 1,
    "fitToPagesWide": 1,
    "centerHorizontally": true,
    "centerVertically": false
  }
}
```

The <a href="https://reference.aspose.cloud/cells/#/PageSetup/PostPageSetup" target="_blank" rel="noopener noreferrer">OpenAPI Specification</a> defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Tasks/pagesetup" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{
  "pageSetup": {
    "orientation": "Portrait",
    "paperSize": "A4",
    "fitToPagesTall": 1,
    "fitToPagesWide": 1,
    "centerHorizontally": true,
    "centerVertically": false
  }
}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

The API returns a JSON object indicating the result of the operation:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Possible response status codes**

### **Response**

```json
[
  {
    "Name": "CellsCloudResponse",
    "DataType": {
      "Identifier": "Class",
      "Reference": "CellsCloudResponse"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/json
```

**HTTP Status Codes**

| Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request completed successfully. |
| 400 | Bad Request | The request is malformed or one or more parameters are invalid. |
| 401 | Unauthorized | Authentication failed, or the JWT token is missing or expired. |
| 404 | Not Found | The requested workbook, worksheet, or resource was not found. |
| 413 | Payload Too Large | The uploaded file exceeds the allowed size limit. |
| 500 | Internal Server Error | The server encountered an unexpected error while processing the request. |

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details and lets you focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostPageSetup.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostPageSetup.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostPageSetup.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostPageSetup.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostPageSetup.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostPageSetup.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostPageSetup.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostPageSetup.go" >}}

{{< /tab >}}

{{< /tabs >}}
