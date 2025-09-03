---
title: "Move Folder"
second_title: "Aspose.Cells Cloud"
linktitle: "Move Folder"
type: docs
url: /move-folder/
keywords: "Move folder API, Excel API, Folder management, REST API, Aspose.Cells, Cloud storage"
description: "This documentation provides a comprehensive guide to using the Move Folder API for managing folders within the Aspose.Cells cloud storage."
weight: 100
kwords: "Excel API, Move folder API, Office Cloud, REST API, Spreadsheet management, PDF, CSV, JSON, Markdown, Match all blank cells in an Excel worksheet"
---

# **Excel API: Move Folder**

## **Interface Details**

### **Endpoint** 

```
PUT http://api.aspose.cloud/v4.0/cells/storage/folder/move/{srcPath}
```

### **Function Description**

This API allows users to move a folder from one location to another within the Aspose.Cells cloud storage. It is essential for organizing files and managing cloud storage effectively.

### The request parameters of **moveFolder** API are: 

| Parameter Name       | Type   | Path/Query String/HTTP Body | Description                                                  | 
|----------------------|--------|------------------------------|--------------------------------------------------------------| 
| srcPath              | String | Path                         | The source path of the folder to be moved.                  |
| destPath             | String | Query                        | The destination path where the folder should be moved.      |
| srcStorageName       | String | Query                        | The name of the source storage.                              |
| destStorageName      | String | Query                        | The name of the destination storage.                         |

### **Response Description**
```json
{
Void
}
```

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/FolderController/MoveFolder) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

## Excel API SDK 

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MoveFolder.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MoveFolder.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MoveFolder.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MoveFolder.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MoveFolder.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MoveFolder.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MoveFolder.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MoveFolder.go" >}}
{{</tab>}}
{{< /tabs >}}