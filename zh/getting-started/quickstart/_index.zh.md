---
title: "Aspose.Cells Cloud 快速入门：5 分钟内创建电子表格应用程序"
second_title: "文档"
ArticleTitle: "Aspose.Cells Cloud 快速入门"
linktitle: "快速入门"
type: docs
url: /zh/quickstart/
description: "Aspose.Cells Cloud 支持创建、转换、合并、拆分、保护 Excel 文件，并执行多种其他功能，例如内部对象操作等。"
weight: 20
keywords: "Aspose.Cells Cloud, Excel, 电子表格, API, 云 SDK, REST API, PDF, CSV, JSON, 快速入门"
---

以下说明将引导您完成 Aspose.Cells Cloud API 的初始化及所需电子表格处理库的安装过程。

您可以轻松地将电子表格转换、生成和编辑功能集成到任何现代操作系统上运行的应用程序中。这些功能使您能够读取、编辑、合并和拆分电子表格，并将其转换为多种文件格式。这些编程库支持您使用完整的电子表格组件集合，包括数据、样式、公式、表格、图表、数据透视表、页眉、页脚、批注、绘图对象、超链接、水印等。

## 创建免费账户

Aspose Cloud 采用清晰、舒适的计费模式，让您在决定购买前能够充分评估和测试产品功能。

首先，您需要创建一个免费账户以访问云基础设施：

- 请前往 [Aspose 仪表板](https://dashboard.aspose.cloud/#/) 登录页面
- 为加快登录速度，可点击 **使用 GitHub 登录** 或 **使用 Google 登录** 按钮
- 提供所需信息

{{% alert style="info" %}}

恭喜！您已成功注册 Aspose Cloud 账户。

{{% /alert %}}

## 查看并更新账户信息

接下来，您需要对账户进行个性化设置：

- 点击页面右上角的图标，访问您的 [Aspose 账户设置](https://id.containerize.com/admin/)。

![dashboard.png](dashboard.png)

- 在菜单栏中选择 **账户设置** 项目。检查您的设置，然后点击 **保存更改** 按钮确认。

![settings.png](settings.png)

## 获取您的安全凭证（Client Id 与 Secret）

Aspose 高度重视安全问题。我们使用 JWT 令牌进行身份验证，并采用端到端 HTTPS 加密，以保障所有客户端与服务器之间的交互安全。

应用程序（Application）是一组唯一的 API 凭证 —— **Client Id** 和 **Client Secret**。您可使用它们在调用我们的云 API 时进行身份验证。大多数情况下，您仅需一个应用程序。在某些高级场景中，您可能希望注册并使用多个应用程序，每个应用程序拥有独立的 **Client Id 与 Secret** 凭证。

要查看您的应用程序信息，请执行以下步骤：

1. 登录 [Aspose 仪表板](https://dashboard.aspose.cloud/#/)
2. 点击页面左侧的 [Applications](https://dashboard.aspose.cloud/applications)（应用程序）标签页。

![applications.png](applications.png)

3. 向下滚动至页面底部，您将看到 **Create New Application**（创建新应用程序）按钮。点击该按钮创建一个新应用程序。

![createnewapplication.png](createnewapplication.png)

4. 在创建页面，输入您希望设置的应用程序名称、描述和存储地址，然后点击 **Save**（保存）按钮。创建成功后将返回上一页。

![applicationinfo.png](applicationinfo.png)

5. 向下滚动至页面底部，您将看到刚刚创建的应用程序信息框。点击它以查看并更新您的安全凭证。

![firstapp.png](firstapp.png)

{{% alert style="info" %}}

恭喜！您已成功获取用于认证 Aspose.Cells API 调用的安全凭证。

{{% /alert %}}

## 选择并安装 SDK

请花一点时间熟悉 Aspose.Cells Cloud 提供的各类产品，以便更好地了解您的使用可能性。这些软件产品基于高性能的 [Cloud API](https://apireference.aspose.com/)，全天候（24/7）可用。

为有效使用 Cloud API，我们提供了一整套强大的 [Cloud SDK](https://products.aspose.cloud/cells/family)，支持几乎所有主流操作系统（Windows、macOS、Linux、Android）和流行编程语言，包括 [Android](https://products.aspose.cloud/cells/android)、[C#](https://products.aspose.cloud/cells/net)、[Python](https://products.aspose.cloud/cells/python)、[Golang](https://products.aspose.cloud/cells/go)、[Java](https://products.aspose.cloud/cells/java)、[Node.js](https://products.aspose.cloud/cells/nodejs)、[Perl](https://products.aspose.cloud/cells/perl)、[PHP](https://products.aspose.cloud/cells/php)、[Ruby](https://products.aspose.cloud/cells/ruby) 和 [Swift](https://products.aspose.cloud/cells/swift)。

上述所有 SDK 均托管于 [GitHub](https://github.com/aspose-cells-cloud/)。每个代码仓库均包含大量代码示例，以说明其用法。

## 查阅开发者文档及代码示例

现在，您的账户已完成配置，开发环境也已安装完毕。您可以开始使用所选 SDK 编写代码。请参考 [开发者指南](https://docs.aspose.cloud/cells/developer-guide/)，了解如何轻松使用 Cloud API。

例如：将工作簿转换为其他格式。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_Quickstart.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_Quickstart.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_Quickstart.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}

## 如有需要，请寻求帮助

欢迎随时在我们的 [Cloud 论坛](https://forum.aspose.cloud/c/cells/7) 描述您的问题并提出疑问。Aspose 技术支持团队随时准备为您提供帮助。请注意：Aspose 不提供电话技术支持；电话支持仅面向销售与购买相关问题。