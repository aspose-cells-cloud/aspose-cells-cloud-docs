---
title: "Delete all OLE objects in an Excel worksheet"
second_title: "Document"
linktitle: "Clear"
type: docs
url: /oleobjects/clear/
aliases: [/delete-all-oleobjects-from-excel-worksheet/]
keywords: "Aspose.Cells Cloud, delete OLE objects, Excel API, REST API, worksheet OLE clear, cloud SDK"
description: "Learn how to remove every OLE object from an Excel worksheet using Aspose.Cells Cloud REST API (v3.0). Includes endpoint, parameters, HTTPS cURL example, SDK snippets, authentication steps, error handling, and FAQ."
weight: 60
---

### Overview
An **OLE (Object Linking and Embedding) object** is an embedded file such as a Word document, PowerPoint slide, image, or another workbook that resides inside an Excel worksheet.  
The *Clear* operation removes **all** such OLE objects from a specified worksheet, leaving only the cell data. This is useful for cleaning up legacy spreadsheets or preparing a workbook for redistribution.

## Prerequisites
- Aspose.Cells Cloud SDK version v3.0 or later.  
- A valid Aspose Cloud **OAuth 2.0 JWT** access token with the `Cells.ReadWrite` scope.  
- HTTPS access to the Aspose Cloud service (`https://api.aspose.cloud`).

## Authentication
1. **Obtain a JWT token** by sending a `POST` request to the OAuth endpoint:  

   ```bash
   curl -X POST "https://api.aspose.cloud/connect/token" \
        -H "Content-Type: application/x-www-form-urlencoded" \
        -d "grant_type=client_credentials&client_id=<your_client_id>&client_secret=<your_client_secret>"
   ```

2. The response contains an access token (`access_token`).  
3. Include the token in every API call using the `Authorization: Bearer <token>` header.  

> **Note:** All requests must use **HTTPS**; the service does not accept plain HTTP.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects
```

**Request parameters**

| Parameter Name | Type   | Location | Description |
|----------------|--------|----------|-------------|
| name           | string | path     | The name of the workbook. |
| sheetName      | string | path     | The name of the worksheet. |
| folder         | string | query    | The folder that contains the workbook. |
| storageName    | string | query    | The storage name where the workbook is located. |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/OleObjects/DeleteWorksheetOleObjects) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to call Aspose.Cells web services. The example below shows how to delete all OLE objects **using** cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects" \
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

### Response Codes
| HTTP Status | Description | Example |
|-------------|-------------|---------|
| **200 OK** | The request succeeded. All OLE objects were removed (or none existed, because the operation is idempotent). | `{ "Code": 200, "Status": "OK" }` |
| **400 Bad Request** | Missing or invalid parameters. | `{ "Code": 400, "Message": "Invalid worksheet name." }` |
| **401 Unauthorized** | Authentication failed or token missing/expired. | `{ "Code": 401, "Message": "Access token is invalid." }` |
| **404 Not Found** | The specified workbook or worksheet does not exist. | `{ "Code": 404, "Message": "Workbook not found." }` |
| **500 Internal Server Error** | An unexpected server error occurred. | `{ "Code": 500, "Message": "Unexpected error." }` |

### Version / Last Updated
- **API version:** v3.0  
- **Document last updated:** 2024‑11‑01  

## Cloud SDK Family

Using an SDK is the fastest way to integrate this operation into your application. An SDK abstracts low‑level details, allowing you to focus on business logic. See the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call the **DeleteWorksheetOleObjects** operation with various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetOleObjects.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetOleObjects.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetOleObjects.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetOleObjects.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetOleObjects.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetOleObjects.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetOleObjects.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetOleObjects.go" >}}

{{< /tab >}}

{{< /tabs >}}

## FAQ

**Q:** *What does “clear all OLE objects” mean in an Excel worksheet?*  
**A:** An OLE (Object Linking and Embedding) object is an embedded file such as a Word document, PowerPoint slide, image, or another workbook. Clearing all OLE objects removes every such embedded element from the specified worksheet, leaving only the cell data.

**Q:** *How do I authenticate the DELETE request?*  
**A:** First obtain a JWT access token via the Aspose Cloud OAuth 2.0 endpoint (`POST /connect/token`). Include the token in the `Authorization: Bearer <token>` header. The token must have the `Cells.ReadWrite` scope. All calls must be made over **HTTPS**.

**Q:** *What response will I receive if the worksheet does not contain any OLE objects?*  
**A:** The API returns HTTP 200 with a JSON body `{ "Code": 200, "Status": "OK" }`. The operation is idempotent, so deleting zero objects is considered successful.  

---