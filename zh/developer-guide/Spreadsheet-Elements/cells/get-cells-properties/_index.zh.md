---
title: 获取 Cells 属性
type: docs
url: /zh/get-cells-properties/
weight: 130
kwords: Excel、Office 云、REST API、电子表格、PDF、CSV、Json、Markdown、获取 Cells 属性
---
此 REST API 表示如何在 Excel 文件中执行 `get a specific cell`。

## 重新设置 API

```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellOrMethodName}
 
```

请求参数为：

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|姓名|细绳|小路|文档名称。|
|工作表名称|细绳|小路|工作表名称。|
|单元格或方法名称|细绳|小路|单元格或方法的名称。（方法名称值：firstcell、endcell、maxrow、maxdatarow、maxcolumn、maxdatacolumn、minrow、mindatarow、mincolumn、mindatacolumn 和 cellName。）|
|文件夹|细绳|询问|文档的文件夹。|
|存储名称|细绳|询问|存储名称。|

这[OpenAPI规范](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell)定义一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。

### **Cloud SDK 系列**

使用 SDK 是加速开发的最佳方式。SDK 负责处理底层细节，让您专注于项目任务。请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)以获取 Aspose.Cells Cloud SDKs 的完整列表。

以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCell.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCell.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCell.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCell.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCell.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCell.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCell.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCell.go" >}}

{{< /tab >}}

{{< /tabs >}}

### **如何获取特定单元格**

- [从工作表获取单元格数据](/cells/zh/get-cell-data-from-a-worksheet/)
- [从 Excel 工作表中获取第一个单元格](/cells/zh/get-first-cell-from-excel-worksheet/)
- [获取 Excel 工作表的最后一个单元格](/cells/zh/get-last-cell-of-excel-worksheet/)
- [从 Excel 工作表中获取 MaxRow](/cells/zh/get-maxrow-from-excel-worksheet/)
- [从 Excel 工作表中获取 MaxDataRow](/cells/zh/get-maxdatarow-from-excel-worksheet/)
- [从 Excel 工作表中获取 MaxColumn](/cells/zh/get-maxcolumn-from-excel-worksheet/)
- [从 Excel 工作表中获取 MaxDataColumn](/cells/zh/get-maxdatacolumn-from-excel-worksheet/)
- [从 Excel 工作表中获取 MinRow](/cells/zh/get-minrow-from-excel-worksheet/)
- [从 Excel 工作表中获取 MinDataRow](/cells/zh/get-mindatarow-from-excel-worksheet/)
- [从 Excel 工作表中获取 MinColumn](/cells/zh/get-mincolumn-from-excel-worksheet/)
- [从 Excel 工作表中获取 MinDataColumn](/cells/zh/get-mindatacolumn-from-excel-worksheet/)
