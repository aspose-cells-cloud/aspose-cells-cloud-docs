---
title: 获取Cells属性
type: docs
url: /zh/get-cells-properties/
weight: 130
---
此 REST API 指示显示如何在 Excel 文件中使用 `get a specific cell`。

## RSET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellOrMethodName}
 
```
请求参数为：
 
|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|姓名|细绳|小路|文档名称。|
|工作表名称|细绳|小路|工作表名称。|
|单元格或方法名|细绳|小路|单元格或方法的名称。 （方法名称值：firstcell、endcell、maxrow、maxdatarow、maxcolumn、maxdatacolumn、minrow、mindatarow、mincolumn、mindatacolumn 和 cellName。）|
|文件夹|细绳|询问|文档的文件夹。|
|存储名称|细绳|询问|存储名称。|
 
这[开放API规范](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell)定义了一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。


- **如何获取特定细胞**

   - [从工作表中获取单元格数据](/cells/zh/get-cell-data-from-a-worksheet/)
   - [从 Excel 工作表获取第一个单元格](/cells/zh/get-first-cell-from-excel-worksheet/)
   - [获取 Excel 工作表的最后一个单元格](/cells/zh/get-last-cell-of-excel-worksheet/)
   - [从 Excel 工作表获取 MaxRow](/cells/zh/get-maxrow-from-excel-worksheet/)
   - [从 Excel 工作表获取 MaxDataRow](/cells/zh/get-maxdatarow-from-excel-worksheet/)
   - [从 Excel 工作表获取 MaxColumn](/cells/zh/get-maxcolumn-from-excel-worksheet/)
   - [从 Excel 工作表获取 MaxDataColumn](/cells/zh/get-maxdatacolumn-from-excel-worksheet/)
   - [从 Excel 工作表获取 MinRow](/cells/zh/get-minrow-from-excel-worksheet/)
   - [从 Excel 工作表获取 MinDataRow](/cells/zh/get-mindatarow-from-excel-worksheet/)
   - [从 Excel 工作表获取 MinColumn](/cells/zh/get-mincolumn-from-excel-worksheet/)
   - [从 Excel 工作表获取 MinDataColumn](/cells/zh/get-mindatacolumn-from-excel-worksheet/)
