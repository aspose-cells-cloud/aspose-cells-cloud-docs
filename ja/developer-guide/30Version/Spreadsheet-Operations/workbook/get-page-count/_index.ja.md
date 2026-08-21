---
title: "Excel ファイルからページ数を取得する"
second_title: "Document"
linktitle: "Pages"
type: docs
url: /get-page-count-from-an-excel-file/
aliases: [/workbook/page-count/, /workbook/get/page-count/]
keywords: "Aspose.Cells, Cloud API, Excel ページ数, ワークブックのページ分割"
description: "Aspose.Cells Cloud REST API (v3.0) を使用して Excel ワークブックの印刷可能なページの総数を取得します。リクエスト形式、必要なパラメータ、cURL の例、レスポンススキーマ、エラーハンドリング、および複数言語向けの SDK スニペットを含みます。"
weight: 10
version: "v3.0"
ArticleTitle: "Aspose.Cells Cloud API を使用して Excel ファイルからページ数を取得する"
---

この REST API は、ワークブックの**ページ数**を返します。

## セキュリティと認証
Aspose.Cells Cloud API は安全であり、[JWT トークンベースの認証](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)が必須です。

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/pagecount
```

### リクエストパラメータ

| パラメータ名 | 型     | 位置   | 必須 | 説明                            |
| ------------ | ------ | ------ | ---- | -------------------------------------- |
| name         | string | path   | はい  | Excel ドキュメントの名前です。        |
| folder       | string | query  | いいえ | ドキュメントを含むフォルダです。      |
| storageName  | string | query  | いいえ | 使用するストレージの名前です。        |

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/Workbook/GetPageCount) はパブリックにアクセス可能なプログラミングインタフェースを定義し、Web ブラウザから直接 REST のやり取りを実行できるようにします。

cURL コマンドラインツールを使用して、Aspose.Cells REST API に簡単にアクセスできます。以下の例は、cURL を使用してエンドポイントを呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/YourFile.xlsx/pagecount" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

*`YourFile.xlsx` を実際のクエリ対象のワークブック名に置き換えてください。*

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
13
```

{{< /tab >}}

{{< /tabs >}}

### レスポンススキーマ

| HTTP ステータス | データ型 | 説明                                                       |
| --------------- | -------- | ----------------------------------------------------------------- |
| 200             | integer  | ワークブック内の印刷可能なページの総数 (例: `13`)。             |
| 4xx‑5xx         | JSON     | エラーオブジェクト (「エラーハンドリング」セクション参照)。      |

## クラウド SDK ファミリー

SDK を使用することで、開発を最適化できます。SDK は低レベルの詳細な処理を担い、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetPageCount.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetPageCount.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetPageCount.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetPageCount.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82deb2e4189bc27ae92abf73c36b4df0" "Example_GetPageCount.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetPageCount.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetPageCount.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetPageCount.go" >}}

{{< /tab >}}

{{< /tabs >}}

## エラーハンドリング

| HTTP ステータス | 説明                           | 例: JSON ボディ                                                                      |
| --------------- | ------------------------------ | ------------------------------------------------------------------------------------ |
| 401             | 無効または不足している JWT トークン。 | `{ "Code": "InvalidAuthenticationToken", "Message": "Access token is missing or invalid." }` |
| 404             | 指定されたワークブックが見つかりません。 | `{ "Code": "FileNotFound", "Message": "The requested file does not exist." }`         |
| 400             | 不正なリクエスト – 必須パラメータが不足しています。 | `{ "Code": "BadRequest", "Message": "Required parameter 'name' is missing." }`        |
| 500             | サーバー内部エラー。           | `{ "Code": "InternalError", "Message": "An unexpected error occurred." }`             |
---