---
title: "可用的 Aspose.Cells Cloud SDK"
second_title: "文档"
ArticleTitle: "可用的 Aspose.Cells Cloud SDK：C#、Java、PHP、Python、Ruby、Node.js、Go、Perl"
LinkTitle: "可用 SDK"
type: docs
url: /zh/available-sdks/
description: "探索 Aspose.Cells Cloud 的 C#、Java、PHP、Python、Ruby、Node.js、Go 和 Perl SDK。借助低成本、跨平台的 API，在云端构建、转换和分析 Excel 文件。"
weight: 30
keywords: "Aspose.Cells Cloud SDK、C#、Java、PHP、Python、Ruby、Node.js、Go、Perl、Excel、云 API"
---

# **为何使用 Aspose.Cells Cloud SDK**

## **跨平台兼容性**

Aspose.Cells Cloud SDK 提供了适用于多种开发语言的可靠、稳定的库。它为开发者提供了强大的跨平台支持，使在 Windows、Linux 或 macOS 上集成变得轻松便捷。

## **高效的 Excel 处理与丰富的功能集**

Aspose.Cells Cloud SDK 允许开发者在云端高效地处理 Excel 文件，包括读取、写入、修改和转换，无需安装任何本地 Office 软件。该 SDK 提供了丰富的 API 和功能，以支持复杂的 Excel 操作，例如公式计算、图表创建、条件格式化等，满足开发者的多样化需求。

## **易于集成**

SDK 提供了简洁、清晰的 API，使开发者能够快速将其集成到现有项目中，从而缩短开发时间并降低成本。

## **降低运营成本**

使用 Aspose.Cells Cloud SDK 可以避免采购和维护昂贵的本地 Office 软件或服务器，从而降低您的业务运营成本。

### SDK 概览

<table>
<thead>
<tr>
<th>语言</th>
<th>最新版本</th>
<th>安装方式</th>
<th>快速入门示例</th>
</tr>
</thead>
<tbody>
<tr>
<td>C#</td>
<td>23.12</td>
<td><code>dotnet add package Aspose.Cells-Cloud</code></td>
<td>
<pre><code class="language-csharp">var api = new CellsApi("clientId", "clientSecret");
var result = api.ConvertSpreadsheet(new ConvertSpreadsheetRequest("sample.xlsx", "pdf"));</code></pre>
</td>
</tr>
<tr>
<td>Java</td>
<td>23.12</td>
<td><code>mvn dependency:copy -Dartifact=aspose:aspose-cells-cloud:23.12</code></td>
<td>
<pre><code class="language-java">CellsApi api = new CellsApi("clientId", "clientSecret");
ConvertSpreadsheetRequest request = new ConvertSpreadsheetRequest();
request.setSpreadsheet("Book1.xlsx");
request.setFormat("pdf");
File result = api.ConvertSpreadsheetRequest(request);</code></pre>
</td>
</tr>
<tr>
<td>PHP</td>
<td>23.12</td>
<td><code>composer require aspose/cells-cloud-sdk</code></td>
<td>
<pre><code class="language-php">$instance = new CellsApi(getenv("CellsCloudClientId"), getenv("CellsCloudClientSecret"));
$convertSpreadsheetRequest = new ConvertSpreadsheetRequest();
$convertSpreadsheetRequest->setSpreadsheet($EmployeeSalesSummaryXlsx);
$convertSpreadsheetRequest->setFormat("pdf");
$instance->convertSpreadsheet($convertSpreadsheetRequest, "export-out1.pdf");</code></pre>
</td>
</tr>
<tr>
<td>Python</td>
<td>23.12</td>
<td><code>pip install aspose-cells-cloud</code></td>
<td>
<pre><code class="language-python">instance = CellsApi(os.getenv('CellsCloudClientId'), os.getenv('CellsCloudClientSecret'))
instance.convert_spreadsheet(ConvertSpreadsheetRequest('EmployeeSalesSummary.xlsx', 'pdf'), local_outpath="EmployeeSalesSummary.pdf")</code></pre>
</td>
</tr>
<tr>
<td>Ruby</td>
<td>23.12</td>
<td><code>gem install aspose_cells_cloud</code></td>
<td>
<pre><code class="language-ruby">@instance = AsposeCellsCloud::CellsApi.new(ENV['CellsCloudClientId'], ENV['CellsCloudClientSecret'])
request = AsposeCellsCloud::ConvertSpreadsheetRequest.new(:Spreadsheet=>'EmployeeSalesSummary.xlsx', :format=>'pdf')
response = @instance.convert_spreadsheet(request)</code></pre>
</td>
</tr>
<tr>
<td>Node.js</td>
<td>23.12</td>
<td><code>npm install asposecellscloud</code></td>
<td>
<pre><code class="language-javascript">const cellsApi = new CellsApi(process.env.CellsCloudClientId, process.env.CellsCloudClientSecret, "v4.0", process.env.CellsCloudApiBaseUrl);
var request = new model.ConvertSpreadsheetRequest();
request.spreadsheet = "Book1.xlsx";
request.format = "pdf";
return cellsApi.convertSpreadsheet(request).then((result) => {
    expect(result.response.statusCode).to.equal(200);
});</code></pre>
</td>
</tr>
<tr>
<td>Go</td>
<td>23.12</td>
<td><code>go get github.com/aspose/cells-cloud-go/v2</code></td>
<td>
<pre><code class="language-go">instance := NewCellsApiService(os.Getenv("ProductClientId"), os.Getenv("ProductClientSecret"))
convertedData, httpResponse, err := instance.ConvertSpreadsheet(&amp;ConvertSpreadsheetRequest{Spreadsheet: employeeSalesSummaryXlsx, Format: "pdf"})</code></pre>
</td>
</tr>
</tbody>
</table>

**前置条件**：.NET 6+ / Java 8+ / PHP 7.4+ / Python 3.7+ / Ruby 2.6+ / Node 12+ / Go 1.16+ / Perl 5.30+。您还需拥有有效的 Aspose Cloud 客户端 ID 和客户端密钥。

**示例 API 请求与响应**：将 Excel 工作簿转换为 PDF：

```json
{
  "Input": "EmployeeSalesSummary.xlsx",
  "OutputFormat": "pdf"
}
```

这些 SDK 均为开源项目，托管于 GitHub；您可 Fork 或参与贡献：

- C#：https://github.com/aspose-cells-cloud/aspose-cells-cloud-csharp  
- Java：https://github.com/aspose-cells-cloud/aspose-cells-cloud-java  
- PHP：https://github.com/aspose-cells-cloud/aspose-cells-cloud-php  
- Python：https://github.com/aspose-cells-cloud/aspose-cells-cloud-python  
- Ruby：https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby  
- Node.js：https://github.com/aspose-cells-cloud/aspose-cells-cloud-node  
- Go：https://github.com/aspose-cells-cloud/aspose-cells-cloud-go  
- Perl：https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl  

总而言之，使用 Aspose.Cells Cloud SDK 可带来诸多优势，包括跨平台兼容性、高效的 Excel 文件处理能力、丰富的功能集、安全与隐私保护、高可扩展性、易于集成、社区支持与文档资源，以及降低成本等。这些优势使其成为处理 Excel 文件的开发者的理想选择。

# **应用场景**

## **电子表格处理自动化**

- 利用 Aspose.Cells Cloud SDK，开发者可编写自动化脚本，实现 Excel 等电子表格文件的批量处理。  
- 自动化任务可包括数据导入/导出、格式设置、公式计算、图表生成等。

## **云端数据处理与分析**

- 借助云端 Aspose.Cells 服务，可在不占用本地计算资源的前提下处理大型电子表格数据。  
- 特别适用于需要进行复杂数据分析、数据挖掘或报表生成的场景。

## **跨平台兼容性**

- 由于 SDK 具备跨平台特性，Aspose.Cells Cloud SDK 可轻松实现在不同操作系统和架构上的电子表格处理。  
- 特别适用于需支持多操作环境的场景，例如 Web 应用后端、桌面应用及移动应用后端。

## **API 集成与扩展**

- Aspose.Cells Cloud SDK 可集成至现有 API 中，作为服务的一部分提供电子表格处理能力。  
- 特别适用于构建企业级应用、SaaS 平台或提供 API 服务。

## **文档协作与共享**

- 利用 Aspose.Cells Cloud SDK，可实现多人在线协同编辑电子表格。  
- 用户可在云端实时编辑、评论并共享电子表格文件，从而提升团队协作效率。

## **数据迁移与转换**

- 当需将数据从其他格式或系统迁移时，Aspose.Cells Cloud SDK 可作为数据转换的桥梁。  
- 可将其他格式的数据转换为 Excel 格式，便于后续分析与处理。

## **自动化报表生成**

- 通过定期运行脚本，可利用 Aspose.Cells Cloud SDK 自动生成周期性报表或仪表板。  
- 特别适用于需定期监控业务指标、销售数据或财务数据的组织。

## **集成至 CI/CD 流程**

- 将 Aspose.Cells Cloud SDK 集成至持续集成/持续部署（CI/CD）流程中，以自动化测试电子表格数据的正确性。  
- 有助于确保代码变更不会影响电子表格数据的完整性或格式。

## **定制化电子表格应用**

- 利用 Aspose.Cells Cloud SDK，可构建满足特定业务需求的定制化电子表格应用。  
- 例如开发自定义表单处理应用、财务数据管理工具等。

# **SDK 优势**

我们的 SDK 均经过 100% 全面测试，开箱即用。所有 SDK 均为开源项目，采用 MIT 许可证，您可以免费使用并完全自定义。