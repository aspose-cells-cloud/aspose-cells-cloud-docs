---
title: "隐藏数据透视表中的数据透视字段项"
second_title: "Document"
linktype: Hide
type: docs
url: /zh/pivot-tables/hide-pivot-field-item/
aliases: [  /zh/hide-pivot-field-item/ ]
keywords: "Aspose.Cells, 隐藏数据透视字段项, PivotTable API, REST API, 云 SDK"
description: "了解如何使用 Aspose.Cells Cloud REST API 隐藏数据透视表中的数据透视字段项。包含请求详情、cURL 示例以及多种编程语言的 SDK 代码片段。"
weight: 110
ArticleTitle: "在数据透视表中隐藏数据透视字段项 – Aspose.Cells Cloud API 指南"
---

在调用 API 之前，请确保您已完成以下准备：

* 拥有有效的 **JWT 访问令牌**（可通过 Aspose Cloud 认证流程获取）。  
* 已将目标工作簿上传至您的 Aspose Cloud 存储空间。  
* 已创建包含目标工作表和数据透视表。

这些前置条件可避免身份验证错误及“资源未找到”等响应。以下步骤概述了调用 API 前所需的设置。

该 REST API 用于隐藏数据透视表中的某个数据透视字段项。

## PostPivotTableFieldHideItem API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotField/Hide
```

### **安全性与身份验证**

Aspose.Cells Cloud API 安全可靠，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### **请求参数**

| 参数名称        | 类型    | 位置   | 描述                                                                 |
| --------------- | ------- | ------ | -------------------------------------------------------------------- |
| name            | string  | 路径   | Excel 文件名称。                                                     |
| sheetName       | string  | 路径   | 包含数据透视表的工作表名称。                                         |
| pivotTableIndex | integer | 路径   | 工作表内数据透视表的索引。                                           |
| pivotFieldType  | string  | 查询   | 数据透视字段类型（行、列、页面、数据等）。                           |
| fieldIndex      | integer | 查询   | 待修改的数据透视字段的从零开始索引。                                 |
| itemIndex       | integer | 查询   | 待隐藏字段项在该字段中的从零开始索引。                               |
| isHide          | boolean | 查询   | 设置为 **true** 表示隐藏该项；设置为 **false** 表示显示该项。       |
| needReCalculate | boolean | 查询   | 表示更改后是否需重新计算数据透视表。默认值为 **false**。             |
| folder          | string  | 查询   | 工作簿所在的文件夹路径。                                             |
| storageName     | string  | 查询   | 存储服务的名称。                                                     |

**所需查询参数速查表**

- **pivotFieldType** – 字段类型（例如 `Row`）。  
- **fieldIndex** – 待修改字段的从零开始索引。  
- **itemIndex** – 待隐藏/显示项的从零开始索引。  
- **isHide** – `true` 表示隐藏，`false` 表示显示。  
- **needReCalculate** – 可选，默认为 `false`。

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableFieldHideItem) 定义了一个公开可访问的编程接口，可让您直接通过网页浏览器执行 REST 交互。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用该 API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/pivottables/0/PivotField/Hide?pivotFieldType=Row&fieldIndex=0&itemIndex=1&isHide=true&needReCalculate=true" \
  -X POST \
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

**响应详情**

| 状态码 | 描述                                   |
| ------ | -------------------------------------- |
| 200    | 项已成功隐藏。                         |
| 400    | 错误请求 – 缺少或参数无效。            |
| 401    | 未授权 – JWT 令牌无效或缺失。           |
| 500    | 服务器错误 – 操作无法完成。            |

**注意**：若提供的 `fieldIndex` 或 `itemIndex` 超出范围，API 将返回 **400 错误请求** 响应。

## 云 SDK 家族

使用 SDK 是最快捷的 API 开发方式。SDK 会处理底层细节，让您专注于业务逻辑。查看 [GitHub 仓库](https://github.com/aspose-cells-cloud) 获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 隐藏数据透视字段项。

{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

```csharp
public void Run_PivotTable_NeedReCalculate()
{
    // 准备工作簿和工作表
    url = @"https://api.aspose.cloud/v3.0/storage/file/Temp/V17.02.00_01.xlsx";
    using (HttpWebResponse response = _helper.CallDelete(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // 上传工作簿
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // 创建包含数据透视表的工作表
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // 创建第二个包含示例数据的工作表
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/Sheet2?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // 将示例数据导入 Sheet2
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/importdata?folder=Temp";
    data = "{ \"BatchData\":[{...}] }"; // 为简洁起见已省略部分内容
    using (HttpWebResponse response = _helper.CallPost(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // 向 PivotSheet 添加数据透视表
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables?folder=Temp";
    data = "{\"Name\":\"TestPivot\",\"SourceData\":\"=Sheet2!A1:E8\",\"DestCellName\":\"C1\",\"UseSameSource\":true,\"PivotFieldRows\":[0,1],\"PivotFieldColumns\":[2],\"PivotFieldData\":[3,4]}";
    using (HttpWebResponse response = _helper.CallPut(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // 隐藏特定的行字段项
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/PivotField/Hide?pivotFieldType=Row&fieldIndex=0&itemIndex=1&isHide=true&needReCalculate=true&folder=Temp";
    using (HttpWebResponse response = _helper.CallPost(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "a0bec26a8274b9f7cb514015843a214e" >}}

{{< /tab >}}

{{< /tabs >}}

**注意**：SDK 示例假设您已完成身份验证配置（JWT 令牌），且工作簿位于指定存储文件夹中。请根据您的环境调整 `folder` 和 `storageName` 参数。