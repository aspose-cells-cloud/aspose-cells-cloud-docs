---  
title: "Unprotect Excel Workbook – Aspose.Cells Cloud API"  
second_title: "Document"  
linktitle: "Unprotect Excel File"  
type: docs  
url: /excel-file-unprotect/  
aliases:  
  - /unprotect-excel-workbooks/  
  - /workbook/unprotect/  
keywords: "Aspose Cells, Excel unprotect API, remove workbook protection, REST API, cloud spreadsheet"  
description: "Learn how to remove protection from an Excel workbook using Aspose.Cells Cloud REST API. Includes request syntax, parameters, cURL example, and SDK code in multiple languages."  
weight: 60  
---  

Use this REST API to unprotect an Excel workbook.

### Prerequisites  

1. An Aspose.Cells Cloud account.  
2. API **client id** and **client secret** (used to obtain an OAuth 2.0 access token).  
3. A storage location (default “DefaultStorage”) where the workbook is stored.  
4. The API version `v3.0` (used in the request URL).

### Authentication  

The API requires an OAuth 2.0 **Bearer** token.  

```http
Authorization: Bearer <access_token>
```  

Obtain the token by sending a `POST` request to `https://api.aspose.cloud/connect/token` with your client id and secret. Include the token in every request header as shown above.

### Path Parameters  

| Parameter | Type   | Description                                    | Required |
|-----------|--------|------------------------------------------------|----------|
| **name**  | string | Name of the workbook file (including extension). | Yes      |

### Query Parameters  

| Parameter Name | Type   | Description                                             |
|----------------|--------|---------------------------------------------------------|
| folder         | string | Path to the folder that contains the original workbook. |
| storageName    | string | Name of the storage service where the workbook resides. |

### Request Body Parameters  

| Parameter Name | Type                     | Description                                          |
|----------------|--------------------------|------------------------------------------------------|
| protection     | WorkbookProtectionRequest | Object that specifies the protection settings to remove. |

#### WorkbookProtectionRequest  

| Parameter Name | Type   | Description                                                                 |
|----------------|--------|-----------------------------------------------------------------------------|
| ProtectionType | string | Type of protection to remove (`ALL`, `CONTENTS`, `NONE`, `OBJECTS`, `SCENARIOS`, `STRUCTURE`, `WINDOWS`). |
| Password       | string | Password required to remove the protection (optional).                     |

### Step‑by‑Step Request  

1. **Generate an access token** and add the `Authorization: Bearer <token>` header.  
2. **Construct the URL**: `https://api.aspose.cloud/v3.0/cells/{name}/protection` (replace `{name}` with the workbook filename).  
3. **Add optional query parameters** `folder` and `storageName` if needed.  
4. **Send a `DELETE` request** with the JSON body shown below.

### REST API  

| **API**                     | **Type** | **Description**      | **Swagger Link** |
|-----------------------------|----------|----------------------|------------------|
| /cells/{name}/protection    | DELETE   | Unprotect a document | [DeleteUnProtectWorkbook](https://apireference.aspose.cloud/cells/#/Workbook/DeleteUnProtectWorkbook) |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/DeleteUnProtectWorkbook) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

#### cURL Example  

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/protection?folder=MyFolder&storageName=MyStorage" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -d '{ "ProtectionType": "ALL", "Password": "aspose"}'
```

#### Response (Success)  

```json
{
  "Code": "200",
  "Status": "OK"
}
```

### Error Responses  

| HTTP Status | Code | Description |
|-------------|------|-------------|
| 400 | BadRequest | Missing or invalid parameters. |
| 401 | Unauthorized | Invalid or missing access token. |
| 404 | NotFound | Specified workbook not found in the given folder/storage. |
| 500 | InternalServerError | Unexpected server error. |

Each error returns a JSON object containing `Code` and `Message`.

## Cloud SDK Family  

Using an SDK is the best way to speed up development. An SDK handles low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteUnProtectWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteUnProtectWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteUnProtectWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteUnProtectWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteUnProtectWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteUnProtectWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteUnProtectWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteUnProtectWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}