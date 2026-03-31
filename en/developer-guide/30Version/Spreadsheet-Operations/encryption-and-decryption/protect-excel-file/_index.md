---  
title: "Protect an Excel Workbook with Aspose.Cells Cloud API"  
second_title: "Document"  
linktitle: "Protect an Excel File"  
type: docs  
url: /protect-excel-file/  
aliases: [/protect-excel-workbooks/,/workbook/protect/]  
keywords: "Aspose Cells protect workbook, Excel protection API, REST protect workbook, Aspose Cells SDK"  
description: "Learn how to protect an Excel workbook via Aspose.Cells Cloud REST API. Includes authentication steps, query & body parameters, cURL request, and SDK code samples for C#, Java, PHP, Ruby, Node.js, Python, Perl, and Go."  
weight: 30  
---  

This REST API **protects** an Excel workbook.

### Prerequisites / Authentication  

1. **Create an Aspose Cloud account** and obtain a **Client ID** and **Client Secret**.  
2. Request an OAuth 2.0 access token:  

   ```bash
   curl -X POST "https://api.aspose.cloud/connect/token" \
        -H "Content-Type: application/x-www-form-urlencoded" \
        -d "grant_type=client_credentials&client_id=<YOUR_CLIENT_ID>&client_secret=<YOUR_CLIENT_SECRET>"
   ```  

   The response contains an `access_token`.  
3. Include the token in every API call:  

   ```
   Authorization: Bearer <access_token>
   ```

> **Note:** The workbook must already be uploaded to the chosen storage before you protect it.

### Query Parameters  

| Parameter Name | Type   | Description                                   |
|----------------|--------|-----------------------------------------------|
| folder         | string | Folder that contains the source workbook. *(optional)* |
| storageName    | string | Name of the storage location. *(optional; default = “Default”)* |

### Request Body Parameters  

| Parameter Name | Type                     | Description                                           |
|----------------|--------------------------|-------------------------------------------------------|
| protection     | WorkbookProtectionRequest | Object that defines the protection settings for the workbook. |

#### WorkbookProtectionRequest  

| Parameter Name | Type   | Description                                                                                                                                 |
|----------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------|
| ProtectionType | string | Type of protection to apply. Allowed values (case‑insensitive): **ALL**, **CONTENTS**, **NONE**, **OBJECTS**, **SCENARIOS**, **STRUCTURE**, **WINDOWS**. |
| Password       | string | Optional password to set for the protection.                                                                                                 |

## REST API  

| **API**                     | **HTTP Method** | **Description**    | **Swagger Link** |
|-----------------------------|-----------------|--------------------|------------------|
| /cells/{name}/protection    | POST            | Protect a workbook | [PostProtectDocument](https://apireference.aspose.cloud/cells/#/Workbook/PostProtectDocument) |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/PostProtectDocument) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Example: Protect a Workbook with cURL  

1. Obtain an access token as described in **Prerequisites / Authentication**.  
2. Execute the request:

   ```bash
   curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/protection?folder=MyFolder&storageName=MyStorage" \
        -H "accept: application/json" \
        -H "Content-Type: application/json" \
        -H "Authorization: Bearer <access_token>" \
        -d '{ "ProtectionType": "ALL", "Password": "aspose" }'
   ```

#### Expected Responses  

| HTTP Status | Description                               | Example Payload |
|-------------|-------------------------------------------|-----------------|
| **200**     | Workbook protected successfully.          | `{ "Code": "200", "Status": "OK" }` |
| **401**     | Unauthorized – missing or invalid token.  | `{ "Code": "401", "Message": "Invalid access token." }` |
| **400**     | Bad request – malformed JSON or unsupported `ProtectionType`. | `{ "Code": "400", "Message": "Invalid request data." }` |
| **500**     | Internal server error.                    | `{ "Code": "500", "Message": "An unexpected error occurred." }` |

## Cloud SDK Family  

Using an SDK is the fastest way to develop against Aspose.Cells Cloud. An SDK abstracts low‑level details, allowing you to focus on your business logic. See the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostProtectWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostProtectWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostProtectWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostProtectWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostProtectWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostProtectWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostProtectWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostProtectWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}