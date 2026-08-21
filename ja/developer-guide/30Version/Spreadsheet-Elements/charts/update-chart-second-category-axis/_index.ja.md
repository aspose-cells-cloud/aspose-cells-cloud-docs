---
title: "チャートの第2カテゴリ軸を更新する"
type: docs
url: /charts/second-category-axis/update/
weight: 160
keywords: "Aspose.Cells, チャート, 第2カテゴリ軸, REST API, チャート更新, Excel, クラウドAPI"
description: "Aspose.Cells Cloud REST API を使用して、Excelワークシート内のチャートの第2カテゴリ軸を更新する方法を学びます。"
ArticleTitle: "チャートの第2カテゴリ軸を更新する – Aspose.Cells Cloud API"
---

この REST API は、チャートの第2カテゴリ軸を更新します。

## PostChartSecondCategoryAxis API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメーター

| パラメーター名 | 型     | 位置   | 説明                                      |
| -------------- | ------ | ------ | ----------------------------------------- |
| name           | string | path   | Excel ファイルの名前。                    |
| sheetName      | string | path   | チャートを含むワークシートの名前。        |
| chartIndex     | integer| path   | 更新するチャートの 0 から始まるインデックス。|
| axis           | object | body   | 新しい設定を持つ第2カテゴリ軸オブジェクト。|
| folder         | string | query  | ファイルが格納されているフォルダーのパス。|
| storageName    | string | query  | ストレージサービスの名前。                |

**認証** – API は有効な OAuth 2.0 アクセストークンを必要とします。[認証ガイド](https://docs.aspose.cloud/cells/authentication/)に従って JWT トークンを生成し、以下に示す cURL の例のように `Authorization` ヘッダーにトークンを含めてください。

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Charts/PostChartSecondCategoryAxis)は公開可能なプログラミングインターフェースを定義し、Web ブラウザーから直接 REST によるやり取りを可能にします。

cURL コマンドラインツールを使用すると、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis?folder={folder}&storageName={storageName}" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{ 
        "axis": {
          /* 軸の設定例: "Title": "新しい軸タイトル", "IsVisible": true */
        }
      }'
```

* `{name}`, `{sheetName}`, `{chartIndex}`, `{folder}`, および `{storageName}` を実際の値に置き換えてください。リクエスト本文には、希望する設定を持つ `axis` オブジェクトを含める必要があります。*

{{< /tab >}}

{{< tab tabNum="2" >}}

**成功したレスポンス (200)**  

```json
{
  "Code": 200,
  "Status": "OK",
  "Chart": {
    "Id": "chart_1",
    "SecondCategoryAxis": {
      "Title": "新しい軸タイトル",
      "IsVisible": true,
      /* その他の軸プロパティ */
    }
  }
}
```

**エラーレスポンス**  

| ステータスコード | 説明                                           |
|------------------|----------------------------------------------|
| 400              | 不正なリクエスト – パラメーターが不足しているか、無効です。 |
| 401              | 認証エラー – JWT トークンが無効または不足しています。     |
| 404              | 見つかりません – 指定されたファイル、ワークシート、またはチャートが存在しません。 |
| 500              | サーバー内部エラー – サーバーで予期しない状況が発生しました。 |

```json
{
  "Code": 400,
  "Message": "無効なリクエストペイロードです。"
}
```

{{< /tab >}}

{{< /tabs >}}

## クラウド SDK ファミリー

SDK は低レベルの詳細を処理し、ビジネスロジックの開発に集中できるようにすることで、開発を簡素化します。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリー](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスにリクエストを送信する方法を示しています。

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

<!-- C# の例のプレースホルダー -->

{{< /tab >}}

{{< tab tabNum="2" >}}

<!-- Java の例のプレースホルダー -->

{{< /tab >}}

{{< tab tabNum="3" >}}

<!-- PHP の例のプレースホルダー -->

{{< /tab >}}

{{< tab tabNum="4" >}}

<!-- Ruby の例のプレースホルダー -->

{{< /tab >}}

{{< tab tabNum="5" >}}

<!-- Python の例のプレースホルダー -->

{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Post-ChartSecondCategoryAxis.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}

<!-- Android の例のプレースホルダー -->

{{< /tab >}}

{{< tab tabNum="8" >}}

<!-- Swift の例のプレースホルダー -->

{{< /tab >}}

{{< tab tabNum="9" >}}

<!-- Perl の例のプレースホルダー -->

{{< /tab >}}

{{< tab tabNum="10" >}}

<!-- Go の例のプレースホルダー -->

{{< /tab >}}

{{< /tabs >}}

**注意事項とベストプラクティス**

* `chartIndex` パラメーターは 0 から始まります。ワークシート内の最初のチャートのインデックスは 0 です。  
* API は `.xlsx` および `.xls` の両方のワークブック形式をサポートします。  
* `axis` オブジェクトには、必要なプロパティのみを含めてください。指定されなかったプロパティは、既存の値を維持します。  
* スロットリングを回避するため、レート制限のガイドライン（通常はアカウントあたり1分あたり100リクエスト）を遵守してください。  
---