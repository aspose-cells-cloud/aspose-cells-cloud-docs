---
title: "Clear"
type: docs
url: /comments/clear/
aliases: [/delete-all-comments-in-a-worksheet/]
keywords: "REST API, spreadsheets, excel, clear comments"
description: "Cells.Cloud API for Excel operate: clear comments."
weight: 50
---

This REST API indicates Delete all comments for worksheet.
 
## RSET API
 
```bash
 
DELETE http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments
 
```
The request parameters are: 
 
| Parameter Name | Type | Path/Query String/HTTPBody | Description| 
| :- | :- | :- |:- | 
| name | string | path |   |
| sheetName | string | path |   |
| folder | string | query |   |
| storageName | string | query | storage name. |
 
The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetComments) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.
 
You can use cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments" \
-X DELETE \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```java

{
    "Code": 200,
    "Status": "OK"
}

```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family
 
Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.
 
The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "51c3a018dbaff3df7cd2244f21845bdc" >}}

{{< /tab >}}

{{< /tabs >}}
