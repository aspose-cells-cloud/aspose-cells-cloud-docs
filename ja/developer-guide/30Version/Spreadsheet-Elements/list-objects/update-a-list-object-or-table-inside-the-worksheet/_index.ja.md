---
title: "Excelワークシート内のリストオブジェクトを更新する"
ArticleTitle: "Excelワークシート内のリストオブジェクトを更新する – Aspose.Cells Cloud API ドキュメント"
second_title: "ドキュメント"
linktype: "docs"
url: /ja/list-objects/update/
aliases:
  - /update-a-list-object-or-table-inside-the-worksheet/
  - /tables/update/
keywords: "Aspose.Cells, ListObject, テーブル更新, Excel API, REST, クラウドSDK, リストオブジェクト更新, Excelワークシート, テーブル"
description: "Aspose.Cells Cloud API（v3.0）を使用してExcelテーブルを更新する方法を学びます。エンドポイント、パラメータ、サンプルcURL、エラーコード、SDKの使用例を含みます。"
weight: 20
---

このREST APIは、Excelワークシート内の**リストオブジェクト**（テーブル）のプロパティを更新します。

## セキュリティと認証

Aspose.Cells Cloud APIは安全であり、[JWTトークンベースの認証](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)が必要です。

## リクエストボディのスキーマ

`listObject` DTOは以下のフィールドを含みます。リクエストボディには、変更したいフィールドのみを含める必要があります。

| フィールド                                         | 型                 | 必須     | 説明                                                                     |
| ------------------------------------------------- | ------------------ | -------- | ------------------------------------------------------------------------ |
| **DisplayName**                                   | string             | 任意     | テーブルに表示される名前。                                               |
| **StartRow** / **StartColumn**                    | integer            | 任意     | テーブルの最初の行/列の0始まりのインデックス。                           |
| **EndRow** / **EndColumn**                        | integer            | 任意     | テーブルの最後の行/列の0始まりのインデックス。                           |
| **Range**                                         | string             | 任意     | テーブル範囲を定義するA1形式のアドレス（例: `A1:D10`）。                 |
| **ShowHeaderRow**                                 | boolean            | 任意     | ヘッダー行を表示するかどうか（`true`で表示）。                           |
| **ShowTotals**                                    | boolean            | 任意     | 合計行を表示するかどうか（`true`で表示）。                               |
| **TableStyleName**                                | string             | 任意     | 適用する組み込みテーブルスタイルの名前。                                 |
| **TableStyleType**                                | string             | 任意     | スタイルの種類（`TableStyleLight`、`TableStyleMedium` など）。           |
| **ListColumns**                                   | objectの配列       | 任意     | 列定義のコレクション（`Name`、`TotalsCalculation`など）。               |
| **Sorter**、**AutoFilter**、**ShowTableStyle…**  | object             | 任意     | 詳細なスタイリングおよびフィルタリングオプション（OpenAPI仕様を参照）。 |

### 最小限のペイロード例

```json
{
  "DisplayName": "SalesData",
  "Range": "A1:E20",
  "ShowHeaderRow": true,
  "ShowTotals": false
}
```

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}
```

### **リクエストパラメータ**

| パラメータ名        | 型      | 位置   | 説明                                     |
| ------------------- | ------- | ------ | ---------------------------------------- |
| **name**            | string  | path   | ドキュメント名。                         |
| **sheetName**       | string  | path   | ワークシート名。                         |
| **listObjectIndex** | integer | path   | 更新するリストオブジェクトのインデックス。 |
| **listObject**      | object  | body   | リクエストボディ内のListObject DTO。    |
| **folder**          | string  | query  | ドキュメントを含むフォルダ。             |
| **storageName**     | string  | query  | ストレージ名。                           |

[OpenAPI仕様](https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObject)は、パブリックに利用可能なプログラミングインターフェースを定義し、ウェブブラウザから直接RESTによるやり取りを実行できるようにします。

### リクエスト

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet7/listobjects/0" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
    "DisplayName": "SalesData",
    "Range": "A1:E20",
    "ShowHeaderRow": true,
    "ShowTotals": false,
    "ListColumns": [
      { "Name": "Product", "TotalsCalculation": "None" },
      { "Name": "Quantity", "TotalsCalculation": "Sum" },
      { "Name": "Price", "TotalsCalculation": "Average" }
    ]
  }'
```

{{< /tab >}}

### 応答

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

成功した応答には以下のフィールドが含まれます：

| フィールド                  | 型     | 説明                                     |
| -------------------------- | ------ | ---------------------------------------- |
| **Code**                   | integer| HTTPステータスコード（成功時は200）。    |
| **Status**                 | string | ステータスのテキストによる説明。         |
| **UpdatedObject**（任意） | object | 更新された`ListObject`の表現（変更されたプロパティを含む）。 |

{{< /tab >}}

{{< /tabs >}}

## エラーレスポンス

| HTTPコード | 説明                                                                       | サンプルペイロード                                     |
| ---------- | -------------------------------------------------------------------------- | ------------------------------------------------------ |
| **400**    | 不正リクエスト — 必須フィールドの不足または不正なJSON形式。               | `{ "Code": 400, "Message": "Invalid request body." }`  |
| **401**    | 認証失敗 — JWTトークンが不足しているか、無効です。                         | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404**    | 見つかりません — 指定されたワークブック、ワークシート、またはリストオブジェクトが存在しません。 | `{ "Code": 404, "Message": "Resource not found." }`    |
| **500**    | サーバー内部エラー — サーバー側で予期せぬ状況が発生しました。             | `{ "Code": 500, "Message": "Server error." }`          |

## よくある質問（FAQ）

<details>  
<summary>Aspose.Cells Cloud APIを使用してリストオブジェクトを更新するにはどうすればよいですか？</summary>

`POST /cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}`エンドポイントを使用します。リクエストボディに変更したいプロパティ（例: `DisplayName`、`ShowHeaderRow`など）を含めたJSONを含めて送信してください。`Authorization`ヘッダーにJWTトークンを設定して認証を行います。

</details>

<details>  
<summary>更新が成功した場合、どのような応答が返されますか？</summary>

`Code: 200` および `Status: "OK"` を含むJSONオブジェクトが返されます。エラーが発生した場合は、適切なHTTPステータスコードと、問題を説明する`Error`オブジェクトが含まれます。

</details>

<details>  
<summary>リストオブジェクトのプロパティの一部のみを更新することは可能ですか？</summary>

はい、可能です。リクエストボディに変更したいフィールドのみを含めることで、省略されたフィールドは変更されません。

</details>

## 関連ドキュメント

- [リストオブジェクトを追加する](https://docs.aspose.cloud/cells/list-objects/add/)
- [リストオブジェクトを取得する](https://docs.aspose.cloud/cells/list-objects/get/)
- [リストオブジェクトを削除する](https://docs.aspose.cloud/cells/list-objects/delete/)

## クラウドSDKファミリー

SDKを使用することで、開発を最適化できます。SDKは低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDKの完全な一覧は[GitHubリポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、 various SDKを使用してAspose.Cells Webサービスを呼び出す方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObject.go" >}}

{{< /tab >}}

{{< /tabs >}}