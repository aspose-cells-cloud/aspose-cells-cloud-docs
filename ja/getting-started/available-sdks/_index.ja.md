---
title: "利用可能な Aspose.Cells Cloud SDK"
second_title: "ドキュメント"
ArticleTitle: "利用可能な Aspose.Cells Cloud SDK：C#、Java、PHP、Python、Ruby、Node.js、Go、Perl"
LinkTitle: "利用可能な SDK"
type: docs
url: /ja/available-sdks/
description: "Aspose.Cells Cloud SDK を C#、Java、PHP、Python、Ruby、Node.js、Go、Perl 用に探索しましょう。低コストのクロスプラットフォーム API を使用して、クラウド上で Excel ファイルを構築・変換・分析します。"
weight: 30
keywords: "Aspose.Cells Cloud SDK、C#、Java、PHP、Python、Ruby、Node.js、Go、Perl、Excel、クラウド API"
---

# **Aspose.Cells Cloud SDK を使用する理由**

## **クロスプラットフォーム互換性**

Aspose.Cells Cloud SDK は、複数の開発言語向けに信頼性が高く安定したライブラリを提供します。これにより、Windows、Linux、macOS など、さまざまなプラットフォームでの統合が容易になり、強力なクロスプラットフォーム対応を実現します。

## **効率的な Excel 処理と豊富な機能セット**

Aspose.Cells Cloud SDK を使用すると、ローカルに Office ソフトウェアをインストールすることなく、クラウド上で Excel ファイルを効率的に読み取り・書き込み・修正・変換できます。SDK は、数式計算、チャート作成、条件付き書式設定など、複雑な Excel 操作をサポートする豊富な API と機能を提供し、開発者の多様なニーズに対応します。

## **簡単に統合可能**

SDK は簡潔で明確な API を提供し、既存のプロジェクトへすぐに統合できるため、開発時間とコストを削減できます。

## **コスト削減**

Aspose.Cells Cloud SDK を使用すると、高額なオンプレミスの Office ソフトウェアやサーバーの購入・保守の必要がなくなり、ビジネスの運用コストを削減できます。

### SDK 概要

<table>
<thead>
<tr>
<th>言語</th>
<th>最新バージョン</th>
<th>インストール方法</th>
<th>クイックスタート例</th>
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

**前提条件** – .NET 6+ / Java 8+ / PHP 7.4+ / Python 3.7+ / Ruby 2.6+ / Node 12+ / Go 1.16+ / Perl 5.30+。また、有効な Aspose Cloud クライアント ID とクライアント シークレットが必要です。

**サンプル API リクエストとレスポンス** – Excel ブックを PDF に変換する場合：

```json
{
  "Input": "EmployeeSalesSummary.xlsx",
  "OutputFormat": "pdf"
}
```

SDK はオープンソースであり、GitHub でホストされています。フォークしたり、貢献することも可能です：

- C#：https://github.com/aspose-cells-cloud/aspose-cells-cloud-csharp  
- Java：https://github.com/aspose-cells-cloud/aspose-cells-cloud-java  
- PHP：https://github.com/aspose-cells-cloud/aspose-cells-cloud-php  
- Python：https://github.com/aspose-cells-cloud/aspose-cells-cloud-python  
- Ruby：https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby  
- Node.js：https://github.com/aspose-cells-cloud/aspose-cells-cloud-node  
- Go：https://github.com/aspose-cells-cloud/aspose-cells-cloud-go  
- Perl：https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl  

要約すると、Aspose.Cells Cloud SDK を使用することで、クロスプラットフォーム互換性、Excel ファイルの効率的な処理、豊富な機能セット、セキュリティとプライバシー保護、高いスケーラビリティ、簡単な統合、コミュニティによるサポートとドキュメント、コスト削減など、多くの利点が得られます。これらの特長により、SDK は Excel ファイルを扱う開発者にとって理想的な選択肢となります。

# **応用シーン**

## **スプレッドシート処理の自動化**

- Aspose.Cells Cloud SDK を使用すると、Excel などのスプレッドシートファイルを一括処理する自動化スクリプトを作成できます。  
- 自動化タスクには、データのインポート・エクスポート、書式設定、数式計算、チャート生成などがあります。

## **クラウドでのデータ処理と分析**

- クラウド上の Aspose.Cells サービスを使用すると、ローカルのコンピューティングリソースを占有することなく、大規模なスプレッドシートデータを処理できます。  
- 複雑なデータ分析、データマイニング、レポート生成が必要なシナリオに適しています。

## **クロスプラットフォーム互換性**

- SDK のクロスプラットフォーム性により、Aspose.Cells Cloud SDK を使用すると、さまざまなオペレーティングシステムやアーキテクチャ上でスプレッドシート処理を容易に実装できます。  
- Web アプリケーションのバックエンド、デスクトップアプリケーション、モバイルアプリケーションのバックエンドなど、複数のオペレーティング環境に対応する必要があるシナリオに特に適しています。

## **API 統合と拡張**

- Aspose.Cells Cloud SDK を既存の API に統合することで、スプレッドシート処理機能をサービスの一部として提供できます。  
- エンタープライズ向けアプリケーション、SaaS プラットフォームの構築、または API サービスの提供に適しています。

## **ドキュメントの共同編集と共有**

- Aspose.Cells Cloud SDK を使用すると、複数ユーザーによるスプレッドシートのオンライン共同編集が可能になります。  
- ユーザーはクラウド上でスプレッドシートファイルをリアルタイムで編集・コメント・共有でき、チームのコラボレーションを向上させます。

## **データの移行と変換**

- 他の形式やシステムからデータを移行する必要がある場合、Aspose.Cells Cloud SDK をデータ変換の橋渡しとして使用できます。  
- 他の形式のデータを Excel 形式に変換し、その後の分析・処理に利用できます。

## **レポートの自動生成**

- 定期的にスクリプトを実行することで、Aspose.Cells Cloud SDK を使用して定期的なレポートやダッシュボードを自動生成できます。  
- 業務指標、販売データ、財務データなどを定期的にモニタリングする必要がある組織にとって有用です。

## **CI/CD プロセスへの統合**

- Aspose.Cells Cloud SDK を継続的インテグレーション／継続的デプロイメント（CI/CD）プロセスに統合し、スプレッドシートデータの正確性を自動的にテストできます。  
- これにより、コード変更がスプレッドシートデータの整合性や書式設定に影響を与えないことを確保できます。

## **カスタムスプレッドシートアプリケーション**

- Aspose.Cells Cloud SDK を使用して、特定のビジネスニーズに合わせたカスタムスプレッドシートアプリケーションを構築できます。  
- たとえば、独自のフォーム処理アプリケーションや財務データ管理ツールの開発などが可能です。

# **SDK の利点**

当社の SDK は 100% テスト済みで、すぐに利用可能な状態で提供されます。オープンソースであり、MIT ライセンスの下で提供されているため、完全に無料で使用・カスタマイズできます。
---