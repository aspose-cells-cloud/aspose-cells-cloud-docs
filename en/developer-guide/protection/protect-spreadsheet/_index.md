---
title: "Excel Password Protection API – Set Open and Modify Passwords Programmatically"
url: /protect-spreadsheet/
linktitle: "Protect Spreadsheet"
type: docs
summary: "Learn how to programmatically protect Excel files with open and modify passwords using Aspose.Cells Cloud REST API. Includes cURL, SDK examples, and OAuth 2.0 integration guide."
description: "Protect Excel files with open or modify passwords using Aspose.Cells Cloud REST API for enterprise workflows."
keywords: "Excel password protection API, open password, modify password, spreadsheet security, Excel encryption, Aspose.Cells Cloud, REST API"
weight: 100
ArticleTitle: "Aspose.Cells Cloud Protect Spreadsheet API: Set Open & Modify Passwords Programmatically"
---
The **ProtectSpreadsheet** API (`PUT https://api.aspose.cloud/v4.0/cells/protection/spreadsheet`) in Aspose.Cells Cloud applies dual-layer password protection to Excel spreadsheets, allowing developers to set both an open password (to restrict file access) and a modify password (to prevent editing) in a single request, with passwords encrypted for enhanced security.

This API supports modern formats (`.xlsx`, `.xlsm`, `.xlsb`) and legacy `.xls` files, and integrates seamlessly with cloud storage and regional settings for global deployments.

## The Protect Spreadsheet Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/protection/spreadsheet
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### **Request Parameters**

| Parameter Name | Type   | Path/Query String/HTTPBody | Description                                                                                                                             |
| -------------- | ------ | -------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | File   | FormData                   | Upload spreadsheet file.                                                                                                                |
| password       | String | Query                      | Spreadsheet file encryption password.                                                                                                   |
| modifyPassword | String | Query                      | Sets the protected password to modify the file.                                                                                         |
| outPath        | String | Query                      | (Optional) The folder path where the workbook is stored. The default is null.                                                           |
| outStorageName | String | Query                      | Output file Storage Name.                                                                                                               |
| region         | String | Query                      | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |

### **Response**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result"
```

Returns the protected workbook as a binary file stream (or saves to cloud storage if `outPath` is provided).

> ✅ **API Version Note**: This page documents the current `v4.0` endpoint. Check the [API Changelog](/cells/changelog/) for updates, including potential `v5.0` migration guidance.

### 🔐 Security Best Practices

- Never hardcode passwords in client code. Use secure vaults (e.g., AWS Secrets Manager, Azure Key Vault).
- Prefer `modifyPassword` alone for read-only sharing (no open password needed).
- Use HTTPS for all requests to protect credentials in transit.

### **HTTP Status Codes**

| Code  | Meaning               | Description                                                                                                |
| ----- | --------------------- | ---------------------------------------------------------------------------------------------------------- |
| `200` | OK                    | Protection applied successfully. Response contains the protected workbook.                                 |
| `400` | Bad Request           | Missing/invalid parameters (e.g., unsupported file type, empty `password`/`modifyPassword` when required). |
| `401` | Unauthorized          | Invalid, expired, or missing JWT token.                                                                    |
| `404` | Not Found             | Source file not found in cloud storage (if used).                                                          |
| `413` | Payload Too Large     | File exceeds 2 GB limit.                                                                                   |
| `500` | Internal Server Error | Unexpected error during processing (e.g., corruption, encoding issues).                                    |

## **Where to Use This API**

- **Secure Financial Data**  
  Protect budgets, invoices, and payroll files with open and modify passwords to prevent unauthorized viewing or tampering.

- **Compliance & Audit Reporting**  
  Enforce access controls for SOX, HIPAA, or GDPR-sensitive data in Excel reports — ensure only authorized teams can modify audit trails.

- **Automated Document Workflows**  
  Integrate into ERP/CRM pipelines (e.g., SAP, Salesforce) to auto-protect generated reports before storage or email delivery.

- **Template Distribution**  
  Share finalized templates (e.g., budgets, forecasts) as read-only by setting only a `modifyPassword`, allowing users to view but not edit.

- **Enterprise Data Governance**  
  Centralize spreadsheet security policies across departments using programmatic enforcement — no manual steps.

## **Why Use Aspose.Cells Cloud Protection API?**

| Benefit                    | Details                                                                                                                                       |
| -------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| **Developer-Friendly**     | SDKs for 8+ languages (C#, Java, Python, Node.js, Go, PHP, Ruby, Perl) + REST support. Minimal code needed.                                   |
| **Zero Infrastructure**    | Fully managed cloud service — no servers, updates, or compatibility overhead.                                                                 |
| **Preserves Formatting**   | All Excel formatting, charts, and pivot tables remain intact after protection.                                                                |
| **Scalable & Pay-Per-Use** | Scale with usage. Free tier available for testing. [See pricing details](/pricing/).                                                          |
| **Compliance Ready**       | Encrypts data in transit (TLS 1.2+) and at rest (AES-256). Supports GDPR, HIPAA, and SOC 2. [Learn about certifications](/total/compliance/). |

## **How to Use the Protect Spreadsheet API**

### Prerequisites

1. [Create an Aspose Cloud account](https://dashboard.aspose.cloud/)
2. Get `Client ID` and `Client Secret` from the dashboard
3. Generate an `access_token` via OAuth 2.0

### cURL Example

```bash
# Step 1: Obtain access token (replace placeholders)
TOKEN=$(curl -X POST "https://api.aspose.cloud/connect/token" \
  -d "grant_type=client_credentials&client_id=YOUR_CLIENT_ID&client_secret=YOUR_CLIENT_SECRET" \
  | jq -r '.access_token')

# Step 2: Protect the spreadsheet
curl -X PUT "https://api.aspose.cloud/v4.0/cells/protection/spreadsheet?password=open123&modifyPassword=edit456" \
  -H "Authorization: Bearer $TOKEN" \
  -H "Content-Type: multipart/form-data" \
  -F "Spreadsheet=@/path/to/workbook.xlsx" \
  --output protected_workbook.xlsx
```

> 💡 **Tip**: Replace `open123`/`edit456` with strong passwords. Use empty strings (`password=&modifyPassword=`) to _remove_ protection.

### Using Cloud Storage Paths

Save directly to cloud storage with `outPath` and `outStorageName`:

```bash
curl -X PUT \
  "https://api.aspose.cloud/v4.0/cells/protection/spreadsheet?password=open123&modifyPassword=edit456&outPath=/protected/reports/report.xlsx&outStorageName=First Aspose Cloud Storage" \
  -H "Authorization: Bearer $TOKEN" \
  -F "Spreadsheet=@workbook.xlsx"
```

## How to Use the Protect Spreadsheet API with SDKs?

### Protect Spreadsheet API Specification

The <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Protection/ProtectSpreadsheet" rel="noopener noreferrer">Protect Spreadsheet API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="2" tabID="1" tabName1="PHP" tabName2="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ProtectSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ProtectSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}
