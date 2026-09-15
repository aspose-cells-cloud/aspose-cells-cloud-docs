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

The **uploadFile** API enables developers to upload files directly to cloud storage for processing with Aspose Cells.

## **Aspose Cells API: Upload File**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### The request parameters of the **uploadFile** API are

| Parameter Name | Type   | Path/Query String/HTTP Body | Description                                                                                    |
| :------------- | :----- | :-------------------------- | :--------------------------------------------------------------------------------------------- |
| UploadFiles    | File   | FormData                    | Upload files to cloud storage.                                                                 |
| path           | String | Path                        | The destination path in the cloud storage. Specify the path where the file should be uploaded. |
| storageName    | String | Query                       | The name of the storage where the file will be uploaded.                                       |

### **Response**

```json
{
  "Name": "FilesUploadResult",
  "Description": ["File upload result"],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Uploaded",
      "Description": ["List of uploaded file names"],
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
      "Description": ["List of errors."],
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

| Status Code                   | Description                                         |
| ----------------------------- | --------------------------------------------------- |
| **200 OK**                    | File uploaded successfully.                         |
| **400 Bad Request**           | Invalid parameters or malformed request.            |
| **401 Unauthorized**          | Missing or invalid authentication token.            |
| **403 Forbidden**             | Insufficient permissions for the specified storage. |
| **500 Internal Server Error** | Unexpected server error.                            |

## How to Use the upload file API with SDKs?

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/FileController/UploadFile) provides a detailed description of the API, enabling developers to interact with it directly via a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/Folder/Book1.xlsx" \
  -H "Authorization: Bearer {access_token}" \
  -F "UploadFiles=@/path/to/Book1.xlsx" \
  -F "path=Folder/Book1.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Uploaded": ["Book1.xlsx"],
  "Errors": []
}
```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose.Cells Cloud SDKs

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
