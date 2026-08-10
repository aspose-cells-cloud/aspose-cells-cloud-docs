---
title: "Aspose.Cells Cloud Excel Compression Web API – Reduce Spreadsheet File Size Programmatically"
second_title: "Document"
ArticleTitle: "How to Compress Excel Files – Reduce Spreadsheet Size & Optimize Performance"
linktitle: "Compress Spreadsheet"
type: docs
url: /compress-spreadsheet/
keywords: "Excel compression, Aspose.Cells Cloud, spreadsheet size reduction, API, workbook optimization"
description: "Learn how to compress Excel workbooks with Aspose.Cells Cloud API. Get step‑by‑step examples, parameters, authentication, and best practices."
weight: 100
---

Programmatically compress Excel spreadsheets and reduce file size with Aspose.Cells Cloud API. Optimize workbook performance by removing unused data, compressing embedded objects, and cleaning formatting. This RESTful API enables automated Excel file compression and optimization workflows.

## **Compress Spreadsheet API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/compress
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

```bash
-H "Authorization: Bearer {access_token}"
```


### Request Parameters

| Parameter Name | Type    | Path/Query/String/HTTP Body | Description                                                                                                                           |
| -------------- | ------- | --------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | File    | FormData                    | **Required.** The source Excel workbook file (`.xlsx`, `.xls`, etc.) to compress.                                                     |
| level          | Integer | Query                       | **Optional.** Compression intensity (0 = fastest/lowest, 9 = slowest/highest). If omitted, a balanced default (5) is applied.         |
| outPath        | String  | Query                       | **Optional.** Destination folder path in your cloud storage. If omitted, the file is saved in the same folder as the source workbook. |
| outStorageName | String  | Query                       | **Required.** Identifier of the configured cloud storage service (e.g., `CorporateDrive`).                                            |
| region         | String  | Query                       | **Optional.** Locale setting (e.g., `de-DE`) that may affect region‑specific data handling.                                           |
| password       | String  | Query                       | **Optional.** Password for decrypting a protected spreadsheet. Leave blank if the file is not encrypted.                              |

**Sample cURL request**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/compress?level=5&outStorageName=MyStorage" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/input.xlsx"
```

### Response

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

**HTTP Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter applied successfully; response contains operation details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |
## Where should we use the Compress Spreadsheet API?

- **Automated report distribution** – Compress monthly financial statements before emailing them to ensure successful delivery and improve the recipient’s experience.
- **User file‑upload optimization** – Compress uploaded Excel files in the background to save cloud storage space and reduce storage costs.
- **Data‑pipeline processing and migration** – Compress intermediate Excel files generated during ETL processes to speed up network transfer and lower temporary‑storage pressure.

## Why should you use the Compress Spreadsheet API?

- **Developer‑friendly** – Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling rapid development with comprehensive documentation.
- **Reduced labor costs** – Eliminates the need for dedicated personnel to consolidate documents manually.
- **Pay‑per‑use pricing** – No upfront investment; you only pay for the API calls you actually make.
- **No server maintenance required** – No servers to maintain, no software updates, and no compatibility concerns.

## How to Use the Compress Spreadsheet API with SDKs

### Compress Spreadsheet API Specification

The [Compress Spreadsheet API Specification](https://reference.aspose.cloud/cells/#/ManagementController/CompressSpreadsheet) provides a publicly accessible interface for REST interactions, allowing direct API calls from a web browser.

### Use Aspose.Cells Cloud SDKs

Using an SDK is the fastest way to develop, as it abstracts low‑level details and lets you compress a spreadsheet with just a few lines of code. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to interact with Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CompressSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CompressSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CompressSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CompressSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CompressSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CompressSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CompressSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CompressSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}

