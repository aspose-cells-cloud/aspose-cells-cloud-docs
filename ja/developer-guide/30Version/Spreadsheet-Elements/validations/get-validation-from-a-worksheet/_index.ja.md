---
title: "Excelワークシートからインデックスで検証ルールを取得する"
second_title: "Document"
linktitle: "Get"
type: docs
url: /ja/validations/get/
aliases: [  /ja/get-validation-from-a-worksheet/ ]
keywords: "Aspose.Cells Cloud, ワークシート検証API, インデックスで検証ルールを取得, Excel REST API, Aspose.Cells SDK"
description: "Aspose.Cells Cloud API（v3.0）を使用して、Excelワークブック内のワークシートからゼロベースのインデックスで検証ルールを取得します。cURLの例、レスポンススキーマ、エラーコード、C#、Java、Pythonなど複数の言語向けSDKスニペットを含みます。"
weight: 10
---

このREST APIは、Excelワークシート内の検証ルールをインデックスで取得します。  
エンドポイントを呼び出す前に、`/connect/token`エンドポイントを通じてJWTトークンを取得し、`Authorization`ヘッダーに`Bearer <jwt token>`として含めてください。

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations/{validationIndex}
```

### **リクエストパラメータ**

| パラメータ名       | 型      | 位置   | 説明                                           |
| ------------------ | ------- | ------ | ---------------------------------------------- |
| name               | string  | path   | ワークブックファイルの名前。                   |
| sheetName          | string  | path   | ワークシートの名前。                           |
| validationIndex    | integer | path   | 取得する検証ルールのゼロベースインデックス。   |
| folder             | string  | query  | ワークブックが格納されているフォルダー。       |
| storageName        | string  | query  | ストレージサービスの名前。                     |

[OpenAPI仕様書](https://apireference.aspose.cloud/cells/#/WorksheetValidations/GetWorksheetValidation)では、パブリックに利用可能なプログラミングインタフェースを定義しており、ウェブブラウザーから直接REST通信を実行できます。

cURLコマンドラインツールを使用すると、Aspose.Cellsウェブサービスに簡単にアクセスできます。以下の例は、cURLでAPIを呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Validation": {
    "AlertStyle": "Stop",
    "AreaList": [
      {
        "EndColumn": 0,
        "EndRow": 0,
        "StartColumn": 0,
        "StartRow": 0
      },
      {
        "EndColumn": 27,
        "EndRow": 0,
        "StartColumn": 26,
        "StartRow": 0
      }
    ],
    "IgnoreBlank": false,
    "InCellDropDown": false,
    "Operator": "None",
    "ShowError": false,
    "ShowInput": false,
    "Type": "AnyValue",
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/Validations/0",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**レスポンススキーマ**

| フィールド       | 型      | 説明                                                                 |
| --------------- | ------- | ------------------------------------------------------------------- |
| AlertStyle      | string  | ユーザーに表示されるアラートのスタイル（Stop、Warning、Information）。 |
| AreaList        | array   | 検証が適用されるセル範囲のコレクション。                            |
| IgnoreBlank     | boolean | `true`の場合、検証時に空白セルを無視します。                         |
| InCellDropDown  | boolean | `true`の場合、セル内にドロップダウンリストが表示されます。            |
| Operator        | string  | 検証で使用される比較演算子（例：`None`、`Between`など）。            |
| ShowError       | boolean | 検証失敗時にエラーメッセージを表示するかどうかを指定します。         |
| ShowInput       | boolean | セルが選択されたときに入力メッセージを表示するかどうかを指定します。   |
| Type            | string  | 検証の種類（例：`AnyValue`、`WholeNumber`、`Decimal`など）。         |
| link.Href       | string  | 検証リソースへの自己参照URL。                                        |
| link.Rel        | string  | 関係タイプ（常に`self`）。                                           |

**発生し得るエラーコード**

| HTTPステータス | 意味                                                            |
| -------------- | -------------------------------------------------------------- |
| 200            | 検証ルールの取得に成功しました。                                |
| 400            | 不正なリクエスト – パラメータが不足しているか、無効です。       |
| 401            | 認証エラー – JWTトークンが無効または不足しています。            |
| 404            | 見つかりません – ワークブック、ワークシート、または検証インデックスが存在しません。 |
| 500            | サーバー内部エラー – 予期しない条件が発生しました。             |

## Cloud SDK Family

SDKを使用すると、Aspose.Cells Cloudに対する開発を最速で行えます。SDKは低レベルの詳細を抽象化し、ビジネスロジックに集中できるようにします。Aspose.Cells Cloud SDKの完全な一覧は[GitHubリポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまなSDKを使用してAspose.Cellsウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}

---