---
title: "处理 Excel 图表"
second_title: "文档"
linktype: "图表"
type: docs
url: /zh/charts/
aliases: [  /zh/working-with-charts/ ]
keywords: "Aspose, Cells, Excel, 图表, API, REST, 云, 电子表格"
description: "了解如何使用 Aspose.Cells Cloud API 管理 Excel 图表。提供分步指南、代码示例以及错误处理，涵盖检索、添加、更新、删除图表，以及将图表转换为图像。"
weight: 100
ArticleTitle: "处理 Excel 图表 – Aspose.Cells Cloud 文档"
---

## 处理 Excel 文件中的图表

**最后更新时间：** 2026 年 7 月  

Excel 图表是数据的可视化表示形式，有助于用户快速理解趋势与模式。  
Aspose.Cells Cloud API 允许开发者以编程方式操作存储在云端的 Excel 工作簿中的图表。借助该 API，您可以检索现有图表、添加新图表、修改其属性（例如标题、坐标轴和图例）、删除不需要的图表，以及将图表转换为图像格式，以便用于报告或后续处理。以下链接可直接访问每种受支持的图表相关操作的详细页面。

### 快速参考

| 操作 | HTTP 方法 | 端点（模板） | 文档 |
|------|-----------|-------------|------|
| 获取图表 | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}` | [从工作表获取图表](/zh/cells/get-chart-from-a-worksheet/) |
| 添加图表 | POST | `/cells/{file}/worksheets/{sheet}/charts` | [在工作表中添加图表](/zh/cells/add-a-chart-in-a-worksheet/) |
| 删除所有图表 | DELETE | `/cells/{file}/worksheets/{sheet}/charts` | [从工作表删除所有图表](/zh/cells/delete-all-charts-from-a-worksheet/) |
| 删除图表 | DELETE | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}` | [从工作表删除图表](/zh/cells/delete-a-chart-from-a-worksheet/) |
| 将图表转换为图像 | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/image` | [将图表转换为图像](/zh/cells/convert-chart-to-image/) |
| 获取图表区域 | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/area` | [从工作表获取图表区域](/zh/cells/get-chart-area-from-a-worksheet/) |
| 获取填充格式 | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/area/fillformat` | [从工作表获取图表区域的填充格式](/zh/cells/get-fill-format-of-a-chart-area-from-a-worksheet/) |
| 获取图例 | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend` | [从工作表获取图表图例](/zh/cells/get-chart-legend-from-a-worksheet/) |
| 更新图例 | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend` | [在工作表中更新图表图例](/zh/cells/update-chart-legend-in-a-worksheet/) |
| 显示图例 | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend/show` | [在工作表中显示图表图例](/zh/cells/show-chart-legend-in-a-worksheet/) |
| 隐藏图例 | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend/hide` | [在工作表中隐藏图表图例](/zh/cells/hide-chart-legend-in-a-worksheet/) |
| 获取标题 | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [从工作表获取图表标题](/zh/cells/get-chart-title-from-a-worksheet/) |
| 设置标题 | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [在 Excel 工作表中设置图表标题](/zh/cells/set-chart-title-in-excel-worksheet/) |
| 更新标题 | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [在 Excel 工作表中更新图表标题](/zh/cells/update-chart-title-in-excel-worksheet/) |
| 删除标题 | DELETE | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [在工作表中删除图表标题](/zh/cells/delete-chart-title-in-a-worksheet/) |
| 更新图表属性 | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}` | [更新图表属性](/zh/cells/charts/properties/update/) |
| 获取分类轴 | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/categoryaxis` | [获取图表分类轴](/zh/cells/charts/category-axis/get/) |
| 获取数值轴 | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/valueaxis` | [获取图表数值轴](/zh/cells/charts/value-axis/get/) |
| 获取第二分类轴 | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondcategoryaxis` | [获取图表第二分类轴](/zh/cells/charts/second-category-axis/get/) |
| 获取第二数值轴 | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondvalueaxis` | [获取图表第二数值轴](/zh/cells/charts/second-value-axis/get/) |
| 更新分类轴 | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/categoryaxis` | [更新图表分类轴](/zh/cells/charts/category-axis/update/) |
| 更新数值轴 | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/valueaxis` | [更新图表数值轴](/zh/cells/charts/value-axis/update/) |
| 更新第二分类轴 | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondcategoryaxis` | [更新图表第二分类轴](/zh/cells/charts/second-category-axis/update/) |
| 更新第二数值轴 | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondvalueaxis` | [更新图表第二数值轴](/zh/cells/charts/second-value-axis/update/) |

- [从工作表获取图表](/zh/cells/get-chart-from-a-worksheet/)
- [在工作表中添加图表](/zh/cells/add-a-chart-in-a-worksheet/)
- [从工作表删除所有图表](/zh/cells/delete-all-charts-from-a-worksheet/)
- [从工作表删除图表](/zh/cells/delete-a-chart-from-a-worksheet/)
- [将图表转换为图像](/zh/cells/convert-chart-to-image/)
- [从工作表获取图表区域](/zh/cells/get-chart-area-from-a-worksheet/)
- [从工作表获取图表区域的填充格式](/zh/cells/get-fill-format-of-a-chart-area-from-a-worksheet/)
- [从工作表获取图表图例](/zh/cells/get-chart-legend-from-a-worksheet/)
- [在工作表中更新图表图例](/zh/cells/update-chart-legend-in-a-worksheet/)
- [在工作表中显示图表图例](/zh/cells/show-chart-legend-in-a-worksheet/)
- [在工作表中隐藏图表图例](/zh/cells/hide-chart-legend-in-a-worksheet/)
- [从工作表获取图表标题](/zh/cells/get-chart-title-from-a-worksheet/)
- [在 Excel 工作表中设置图表标题](/zh/cells/set-chart-title-in-excel-worksheet/)
- [在 Excel 工作表中更新图表标题](/zh/cells/update-chart-title-in-excel-worksheet/)
- [在工作表中删除图表标题](/zh/cells/delete-chart-title-in-a-worksheet/)
- [更新图表属性](/zh/cells/charts/properties/update/)
- [获取图表分类轴](/zh/cells/charts/category-axis/get/)
- [获取图表数值轴](/zh/cells/charts/value-axis/get/)
- [获取图表第二分类轴](/zh/cells/charts/second-category-axis/get/)
- [获取图表第二数值轴](/zh/cells/charts/second-value-axis/get/)
- [更新图表分类轴](/zh/cells/charts/category-axis/update/)
- [更新图表数值轴](/zh/cells/charts/value-axis/update/)
- [更新图表第二分类轴](/zh/cells/charts/second-category-axis/update/)
- [更新图表第二数值轴](/zh/cells/charts/second-value-axis/update/)