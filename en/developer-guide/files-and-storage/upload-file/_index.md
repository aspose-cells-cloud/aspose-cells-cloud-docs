---
title: "Aspose.Cells Cloud Upload File API – An Interface for Fast Uploading of Files in the Cloud"
second_title: "Document"
ArticleTitle: "Aspose.Cells Cloud Upload File API – An Interface for Fast Uploading of Files in the Cloud"
linktitle: "Upload File"
type: docs
url: /upload-file/
keywords: "Aspose.Cells, file upload, Excel API, cloud storage, REST API"
description: "Guide to uploading files with Aspose.Cells Cloud API, covering request parameters, HTTP status codes, error handling, and code examples."
weight: 100
---

## **Aspose Cells API: Upload File**

**Prerequisites**: Before calling this endpoint you must obtain an OAuth 2.0 access token using your Aspose Cloud client ID and client secret. Include the token in the `Authorization: Bearer {access_token}` header. The token must have the **Storage** scope. See the authentication guide for details.

```
PUT http://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **Function Description**

The **uploadFile** API enables developers to upload files directly to cloud storage for processing with Aspose Cells.

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### The request parameters of the **uploadFile** API are

| Parameter Name | Type | Path/Query String/HTTP Body | Description |
| :- | :- | :- |:- |
| UploadFiles | File | FormData | Upload files to cloud storage. |
| path | String | Path | The destination path in the cloud storage. Specify the path where the file should be uploaded. |
| storageName | String | Query | The name of the storage where the file will be uploaded. |

**cURL Example**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/Folder/Book1.xlsx" \
  -H "Authorization: Bearer {access_token}" \
  -F "UploadFiles=@/path/to/Book1.xlsx" \
  -F "path=Folder/Book1.xlsx"
```

### **Response Description**

```json
{
  "Name": "FilesUploadResult",
  "Description": [
    "File upload result"
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Uploaded",
      "Description": [
        "List of uploaded file names"
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "String",
        "ElementDataType": {
          "Identifier": "String",
          "Name": "string"
        },
        "Name": "container"
      }
    },
    {
      "Name": "Errors",
      "Description": [
        "List of errors."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "Error",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "Error",
          "Name": "class:error"
        },
        "Name": "container"
      }
    }
  ]
}
```

The API returns the following HTTP status codes:

| Status Code | Description |
|-------------|-------------|
| **200 OK** | File uploaded successfully. |
| **400 Bad Request** | Invalid parameters or malformed request. |
| **401 Unauthorized** | Missing or invalid authentication token. |
| **403 Forbidden** | Insufficient permissions for the specified storage. |
| **500 Internal Server Error** | Unexpected server error. |

For a complete list of error codes, refer to the [Error Codes reference](/error-codes/).

**Best Practices**

- Ensure the file size does not exceed the service limit (default 500 MB).  
- Use HTTPS endpoints to protect data in transit.  
- Retry transient failures (e.g., 5xx responses) with exponential back‑off.  
- Validate file formats before uploading to avoid unnecessary errors.

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/FileController/UploadFile) provides a detailed description of the API, enabling developers to interact with it directly via a web browser.

## Aspose Cells API SDK

Utilizing an SDK enhances development efficiency by managing low‑level details, allowing developers to concentrate on project tasks. Visit the [GitHub repository](https://github.com/aspose-cells-cloud) for a comprehensive list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to call Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UploadFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UploadFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UploadFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UploadFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UploadFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UploadFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UploadFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UploadFile.go" >}}
{{</tab>}}
{{< /tabs >}}

**See also**

- [Download File API](/download-file/) – Retrieve a file from cloud storage.  
- [Copy File API](/copy-file/) – Duplicate a file within cloud storage.  
- [Delete File API](/delete-file/) – Remove a file from cloud storage.  