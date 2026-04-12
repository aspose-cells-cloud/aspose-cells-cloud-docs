---
title: "Aspose.Cells Cloud Download File API – Interface for Fast File Download in the Cloud"
second_title: "Document"
ArticleTitle: "Cloud-based Excel File Management Solution – Interface for Fast File Download in the Cloud"
linktitle: "Download File API"
type: docs
url: /download-file/
keywords: "Aspose.Cells, Download File API, Excel cloud storage, REST API, file download, PDF, CSV, SDK"
description: "Learn how to download Excel, PDF, CSV, and other files from Aspose.Cells Cloud storage using the secure Download File API (v4.0). Includes endpoint, parameters, authentication, and code samples."
weight: 100
---

## **Excel API: Download File**

### Web API

```http
GET https://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

**Version** – This documentation refers to API version **v4.0**, which is the latest release at the time of publishing.

### **Function Description**

The **DownloadFile** API enables you to retrieve files stored in Aspose.Cells Cloud storage. The Download File API is essential for accessing Excel spreadsheets, PDFs, CSVs, and other supported formats directly from the cloud.

### The request parameters of **DownloadFile** API are

| Parameter Name | Type   | Location (Path / Query) | Description                                                    |
| -------------- | ------ | ----------------------- | -------------------------------------------------------------- |
| path           | String | Path                    | The virtual path to the file you want to download.             |
| storageName    | String | Query                   | The name of the storage from which the file will be retrieved. |
| versionId      | String | Query                   | The version identifier of the file to download, if applicable. |

### **Response Description**

The API returns a **binary file stream**. The `Content-Type` header matches the file format (e.g., `application/vnd.openxmlformats-officedocument.spreadsheetml.sheet` for XLSX). No JSON payload is returned.

**Error handling**

| HTTP Code | Error Code   | Message                                                  |
| --------- | ------------ | -------------------------------------------------------- |
| 400       | BadRequest   | The request is malformed or missing required parameters. |
| 401       | Unauthorized | Authentication failed – missing or invalid token.        |
| 404       | FileNotFound | The specified file does not exist in the given storage.  |
| 500       | ServerError  | An unexpected error occurred on the server.              |

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/FileController/DownloadFile) defines a publicly accessible programming interface and allows you to perform REST interactions directly from a web browser.

## Excel API SDK

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
