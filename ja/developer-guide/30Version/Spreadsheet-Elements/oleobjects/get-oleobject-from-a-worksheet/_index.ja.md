---
title: "ExcelワークシートからOLEオブジェクトを取得する – Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktitle: "取得"
type: docs
url: /ja/oleobjects/get/
aliases: [  /ja/get-oleobject-from-a-worksheet/ ]
keywords: "aspose, cells, ole object, excel, worksheet, get ole object, rest api"
description: "Aspose.Cells Cloud REST APIを使用して、ワークシートからOLEオブジェクト（画像、チャート、埋め込みファイル）を取得します。HTTPSエンドポイント、必要なパラメータ、cURLのサンプル、複数言語のSDKコードを含みます。"
ArticleTitle: "ExcelワークシートからOLEオブジェクトを取得する – Aspose.Cells Cloud API"
weight: 10
---

このREST APIは、Excelワークシートから**OLEオブジェクト**を取得します。

## セキュリティと認証
Aspose.Cells Cloud APIは安全であり、[JWTトークンベースの認証](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)を必要とします。

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}?format={format}
```

### リクエストパラメータ

| パラメータ名 | 型      | 位置   | 説明                                                 |
| ------------ | ------- | ------ | ----------------------------------------------------- |
| name         | 文字列  | パス   | ドキュメント名。                                      |
| sheetName    | 文字列  | パス   | ワークシート名。                                      |
| objectNumber | 整数    | パス   | ワークシート内のオブジェクト番号。                    |
| format       | 文字列  | クエリ | オブジェクトのエクスポート先として希望するフォーマット（例: `png`, `jpeg`）。 |
| folder       | 文字列  | クエリ | ドキュメントが格納されているフォルダ。                |
| storageName  | 文字列  | クエリ | 使用するストレージ名。                                |

### ストレージオプション

- **folder** – ワークブックが存在するデフォルトストレージ内のサブフォルダを指定します。
- **storageName** – ワークブックが他の場所に格納されている場合、デフォルトのストレージ名を上書きします。

[OpenAPI仕様](https://apireference.aspose.cloud/cells/#/OleObjects/GetWorksheetOleObject)は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Webブラウザから直接RESTインタラクションを実行できるようにします。

**cURL** コマンドラインツールを使用してAspose.Cellsウェブサービスを呼び出すことができます。以下の例では、OLEオブジェクトをPNG画像としてリクエストする方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

### バイナリ画像レスポンス

`format` を画像形式（例: `png`）に設定した場合、APIは以下のヘッダーとともにバイナリ画像データを返します：

```
Content-Type: image/png
```

_(画像ファイルはクライアントに直接ストリーミングされます。)_

### JSONメタデータレスポンス

`format` を省略した場合、または `json` を設定した場合、APIはOLEオブジェクトを記述するJSONペイロードを返します：

```json
{
  "Code": 200,
  "Status": "OK",
  "OLEObject": {
    "Name": "Object1",
    "Width": 200,
    "Height": 150,
    "Left": 10,
    "Top": 20,
    "IsLocked": false,
    "FileFormat": "png"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

## エラーレスポンス

| HTTPステータス | エラーコード   | 説明                               |
| -------------- | ------------ | ----------------------------------- |
| 400            | BadRequest   | パラメータが不足または無効です。    |
| 401            | Unauthorized | JWTトークンが無効または不足しています。 |
| 404            | NotFound     | ワークブック、ワークシート、またはOLEオブジェクトが見つかりません。 |
| 500            | ServerError  | 予期しないサーバーエラーです。      |

**404エラーレスポンスの例**

```json
{
  "Code": 404,
  "Status": "NotFound",
  "Message": "ワークシート 'Sheet1' 内で、番号0のOLEオブジェクトが見つかりませんでした。"
}
```

## クラウドSDKファミリー
SDKを使用すると、APIを統合する最も迅速な方法です。SDKは低レベルの詳細を処理するため、ビジネスロジックに集中できます。Aspose.Cells Cloud SDKの完全なリストは[GitHubリポジトリ](https://github.com/aspose-cells-cloud)をご覧ください。

以下のコード例は、さまざまなSDKを使用してAspose.Cellsウェブサービスを呼び出す方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}