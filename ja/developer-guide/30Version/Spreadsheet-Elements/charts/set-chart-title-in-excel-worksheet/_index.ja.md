---
title: "Aspose.Cells Cloud API – Excelワークシート内のチャートタイトルの設定"
type: docs
url: /chart/title/add/
aliases: [/set-chart-title-in-excel-worksheet/]
weight: 30
keywords: "Aspose.Cells Cloud, チャートタイトル API, Excel チャートタイトル, REST API, SDK サンプル"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークシート内のチャートタイトルを追加または更新する方法を学びます。cURL、SDK サンプル、必要なパラメータ、認証手順、エラー処理を含みます。"
---

チャートタイトルを追加するか、既存のタイトルを表示状態にします。

## PutWorksheetChartTitle API

```http
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名     | 型     | 位置   | 説明                           |
| --------------- | ------ | ------ | ------------------------------ |
| name            | 文字列 | path   | ワークブック名。               |
| sheetName       | 文字列 | path   | ワークシート名。               |
| chartIndex      | 整数   | path   | チャートのインデックス。       |
| title           | 文字列 | body   | チャートタイトルのテキスト。   |
| folder          | 文字列 | query  | ワークブックを含むフォルダ。   |
| storageName     | 文字列 | query  | ストレージ名。                 |

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetChartTitle) は公開可能なプログラミングインターフェースを定義し、ウェブブラウザから直接 REST 通信を実行できるようにします。

cURL コマンドラインツールを使用して Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/title" \
  -d '{"Text":"Sales Chart"}' \
  -X PUT \
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

**エラー応答**

| HTTP コード | 例ペイロード                                                                     | 説明                                     |
| ----------- | -------------------------------------------------------------------------------- | ----------------------------------------- |
| 400         | `{ "Code": "400", "Message": "Invalid request payload." }`                      | リクエストボディが不正、または必須フィールドが不足しています。 |
| 401         | `{ "Code": "401", "Message": "Authentication failed. Invalid or expired JWT token." }` | ベアラートークンが不足、無効、または期限切れです。 |
| 404         | `{ "Code": "404", "Message": "Workbook, worksheet, or chart not found." }`       | 指定されたリソースが存在しません。        |
| 500         | `{ "Code": "500", "Message": "Internal server error." }`                         | サーバー上で予期せぬエラーが発生しました。 |

## Cloud SDK ファミリー

SDK を使用すると、開発が最も迅速に行えます。SDK は低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-SetChartTitle-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-SetChartTitle-set-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PutWorksheetChartTitle-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-add_chart_title-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SetChartTitle.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-SetChartTitle-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-SetChartTitle-set-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-SetChartTitle-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "728d523e11f8751f5f601bafb04ab86f" >}}

{{< /tab >}}

{{< /tabs >}}