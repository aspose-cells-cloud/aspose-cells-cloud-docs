---
title: "Delete Conditional Formatting – Aspose.Cells Cloud API Reference"
type: docs
url: /conditional-formattings/delete/
aliases: [/remove-conditional-formatting/]
keywords: "Aspose.Cells Cloud, REST API, conditional formatting, delete, Excel, spreadsheet"
description: "Delete a conditional formatting rule from a worksheet using Aspose.Cells Cloud REST API. Learn required parameters, cURL example, and SDK usage."
weight: 60
---

This REST API removes conditional formatting from a worksheet.

## Prerequisites

- **API version**: v3.0 (current version at the time of writing).  
- **Authentication**: A valid JWT Bearer token is required for every request.  
- **Storage**: The workbook must be stored in Aspose Cloud Storage (or a connected external storage).  
- **Permissions**: The token must include the `Cells` scope.  

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}
```

The request parameters are:

| Parameter Name | Type    | Location | Description |
|----------------|---------|----------|-------------|
| name           | string  | path     | The name of the workbook file. |
| sheetName      | string  | path     | The name of the worksheet that contains the formatting. |
| index          | integer | path     | The zero-based index of the conditional formatting rule to delete. |
| folder         | string  | query    | The folder in cloud storage where the file is located. |
| storageName    | string  | query    | The name of the storage service. |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormatting) defines a publicly accessible programming interface and provides full details of the endpoint.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make the call with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings/0" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Authentication

Aspose.Cells Cloud uses OAuth 2.0. To obtain a JWT token:

1. Send a `POST` request to `https://api.aspose.cloud/connect/token` with your client ID and client secret.  
2. Include the `grant_type=client_credentials` and the required scope (`Cells`).  
3. The response contains an `access_token` field—use this value as the Bearer token in the `Authorization` header of every API call.

### Example token request (cURL)

```bash
curl -X POST "https://api.aspose.cloud/connect/token" \
  -d "grant_type=client_credentials&client_id=<your_client_id>&client_secret=<your_client_secret>&scope=Cells"
```

The response will be similar to:

```json
{
  "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
  "token_type": "Bearer",
  "expires_in": 3600
}
```

Use the `access_token` value in the `Authorization` header as shown in the request example above.

## Error Handling & Response Codes

| HTTP Status | Description | Example Response |
|-------------|-------------|------------------|
| **200 OK** | The conditional formatting rule was deleted successfully. | `{ "Code": "200", "Status": "OK" }` |
| **400 Bad Request** | The request is malformed (e.g., missing required parameters). | `{ "Code":"400", "Message":"Invalid request parameters." }` |
| **401 Unauthorized** | Missing or invalid JWT token. | `{ "Code":"401", "Message":"Authentication failed." }` |
| **404 Not Found** | The specified workbook, worksheet, or formatting index does not exist. | `{ "Code":"404", "Message":"Conditional formatting index out of range." }` |
| **500 Internal Server Error** | An unexpected server error occurred. | `{ "Code":"500", "Message":"An unexpected error has occurred." }` |

## Quick‑Start Checklist

1. **Obtain a JWT token** (see the *Authentication* section).  
2. **Confirm the workbook location** (`folder` and `storageName` if applicable).  
3. **Identify the zero‑based index** of the conditional formatting rule you want to delete.  
4. **Execute the DELETE request** using the endpoint shown above.  
5. **Verify the response** – a `200 OK` indicates success; handle other status codes as needed.

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK takes care of low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-RemoveConditionalFormatting-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-remove-conditional-formatting.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-delete_worksheet_conditional_formatting-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-RemoveConditionalFormatting-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-RemoveConditionalFormatting-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "fa6aed4b68d309d8de12d91ff7c0111d" >}}

{{< /tab >}}

{{< /tabs >}}