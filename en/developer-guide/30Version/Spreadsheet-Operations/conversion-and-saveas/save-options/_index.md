---
title: "Aspose.Cells Cloud Save Options – Configure Workbook Save Behavior"
second_title: "Document"
linktitle: "Save options"
type: docs
url: /save-options/
keywords: "Aspose.Cells SaveOptions, Excel save options API, Aspose Cells Cloud save format, HTTP compression, chart cache refresh, directory creation, workbook"
description: "Learn how to use Aspose.Cells Cloud SaveOptions to control workbook saving – set format, HTTP compression, directory creation, chart cache refresh, and more. Includes defaults, code samples, and FAQ."
weight: 79
---

# SaveOptions Properties

| Name                      | Type       | Description                                                                                        | Notes      |
| ------------------------- | ---------- | -------------------------------------------------------------------------------------------------- | ---------- |
| **EnableHTTPCompression** | **bool?**  | Enables HTTP compression for the response.                                                         | [optional] |
| **SaveFormat**            | **string** | Specifies the target file format for saving the workbook.                                          | [optional] |
| **ClearData**             | **bool?**  | Makes the workbook empty after saving the file.                                                    | [optional] |
| **CachedFileFolder**      | **string** | The cached file folder used to store large data temporarily.                                       | [optional] |
| **ValidateMergedAreas**   | **bool?**  | Indicates whether to validate merged areas before saving the file. The default value is false.     | [optional] |
| **RefreshChartCache**     | **bool?**  | Refreshes chart cache data before saving.                                                          | [optional] |
| **CreateDirectory**       | **bool?**  | If true and the directory does not exist, it will be automatically created before saving the file. | [optional] |
| **SortNames**             | **bool?**  | Sorts named ranges alphabetically when saving.                                                     | [optional] |