---
title: "Excel Password Protection API – Set Open and Modify Passwords Programmatically"
date: 2024-05-10
lastmod: 2024-06-15
url: /protect-spreadsheet/
linktitle: "Protect Spreadsheet"
summary: "Learn how to programmatically protect Excel files with open and modify passwords using Aspose.Cells Cloud REST API. Includes cURL, SDK examples, and OAuth 2.0 integration guide."
description: "Automate Excel spreadsheet protection via REST API — set open & modify passwords in .xlsx/.xls/.xlsm files. Includes cURL, Python, Java, Node.js, and Go examples, plus OAuth 2.0 authentication and compliance best practices."
keywords: "Excel password protection API, open password, modify password, spreadsheet security, Excel encryption, Aspose.Cells Cloud, REST API"
weight: 100
---

Secure Excel files programmatically with dual-layer password protection using Aspose.Cells Cloud. Apply both **open** (decrypt required to view) and **modify** (edit restriction) passwords in a single API call — ideal for enterprise workflows handling financial reports, compliance documents, or sensitive datasets.

This API supports modern formats (`.xlsx`, `.xlsm`, `.xlsb`) and legacy `.xls` files, and integrates seamlessly with cloud storage and regional settings for global deployments.

## **Protect Spreadsheet REST API Endpoint**

```http
PUT https://api.aspose.cloud/v4.0/cells/protection/spreadsheet
```

> ✅ **API Version Note**: This page documents the current `v4.0` endpoint. Check the [API Changelog](/cells/changelog/) for updates, including potential `v5.0` migration guidance.

## **Authentication**

All requests require a valid OAuth 2.0 access token with the **Cells** scope. Tokens are obtained via Aspose Cloud’s [OAuth 2.0 flow](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

Include the token in the `Authorization` header:

```http
Authorization: Bearer YOUR_ACCESS_TOKEN
```

> **Prerequisites**  
> - Register at [Aspose Cloud Dashboard](https://dashboard.aspose.cloud/) to get your `Client ID` and `Client Secret`  
> - Exchange credentials for an access token using the [OAuth 2.0 documentation](/cells/authentication/)

## **Request Parameters**

| Parameter Name   | Type   | Location     | Required | Description |
|------------------|--------|--------------|----------|-------------|
| `Spreadsheet`    | File   | FormData     | Yes      | The Excel file to protect. Supports `.xlsx`, `.xls`, `.xlsm`, `.xlsb`, `.csv`, `.tsv`, `.ods`. |
| `password`       | String | Query        | Yes      | **Open password** — required to open/decrypt the file. Empty string (`""`) removes open protection. |
| `modifyPassword` | String | Query        | Yes      | **Modify password** — required to edit the file. Empty string (`""`) removes modify protection. |
| `outPath`        | String | Query        | No       | Path (e.g., `/output/report.xlsx`) where the protected file is saved in cloud storage. If omitted, the file is returned in the response. |
| `outStorageName` | String | Query        | No       | Name of the cloud storage (e.g., `First Aspose Cloud Storage`) to use for `outPath`. Defaults to the primary storage. |
| `region`         | String | Query        | No       | Locale setting (e.g., `en-US`, `fr-FR`, `ja-JP`) to control formatting (date, number, currency) during processing. |

### 🔐 Security Best Practices
- Never hardcode passwords in client code. Use secure vaults (e.g., AWS Secrets Manager, Azure Key Vault).
- Prefer `modifyPassword` alone for read-only sharing (no open password needed).
- Use HTTPS for all requests to protect credentials in transit.

## **Response**

Returns the protected workbook as a binary file stream (or saves to cloud storage if `outPath` is provided).

```json
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 encoded)",
  "contentType": "application/vnd.openxmlformats-officedocument.spreadsheetml.sheet",
  "fileDownloadName": "protected_workbook.xlsx"
}
```

### **HTTP Status Codes**

| Code  | Meaning               | Description |
|-------|-----------------------|-------------|
| `200` | OK                    | Protection applied successfully. Response contains the protected workbook. |
| `400` | Bad Request           | Missing/invalid parameters (e.g., unsupported file type, empty `password`/`modifyPassword` when required). |
| `401` | Unauthorized          | Invalid, expired, or missing JWT token. |
| `404` | Not Found             | Source file not found in cloud storage (if used). |
| `413` | Payload Too Large     | File exceeds 2 GB limit. |
| `500` | Internal Server Error | Unexpected error during processing (e.g., corruption, encoding issues). |

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

| Benefit | Details |
|---------|---------|
| **Developer-Friendly** | SDKs for 8+ languages (C#, Java, Python, Node.js, Go, PHP, Ruby, Perl) + REST support. Minimal code needed. |
| **Zero Infrastructure** | Fully managed cloud service — no servers, updates, or compatibility overhead. |
| **Preserves Formatting** | All Excel formatting, charts, and pivot tables remain intact after protection. |
| **Scalable & Pay-Per-Use** | Scale with usage. Free tier available for testing. [See pricing details](/pricing/). |
| **Compliance Ready** | Encrypts data in transit (TLS 1.2+) and at rest (AES-256). Supports GDPR, HIPAA, and SOC 2. [Learn about certifications](/total/compliance/). |

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

> 💡 **Tip**: Replace `open123`/`edit456` with strong passwords. Use empty strings (`password=&modifyPassword=`) to *remove* protection.

### SDK Examples

#### Python
```python
import asposecellscloud
from asposecellscloud.api import cells_api

# Initialize API client
configuration = asposecellscloud.Configuration(
    app_sid="YOUR_CLIENT_ID",
    app_key="YOUR_CLIENT_SECRET"
)
api = cells_api.CellsApi(configuration)

# Protect with open + modify passwords
response = api.cells_workbook_put_protection(
    name="workbook.xlsx",
    password="open123",
    modify_password="edit456",
    folder="input",
    out_folder="output"
)
print("Protected file saved to:", response.file_name)
```

#### Java
```java
import com.aspose.cells.cloud.*;

public class ProtectSpreadsheet {
    public static void main(String[] args) {
        String clientId = "YOUR_CLIENT_ID";
        String clientKey = "YOUR_CLIENT_SECRET";
        
        CellsApi api = new CellsApi(clientId, clientKey);
        
        try {
            File file = new File("workbook.xlsx");
            String response = api.cellsWorkbookPutProtection(
                "workbook.xlsx", 
                "open123", 
                "edit456", 
                null, 
                null
            );
            System.out.println("Protection applied: " + response);
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

> 📚 Browse all SDKs: [Aspose.Cells Cloud GitHub Repository](https://github.com/aspose-cells-cloud)  
> 🔗 See language-specific guides: [Python SDK](/cells/python/), [Java SDK](/cells/java/), [Node.js SDK](/cells/nodejs/)

### Using Cloud Storage Paths

Save directly to cloud storage with `outPath` and `outStorageName`:

```bash
curl -X PUT \
  "https://api.aspose.cloud/v4.0/cells/protection/spreadsheet?password=open123&modifyPassword=edit456&outPath=/protected/reports/report.xlsx&outStorageName=First Aspose Cloud Storage" \
  -H "Authorization: Bearer $TOKEN" \
  -F "Spreadsheet=@workbook.xlsx"
```

## **Frequently Asked Questions**

### ❓ Can I protect .xlsm (macro-enabled) files?
Yes. The API preserves macros and VBA projects. Ensure `password` and `modifyPassword` are set correctly to avoid macro execution errors.

### ❓ What happens if I forget the open password?
If you lose the open password, the file is unrecoverable — Aspose.Cells Cloud does not store passwords. Always use a secure password manager.

### ❓ Does this work with Excel Online/SharePoint?
Yes — protect files in SharePoint Online or OneDrive by saving them via `outPath` to your cloud storage, then access via the online UI (password-protected files open in Excel Online with full security).

### ❓ How do I remove password protection?
To remove protection, call the API with `password=""` and/or `modifyPassword=""`. Example:

```bash
curl -X PUT \
  "https://api.aspose.cloud/v4.0/cells/protection/spreadsheet?password=&modifyPassword=" \
  -H "Authorization: Bearer $TOKEN" \
  -F "Spreadsheet=@workbook.xlsx"
```

### ❓ Is this compliant with enterprise encryption standards?
Yes. Passwords are encrypted using AES-256 before storage. All API traffic uses TLS 1.2+. We’re aligned with ISO 27001, GDPR, and HIPAA requirements.

## **Next Steps**

- 🔒 **Explore other protection APIs**: [Remove Protection](/cells/remove-protection/), [Encrypt Document](/cells/encrypt-document/)
- 🧪 **Test in Postman**: [Download OpenAPI spec](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Protection/ProtectSpreadsheet)
- 🤝 **Integrate with your stack**: See our [integration guides for ERP/CRM](/cells/integrations/)
- 📊 **Monitor usage**: Track API calls in the [Aspose Cloud Dashboard](https://dashboard.aspose.cloud/usage)

> 🌐 **Need Help?**  
> Join our [developer community](https://forum.aspose.cloud/c/cells/) or [submit a support ticket](https://helpdesk.aspose.cloud/).