---
title: "Get File Versions"
second_title: "Aspose.Cells Cloud Document"
linktitle: "Get File Versions"
type: docs
url: /get-file-versions/
keywords: "file versions, Excel API, Office Cloud, REST API, spreadsheet management, document history"
description: "Retrieve and manage the versions of files stored in the Aspose.Cells Cloud, enhancing document management and collaboration."
weight: 100
kwords: "Get File Versions, Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, JSON, Markdown, document management"
---

## **Excel API: Get File Versions**

```
GET http://api.aspose.cloud/v4.0/cells/storage/version/{path}
```

### **Function Description**

The **GetFileVersions** API allows users to retrieve the different versions of a specified file stored in the Aspose.Cells Cloud. This functionality is crucial for maintaining document integrity and tracking changes over time.

### The request parameters of **GetFileVersions** API are

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
| path | String | Path | The path to the file for which versions are to be retrieved. |
| storageName | String | Query | The name of the storage where the file is located. |

### **Response Description**

```json
{
  "Name": "FileVersions",
  "Description": [
    "Contains a list of file versions for the specified document."
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Value",
      "Description": [
        "A collection of file version details."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "FileVersion",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "FileVersion",
          "Name": "class:fileversion"
        },
        "Name": "container"
      }
    }
  ]
}
```

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/StorageController/GetFileVersions) provides a comprehensive programming interface for executing REST interactions directly from a web browser.

## Excel API SDK

Utilizing an SDK streamlines development by abstracting low-level complexities, allowing developers to focus on core functionalities. Explore the [GitHub repository](https://github.com/aspose-cells-cloud) for a full list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to interact with Aspose.Cells web services across various programming languages:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetFileVersions.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetFileVersions.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetFileVersions.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetFileVersions.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetFileVersions.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetFileVersions.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetFileVersions.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetFileVersions.go" >}}
{{</tab>}}
{{< /tabs >}}
