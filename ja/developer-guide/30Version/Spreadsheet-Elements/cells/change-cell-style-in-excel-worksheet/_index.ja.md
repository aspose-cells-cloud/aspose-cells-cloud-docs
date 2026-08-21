---
title: "Excelワークシート内のセルスタイルを変更する"
type: docs
url: /change-cell-style-in-excel-worksheet/
weight: 30
keywords:
  - Aspose.Cells
  - Aspose.Cells Cloud
  - Excel
  - Cell Style（セルスタイル）
  - REST API
  - Cloud SDK
  - cURL
  - cell style update（セルスタイル更新）
  - Excel API
description: "Aspose.Cells Cloud REST API を使用して Excel ワークシート内の特定のセルのスタイルを更新する方法を学びます。ここでは、リクエスト・レスポンスの例および SDK のコードスニペットも提供します。"
ArticleTitle: "Excelワークシート内のセルスタイルを変更する – Aspose.Cells Cloud API ガイド"
---

この REST API は、Excel ファイルの**セルスタイル**を更新します。

## PostUpdateWorksheetCellStyle API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/style
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全で、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名 | 型     | 位置   | 説明                                       |
|--------------|--------|--------|---------------------------------------------|
| name         | string | path   | ワークブックのファイル名。                  |
| sheetName    | string | path   | ワークシート名。                            |
| cellName     | string | path   | 対象セル（例：**A1**）。                    |
| style        | object | body   | セルに適用するスタイル設定を定義する JSON オブジェクト。 |
| folder       | string | query  | ワークブックが格納されているフォルダ。      |
| storageName  | string | query  | ワークブックが格納されているストレージ名。  |

### **レスポンス**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP ステータスコード**

| コード | 意味             | 説明                                             |
|--------|------------------|--------------------------------------------------|
| 200    | OK               | フィルターが正常に適用され、レスポンスに操作詳細が含まれます。 |
| 400    | Bad Request      | パラメータが不足または不正（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized     | JWT トークンが不正または不足しています。         |
| 413    | Payload Too Large| アップロードされたファイルがサイズ制限を超えています。 |
| 500    | Internal Server Error | サーバー内で予期しないエラーが発生しました。     |

## SDK を使用した PostUpdateWorksheetCellStyle API の利用方法

### PostUpdateWorksheetCellStyle API の仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Cells/PostUpdateWorksheetCellStyle) は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST アクセスを実行できるようにします。

**cURL** コマンドラインツールを使用して、Aspose.Cells ウェブサービスに簡単にアクセスできます。`<jwt token>` を、Aspose Cloud 認証エンドポイントから取得した有効な OAuth 2.0 アクセストークンに置き換えてください。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test_cells.xlsx/worksheets/Sheet3/cells/A1/style" \
-d '{ "BackgroundThemeColor": { "ColorType": "Text2", "Tint": 1 } }' \
-X POST \
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
      "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
      "DoubleSize": 11,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Calibri",
      "Size": 11,
      "Underline": "None"
    },
    "Name": null,
    "CultureCustom": null,
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
      { "LineStyle": "None", "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }, "BorderType": "BottomBorder" },
      { "LineStyle": "None", "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }, "BorderType": "DiagonalDown" },
      { "LineStyle": "None", "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }, "BorderType": "DiagonalUp" },
      { "LineStyle": "None", "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }, "BorderType": "Horizontal" },
      { "LineStyle": "None", "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }, "BorderType": "LeftBorder" },
      { "LineStyle": "None", "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }, "BorderType": "RightBorder" },
      { "LineStyle": "None", "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }, "BorderType": "TopBorder" },
      { "LineStyle": "None", "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }, "BorderType": "Vertical" }
    ],
    "BackgroundThemeColor": null,
    "ForegroundThemeColor": null,
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/test_cells.xlsx/worksheets/Sheet3/cells/A1/style",
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

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、API に対して最も高速に開発が可能です。SDK は低レベルの詳細を抽象化するため、ビジネスロジックの開発に集中できます。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUpdateWorksheetCellStyle.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUpdateWorksheetCellStyle.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUpdateWorksheetCellStyle.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUpdateWorksheetCellStyle.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUpdateWorksheetCellStyle.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUpdateWorksheetCellStyle.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUpdateWorksheetCellStyle.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUpdateWorksheetCellStyle.go" >}}

{{< /tab >}}

{{< /tabs >}}

**関連項目:**  
- [セルスタイルの取得](https://docs.aspose.cloud/cells/get-cell-style/) – セルの現在のスタイルを取得します。  
- [複数セルのスタイルを一括更新](https://docs.aspose.cloud/cells/update-multiple-cells-style/) – 1 つのリクエストでセル範囲にスタイルを適用します。  
---