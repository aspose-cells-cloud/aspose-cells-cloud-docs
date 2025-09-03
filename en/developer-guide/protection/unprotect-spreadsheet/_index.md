---
title: "Unprotect Spreadsheet - Excel API"
second_title: "Aspose.Cells Cloud"
linktitle: "Unprotect Spreadsheet"
type: docs
url: /unprotect-spreadsheet/
keywords: "Excel API, Unprotect Spreadsheet, Password Removal, Encryption, Office Cloud, REST API, Spreadsheet Security, Excel File Management"
description: "Efficiently removes dual-layer password protection from Excel spreadsheets, supporting both open and modify passwords with advanced encryption techniques."
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, JSON, Markdown, Match all blank cells in an Excel worksheet
---

# **Excel API : Unprotect Spreadsheet**

## **Overview**

This API efficiently removes dual-layer password protection from Excel spreadsheets, allowing for the decryption of both open and modify passwords.

## **Function Description**

This WEB API allows you to remove dual-layer password protection from Excel spreadsheets, supporting both open and modify passwords. Passwords can be encrypted to enhance security.

## **API Endpoint**

```http
PUT http://api.aspose.cloud/v4.0/cells/unprotection/spreadsheet
```

## The request parameters of **unprotectSpreadsheet** API are

| Parameter Name | Type | Path/Query String/HTTP Body | Description |
| :- | :- | :- |:- |
|Spreadsheet|File|FormData|Upload the spreadsheet file to be unprotected.|
|password|String|Query|The encryption password for the spreadsheet file.|
|modifyPassword|String|Query|The password required to modify the protected file.|
|outPath|String|Query|(Optional) The folder path where the unprotected workbook will be stored. Defaults to null.|
|outStorageName|String|Query|Specifies the output file storage name.|
|region|String|Query|Defines the spreadsheet region settings.|

## **Response Structure**

```json
{
File
}
```

## Error Handling

- **400 Bad Request**: The URL is invalid.
- **401 Unauthorized**: Authentication has failed, or no credentials were provided.
- **404 Not Found**: The source file is not accessible.
- **500 Server Error**: An anomaly occurred while processing the spreadsheet.

## Usage Scenarios

## Key Features and Benefits

- **Dual-Layer Password Removal**: Effectively removes both open and modify passwords from Excel spreadsheets, streamlining access to protected files.

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/ProtectionController/UnprotectSpreadsheet) defines a publicly accessible programming interface, enabling you to perform REST interactions directly from a web browser.

## Excel API SDK

Utilizing an SDK is the most effective way to accelerate your development process. An SDK manages low-level details, allowing you to concentrate on your project tasks. Explore the [GitHub repository](https://github.com/aspose-cells-cloud) for a comprehensive list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to call Aspose.Cells web services using various SDKs:

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
