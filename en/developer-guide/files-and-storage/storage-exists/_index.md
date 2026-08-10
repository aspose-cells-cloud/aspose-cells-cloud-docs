---
title: "Check if a Storage Exists – Aspose.Cells Cloud API (v4.0)"
second_title: "Document"
ArticleTitle: "Cloud-based Excel File Management – Check Storage Existence"
linktitle: "Storage Exists"
type: docs
url: /storage-exists/
keywords: "Aspose.Cells, storage exists, cloud storage API, REST, Excel"
description: "Verify the existence of a storage container in Aspose.Cells Cloud. Learn the GET /v4.0/cells/storage/{storageName}/exist endpoint, required parameters, response format, and see SDK examples in C#, Java, Python, and more."
weight: 100
---

## Check Storage Existence (storageExists)

**Summary** – The `storageExists` endpoint lets you confirm whether a specific storage container is available in Aspose.Cells Cloud. Use it before performing file‑related operations to avoid runtime errors.

**Prerequisites** – The request must include a valid JWT access token with the necessary scope for storage operations. Ensure the token is obtained via the standard Aspose.Cells authentication flow before invoking this endpoint.

### Web API

```
GET https://api.aspose.cloud/v4.0/cells/storage/{storageName}/exist
```

**cURL example**

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/{storageName}/exist" \
     -H "Authorization: Bearer {access_token}"
```

### Function Description

The `storageExists` API checks whether a specified storage exists in the Aspose.Cells cloud service. This functionality is critical for ensuring that all operations dependent on storage can proceed without errors.

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type   | Location | Description                                     |
| -------------- | ------ | -------- | ----------------------------------------------- |
| storageName    | String | Path     | The name of the storage to check for existence. |

### Response Description

```json
{
  "Name": "StorageExist",
  "Description": ["Indicates whether the specified storage exists."],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Exists",
      "Description": [
        "Indicates if the storage exists.",
        "This property returns true if the storage is present; otherwise, it returns false."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Boolean",
        "Name": "boolean"
      }
    }
  ]
}
```

**Example response**

```json
{
  "Exists": true
}
```

**HTTP Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter applied successfully; response contains operation details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |
## OpenAPI Specification

The <a href="https://reference.aspose.cloud/cells/#/StorageController/StorageExists" rel="nofollow noopener noreferrer">OpenAPI Specification</a> defines a publicly accessible programming interface, allowing developers to seamlessly interact with the REST API directly from a web browser.

## Excel API SDK

Utilizing an SDK is the most efficient approach to accelerate development. An SDK abstracts low‑level implementation details, enabling developers to concentrate on their project tasks. For a comprehensive list of available Aspose.Cells Cloud SDKs, please visit the <a href="https://github.com/aspose-cells-cloud" rel="nofollow noopener noreferrer">GitHub repository</a>.

The following code examples demonstrate how to make API calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_StorageExists.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_StorageExists.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_StorageExists.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_StorageExists.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_StorageExists.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_StorageExists.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_StorageExists.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_StorageExists.go" >}}
{{</tab>}}
{{< /tabs >}}