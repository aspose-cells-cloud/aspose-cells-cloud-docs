---  
title: "Aspose.Cells Cloud API – Get Files List (Folder Contents)"  
second_title: "Document"  
ArticleTitle: "Cloud-based Excel File Management Solution – Interface for Quickly Getting File List in the Cloud"  
linktitle: "Get Files List"  
type: docs  
url: /get-files-list/  
description: "Retrieve a list of files and sub‑folders from a specific folder in Aspose.Cells Cloud storage. Includes endpoint, parameters, sample request, and SDK examples."  
keywords: "Aspose.Cells, API, Get Files List, Cloud Storage, Excel, REST"  
weight: 100  
---  

## **Excel API: Get Files List**

The **Get Files List** operation returns the collection of files and sub‑folders stored in a specified folder.

### API Endpoint  

```
GET https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

**Authentication** – Every request must contain a valid OAuth 2.0 bearer token:  

```
Authorization: Bearer <access_token>
```

**Sample Request**  

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/folder/MyFolder?storageName=MyStorage" \
     -H "Authorization: Bearer {access_token}"
```  

### Function Description  

The **getFilesList** API retrieves a comprehensive list of files and folders contained within a specified directory in Aspose.Cells Cloud storage. This endpoint is essential for efficient file management and supports a variety of Excel‑related file formats.

### Request Parameters for Get Files List API  

| Parameter Name | Type   | Location | Description |
|----------------|--------|----------|-------------|
| **path**       | String | Path     | The path to the folder in cloud storage from which the file list is retrieved. |
| **storageName**| String | Query    | (Optional) The name of the storage to access. |
| **pageSize**   | Integer| Query    | (Optional) Maximum number of items to return per page. |
| **pageNumber** | Integer| Query    | (Optional) Page number to retrieve (starting at 1). |

### Response Description  

```json
{
  "Name": "FilesList",
  "Description": [
    "Files list"
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Value",
      "Description": [
        "Files and folders contained by the specified StorageFile."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "StorageFile",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "StorageFile",
          "Name": "class:storagefile"
        },
        "Name": "container"
      }
    }
  ]
}
```

#### Common Error Responses  

| HTTP Status | Meaning                     | Response Body (example) |
|-------------|----------------------------|--------------------------|
| **200 OK**  | Successful retrieval.      | `{ "Value": [ … ] }` |
| **400 Bad Request** | Invalid parameters. | `{ "Code": 400, "Message": "Invalid request." }` |
| **401 Unauthorized** | Missing or invalid token. | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404 Not Found** | Specified folder does not exist. | `{ "Code": 404, "Message": "Folder not found." }` |
| **500 Internal Server Error** | Server‑side problem. | `{ "Code": 500, "Message": "Unexpected error." }` |

## OpenAPI Specification  

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/FolderController/GetFilesList) defines a publicly accessible programming interface that enables REST interactions directly from a web browser, facilitating easy integration and testing.

## Excel API SDK  

Utilizing an SDK is the optimal approach to accelerate your development process. An SDK manages low‑level details, allowing you to concentrate on your project tasks. For a complete list of Aspose.Cells Cloud SDKs, please visit the [GitHub repository](https://github.com/aspose-cells-cloud).

The following code examples illustrate how to invoke Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetFilesList.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetFilesList.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetFilesList.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetFilesList.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetFilesList.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetFilesList.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetFilesList.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetFilesList.go" >}}
{{</tab>}}
{{< /tabs >}}