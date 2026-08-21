---
title: "ワークシートからセルのスタイルを取得する – Aspose.Cells Cloud API"
type: docs
url: /ja/get-cell-style-from-a-worksheet/
weight: 10
keywords: "Aspose.Cells, Excel, REST API, セルのスタイル, スプレッドシート, クラウド SDK, API ドキュメント"
description: "Aspose.Cells Cloud REST API v3 を使用して、Excel ワークシート内の特定のセルのスタイルを取得する方法を学びます。cURL の例、レスポンススキーマ、ステータスコード、SDK スニペットを含みます。"
ArticleTitle: "Aspose.Cells Cloud API を使用してワークシートからセルのスタイルを取得する – 詳細ガイド"
---

この REST API を使用して、Excel ワークシート内のセルの**スタイル**を取得します。

## GetWorksheetCellStyle API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/style
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ


| パラメータ名     | タイプ   | 位置   | 説明                              |
| -------------- | ------ | ----- | --------------------------------- |
| name           | string | path  | Excel ドキュメントの名前です。       |
| sheetName      | string | path  | ワークシートの名前です。            |
| cellName       | string | path  | セルのアドレスです（例: A1）。       |
| folder         | string | query | ファイルを含むフォルダーです。       |
| storageName    | string | query | 使用するストレージの名前です。       |


### **レスポンス**

```json
{
  "Style": {
    "Font": {
      "Color": { "A": 255, "R": 5, "G": 99, "B": 193 },
      "DoubleSize": 11,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Calibri",
      "Size": 11,
      "Underline": "Single"
    },
    "Name": null,
    "CultureCustom": "General",
    "Custom": "",
    "BackgroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "ForegroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "IsFormulaHidden": false,
    "IsDateTime": false,
    "IsTextWrapped": false,
    "IsGradient": false,
    "IsLocked": true,
    "IsPercent": false,
    "ShrinkToFit": false,
    "IndentLevel": 0,
    "Number": 0,
    "RotationAngle": 0,
    "Pattern": "None",
    "TextDirection": "Context",
    "VerticalAlignment": "Bottom",
    "HorizontalAlignment": "General",
    "BorderCollection": [
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "BottomBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalDown"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalUp"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Horizontal"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "LeftBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "RightBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "TopBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Vertical"
      }
    ],
    "BackgroundThemeColor": null,
    "ForegroundThemeColor": null,
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/cells/a1/style",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

**HTTP ステータスコード**

| コード | 意味                      | 説明                                             |
|------|---------------------------|--------------------------------------------------|
| 200  | OK                        | フィルターが正常に適用された。レスポンスには操作の詳細が含まれます。 |
| 400  | Bad Request               | パラメータが不足している、または無効です（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized              | JWT トークンが無効または不足しています。          |
| 413  | Payload Too Large         | アップロードされたファイルがサイズ制限を超えています。 |
| 500  | Internal Server Error     | 予期しないサーバーエラーが発生しました。          |

**エラーレスポンス**  
このエンドポイントの典型的なエラーペイロードは、標準の Aspose.Cells エラー形式に従います。たとえば、400 Bad Request の場合は以下のようになります：

```json
{
  "Code": 400,
  "Message": "Invalid parameter 'cellName'.",
  "Description": "The cell name provided is not in a valid A1 format."
}
```

同様に、401 Unauthorized の場合は以下のようになります：

```json
{
  "Code": 401,
  "Message": "Authentication failed.",
  "Description": "The JWT token is missing or invalid."
}
```

## SDK を使用した GetWorksheetCellStyle API の使用方法

### GetWorksheetCellStyle API 仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCellStyle) は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST アクセスを実行できるようにします。

cURL コマンドラインツールを使用して、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/a1/style" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Style": {
    "Font": {
      "Color": { "A": 255, "R": 5, "G": 99, "B": 193 },
      "DoubleSize": 11,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Calibri",
      "Size": 11,
      "Underline": "Single"
    },
    "Name": null,
    "CultureCustom": "General",
    "Custom": "",
    "BackgroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "ForegroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "IsFormulaHidden": false,
    "IsDateTime": false,
    "IsTextWrapped": false,
    "IsGradient": false,
    "IsLocked": true,
    "IsPercent": false,
    "ShrinkToFit": false,
    "IndentLevel": 0,
    "Number": 0,
    "RotationAngle": 0,
    "Pattern": "None",
    "TextDirection": "Context",
    "VerticalAlignment": "Bottom",
    "HorizontalAlignment": "General",
    "BorderCollection": [
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "BottomBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalDown"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalUp"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Horizontal"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "LeftBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "RightBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "TopBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Vertical"
      }
    ],
    "BackgroundThemeColor": null,
    "ForegroundThemeColor": null,
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/cells/a1/style",
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

## レスポンススキーマ

| フィールド                  | タイプ    | 説明                                                                   |
| ------------------------ | ------- | --------------------------------------------------------------------- |
| **Style**                | object  | セルのすべてのスタイル関連プロパティを含むコンテナです。                    |
| Style.Font               | object  | フォント設定（名前、サイズ、色、スタイルフラグ）です。                      |
| Style.Font.Color         | object  | フォントの RGBA 色値です。                                              |
| Style.Font.IsBold        | boolean | フォントが太字の場合に `true` です。                                      |
| Style.Font.IsItalic      | boolean | フォントが斜体の場合に `true` です。                                      |
| Style.Font.IsStrikeout   | boolean | フォントに取り消し線が適用されている場合に `true` です。                    |
| Style.Font.IsSubscript   | boolean | フォントが下付き文字の場合に `true` です。                                |
| Style.Font.IsSuperscript | boolean | フォントが上付き文字の場合に `true` です。                                |
| Style.Font.Name          | string  | フォントファミリー名（例: **Calibri**）です。                             |
| Style.Font.Size          | number  | フォントサイズ（ポイント単位）です。                                      |
| Style.Font.Underline     | string  | 下線スタイル（例: **Single**）です。                                      |
| Style.IsLocked           | boolean | セルが編集から保護されているかどうかを示します。                           |
| Style.IsTextWrapped      | boolean | テキストの折り返しが有効な場合に `true` です。                            |
| Style.IsGradient         | boolean | グラデーション塗りつぶしが適用されている場合に `true` です。               |
| Style.Pattern            | string  | 塗りつぶしパターン名（例: **None**）です。                                |
| Style.BorderCollection   | array   | 線のスタイル、色、境界線タイプを定義する境界線オブジェクトのリストです。       |
| Style.BackgroundColor    | object  | セルの背景色の RGBA 値です。                                             |
| Style.ForegroundColor    | object  | セルの前景色の RGBA 値です。                                             |
| …                        | …       | _（その他のフィールドは API リファレンスで定義されたパターンに従います。）_ |

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、開発をスピードアップできます。SDK は低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全なリストについては、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) を確認してください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCellStyle.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCellStyle.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCellStyle.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCellStyle.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCellStyle.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCellStyle.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCellStyle.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCellStyle.go" >}}

{{< /tab >}}

{{< /tabs >}}

**関連項目**  
- [セルのスタイルを設定する](https://apireference.aspose.cloud/cells/#/Cells/SetWorksheetCellStyle)  
- [セルの値を取得する](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell)
---