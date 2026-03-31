---
title: "Clear Conditional Formatting"
type: docs
url: /conditional-formattings/clear/
aliases: [/clear-all-condition-formattings/]
keywords: "Aspose.Cells Cloud, REST API, clear conditional formatting, Excel, worksheets, JWT, v3.2"
description: "Delete all conditional formatting rules from a worksheet with Aspose.Cells Cloud API (v3.2). Learn the request syntax, required parameters, authentication steps, and see sample code in multiple SDKs."
weight: 80
---

This REST API clears all conditional formatting rules from a worksheet.

## Prerequisites

- A valid **Aspose Cloud** subscription.  
- An Excel workbook uploaded to Aspose Cloud Storage (or accessible via default storage).  
- Ability to generate a **JWT access token** for authentication.  

## Authentication

To call the API you must include a Bearer token in the `Authorization` header.

1. **Obtain a JWT token**  

   ```bash
   POST https://api.aspose.cloud/connect/token
   Content-Type: application/x-www-form-urlencoded

   grant_type=client_credentials&client_id=<your_client_id>&client_secret=<your_client_secret>
   ```

2. **Use the token** in the request header:

   ```
   Authorization: Bearer <jwt token>
   ```

## Versioning & Compatibility

The endpoint shown below uses the current API version **v3.2**.  
Older versions (e.g., v3.0) are deprecated and will be removed in future releases.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.2/cells/{name}/worksheets/{sheetName}/conditionalFormattings
```

The request parameters are listed below:

| Parameter Name | Type   | Location | Description |
|----------------|--------|----------|-------------|
| **name**       | string | path     | The name of the workbook file (e.g., `Book1.xlsx`). |
| **sheetName**  | string | path     | The name of the worksheet from which to remove conditional formatting. |
| **folder**     | string | query    | *(Optional)* Folder path in storage where the workbook is located. |
| **storageName**| string | query    | *(Optional)* Name of the storage service. |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormattings) defines a publicly accessible programming interface and **the OpenAPI Specification** lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.2/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings" \
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

### Error Responses

| HTTP Code | Reason                     | Example Body |
|-----------|---------------------------|--------------|
| **400**   | Bad Request – missing or invalid parameters. | `{ "Code":"400", "Message":"Invalid parameter value." }` |
| **401**   | Unauthorized – missing or invalid JWT token. | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**   | Not Found – workbook or worksheet does not exist. | `{ "Code":"404", "Message":"File not found." }` |
| **500**   | Internal Server Error – unexpected server failure. | `{ "Code":"500", "Message":"An unexpected error occurred." }` |

## SDK Examples

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-ClearConditionFormattings-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-clear-all-formatting.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-delete_worksheet_conditional_formattings-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-ClearConditionFormattings-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-ClearConditionFormattings-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "63fda1be9e5149f83edca47ce58dac87" >}}

{{< /tab >}}

{{< /tabs >}}

## FAQ

**Q:** *How do I clear all conditional formatting from a worksheet using Aspose.Cells Cloud?*  
**A:** Send a `DELETE` request to  

```
https://api.aspose.cloud/v3.2/cells/{name}/worksheets/{sheetName}/conditionalFormattings
```  

including a valid JWT token in the `Authorization` header. Optional query parameters `folder` and `storageName` can be used if needed.

**Q:** *What response indicates a successful operation?*  
**A:** HTTP 200 with JSON body `{ "Code":"200", "Status":"OK" }`.

**Q:** *What error is returned if the workbook does not exist?*  
**A:** HTTP 404 with body `{ "Code":"404", "Message":"File not found." }`.

## Author

*Written by the Aspose Cloud SDK Team – over 15 years of experience building Excel automation solutions.*