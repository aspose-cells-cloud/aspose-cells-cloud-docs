---
title: "在 Excel 工作表中添加数据透视表"
second_title: "文档"
linktitle: 添加
type: docs
url: /zh/pivot-tables/add/
aliases: [  /zh/add-a-pivot-table-in-a-worksheet/ ]
keywords: "添加数据透视表, Excel 工作表, Aspose.Cells Cloud, REST API, SDK, Excel 数据透视表"
description: "使用 Aspose.Cells Cloud REST API 向 Excel 工作表添加数据透视表。支持通过 C#、Java、PHP、Python、Node.js、Android、Swift、Perl、Go 的 SDK 调用。"
weight: 30
ArticleTitle: "如何使用 Aspose.Cells Cloud 在 Excel 工作表中添加数据透视表"
---

此 REST API 可向工作表中添加数据透视表。

**先决条件：**  
- 一个已获取有效 JWT 访问令牌的 Aspose.Cells Cloud 账户。  
- 目标工作簿必须存储在受支持的存储位置中（默认存储或用户指定的存储）。  
- 通过 `sheetName` 指定的工作表必须存在于该工作簿中。  

## PutWorksheetPivotTable API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### **请求参数**

| 参数名称       | 类型    | 位置   | 描述                                                                 |
| -------------- | ------- | ------ | -------------------------------------------------------------------- |
| name           | string  | path   | Excel 文档的名称。                                                   |
| sheetName      | string  | path   | 将创建数据透视表的工作表名称。                                       |
| request        | object  | body   | `CreatePivotTableRequest` 数据传输对象（DTO），包含数据透视表定义。 |
| folder         | string  | query  | 包含文档的文件夹。                                                   |
| storageName    | string  | query  | 文档所在存储的名称。                                                 |
| sourceData     | string  | query  | 新数据透视表缓存的源数据范围（例如：`A5:E10`）。                     |
| destCellName   | string  | query  | 数据透视表报表目标区域左上角单元格的地址。                           |
| tableName      | string  | query  | 为新数据透视表指定的名称。                                           |
| useSameSource  | boolean | query  | 若为 `true`，新数据透视表将复用已存在的数据源，从而节省内存（前提是已有其他数据透视表使用了该源）。 |

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/PivotTables/PutWorksheetPivotTable) 定义了一个公开可访问的编程接口，允许您直接通过网页浏览器发起 REST 调用。

您可以使用 **cURL** 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

**安全提示：** 调用 API 时务必使用 `https://` 协议，并严格保密您的 JWT 令牌；通过明文 HTTP 传输令牌可能导致其被截获。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/pivottables" \
-X PUT \
-d '{"Name":"MyPivot","SourceData":"A5:E10","DestCellName":"H20","UseSameSource":true,"PivotFieldRows":[1],"PivotFieldColumns":[1],"PivotFieldData":[1]}' \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**HTTP 状态码**

| 状态码 | 含义           | 描述                                         |
|--------|----------------|----------------------------------------------|
| 200    | OK（成功）     | 筛选器应用成功；响应包含操作详情。           |
| 400    | Bad Request（错误请求） | 参数缺失或无效（例如：不支持的文件类型）。   |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                         |
| 413    | Payload Too Large（载荷过大） | 上传的文件超出大小限制。                   |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。                       |

## 云 SDK 家族

使用 SDK 是加速开发进程的最佳方式。SDK 封装了底层细节，使您能专注于项目核心任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-AddPivottableWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-AddPivottableWorksheet-add-pivot-table-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddPivotTableInw" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-AddPivottableWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-AddPivottableWorksheet-add-pivot-table-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-AddPivottableWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "980246b631d7816f257f2ad4664788ea" >}}

{{< /tab >}}

{{< /tabs >}}

更多操作请参阅相关 API 页面：**[获取数据透视表](https://docs.aspose.cloud/cells/pivot-tables/get/)**、**[删除数据透视表](https://docs.aspose.cloud/cells/pivot-tables/delete/)** 和 **[更新数据透视表](https://docs.aspose.cloud/cells/pivot-tables/update/)**。