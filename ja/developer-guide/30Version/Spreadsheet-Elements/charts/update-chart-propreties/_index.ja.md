---
title: "チャートのプロパティを更新する"
type: docs
url: /charts/properties/update/
aliases: [/update-chart-properties/]
weight: 160
keywords: "Aspose.Cells, チャート, 更新, Excel, REST API, SDK"
description: "Aspose.Cells Cloud REST API（v3.0）を使用して、Excelワークブック内のチャートのプロパティ（タイプ、タイトル、凡例など）を更新する方法を学びます。エンドポイント、パラメータ、cURLの使用例、およびC#、Java、PHP、Ruby、Node.js、Perl、Go用のSDKスニペットを含みます。"
ArticleTitle: "チャートのプロパティを更新する – Aspose.Cells Cloud REST API"
---

このREST APIは、チャートのプロパティを更新します。

### **セキュリティと認証**

Aspose.Cells Cloud APIは安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWTトークンベースの認証</a>が必要です。

## PostWorksheetChart API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}
```

### リクエストパラメータ

| パラメータ名 | 種類    | パス/クエリ文字列/HTTPボディ | 説明                                         |
| ------------ | ------- | -------------------------- | --------------------------------------------- |
| name         | string  | path                       | Excelファイルの名前。                         |
| sheetName    | string  | path                       | チャートを含むワークシートの名前。            |
| chartIndex   | integer | path                       | 更新対象のチャートの0から始まるインデックス。 |
| chart        | object  | body                       | 変更するチャートのプロパティを定義するJSONオブジェクト。 |
| folder       | string  | query                      | ファイルが存在するストレージ内のフォルダ。    |
| storageName  | string  | query                      | ストレージサービスの名前。                     |

### リクエストボディのスキーマ

**`chart`** オブジェクトには、変更可能なプロパティが含まれます。以下は、よく使用されるフィールドをいくつか含む代表的なJSONの例です：

```json
{
  "Title": {
    "Text": "四半期売上高"
  },
  "ShowLegend": true,
  "Type": "Line",
  "DataLabels": {
    "ShowValue": true,
    "ShowPercentage": false
  },
  "ChartArea": {
    "BorderColor": "Blue",
    "FillColor": "White"
  }
}
```

> **注意:** 変更したいフィールドのみを指定すればよいです。指定しなかったプロパティは、既存の値を保持します。

<a href="https://apireference.aspose.cloud/cells/#/Charts/PostWorksheetChart" target="_blank" rel="noopener noreferrer">OpenAPI仕様</a>は、パブリックにアクセス可能なプログラミングインターフェースを定義し、ウェブブラウザから直接RESTによるやり取りを実行できるようにします。

cURLコマンドラインツールを使用すると、Aspose.Cellsウェブサービスへ簡単にアクセスできます。以下の例は、cURLを使ってCloud APIへリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet4/charts/1" \
-d '{"Type": "line"}' \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## レスポンス

APIは、操作結果を示すJSONオブジェクトを返します。正常な更新の場合、以下が返されます：

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**成功時のステータスコード**

| HTTPステータス | 説明                               |
| -------------- | ---------------------------------- |
| 200            | OK – チャートのプロパティが正常に更新されました。 |

**レスポンスヘッダー**

| ヘッダー名       | 説明                                      |
| ---------------- | ----------------------------------------- |
| `Content-Type`   | `application/json` – レスポンスボディがJSON形式であることを示します。 |
| `X-RequestId`    | リクエストの一意識別子（トラブルシューティングに役立ちます）。 |

考えられるエラーレスポンスは以下の通りです：

| HTTPステータス | 説明                                   |
| -------------- | -------------------------------------- |
| 400            | Bad Request – 無効なパラメータまたはボディ |
| 401            | Unauthorized – トークンが不足している、または無効です |
| 404            | Not Found – ファイル、ワークシート、またはチャートが見つかりません |
| 500            | Internal Server Error                  |

その他のチャート関連の操作については、関連トピックである[チャートタイトルの更新](/charts/title/update/)や[チャート凡例の更新](/charts/legend/update/)をご参照ください。

## Cloud SDKファミリー

SDKを使用することが開発を高速化する最良の方法です。SDKは低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDKの完全な一覧については、<a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHubリポジトリ</a>をご確認ください。

以下のコード例は、さまざまなSDKを使用してAspose.Cellsウェブサービスへリクエストを送信する方法を示しています：

{{< tabs tabTotal="6" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Node.js" tabName5="Perl" tabName6="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-Charts-UpdateChartProperties-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-CellsChartsPostWorksheetChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-cells_charts_post_worksheet_chart-.rb" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-UpdateChartProperties-1.js" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-UpdateChartProperties-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "d554e51920e174943a60f4343a97e203" >}}

{{< /tab >}}

{{< /tabs >}}