---
title: "すべてのワークシート検証を削除する – Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktitle: "削除"
type: docs
url: /ja/validations/clear/
keywords: "Aspose.Cells Cloud、ワークシート検証の削除、Excel、REST API、スプレッドシート検証、API"
description: "Aspose.Cells Cloud REST API を使用して、Excel ファイル内のワークシートからすべてのデータ検証ルールを削除します。認証手順、リクエストの詳細、cURL の使用例、レスポンススキーマ、エラーハンドリング、SDK スニペットを含みます。"
weight: 10
---

**前提条件**

- 有効な Aspose Cloud アカウント。
- Aspose Cloud 認証 API（`/connect/token`）を通じて取得した JWT アクセストークン。
- ワークブックは Aspose Cloud ストレージ内に格納されている必要があります（または、適切な `folder`／`storageName` クエリパラメータを指定する必要があります）。

この REST API は、Excel ワークシート上のすべてのワークシート検証を削除します。

## REST API

```bash
DELETE http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations
```

### **リクエストパラメータ**

| パラメータ名   | 型     | 位置   | 説明                                     |
| -------------- | ------ | ------ | ----------------------------------------- |
| name           | string | path   | Excel ドキュメントの名前。                |
| sheetName      | string | path   | 検証を含むワークシートの名前。            |
| folder         | string | query  | ドキュメントが格納されているフォルダ。    |
| storageName    | string | query  | ストレージサービスの名前。                |

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/WorksheetValidations/DeleteWorksheetValidation) は、パブリックにアクセス可能なプログラミングインタフェースを定義し、Web ブラウザから直接 REST 操作を実行できるようにします。

cURL コマンドラインツールを使用すると、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、JWT トークンを取得した後に cURL を使用して API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations" \
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

### エラーハンドリング

| HTTP ステータス | 意味                 | 説明                                         |
| --------------- | -------------------- | --------------------------------------------- |
| 400             | Bad Request（Bad Request）    | リクエストが不正な形式であるか、必須パラメータが不足しています。 |
| 401             | Unauthorized（Unauthorized）  | JWT トークンが欠落している、無効である、または期限切れです。 |
| 404             | Not Found（Not Found）        | 指定されたワークブックまたはワークシートが存在しません。 |
| 500             | Internal Server Error（Internal Server Error） | サーバー側で予期せぬエラーが発生しました。 |

エラーペイロードは、`Code` および `Message` フィールドを含む同じ JSON 構造に従います。例：

```json
{
  "Code": 401,
  "Message": "Invalid or expired token."
}
```

## Cloud SDK ファミリー

SDK を使用すると、開発が最速で行えます。SDK は低レベルの詳細を抽象化し、ビジネスロジックの開発に集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) を確認してください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetValidations.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetValidations.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetValidations.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetValidations.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetValidations.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetValidations.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetValidations.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetValidations.go" >}}

{{< /tab >}}

{{< /tabs >}}