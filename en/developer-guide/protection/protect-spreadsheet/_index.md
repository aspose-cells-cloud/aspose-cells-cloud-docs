---
title: "Protect Spreadsheet - Excel API"
second_title: "Developer Guide for Excel Protection"
linktitle: "Protect Spreadsheet"
type: docs
url: /protect-spreadsheet/
keywords: "Excel API, password protection, encrypt spreadsheet, dual-layer security, modify password, REST API, data encryption"
description: "This API applies dual-layer password protection to Excel spreadsheets, ensuring secure access and modification through encryption."
weight: 100
kwords: "Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, JSON, Markdown, dual-layer password protection, encrypt spreadsheet, secure Excel"
---

# **Protect Spreadsheet API**

## **Overview**

This API applies dual-layer password protection to Excel spreadsheets, supporting both open and modify passwords with encryption to enhance data security.

## **Function Description**

The Protect Spreadsheet API applies dual-layer password security to Excel files, allowing users to set passwords for opening and modifying spreadsheets. Passwords are encrypted to ensure maximum protection.

## **API Endpoint**

```http
PUT http://api.aspose.cloud/v4.0/cells/protection/spreadsheet
```

## The request parameters of **protectSpreadsheet** API are

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
|Spreadsheet|File|FormData|Upload the spreadsheet file to be protected.|
|password|String|Query|Encryption password for the spreadsheet file.|
|modifyPassword|String|Query|Password required to modify the spreadsheet.|
|outPath|String|Query|(Optional) The folder path where the protected workbook will be stored. The default is null.|
|outStorageName|String|Query|Name of the storage for output files.|
|region|String|Query|Defines the region settings for the spreadsheet.|

## **Response Structure**

```json
{
File
}
```

## Error Handling

- **400 Bad Request**: Invalid URL or parameters.
- **401 Unauthorized**: Authentication failed or credentials not provided.
- **404 Not Found**: The source file cannot be accessed.
- **500 Server Error**: An internal error occurred while processing the spreadsheet.

## Usage Scenarios

## Key Features and Benefits

- **Open Password**: Limits access to authorized users only, ensuring that sensitive data remains secure.
- **Modify Password**: Prevents unauthorized changes, allowing users to view the spreadsheet without editing rights.
- **Encryption**: Provides an additional security layer by encrypting passwords to protect sensitive information effectively.

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/ProtectionController/ProtectSpreadsheet) provides a detailed programming interface for executing REST interactions directly from a web browser.

## Excel API SDK

Utilizing an SDK streamlines the development process by managing low-level details, allowing developers to focus on their projects. Visit the [GitHub repository](https://github.com/aspose-cells-cloud) for a comprehensive list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to interact with Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ProtectSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ProtectSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ProtectSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ProtectSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ProtectSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ProtectSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ProtectSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ProtectSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}
