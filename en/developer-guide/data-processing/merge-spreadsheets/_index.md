---
title: "Merge Spreadsheets - Excel API"
second_title: "Aspose.Cells Cloud"
linktitle: "Merge Spreadsheets"
type: docs
url: /merge-spreadsheets/
keywords: "Merge spreadsheets, Excel API, cloud processing, data merging, file format conversion, REST API, XLSX, CSV, PDF"
description: "Easily merge local spreadsheet files into various formats (XLSX, CSV, PDF) using the Excel API."
weight: 100
kwords: "Excel API, Merge spreadsheets, Office Cloud, REST API, Spreadsheet merging, PDF export, CSV format, JSON, Markdown, Excel worksheet blank cells handling"
---

# **Excel API: MergeSpreadsheets**

## **Overview**

This API method allows users to merge local spreadsheet files into a specified output format file, such as XLSX, CSV, or PDF.

## **Function Description**

The **MergeSpreadsheets** method combines multiple spreadsheet files from the local file system into a single output file in the desired format. All input files must be accessible and in a supported format for the merge operation to succeed. The merging process is handled in the cloud without requiring cloud storage, ensuring user data privacy. Proper file permissions must be granted for reading the source files and writing the output file. If any file cannot be accessed or an error occurs during the merging process, an appropriate exception will be thrown. The final output format can be configured based on the available conversion and export capabilities.

## **API Endpoint**

```http
PUT http://api.aspose.cloud/v4.0/cells/merge/spreadsheet
```

## The request parameters of **mergeSpreadsheets** API are

| Parameter Name | Type | Path/Query String/HTTP Body | Description |
| :- | :- | :- |:- |
| Spreadsheet | File | FormData | Upload the spreadsheet file. |
| outFormat | String | Query | Specify the output file format. |
| mergeInOneSheet | Boolean | Query | Indicate whether to combine all data into a single worksheet. |
| outPath | String | Query | (Optional) The folder path for the output workbook. Defaults to null. |
| outStorageName | String | Query | Specify the output file storage name. |
| fontsLocation | String | Query | Define custom fonts to be used. |
| region | String | Query | Set the spreadsheet region. |
| password | String | Query | Provide the password for opening the spreadsheet file. |

## **Response Structure**

```json
{
File
}
```

## Error Handling

- **400 Bad Request**: Invalid URL.
- **401 Unauthorized**: Authentication has failed or no credentials were provided.
- **404 Not Found**: Source file not accessible.
- **500 Server Error**: An anomaly occurred while obtaining data from the spreadsheet.

## **Usage Scenarios**

## **Key Features and Benefits**

- **Local File Merge**: Efficiently combines multiple local spreadsheet files into a single output file in various formats (e.g., XLSX, CSV, PDF).
- **Efficient Data Handling**: Processes the merge operation in the cloud without requiring cloud storage, leveraging cloud processing capabilities for enhanced performance.
- **Format Flexibility**: Supports a diverse range of output formats based on available conversion and export capabilities for user convenience.

## **OpenAPI Specification**

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheets) provides a publicly accessible programming interface, allowing users to perform REST interactions directly from a web browser.

## **Excel API SDK**

Utilizing an SDK expedites development processes by managing low-level details, allowing developers to focus on project tasks. Check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to make calls to Aspose.Cells web services using various SDKs:
