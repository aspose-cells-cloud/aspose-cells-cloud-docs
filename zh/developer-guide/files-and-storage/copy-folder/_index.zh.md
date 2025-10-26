---
title: 复制文件夹
second_title: Documen
linktitle: 复制文件夹
type: docs
url: /zh/copy-folder/
keywords: Excel API, Copy Folder, Office Cloud, REST API, Spreadsheet Management, File Operation
description: 了解如何使用 CopyFolder API 在 Aspose.Cells 云环境中高效复制文件夹
weight: 100
kwords: Excel、Office 云、REST API、复制文件夹、文件管理、PDF、CSV、JSON、Markdown、匹配 Excel 工作表中的所有空白单元格
---
## **Excel API：复制文件夹**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/folder/copy/{srcPath}
```

### **功能描述**

这**复制文件夹**API 允许用户复制 Aspose.Cells 云存储中的现有文件夹。此功能对于高效管理文件至关重要，使用户无需手动传输内容即可创建备份或整理工作。

### 的请求参数**复制文件夹**API 是

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|----------------|--|-----------------------|-------------------------------------|
|源路径|细绳|小路|要复制的源文件夹的路径。|
|目标路径|细绳|询问|新文件夹将被创建的路径。|
|源存储名称|细绳|询问|包含源文件夹的存储的名称。|
|目标存储名称|细绳|询问|应复制文件夹的目标存储的名称。|

### **响应描述**

```json
{
Void
}
```

## OpenAPI 规范

这[OpenAPI 规范](https://reference.aspose.cloud/cells/#/FolderController/CopyFolder)定义一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。

## Excel API SDK

使用 SDK 是加速开发的最佳方式。SDK 负责处理底层细节，让您专注于项目任务。请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)以获取 Aspose.Cells Cloud SDKs 的完整列表。

以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CopyFolder.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CopyFolder.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CopyFolder.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CopyFolder.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CopyFolder.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CopyFolder.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CopyFolder.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CopyFolder.go" >}}
{{< /tab >}}
{{< /tabs >}}
