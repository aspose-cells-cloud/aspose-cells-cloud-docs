---
title: "Get metadata from Excel files"
second_title: "Developer Guide"
linktitle: "Get without using storage"
type: docs
url: /metadata/get/
keywords: "Aspose.Cells, Excel, metadata, REST API, cloud SDK"
description: "Get Excel metadata via Aspose.Cells Cloud API—built-in and custom properties with OAuth-secured POST /cells/metadata/get"
weight: 23
ArticleTitle: "Get metadata from Excel files - Aspose.Cells Cloud API"
---
The **GetMetadata** API (`POST https://api.aspose.cloud/v3.0/cells/metadata/get`) retrieves document properties—such as title, author, or custom built-in metadata—from one or more Excel files uploaded via form-data. Using Aspose.Cells Cloud, this operation supports extracting structured metadata without requiring local Excel installation, enabling programmatic analysis of workbook properties across cloud-based workflows.

## The Get Metadata Web API

```http
POST https://api.aspose.cloud/v3.0/cells/metadata/get
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### Query Parameter

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| File | File | FormData | File to upload |
| type | String | Query | Cells document property name. |
| password | String | Query | The password needed to open an Excel file. |
| checkExcelRestriction | Boolean | Query | Whether check restriction of excel file when user modify cells related objects. |

### Response

```json
[
  {
    "Name": "IList`1",
    "DataType": {
      "Identifier": "Container",
      "Reference": "CellsDocumentProperty"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/json
```

**HTTP Status Codes**

| Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request completed successfully. |
| 400 | Bad Request | The request is malformed or one or more parameters are invalid. |
| 401 | Unauthorized | Authentication failed, or the JWT token is missing or expired. |
| 404 | Not Found | The requested workbook, worksheet, or resource was not found. |
| 413 | Payload Too Large | The uploaded file exceeds the allowed size limit. |
| 500 | Internal Server Error | The server encountered an unexpected error while processing the request. |

The API returns these standard HTTP status codes together with an error‑response JSON object when applicable.

### Request Body Parameter

| Parameter Name | Type      | Description                                                         |
| -------------- | --------- | ------------------------------------------------------------------- |
| excel file     | data file | The Excel file supplied as the first part of the multipart request. |

### Cloud SDK Family

Using a SDK accelerates development by handling low‑level details. See the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services with various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetMetadata.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetMetadata.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetMetadata.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetMetadata.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetMetadata.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetMetadata.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetMetadata.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetMetadata.go" >}}

{{< /tab >}}

{{< /tabs >}}