---
title: "Excelワークシート内のすべての画像を削除する"
second_title: "Document"
linktitle: "クリア"
type: docs
url: /ja/pictures/clear/
aliases: [  /ja/delete-all-pictures-from-excel-worksheet/ ]
keywords: "Aspose.Cells Cloud, Excel, すべての画像を削除, ワークシート, REST API, 画像をクリア"
description: "Aspose.Cells Cloud REST APIを使用してExcelワークシートからすべての画像を削除する方法をcURLおよびSDKの例で学びます。"
weight: 60
ArticleTitle: "Aspose.Cells Cloudを使用してExcelワークシートのすべての画像を削除する方法"
---

このREST APIは、ワークシート内の**すべての**画像を削除します。

**前提条件**  
- 有効なOAuth 2.0アクセストークンを持つ、アクティブなAspose.Cells Cloudアカウント。  
- APIバージョン3.0以上が必要です（それ以前のバージョンは非推奨です）。  
- 対象のExcelファイルは、サポートされているストレージ場所（デフォルトまたはカスタム）に保存されている必要があります。

**バージョン互換性**  
エンドポイントはCells Cloud 3.0 API仕様に準拠しています。クライアントライブラリおよびリクエストURLが`api.aspose.cloud/v3.0`を対象としていることを確認してください。

## DeleteWorksheetPictures API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures
```

### **セキュリティと認証**

Aspose.Cells Cloud APIは安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWTトークンベースの認証</a>が必要です。

### **リクエストパラメータ**

| パラメータ名 | 型     | 位置   | 説明                                      |
| ------------ | ------ | ------ | ----------------------------------------- |
| name         | 文字列 | Path   | Excelファイルの名前。                      |
| sheetName    | 文字列 | Path   | 画像を含むワークシートの名前。              |
| folder       | 文字列 | Query  | ファイルが保存されているフォルダ。          |
| storageName  | 文字列 | Query  | ストレージサービスの名前。                  |

### エラー応答

| HTTPコード | 説明                                                                      |
| ---------- | ------------------------------------------------------------------------- |
| 401        | 認証エラー – トークンが不足している、または無効です。                      |
| 404        | 見つかりません – 指定されたファイル、ワークシート、またはページ区切りインデックスが存在しません。 |
| 400        | 不正リクエスト – リクエスト構文が不正、またはパラメータが無効です。        |
| 500        | サーバー内部エラー – 予期せぬ状態が発生しました。                          |

[OpenAPI仕様](https://apireference.aspose.cloud/cells/#/Pictures/DeleteWorksheetPictures)はパブリックにアクセス可能なプログラミングインターフェースを定義し、Webブラウザから直接REST操作を実行できるようにします。

cURLコマンドラインツールを使用して、Aspose.Cells Webサービスに簡単にアクセスできます。以下の例は、cURLでAPIを呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/pictures" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## クラウドSDKファミリー

SDKを使用すると、開発を最速で行えます。SDKが低レベルの詳細を処理するため、ビジネスロジックに集中できます。Aspose.Cells Cloud SDKの完全な一覧は[GitHubリポジトリ](https://github.com/aspose-cells-cloud)をご覧ください。

以下のコード例は、さまざまなSDKを使用してAspose.Cells Webサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetPictures.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetPictures.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetPictures.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetPictures.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetPictures.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetPictures.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetPictures.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetPictures.go" >}}

{{< /tab >}}

{{< /tabs >}}

**注意:** DELETE操作はページネーションをサポートせず、Aspose.Cells Cloud APIの標準レート制限（デフォルトでは1分あたり100リクエスト）の対象となります。クライアントのロジックを適切に調整してください。

**関連項目**:  
- [/pictures/delete/](../delete/) – ワークシートから特定の画像を削除します。  
- [/pictures/add/](../add/) – ワークシートに画像を追加します。  
---