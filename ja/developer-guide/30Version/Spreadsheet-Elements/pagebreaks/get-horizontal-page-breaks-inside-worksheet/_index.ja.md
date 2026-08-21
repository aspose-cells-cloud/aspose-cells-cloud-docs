---
title: "水平改ページの取得"
second_title: "Document"
linktitle: "水平改ページの取得"
type: docs
url: /ja/page-breaks/get-horizontal-page-breaks/
aliases: [  /ja/get-horizontal-page-breaks-inside-worksheet/ ]
keywords: "水平改ページ, Aspose.Cells Cloud, REST API, Excelワークシート, SDK"
description: "Aspose.Cells Cloud API を使用して Excel ワークシートから水平改ページを取得します。エンドポイント、パラメーター、cURL の使用例、応答形式、および C#、Java、Python など various 言語向けの SDK スニペットを含みます。"
ArticleTitle: "水平改ページの取得 - Aspose.Cells Cloud API ドキュメント"
weight: 10
---

**水平改ページ** – 指定された行の後に新しい印刷ページを強制的に開始する、行単位の改ページです。この REST API は、これらの水平改ページを取得します。

## セキュリティと認証

Aspose.Cells Cloud API は安全であり、[JWT トークンベースの認証](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)を必要とします。

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks
```

### リクエストパラメーター

| パラメーター名 | 型     | 位置   | 説明                                                                 |
| -------------- | ------ | ------ | -------------------------------------------------------------------- |
| name           | string | path   | Excel ファイルの名前。                                               |
| sheetName      | string | path   | ワークシートの名前。                                                 |
| folder         | string | query  | ファイルが存在するストレージ内のフォルダーのパス。（省略可能）     |
| storageName    | string | query  | ストレージの名前。（省略可能）                                       |

<a href="https://apireference.aspose.cloud/cells/#/PageBreaks/GetHorizontalPageBreaks" rel="noopener" title="GetHorizontalPageBreaks の OpenAPI 仕様">OpenAPI 仕様</a> は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザーから直接 REST 通信を実行できるようにします。

cURL コマンドラインツールを使用すると、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例では、cURL を使用してクラウド API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/horizontalpagebreaks" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "HorizontalPageBreaks": {
    "HorizontalPageBreakList": [
      {
        "Row": 6,
        "EndColumn": 16383,
        "StartColumn": 0
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/HorizontalPageBreaks",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## エラーハンドリング

| HTTP ステータス | 説明                                                       | 例 JSON                                                |
| --------------- | ---------------------------------------------------------- | ------------------------------------------------------ |
| 400             | 不正リクエスト – パラメーターが不足している、または無効です。 | `{ "Code": 400, "Message": "Invalid parameter." }`     |
| 401             | 認証エラー – JWT トークンが不足している、または無効です。     | `{ "Code": 401, "Message": "Authentication failed." }` |
| 404             | 見つかりません – 指定されたファイルまたはワークシートが存在しません。 | `{ "Code": 404, "Message": "Resource not found." }`    |
| 500             | サーバー内部エラー – サーバー上で予期しない状態が発生しました。 | `{ "Code": 500, "Message": "Server error." }`          |

## クラウド SDK ファミリー

SDK を使用すると、開発を最速で進めることができます。SDK は低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全なリストは [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetHorizontalPageBreaks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetHorizontalPageBreaks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetHorizontalPageBreaks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetHorizontalPageBreaks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetHorizontalPageBreaks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetHorizontalPageBreaks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetHorizontalPageBreaks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetHorizontalPageBreaks.go" >}}

{{< /tab >}}

{{< /tabs >}}
---