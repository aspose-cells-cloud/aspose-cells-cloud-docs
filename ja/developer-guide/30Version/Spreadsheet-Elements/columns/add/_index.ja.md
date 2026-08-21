---
title: "Excelワークシートに空の列を追加する - Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktitle: "追加"
type: docs
url: /ja/columns/add/
aliases:
  - /add-an-empty-column-in-an-excel-worksheet/
  - /add-an-empty-column-in-a-worksheet/
keywords: "追加, 列, Excel, API, Aspose.Cells, Cloud, REST, 挿入"
description: "Aspose.Cells Cloud REST API を使って Excel シートに新しい列を挿入する方法を学びます。リクエスト構文、cURL の例、および SDK のコードサンプルを含みます。"
weight: 20
ArticleTitle: "Aspose.Cells Cloud API を使用して Excel ワークシートに空の列を追加する"
---

この REST API は、ワークシートに 1 つまたは複数の列を挿入します。

**前提条件**  
このエンドポイントを呼び出す前に、以下の手順を完了していることを確認してください。

- 有効な OAuth 2.0 アクセストークンを取得し、それを `Authorization` ヘッダーに含めます。
- 対象のワークブックを選択したストレージ（デフォルト = “Default”）に保存するか、適切な `folder` および `storageName` パラメーターを指定します。
- `sheetName` で指定されたワークシート名が、ワークブック内に存在することを確認します。

## PutInsertWorksheetColumns API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}?totalColumns=1
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメーター

| パラメーター名      | 型      | 位置   | 説明                                                       |
| ------------------- | ------- | ------ | ---------------------------------------------------------- |
| **name**            | 文字列  | パス   | ワークブックのファイル名。                                 |
| **sheetName**       | 文字列  | パス   | ワークシートの名前。                                       |
| **columnIndex**     | 整数    | パス   | 挿入を開始する列の 0 から始まるインデックス。              |
| **totalColumns**    | 整数    | クエリ | 挿入する列数。                                             |
| **updateReference** | 真偽値  | クエリ | **true** の場合、挿入を反映するようにセル参照が更新されます。 |
| **folder**          | 文字列  | クエリ | ワークブックを含むフォルダーへのパス。                     |
| **storageName**     | 文字列  | クエリ | ストレージサービスの名前。                                 |

**注意事項**

- `columnIndex` は、0 からワークシート内の現在の列数未満の範囲内である必要があります。既存の範囲を超えて挿入すると、シートが自動的に拡張されます。  
- 複数の列（`totalColumns` > 1）を挿入すると、既存の列が右にシフトします。  
- `updateReference` フラグのデフォルトは `false` です。数式や名前付き範囲を更新するには `true` に設定してください。

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/Cells/PutInsertWorksheetColumns)は、パブリックに利用可能なプログラミングインターフェースを定義し、Web ブラウザーから直接 REST 通信を実行できるようにします。

cURL コマンドラインツールを使用して Aspose.Cells Web サービスを呼び出すことができます。以下の例では、認証および正しいパスパラメーターを含む完全なリクエストを示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/1?totalColumns=1&updateReference=true" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: application/json"
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

**レスポンスコード**

| コード | 説明                             |
|------|----------------------------------|
| 200  | 列が正常に挿入されました。       |
| 400  | 不正なリクエスト – パラメーターが不足または無効です。 |
| 401  | 認証エラー – トークンが無効または不足しています。     |
| 404  | ワークブックまたはワークシートが見つかりません。     |
| 500  | サーバー内部エラー。             |

**エラーレスポンスの例**

```json
// 400 Bad Request – パラメーターが不足または無効
{
  "Code": 400,
  "Message": "無効なパラメーター: totalColumns は正の整数である必要があります。"
}

// 401 Unauthorized – トークンが無効または不足
{
  "Code": 401,
  "Message": "認証に失敗しました。アクセストークンが不足しているか、無効です。"
}

// 404 Not Found – ワークブックまたはワークシートが存在しません
{
  "Code": 404,
  "Message": "ワークブック 'test.xlsx' が見つかりません。"
}

// 500 Internal Server Error
{
  "Code": 500,
  "Message": "サーバーで予期しないエラーが発生しました。"
}
```

## Cloud SDK ファミリー

SDK を使用すると、開発が最も迅速に行えます。SDK が低レベルの詳細を処理するため、プロジェクトのロジックに集中できます。Aspose.Cells Cloud SDK の完全な一覧は、<a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub リポジトリー</a>をご参照ください。

以下のコード例は、さまざまな SDK を使って Aspose.Cells Web サービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutInsertWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutInsertWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutInsertWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutInsertWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutInsertWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutInsertWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutInsertWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutInsertWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}