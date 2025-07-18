---
title: "Unprotect spreadsheet"
second_title: "Aspose.Cells Cloud Document"
linktitle: "Unprotect spreadsheet"
type: docs
url: /unprotect-spreadsheet/
keywords: ""
description: "Removes dual-layer password protection from Excel spreadsheets, supporting both open and modify passwords with encryption. "
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdown, Match all blank cells in an Excel worksheet
---

# **Excel API : UnprotectSpreadsheet **

Removes dual-layer password protection from Excel spreadsheets, supporting both open and modify passwords with encryption. 

## **Interface Details**

### **Endpoint** 

```
PUT http://api.aspose.cloud/v4.0/cells/unprotection/spreadsheet
```

### **Function Description**

This WEB API removes dual-layer password protection from Excel spreadsheets, supporting both open and modify passwords. Passwords can be encrypted to enhance security.- **Open Password**: Restricts access to the spreadsheet, ensuring only authorized users can open the file.- **Modify Password**: Restricts the ability to edit the spreadsheet, allowing users to view but not alter the content.- **Encryption**: Passwords are encrypted to provide an additional layer of security.- **Usage**:- Ideal for protecting sensitive data in Excel files.- Ensures that only authorized users can access and modify the spreadsheet.

### The request parameters of **unprotectSpreadsheet** API are: 

| Parameter Name | Type | Path/Query String/HTTPBody | Description | 
| :- | :- | :- |:- | 
|Spreadsheet|File|FormData|Upload spreadsheet file.|
|password|String|Query|Spreadsheet file encryption password.|
|modifyPassword|String|Query|Sets the protected password to modify the file.|
|outPath|String|Query|(Optional) The folder path where the workbook is stored. The default is null.|
|outStorageName|String|Query|Output file Storage Name.|
|regoin|String|Query|The spreadsheet region setting.|


### **Response Description**
```json
{
File
}
```

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/ProtectionController/UnprotectSpreadsheet) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

## Excel API SDK 

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:


{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UnprotectSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UnprotectSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UnprotectSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UnprotectSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UnprotectSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UnprotectSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UnprotectSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UnprotectSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}


