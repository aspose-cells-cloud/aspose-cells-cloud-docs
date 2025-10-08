---
title: 删除文件夹
second_title: Documen
linktitle: 删除文件夹
type: docs
url: /zh/delete-folder/
keywords: Delete folder, Aspose.Cells API, RESTful API, Excel file management, cloud storag
description: 了解如何使用 deleteFolder API 删除 Aspose.Cells 中的文件夹，包括参数和代码示例
weight: 100
kwords: Excel API、Office 云、REST API、电子表格管理、PDF、CSV、JSON、Markdown、删除 Excel 工作表中的文件夹
---
## **Excel API : 删除文件夹**

```
DELETE http://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **功能描述**

`deleteFolder` API 允许用户从与 Aspose.Cells 关联的云存储中删除指定的文件夹。这对于维护组织和有效管理存储很有用。

### 请求参数**删除文件夹**API 是

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|小路|细绳|小路|要删除的文件夹的路径。|
|存储名称|细绳|询问|文件夹所在存储的名称。|
|递归|布尔值|询问|指示删除是否应递归，同时删除文件夹中的所有内容。|

### **响应描述**

```json
{
Void
}
```

## OpenAPI 规范

这[OpenAPI 规范](https://reference.aspose.cloud/cells/#/FolderController/DeleteFolder)定义一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。

## Excel API SDK

使用 SDK 是加速开发的最佳方式。SDK 可以处理底层细节，让您专注于项目任务。请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)以获取 Aspose.Cells Cloud SDKs 的完整列表。

以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteFolder.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteFolder.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteFolder.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteFolder.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteFolder.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteFolder.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteFolder.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteFolder.go" >}}
{{< /tab >}}
{{< /tabs >}}
