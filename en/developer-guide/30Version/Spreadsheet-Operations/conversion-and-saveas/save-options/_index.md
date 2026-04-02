---
title: "Save Options"
second_title: "Document"
linktitle: "Save options"
type: docs
url: /save-options/
keywords: "Aspose.Cells Cloud, SaveOptions, Excel, Workbook, REST API, File Formats, PDF, CSV, JSON, HTTP Compression, Chart Cache, Named Ranges, Directory Creation"
description: "Describes the SaveOptions properties of the Aspose.Cells Cloud REST API, enabling developers to configure workbook‑saving behavior across multiple file formats and options such as HTTP compression, chart cache refresh, and automatic directory creation."
weight: 79
---

# SaveOptions Properties

Name | Type | Description | Notes
---- | ---- | ----------- | -----
**EnableHTTPCompression** | **bool?** | Enables HTTP compression for the response. | [optional] 
**SaveFormat** | **string** | Specifies the target file format for saving the workbook. | [optional] 
**ClearData** | **bool?** | Makes the workbook empty after saving the file. | [optional] 
**CachedFileFolder** | **string** | The cached file folder used to store large data temporarily. | [optional] 
**ValidateMergedAreas** | **bool?** | Indicates whether to validate merged areas before saving the file. The default value is false. | [optional] 
**RefreshChartCache** | **bool?** | Refreshes chart cache data before saving. | [optional] 
**CreateDirectory** | **bool?** | If true and the directory does not exist, it will be automatically created before saving the file. | [optional] 
**SortNames** | **bool?** | Sorts named ranges alphabetically when saving. | [optional]