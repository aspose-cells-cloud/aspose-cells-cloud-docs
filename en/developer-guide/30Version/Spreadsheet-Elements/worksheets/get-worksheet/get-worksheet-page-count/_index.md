---
title: "Get Page Count for an Excel Worksheet"
second_title: "Document"
linktitle: "PageCount"
type: docs
url: /worksheets/page-count/
keywords: "Aspose.Cells, Excel page count, REST API, cloud SDK, worksheet pagination"
description: "Retrieve the number of printable pages in an Excel worksheet using Aspose.Cells Cloud REST API (v3.0). Includes HTTPS request format, authentication steps, sample cURL, full JSON response, status codes, and SDK code samples."
weight: 10
---

This REST API returns the **page count** for a worksheet.

## REST API

### Prerequisites
- **API version:** `v3.0` (see the Version History note below).  
- **Authentication:** OAuth 2.0 Bearer token (JWT).  
- **Storage:** The workbook must be stored in a supported Aspose Cloud storage location.  
- **Permissions:** The token must have permission to read the specified file.

### Authentication
1. **Obtain a token** – send a `POST` request to `https://api.aspose.cloud/connect/token` with your client ID and client secret (client‑credentials flow).  
2. **Receive the JWT** – the response contains an `access_token` that is valid for a limited time (default 1 hour).  
3. **Include the token** in every API call using the header:  

   ```http
   Authorization: Bearer <access_token>
   ```

### Request
```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pagecount
```

### Request Parameters
| Parameter   | Type   | Location | Description                              |
|-------------|--------|----------|------------------------------------------|
| name        | string | path     | Document name.                           |
| sheetName   | string | path     | Worksheet name.                          |
| folder      | string | query    | Folder that contains the document.       |
| storageName | string | query    | Name of the storage.                     |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/GetPageCount) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to access Aspose.Cells web services easily. The example below shows how to call the API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/worksheets/Sheet1/pagecount" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access_token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "PageCount": 3
}
```

{{< /tab >}}

{{< /tabs >}}

### Response Details
| HTTP Status | Meaning                               |
|-------------|---------------------------------------|
| **200**     | Success – returns the JSON payload shown above. |
| **401**     | Unauthorized – missing or invalid token. |
| **404**     | Not Found – the file or worksheet does not exist. |
| **500**     | Internal Server Error – unexpected server condition. |

### Version History
*API version **v3.0** (released 2025). If you are using a newer version, refer to the updated endpoint documentation.*

## Cloud SDK Family

Using an SDK is the fastest way to develop. An SDK abstracts low‑level details so you can focus on your business logic. See the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetPageCount.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetPageCount.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetPageCount.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetPageCount.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetPageCount.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetPageCount.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetPageCount.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetPageCount.go" >}}

{{< /tab >}}

{{< /tabs >}}