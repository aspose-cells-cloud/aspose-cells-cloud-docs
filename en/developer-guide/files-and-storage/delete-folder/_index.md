---
title: "Delete Folder"
second_title: "Aspose.Cells Cloud"
linktitle: "Delete Folder"
type: docs
url: /delete-folder/
keywords: "Delete folder, Aspose.Cells API, RESTful API, Excel file management, cloud storage"
description: "Learn how to delete a folder in Aspose.Cells using the deleteFolder API, including parameters and code examples."
weight: 100
kwords: "Excel API, Office Cloud, REST API, Spreadsheet management, PDF, CSV, JSON, Markdown, delete folder in Excel worksheets"
---

# **Excel API : Delete Folder**

## **Interface Details**

### **Endpoint** 

```
DELETE http://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **Function Description**
The `deleteFolder` API allows users to remove a specified folder from the cloud storage associated with Aspose.Cells. This can be useful for maintaining organization and managing storage effectively.

### The request parameters of **deleteFolder** API are: 

| Parameter Name | Type | Path/Query String/HTTPBody | Description | 
| :- | :- | :- |:- | 
| path | String | Path | The path of the folder to be deleted. |
| storageName | String | Query | The name of the storage where the folder is located. |
| recursive | Boolean | Query | Indicates if the deletion should be recursive, removing all contents within the folder as well. |

### **Response Description**
```json
{
Void
}
```

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/FolderController/DeleteFolder) defines a publicly accessible programming interface and allows you to perform REST interactions directly from a web browser.

## Excel API SDK 

Using an SDK is the best way to speed up development. An SDK handles low-level details, allowing you to focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteFolder.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteFolder.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteFolder.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteFolder.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteFolder.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteFolder.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteFolder.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteFolder.go" >}}
{{</tab>}}
{{< /tabs >}}