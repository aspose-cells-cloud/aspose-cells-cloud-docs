---
title: "ワークシートのセルコメントを更新する"
type: docs
url: /ja/comments/update/
aliases: [  /ja/update-a-comment-in-excel-workbook/ ]
keywords: "Aspose.Cells Cloud, REST API, Excel, ワークシート, セルコメント, ワークシートコメントの更新, コメントオブジェクト"
description: "Aspose.Cells Cloud REST API を使用して Excel ブック内のワークシートのセルに含まれるコメントを更新します。リクエストの詳細、レスポンスコード、SDK の使用例を含みます。"
weight: 30
ArticleTitle: "ワークシートのセルコメントを更新 – Aspose.Cells Cloud API"
---

この REST API は、ワークシート内のセルに付加されたコメントを更新します。このエンドポイントを使用して、Excel ファイル内のワークシートコメントを更新してください。

**前提条件:**  
- `Authorization` ヘッダーに有効な OAuth/JWT アクセストークンを含める必要があります。  
- ブックは、サポートされているクラウドストレージの場所に保存されている必要があります（`folder` およびオプションで `storageName` を指定してください）。

## PostWorksheetComment API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を要求します。

### リクエストパラメーター

| パラメーター名 | 型     | 位置   | 説明                                                                 |
| -------------- | ------ | ------ | ------------------------------------------------------------------- |
| name           | 文字列 | path   | Excel ドキュメントの名前。                                          |
| sheetName      | 文字列 | path   | セルを含むワークシートの名前。                                      |
| cellName       | 文字列 | path   | セルのアドレス（例: **A1**）。                                      |
| comment        | オブジェクト | body | 追加または更新するコメントを定義する **Comment** オブジェクト。      |
| folder         | 文字列 | query  | ドキュメントが保存されているフォルダー。                            |
| storageName    | 文字列 | query  | ストレージサービスの名前。                                          |

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetComment) はパブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST による操作を実行できるようにします。

**cURL** コマンドラインツールを使用して、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例では、cURL を使用して Cloud API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/a1" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "CellName": "a1",
        "Author": "test",
        "HtmlNote": "string",
        "Note": "this is a comment",
        "AutoSize": true,
        "IsVisible": true,
        "Width": 10,
        "Height": 10
      }'
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

可能なレスポンスステータスコード:

| コード | 説明                                       |
|------|-------------------------------------------|
| 200  | コメントが正常に更新されました。           |
| 400  | 不正なリクエスト – 必須パラメーターが不足しているか、無効です。 |
| 401  | 認証エラー – 認証に失敗しました。         |
| 404  | 見つかりません – ブック、ワークシート、またはコメントが存在しません。 |
| 500  | サーバー内部エラー。                       |

**注意 / ヒント:**  
- コメントの最大文字数は 1024 文字です。  
- 使用可能な文字は UTF‑8 です。制御文字は避けてください。

## Cloud SDK ファミリー

SDK を使用すると、Aspose.Cells Cloud を使う開発を最速で行えます。SDK は低レベルの詳細処理を処理するため、プロジェクトの本質的な作業に集中できます。Aspose.Cells Cloud SDK の完全な一覧は <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a> をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetComment.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetComment.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetComment.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetComment.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetComment.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetComment.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetComment.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetComment.go" >}}

{{< /tab >}}

{{< /tabs >}}

関連する操作:  
- [ワークシートコメントを取得する](/comments/get/)  
- [ワークシートコメントを追加する](/comments/add/)  
- [ワークシートコメントを削除する](/comments/delete/)