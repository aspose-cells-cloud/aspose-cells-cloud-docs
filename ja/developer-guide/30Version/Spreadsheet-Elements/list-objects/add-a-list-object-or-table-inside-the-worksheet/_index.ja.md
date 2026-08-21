---
title: "Excelワークシートにリストオブジェクト（表）を追加する"
second_title: "Document"
linktitle: "Add"
type: docs
url: /ja/list-objects/add/
aliases: [  /ja/add-a-list-object-or-table-inside-the-worksheet/ , /ja/tables/add/ ]
keywords: "Aspose.Cells Cloud, Excel API, リストオブジェクト, テーブル, REST API, ワークシート"
description: "Aspose.Cells Cloud REST API を使用して、ワークシートにリストオブジェクト（Excel表）を追加する方法を学びます。エンドポイント、パラメーター、認証手順、cURLの例、SDKコードサンプルを含みます。"
weight: 10
ArticleTitle: "Excelワークシートにリストオブジェクト（表）を追加する – Aspose.Cells Cloud ドキュメント"
---

この REST API は、Excelワークシートに**リストオブジェクト（表）**を追加します。

このエンドポイントを使用する前に、有効なJWTトークンが取得できていること、ワークブックが対応するクラウドストレージに保存されていること、およびワークシートが存在することを確認してください。

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects
```

### リクエストパラメーター

| パラメーター名  | 型      | 位置   | 説明                                                                 |
| --------------- | ------- | ------ | ------------------------------------------------------------------- |
| **name**        | 文字列  | パス   | ワークブックのファイル名。                                           |
| **sheetName**   | 文字列  | パス   | ワークシート名。                                                     |
| **startRow**    | 整数    | クエリ | テーブル範囲の最初の行の0始まりのインデックス。                       |
| **startColumn** | 整数    | クエリ | テーブル範囲の最初の列の0始まりのインデックス。                       |
| **endRow**      | 整数    | クエリ | テーブル範囲の最後の行の0始まりのインデックス。                       |
| **endColumn**   | 整数    | クエリ | テーブル範囲の最後の列の0始まりのインデックス。                       |
| **hasHeaders**  | 真偽値  | クエリ | 最初の行に列見出しが含まれている場合は `true`、それ以外は `false`。   |
| **listObject**  | オブジェクト | 本文 | リストオブジェクトの定義（**リクエスト本文のスキーマ**を参照）。     |
| **folder**      | 文字列  | クエリ | ワークブックが格納されているフォルダー。                             |
| **storageName** | 文字列  | クエリ | ストレージ名。                                                       |

### リクエスト本文のスキーマ

**listObject** オブジェクトは、作成される表を記述します。最も一般的なプロパティのみを示しています。完全なリストについては、OpenAPI仕様を参照してください。

```json
{
  "displayName": "MyTable",
  "showTotals": false,
  "style": "TableStyleMedium2"
}
```

### 例：リクエスト（cURL）

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects?startRow=1&startColumn=1&endRow=10&endColumn=12&hasHeaders=true" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "displayName": "MyTable",
        "showTotals": false,
        "style": "TableStyleMedium2"
      }'
```

### 例：レスポンス

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### エラーコード

| HTTPステータス | 理由                  | 説明                                             |
| -------------- | --------------------- | ------------------------------------------------ |
| **400**        | Bad Request           | 範囲パラメーターが無効、またはJSON本文が不正です。 |
| **401**        | Unauthorized          | JWTトークンが欠落しているか、期限切れです。        |
| **404**        | Not Found             | 指定されたワークブックまたはワークシートが存在しません。 |
| **500**        | Internal Server Error | サーバー側で予期しないエラーが発生しました。       |

**400エラーの例：レスポンス**

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "Invalid range parameters."
}
```

**401エラーの例：レスポンス**

```json
{
  "Code": 401,
  "Status": "Unauthorized",
  "Message": "Authentication token is missing or expired."
}
```

この操作の完全な仕様については、[OpenAPI仕様](https://apireference.aspose.cloud/cells/#/ListObjects/PutWorksheetListObject)を参照してください。

## Cloud SDK Family

SDK を使用すると、開発を最速で進めることができます。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストについては、[GitHubリポジトリ](https://github.com/aspose-cells-cloud)をご覧ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetListObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetListObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetListObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetListObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetListObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetListObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetListObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetListObject.go" >}}

{{< /tab >}}

{{< /tabs >}}
---