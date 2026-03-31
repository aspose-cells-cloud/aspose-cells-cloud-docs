---
title: "Aspose.Cells Cloud Excel Password Protection Web API – Automate Open and Modify Password Encryption"
second_title: "Developer Guide for Excel Protection"
ArticleTitle: "Excel Password Protection Tool – Set Open and Modify Passwords – Secure Your Spreadsheets"
linktitle: "Protect Spreadsheet"
type: docs
url: /protect-spreadsheet/
keywords: "Aspose.Cells, Excel password protection, API, open password, modify password, cloud storage, spreadsheet security"
description: "Secure Excel files programmatically with Aspose.Cells Cloud. Set both open and modify passwords via a single API call. Supports .xlsx, .xls, and cloud storage. Try it free."
weight: 100
---

Automate Excel password protection at scale with our developer API—apply both open and modify passwords programmatically. Ideal for enterprise workflows and compatible with .xlsx and legacy formats. Get documentation and start your free integration today.

## **Protect Spreadsheet API**

### API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/protection/spreadsheet
```

**Authentication** – All calls require an OAuth 2.0 access token. Include the header  
`Authorization: Bearer <access_token>` in the request. Tokens are obtained via the client‑credentials flow and are valid for the period returned by the token service.

### **Request Parameters:**

| Parameter Name | Type   | Path/Query String/HTTPBody | Description |
| :- | :- | :- | :- |
| Spreadsheet     | File   | FormData | The Excel spreadsheet file to be uploaded and protected with password encryption. |
| openPassword    | String | Query    | The password required to open (decrypt) the protected spreadsheet. |
| modifyPassword  | String | Query    | The password required to enable editing or modification of the spreadsheet contents. |
| outPath         | String | Query    | (Optional) Specifies the output folder path where the protected workbook will be saved. If not provided, the file is returned in the response. |
| outStorageName  | String | Query    | The name of the cloud storage used for storing the output protected file. |
| region          | String | Query    | Specifies the regional/cultural settings (e.g., date format, number formatting) applied to the spreadsheet during processing. |

**cURL example**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/protection/spreadsheet?openPassword=MyOpenPwd&modifyPassword=MyEditPwd" \
  -H "Authorization: Bearer <access_token>" \
  -F "Spreadsheet=@/path/to/Report.xlsx" \
  -F "outPath=protected/Report_protected.xlsx"
```

## **Response**

```json
{
  "FileName": "Report_protected.xlsx",
  "Url": "https://api.aspose.cloud/v4.0/storage/file/protected/Report_protected.xlsx",
  "Size": 124567,
  "Status": "OK"
}
```

### Error Codes

- **400 Bad Request** – Invalid Aspose.Cells Cloud API URI.  
- **401 Unauthorized** – Invalid access token, client‑id, or client‑secret.  
- **403 Forbidden** – Token lacks required scope or insufficient permissions.  
- **404 Not Found** – The spreadsheet file is not accessible.  
- **429 Too Many Requests** – Rate limit exceeded; retry after the period indicated in the `Retry-After` header.  
- **500 Server Error** – The spreadsheet encountered an internal processing error.

## Where should we use the Protect Spreadsheet API?

- **Secure Sensitive Financial Data** – Protect Excel files containing budgets, invoices, or payroll information with open and modify passwords to prevent unauthorized access or edits.  
- **Share Confidential Reports Safely** – Ensure only authorized recipients can view or alter business, audit, or compliance reports when distributing internally or externally.  
- **Automate Document Security in Workflows** – Integrate the API into enterprise systems (e.g., ERP, CRM) to automatically password‑protect generated spreadsheets before storage or email delivery.  
- **Enforce Read‑Only Access** – Allow users to open reports for viewing while restricting modifications using a separate modify password—ideal for templates or finalized datasets.  
- **Meet Regulatory Compliance** – Help satisfy GDPR, HIPAA, or SOX requirements by encrypting sensitive spreadsheet data at rest and in transit through automated protection.

## Why should you use the Protect Spreadsheet API?

- **Developer‑Friendly** – Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling quick development and comes with comprehensive documentation. Compared with building custom solutions, this significantly reduces development workload.  
- **Reduces Staffing Needs** – Automates document consolidation and security, lowering the need for dedicated personnel.  
- **Pay‑per‑Use** – No upfront investment; you only pay for the API calls you actually use.  
- **Zero Maintenance Costs** – No servers to maintain, no software updates, and no compatibility concerns.  
- **Preserves All Original Excel Formatting** while applying password protection, ensuring the protected workbook looks exactly like the source file.

## How to Use the Protect Spreadsheet API with SDKs

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/ProtectionController/ProtectSpreadsheet) provides a detailed programming interface for executing REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement protect‑spreadsheet functionality with minimal code. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to interact with Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ProtectSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ProtectSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ProtectSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ProtectSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ProtectSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ProtectSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ProtectSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ProtectSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}