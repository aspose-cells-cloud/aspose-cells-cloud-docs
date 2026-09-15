---
title: "Working with Excel Charts"
second_title: "Document"
linktitle: "Charts"
type: docs
url: /charts/
aliases: [/working-with-charts/]
keywords: ["Aspose.Cells chart API", "Excel chart REST endpoint", "add chart to worksheet cloud", "update chart legend API", "convert Excel chart to PNG"]
description: "Comprehensive guide to managing Excel charts via Aspose.Cells Cloud API — retrieve, add, update, delete, and convert charts to images with REST examples and code samples."
weight: 100
ArticleTitle: "Working with Excel Charts – Aspose.Cells Cloud Documentation"
---

## Working with Charts on an Excel File

**Last updated:** May 2024  

Excel charts are visual representations of data that help users quickly understand trends and patterns.  
The Aspose.Cells Cloud API enables developers to programmatically work with these charts inside Excel workbooks stored in the cloud. With the API you can retrieve existing charts, add new ones, modify their properties (such as titles, axes, and legends), delete unwanted charts, and convert charts to image formats for reporting or downstream processing. The following links provide direct access to the detailed operation pages for each supported chart‑related action.

### Quick Reference

| Operation | HTTP Method | Endpoint (template) | Documentation |
|-----------|-------------|---------------------|---------------|
| Get Chart | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/` | [Get Chart in a Worksheet](/cells/get-chart-from-a-worksheet/) |
| Add Chart | POST | `/cells/{file}/worksheets/{sheet}/charts/` | [Add a Chart in a Worksheet](/cells/add-a-chart-in-a-worksheet/) |
| Delete All Charts | DELETE | `/cells/{file}/worksheets/{sheet}/charts/` | [Delete all Charts in a Worksheet](/cells/delete-all-charts-from-a-worksheet/) |
| Delete Chart | DELETE | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/` | [Delete a Chart in a Worksheet](/cells/delete-a-chart-from-a-worksheet/) |
| Convert Chart to Image | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/image/` | [Convert Chart to Image](/cells/convert-chart-to-image/) |
| Get Chart Area | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/area/` | [Get Chart Area in a Worksheet](/cells/get-chart-area-from-a-worksheet/) |
| Get Fill Format | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/area/fillformat/` | [Get Fill Format of a Chart Area in a Worksheet](/cells/get-fill-format-of-a-chart-area-from-a-worksheet/) |
| Get Legend | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend/` | [Get Chart Legend in a Worksheet](/cells/get-chart-legend-from-a-worksheet/) |
| Update Legend | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend/` | [Update Chart Legend in a Worksheet](/cells/update-chart-legend-in-a-worksheet/) |
| Show Legend | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend/show/` | [Show Chart Legend in a Worksheet](/cells/show-chart-legend-in-a-worksheet/) |
| Hide Legend | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend/hide/` | [Hide Chart Legend in a Worksheet](/cells/hide-chart-legend-in-a-worksheet/) |
| Get Title | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title/` | [Get Chart Title in a Worksheet](/cells/get-chart-title-from-a-worksheet/) |
| Set Title | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title/` | [Set Chart Title in an Excel Worksheet](/cells/set-chart-title-in-excel-worksheet/) |
| Update Title | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title/` | [Update Chart Title in an Excel Worksheet](/cells/update-chart-title-in-excel-worksheet/) |
| Delete Title | DELETE | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title/` | [Delete Chart Title in a Worksheet](/cells/delete-chart-title-in-a-worksheet/) |
| Update Chart Properties | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/` | [Update Chart Properties](/cells/charts/properties/update/) |
| Get Category Axis | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/categoryaxis/` | [Get Chart Category Axis](/cells/charts/category-axis/get/) |
| Get Value Axis | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/valueaxis/` | [Get Chart Value Axis](/cells/charts/value-axis/get/) |
| Get Second Category Axis | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondcategoryaxis/` | [Get Chart Second Category Axis](/cells/charts/second-category-axis/get/) |
| Get Second Value Axis | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondvalueaxis/` | [Get Chart Second Value Axis](/cells/charts/second-value-axis/get/) |
| Update Category Axis | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/categoryaxis/` | [Update Chart Category Axis](/cells/charts/category-axis/update/) |
| Update Value Axis | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/valueaxis/` | [Update Chart Value Axis](/cells/charts/value-axis/update/) |
| Update Second Category Axis | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondcategoryaxis/` | [Update Chart Second Category Axis](/cells/charts/second-category-axis/update/) |
| Update Second Value Axis | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondvalueaxis/` | [Update Chart Second Value Axis](/cells/charts/second-value-axis/update/) |

- [Get Chart in a Worksheet](/cells/get-chart-from-a-worksheet/)
- [Add a Chart in a Worksheet](/cells/add-a-chart-in-a-worksheet/)
- [Delete all Charts in a Worksheet](/cells/delete-all-charts-from-a-worksheet/)
- [Delete a Chart in a Worksheet](/cells/delete-a-chart-from-a-worksheet/)
- [Convert Chart to Image](/cells/convert-chart-to-image/)
- [Get Chart Area in a Worksheet](/cells/get-chart-area-from-a-worksheet/)
- [Get Fill Format of a Chart Area in a Worksheet](/cells/get-fill-format-of-a-chart-area-from-a-worksheet/)
- [Get Chart Legend in a Worksheet](/cells/get-chart-legend-from-a-worksheet/)
- [Update Chart Legend in a Worksheet](/cells/update-chart-legend-in-a-worksheet/)
- [Show Chart Legend in a Worksheet](/cells/show-chart-legend-in-a-worksheet/)
- [Hide Chart Legend in a Worksheet](/cells/hide-chart-legend-in-a-worksheet/)
- [Get Chart Title in a Worksheet](/cells/get-chart-title-from-a-worksheet/)
- [Set Chart Title in an Excel Worksheet](/cells/set-chart-title-in-excel-worksheet/)
- [Update Chart Title in an Excel Worksheet](/cells/update-chart-title-in-excel-worksheet/)
- [Delete Chart Title in a Worksheet](/cells/delete-chart-title-in-a-worksheet/)
- [Update Chart Properties](/cells/charts/properties/update/)
- [Get Chart Category Axis](/cells/charts/category-axis/get/)
- [Get Chart Value Axis](/cells/charts/value-axis/get/)
- [Get Chart Second Category Axis](/cells/charts/second-category-axis/get/)
- [Get Chart Second Value Axis](/cells/charts/second-value-axis/get/)
- [Update Chart Category Axis](/cells/charts/category-axis/update/)
- [Update Chart Value Axis](/cells/charts/value-axis/update/)
- [Update Chart Second Category Axis](/cells/charts/second-category-axis/update/)
- [Update Chart Second Value Axis](/cells/charts/second-value-axis/update/)