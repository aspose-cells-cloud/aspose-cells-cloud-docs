---
title: "Create Folder in Excel API"
second_title: "Developer Guide for Aspose.Cells"
linktitle: "Create Folder"
type: docs
url: /create-folder/
keywords: "Excel API, Create Folder, Office Cloud, REST API, Cloud Storage, Folder Management, Excel, Spreadsheet, PDF, CSV, JSON, Markdown"
description: "Learn how to create a folder in Excel API using REST."
weight: 100
kwords: "Create Folder, Excel API, Office Cloud, REST API, Cloud Storage, Folder Management, Match all blank cells in an Excel worksheet"
---

## **Excel API: Create Folder**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **Function Description**

The **createFolder** API allows users to create a new folder in the specified path within the cloud storage of the Excel API. This functionality is essential for organizing files and maintaining a structured directory.

### The request parameters of **createFolder** API are

| Parameter Name | Type   | Path/Query String/HTTP Body | Description                           |
|----------------|--------|------------------------------|---------------------------------------|
| path           | String | Path                         | The path where the folder will be created. |
| storageName    | String | Query                        | The name of the storage to use.      |

### **Response Description**

```json
{
Void
}
```

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/FolderController/CreateFolder) defines a publicly accessible programming interface and allows you to carry out REST interactions directly from a web browser.

## Excel API SDK

Using an SDK is the best way to speed up development. An SDK manages low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CreateFolder.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CreateFolder.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CreateFolder.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CreateFolder.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CreateFolder.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CreateFolder.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CreateFolder.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CreateFolder.go" >}}
{{</tab>}}
{{< /tabs >}}
