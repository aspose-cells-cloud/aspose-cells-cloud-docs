---
title: "ワークシートのコメントを取得 – Aspose.Cells Cloud API ドキュメント"
type: docs
url: /ja/comments/get/
aliases: [  /ja/get-comment-from-a-worksheet/ ]
keywords: "Aspose.Cells, ワークシート コメント, API, GET, Excel"
description: "Aspose.Cells Cloud API (v3.0) を使用して、セル名でワークシートのコメントを取得する方法を学習します。リクエスト URL、パラメータ、cURL の例、応答詳細、SDK のコードスニペットを含みます。"
weight: 10
ArticleTitle: "ワークシートのコメントを取得 – Aspose.Cells Cloud API ドキュメント"
---

この REST API は、**Aspose.Cells Cloud** を使用してセル名でワークシートのコメントを取得します。

**前提条件:** この操作を呼び出すには、`Authorization` ヘッダー (`Bearer <jwt token>`) に有効な JWT アクセストークンを含める必要があります。トークンは [認証ガイド](/cells/authentication/) に記載されている Aspose.Cells Cloud の認証フローで取得できます。

## GetWorksheetComment API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### **セキュリティと認証**

Aspose.Cells Cloud API はセキュアであり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名   | 型     | 位置 (URL パス / クエリ文字列) | 説明                                                         |
| -------------- | ------ | ----------------------------- | ------------------------------------------------------------ |
| name           | 文字列 | URL パス                      | Excel ファイルの名前。                                        |
| sheetName      | 文字列 | URL パス                      | コメントを含むワークシートの名前。                            |
| cellName       | 文字列 | URL パス                      | コメントを取得するセルのアドレス (例: **A1**)。               |
| folder         | 文字列 | クエリ文字列                  | ドキュメントが保存されているフォルダのパス。                  |
| storageName    | 文字列 | クエリ文字列                  | ストレージサービスの名前。                                    |

<a href="https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetComment" rel="noopener noreferrer">OpenAPI スペック</a> はパブリックにアクセス可能なプログラミングインターフェースを定義し、ウェブブラウザから直接 REST 操作を実行できるようにします。

cURL コマンドラインツールを使用して、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/A1" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Comment": {
    "CellName": "A1",
    "Author": "roy.wang",
    "HtmlNote": "",
    "Note": "Aspose.Cells Cloud.",
    "AutoSize": "True",
    "IsVisible": "True",
    "Width": 30,
    "Height": 10,
    "TextHorizontalAlignment": "Bottom",
    "TextOrientationType": "TopToBottom",
    "TextVerticalAlignment": "Bottom"
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**応答:** API は `Comment` オブジェクトを含む JSON オブジェクトを返します。このオブジェクトには以下のフィールドがあります。

| フィールド                   | 型      | 説明                                               |
| --------------------------- | ------- | -------------------------------------------------- |
| `CellName`                  | 文字列  | セルのアドレス (例: **A1**)。                       |
| `Author`                    | 文字列  | コメントの作成者名。                                |
| `HtmlNote`                  | 文字列  | HTML 形式のコメント内容 (ある場合)。                |
| `Note`                      | 文字列  | プレーンテキスト形式のコメント内容。                |
| `AutoSize`                  | 真偽値  | コメントボックスが自動的にサイズ変更されるかどうかを示します。 |
| `IsVisible`                 | 真偽値  | コメントが表示されているかどうかを判定します。      |
| `Width`                     | 整数    | コメントボックスの幅 (文字数単位)。                 |
| `Height`                    | 整数    | コメントボックスの高さ (文字数単位)。               |
| `TextHorizontalAlignment`   | 文字列  | テキストの水平方向の配置 (例: **Bottom**)。         |
| `TextOrientationType`       | 文字列  | テキストの向き (例: **TopToBottom**)。              |
| `TextVerticalAlignment`     | 文字列  | テキストの垂直方向の配置 (例: **Bottom**)。         |

## 共通エラー

- **401 Unauthorized（未承認）** – JWT トークンが有効で、期限切れでなく、かつ `Authorization` ヘッダーに正しく設定されていることを確認してください。
- **404 Not Found（見つかりません）** – ファイル名、ワークシート名、セルアドレスが正しいこと、およびファイルが指定されたフォルダ/ストレージに存在することを確認してください。
- **500 Internal Server Error（内部サーバーエラー）** – リクエストペイロードのデータが不正でないか確認し、サービスが正常に動作していることを確認してください。

**HTTP ステータスコード**

| コード | 意味                     | 説明                                             |
|------|--------------------------|--------------------------------------------------|
| 200  | OK                       | フィルターが正常に適用され、応答に操作の詳細が含まれます。 |
| 400  | Bad Request（不正なリクエスト） | パラメータが不足または無効 (例: サポートされていないファイル形式)。 |
| 401  | Unauthorized（未承認）   | JWT トークンが無効または不足しています。           |
| 413  | Payload Too Large（ペイロードが大きすぎます） | アップロードされたファイルがサイズ制限を超えています。 |
| 500  | Internal Server Error（内部サーバーエラー） | 予期しないサーバーエラーが発生しました。             |

## Cloud SDK ファミリー

SDK を使用することは、開発を高速化する最良の方法です。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストについては、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a> を確認してください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetComments.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetComments.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetComments.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetComments.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetComments.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetComments.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetComments.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetComments.go" >}}

{{< /tab >}}

{{< /tabs >}}