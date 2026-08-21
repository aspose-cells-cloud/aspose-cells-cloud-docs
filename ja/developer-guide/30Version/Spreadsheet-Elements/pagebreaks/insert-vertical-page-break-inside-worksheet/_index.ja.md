---
title: "垂直ページ区切りの追加"
second_title: "Document"
linktitle: "垂直ページ区切りの追加"
type: docs
url: /ja/page-breaks/add-vertical-page-break/
aliases: [  /ja/insert-vertical-page-break-inside-worksheet/ ]
keywords: "Aspose.Cells Cloud, 垂直ページ区切り, REST API, Excel, SDK, cURL"
description: "Aspose.Cells Cloud REST API (v3.0) を使用して Excel ワークシートに垂直ページ区切りを挿入する方法を学習します。リクエスト構文、cURL の例、SDK サンプル、認証ガイド、エラー処理の詳細を含みます。"
weight: 40
ArticleTitle: "垂直ページ区切りの追加 – Aspose.Cells Cloud API"
---

この REST API は、ワークシートに垂直ページ区切りを挿入します。

## セキュリティと認証
Aspose.Cells Cloud API は安全であり、[JWT トークンベースの認証](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)を必要とします。

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks
```

### リクエストパラメータ

| パラメータ名     | タイプ    | 位置   | 説明                                                                 |
|----------------|---------|------|--------------------------------------------------------------------|
| name           | string  | path | Excel ワークブックの名前。                                                 |
| sheetName      | string  | path | ページ区切りを追加するワークシートの名前。                                          |
| cellname       | string  | query | セル参照（例：**A1**）で、ページ区切りの位置を定義します。                                |
| column         | integer | query | ページ区切りが開始される列の 0 から始まるインデックス。                                     |
| row            | integer | query | ページ区切りが開始される行の 0 から始まるインデックス。                                      |
| startRow       | integer | query | ページ区切り範囲の最初の行。                                                  |
| endRow         | integer | query | ページ区切り範囲の最後の行。                                                   |
| folder         | string  | query | ワークブックが存在するストレージ内のフォルダーパス。                                       |
| storageName    | string  | query | ストレージサービスの名前。                                                    |

**必須パラメータ** – `cellname` **または** `column` のいずれかを指定する必要があります。`column` を使用する場合、範囲を定義するために `row`、`startRow`、`endRow` を追加で指定することもできます。その他のフィールドはすべて任意です。

[OpenAPI 仕様書](https://apireference.aspose.cloud/cells/#/PageBreaks/PutVerticalPageBreak) では、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 通信を実行できるようにしています。

### cURL の例

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/SampleBreaks.xlsx/worksheets/Sheet1/verticalpagebreaks?column=9" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

#### 応答

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**HTTP ステータスコード**

| コード  | 意味              | 説明                                               |
|------|-----------------|--------------------------------------------------|
| 200  | OK              | フィルターが正常に適用され、応答には操作の詳細が含まれます。                      |
| 400  | Bad Request     | パラメータが不足または無効です（例：サポートされていないファイル形式）。             |
| 401  | Unauthorized    | JWT トークンが無効または不足しています。                                |
| 413  | Payload Too Large | アップロードされたファイルがサイズ制限を超えています。                              |
| 500  | Internal Server Error | サーバーで予期せぬエラーが発生しました。                                |

## Cloud SDK ファミリー

SDK を使用すると、開発を最も効率的にスピードアップできます。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストは [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutVerticalPageBreak.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutVerticalPageBreak.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutVerticalPageBreak.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutVerticalPageBreak.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutVerticalPageBreak.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutVerticalPageBreak.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutVerticalPageBreak.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutVerticalPageBreak.go" >}}

{{< /tab >}}

{{< /tabs >}}
---