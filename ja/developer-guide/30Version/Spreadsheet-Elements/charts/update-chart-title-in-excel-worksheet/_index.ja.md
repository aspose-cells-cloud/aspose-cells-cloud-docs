---
title: "Excelワークシート内のチャートタイトルを更新する"
type: docs
url: /charts/title/update/
aliases: [/update-chart-title-in-excel-worksheet/]
weight: 160
keywords: Excel, Aspose.Cells, REST API, チャートタイトル, 更新, クラウドSDK
description: Aspose.Cells Cloud REST API、cURL、および various SDK を使用して、Excelワークシート内のチャートタイトルを更新する方法を学びます。
ArticleTitle: "Excelワークシート内のチャートタイトルを更新する – Aspose.Cells Cloud ドキュメント"
---

この REST API は、チャートタイトルを更新します。

**前提条件:** 有効な Aspose Cloud アカウントと認証用 JWT トークンが必要です。一般的な手順は以下の通りです：

- Aspose Cloud アカウントにサインアップします。  
- 認証エンドポイントを通じて JWT トークンを生成します。  
- 対象のワークブックがサポートされるクラウドストレージ（デフォルトまたはカスタム）に保存されていることを確認します。

## PostWorksheetChartTitle API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

すべての API 呼び出しは、混合コンテンツ警告を回避するために **HTTPS** 経由で行う必要があります。

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を必要とします。

### リクエストパラメーター

| パラメーター名 | 型      | 位置     | 説明                          |
| -------------- | ------- | -------- | ----------------------------- |
| name           | 文字列  | path     | ワークブック名。              |
| sheetName      | 文字列  | path     | ワークシート名。              |
| chartIndex     | 整数    | path     | チャートの 0 から始まるインデックス。 |
| title          | 文字列  | body     | 新しいチャートタイトル。      |
| folder         | 文字列  | query    | ワークブックのフォルダー。    |
| storageName    | 文字列  | query    | ストレージ名。                |

### レスポンスステータスコード

| コード | 説明                                           |
| ------ | ---------------------------------------------- |
| 200    | OK – チャートタイトルが正常に更新されました。 |
| 400    | Bad Request – パラメーターが不足または無効です。 |
| 401    | Unauthorized – JWT トークンが無効または不足しています。 |
| 404    | Not Found – ワークブック、ワークシート、またはチャートが見つかりません。 |
| 500    | Internal Server Error – 予期しないサーバー状態です。 |

**注意:** `chartIndex` は 0 から始まります。ワークシート上の最初のチャートは `0` で参照されます。

<a href="https://apireference.aspose.cloud/cells/#/Charts/PostWorksheetChartTitle" target="_blank" rel="noopener noreferrer">OpenAPI スペック</a> はパブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザーから直接 REST による操作を実行できるようにします。

cURL コマンドラインツールを使用して、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API に呼び出しを行う方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v POST "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/title" \
-d '{"title":"Stock exchange"}' \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## クラウド SDK ファミリー

SDK を使用することが開発を迅速化する最良の方法です。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧については、<a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub リポジトリー</a>をご確認ください。

以下のコード例は、 various SDK を使用して Aspose.Cells Web サービスに呼び出しを行う方法を示しています：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-UpdateChartTitle-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-UpdateChartTitle-update-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PostWorksheetChartTitle-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-update_chart_title-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UpdateChartTitleInExcelWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-UpdateChartTitle-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-UpdateChartTitle-update-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-UpdateChartTitle-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "aab21ae55930321e6eaa46ffe5b8e7bf" >}}

{{< /tab >}}

{{< /tabs >}}