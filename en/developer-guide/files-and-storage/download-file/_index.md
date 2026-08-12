---
title: "Aspose.Cells Cloud Download File API – Interface for Fast File Download in the Cloud"
second_title: "Document"
ArticleTitle: "Aspose.Cells Cloud Download File API – Interface for Fast File Download in the Cloud"
linktitle: "Download File API"
type: docs
url: /download-file/
keywords: "Aspose.Cells, Download File API, Excel cloud storage, REST API, file download, PDF, CSV, SDK"
description: "Download Excel, PDF, CSV, and other files from Aspose.Cells Cloud storage using the Download File API (v4.0). Includes endpoint, parameters, authentication details, and code samples."
weight: 100
---

The **DownloadFile** API enables you to retrieve files stored in Aspose.Cells Cloud storage. The Download File API is essential for accessing Excel spreadsheets, PDFs, CSVs, and other supported formats directly from the cloud.

## **Excel API: Download File**

### Web API

```http
GET https://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### The request parameters of **DownloadFile** API are

| Parameter Name | Type   | Location (Path / Query) | Description                                                    |
| -------------- | ------ | ----------------------- | -------------------------------------------------------------- |
| path           | String | Path                    | The virtual path to the file you want to download.             |
| storageName    | String | Query                   | The name of the storage from which the file will be retrieved. |
| versionId      | String | Query                   | The version identifier of the file to download, if applicable. |

### **Response**

The API returns a **binary file stream**. The `Content-Type` header matches the file format (e.g., `application/vnd.openxmlformats-officedocument.spreadsheetml.sheet` for XLSX). No JSON payload is returned.

**HTTP Status Codes**

| Code | Meaning               | Description                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Filter applied successfully; response contains operation details. |
| 400  | Bad Request           | Missing or invalid parameters (e.g., unsupported file type).      |
| 401  | Unauthorized          | Invalid or missing JWT token.                                     |
| 413  | Payload Too Large     | Uploaded file exceeds size limit.                                 |
| 500  | Internal Server Error | Unexpected server error.                                          |

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/FileController/DownloadFile) defines a publicly accessible programming interface and allows you to perform REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/file/Example.xlsx?storageName=MyStorage" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Accept: application/octet-stream" \
     -o Example.xlsx
```

{{< /tab >}}

{{< tab tabNum="12" >}}

{{< /tab >}}

{{< /tabs >}}

### Use Aspose.Cells Cloud SDKs

Using an SDK is the best way to speed up development. An SDK handles low‑level details and enables you to focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DownloadFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DownloadFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DownloadFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DownloadFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DownloadFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DownloadFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DownloadFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DownloadFile.go" >}}
{{</tab>}}
{{< /tabs >}}
