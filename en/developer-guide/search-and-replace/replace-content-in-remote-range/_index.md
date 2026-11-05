---
url: /replace-content-in-remote-range/
title: "Replace Text in Remote Range"
linktitle: "Replace Remote Range Content"
type: docs
description: "Replace text in a specific Excel range via Aspose.Cells Cloud API with cloud storage integration"
keywords: "replace text remote excel range, Aspose.Cells Cloud API, find and replace Excel, cloud spreadsheet edit, remote Excel file update"
weight: 100
ArticleTitle: "Replace Text in Remote Excel Range via Aspose.Cells Cloud API"
---
The **ReplaceContentInRemoteRange** API (`PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/replace/content`) in Aspose.Cells Cloud v4.0 enables precise, bulk text replacement within a specified cell range of a remote Excel file stored in cloud storage—such as AWS S3, Azure Blob, or Google Cloud Storage—without requiring the file to be downloaded locally.

---

## The Replace Content in Remote Range Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/replace/content
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type   | Path/Query String/HTTPBody | Description                                                                                                                             |
| -------------- | ------ | -------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| name           | String | Path                       | The name of the workbook file to be replace.                                                                                            |
| searchText     | String | Query                      | The searched text.                                                                                                                      |
| replaceText    | String | Query                      | The replaced text.                                                                                                                      |
| worksheet      | String | Path                       | The worksheet name.                                                                                                                     |
| cellArea       | String | Path                       | The cell area for the replace.                                                                                                          |
| folder         | String | Query                      | The folder path where the workbook is stored.                                                                                           |
| storageName    | String | Query                      | (Optional) The name of the storage if using custom cloud storage. Use default storage if omitted.                                       |
| region         | String | Query                      | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password       | String | Query                      | The password for opening spreadsheet file.                                                                                              |

### Response

```json
[
  {
    "Name": "CellsCloudResponse",
    "DataType": {
      "Identifier": "Class",
      "Reference": "CellsCloudResponse"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/json
```

A successful request returns a `200 OK` status with the following JSON body:

The `CellsCloudResponse` object confirms successful execution. The API does **not** return the count or locations of replacements—only success confirmation.

### Error Codes

| Code | Message      | Cause                                                                         |
| ---- | ------------ | ----------------------------------------------------------------------------- |
| 400  | Bad Request  | Invalid URL, malformed parameters, or unsupported file format.                |
| 401  | Unauthorized | Missing, expired, or invalid access token.                                    |
| 404  | Not Found    | Workbook, worksheet, or specified range does not exist.                       |
| 500  | Server Error | Internal failure during processing (e.g., file corruption, permission error). |

---

### HTTP Request

## Use Cases

- **Template Content Updates**: Dynamically replace placeholder text in cloud-hosted Excel templates (e.g., quarterly reports, invoices).
- **Batch Data Standardization**: Standardize text across multiple Excel files in cloud storage (e.g., region-specific currency or unit labels).
- **Cross-Region Deployment**: Synchronize content consistency for Excel files deployed across regions while respecting locale settings.
- **Automated Reporting Pipelines**: Integrate into CI/CD workflows to inject runtime values into Excel reports stored in object storage.

---

## How to Use the Replace Content in Remote Range API with SDKs?

### Replace Content in Remote Range API Specification

The <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceContentInRemoteRange" rel="noopener noreferrer">Replace Content in Remote Range API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.
