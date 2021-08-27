---
title: "Get a List Object or Table inside the Worksheet"
type: docs
url: /get-a-list-object-or-table-inside-the-worksheet/
weight: 9
---

This REST API get an excel `listobject`  object to different format file.

- **REST API**

```bash

POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}

```

- **Path Parameter**


|Parameter Name|Type|Description|
| :- | :- | :- |
| name | string |  The workbook name. |
| sheetName | string | The worksheet name. |
| listobjectindex | int |list object index. |


- **Query Parameter**

|Parameter Name|Type|Description|
| :- | :- | :- |
| folder | string | Original workbook folder. |
| storageName | string |Storage name. |
| format | string | Out file format. Default value is xlsx. |


- **Response**


```bash
{
    "Code": 200,
    "Status": "OK",
    "ListObject" :{
      ...
    }        
}


```

- **Api Reference**   

 [GetWorksheetListObject](https://apireference.aspose.cloud/cells/#/ListObjects/GetWorksheetListObject)



- **Cloud SDK Family**

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:


{{< tabs tabTotal="9" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" >}}

{{< tab tabNum="1" >}}



{{< /tab >}}

{{< tab tabNum="2" >}}


{{< /tab >}}

{{< tab tabNum="3" >}}



{{< /tab >}}

{{< tab tabNum="4" >}}


{{< /tab >}}

{{< tab tabNum="5" >}}


{{< /tab >}}

{{< tab tabNum="6" >}}


{{< /tab >}}

{{< tab tabNum="7" >}}


{{< /tab >}}

{{< tab tabNum="8" >}}


{{< /tab >}}

{{< tab tabNum="9" >}}


{{< /tab >}}

{{< /tabs >}}
