---
title: "複数セルのスタイルを更新 – Aspose.Cells Cloud API リファレンス (v3.0)"
type: docs
url: /ja/update-multiple-cells-style/
weight: 20
keywords: ["Aspose.Cells", "複数セルのスタイル更新", "ExcelセルスタイルAPI", "クラウドSDK", "REST API", "cURLの例", "JSONリクエスト", "JWT認証"]
description: "Aspose.Cells Cloud REST API v3.0 を使用して、Excelワークブック内のセル範囲のスタイルを更新する方法を学びます。エンドポイント、HTTPメソッド、パラメーター、cURLおよびSDKの例、認証、エラー処理、バージョン情報が含まれます。"
ArticleTitle: "複数セルのスタイルを更新 – Aspose.Cells Cloud API リファレンス (v3.0)"
---

## REST API

この REST API は、Excelワークブック内のセル範囲の**スタイル**を設定します。

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/style
```

## セキュリティと認証

Aspose.Cells Cloud API は安全であり、[JWT トークンベースの認証](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)が必須です。

### リクエストパラメーター

| パラメーター名 | 型     | 位置   | 説明                      |
|----------------|--------|--------|---------------------------|
| **name**       | 文字列 | path   | ワークブック名             |
| **sheetName**  | 文字列 | path   | シート名                   |
| **range**      | 文字列 | query  | セル範囲（例: `A1:A10`）    |
| **style**      | オブジェクト | body | 適用するスタイルを定義するJSONオブジェクト |
| **folder**     | 文字列 | query  | ワークブックを含むフォルダー |
| **storageName**| 文字列 | query  | ストレージ名               |

#### Styleオブジェクト
`style` JSONオブジェクトはセルの書式設定を表します。以下のいずれかのオプションプロパティを含めることができます。

- **Font** – フォント設定（`Name`、`Size`、`IsBold`、`IsItalic`、`Color`など）  
- **BackgroundColor** – 背景色（ARGB形式）  
- **ForegroundColor** – 前景色（ARGB形式）  
- **Name**、**CultureCustom**、**Custom** – 追加のスタイルメタデータ  

## **レスポンス**

CellCloudResponse を返します。

- **レスポンスフィールド概要**

| フィールド           | 型      | 説明                    |
| -------------------- | ------- | ----------------------- |
| `Status`             | 文字列  |                         |
| `Code`               | 整数    | 200, 400, 401, 500, ... |

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTPステータスコード**

| コード | 意味             | 説明                                      |
|--------|------------------|-------------------------------------------|
| 200    | OK               | フィルターが正常に適用された；レスポンスには操作の詳細が含まれる |
| 400    | Bad Request      | パラメーターが不足または無効（例：サポートされていないファイル形式） |
| 401    | Unauthorized     | JWTトークンが無効または不足している          |
| 413    | Payload Too Large| アップロードされたファイルがサイズ制限を超過している |
| 500    | Internal Server Error | 予期しないサーバーエラー               |

## SDK を使用して PostUpdateWorksheetRangeStyle API を使用する方法

### PostUpdateWorksheetRangeStyle API 仕様

[OpenAPI仕様](https://apireference.aspose.cloud/cells/#/Cells/PostUpdateWorksheetRangeStyle)には完全なスキーマが記載されています。

cURLコマンドラインツールを使用すると、Aspose.Cells Webサービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
cURL -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/style?range=a1%3Aa10" \
  -X POST \
  -d '{
        "Font": {
          "Color": { "A":255, "R":255, "G":255, "B":0 },
          "Size": 22,
          "IsBold": true,
          "IsItalic": true,
          "IsStrikeout": true,
          "IsSubscript": true,
          "IsSuperscript": true,
          "Name": "Arial"
        },
        "Name": "string",
        "CultureCustom": "string",
        "Custom": "string",
        "BackgroundColor": { "A":10, "R":10, "G":10, "B":10 },
        "ForegroundColor": { "A":255, "R":255, "G":255, "B":0 }
      }' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

### Aspose.Cells Cloud SDK を使用する

SDK を使用すると、開発を高速化できます。SDK は低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全なリストについては、[GitHubリポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeStyle.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeStyle.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeStyle.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeStyle.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeStyle.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeStyle.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeStyle.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeStyle.go" >}}

{{< /tab >}}

{{< /tabs >}}
---