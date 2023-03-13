---
title: 解密 Excel workboo
second_title: Aspose.Cells Cloud Documen
linktitle: 解密
type: docs
url: /zh/workbook/decrypt/
aliases: [/decrypt-excel-workbooks/]
keywords: REST API, spreadsheets, excel, decryp
description: Cells.Cloud API for Excel操作：解密Excel工作簿
weight: 50
---
这个 REST API 解密一个 Excel `workbook`。

**查询参数**

|参数名称|类型|描述|
|:- |:- |:- |
|文件夹|细绳|原始工作簿文件夹。|
|存储名称|细绳|存储名称。|

**请求正文参数**

|参数名称|类型|描述|
|:- |:- |:- |
|加密|工作簿加密请求||

**工作簿加密请求**
|参数名称|类型|描述|
|:- |:- |:- |
|加密类型|细绳|XOR/Compatible/EnhancedCryptographicProviderV1/StrongCryptographicProvider|
|密钥长度|整数||
|密码|细绳||


## 休息 API


|**API**|**类型**|**描述**|**招摇链接**|
|:- |:- |:- |:- |
|/cells/{名称}/加密|删除|解密文档|[删除解密文件](https://apireference.aspose.cloud/cells/#/Workbook/DeleteDecryptDocument)|


这[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Workbook/DeleteDecryptDocument)定义了一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。

您可以使用**cURL**用于轻松访问 Aspose.Cells Web 服务的命令行工具。以下示例显示如何使用 cURL 调用 Cloud API。


{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/encryption" -H "accept: application/json" -H "Content-Type: application/json" -H "x-aspose-client: Containerize.Swagger" -d "{ \"EncryptionType\": \"XOR\", \"KeyLength\": 1280, \"Password\": \"aspose\"}"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

  "Code":"200",

  "Status":"OK"

}

```

{{< /tab >}}

{{< /tabs >}}

## 云 SDK 系列

使用 SDK 是加速开发的最佳方式。 SDK 负责处理底层细节，让您专注于项目任务。请查看[GitHub 仓库](https://github.com/aspose-cells-cloud)有关 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示如何使用各种 SDK 调用 Aspose.Cells Web 服务：


{{< tabs tabTotal="11" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" tabName11="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorkbookDeleteDecryptDocument.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-workbook-DecryptWorkbook-decrypt-excel-workbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-DeleteDecryptDocument-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Document-decrypt_document-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DecryptExcelWorkbooks.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Workbook-DecryptWorkbook-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-workbook-DecryptWorkbook-decrypt-excel-workbook.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Workbook-DecryptWorkbook-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "7e303f6cbff92b225230ca3df7dd3df8" >}}

{{< /tab >}}

{{< tab tabNum="11" >}}

{{< gist "aspose-cells-cloud-gists" "8982baf625e5894b2eb99f2e0f9e957e" >}}

{{< /tab >}}

{{< /tabs >}}
