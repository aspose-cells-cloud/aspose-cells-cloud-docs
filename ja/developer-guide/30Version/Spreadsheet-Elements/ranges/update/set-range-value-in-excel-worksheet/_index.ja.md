---
title: "Excelワークシートで範囲の値を設定する"
second_title: "Document"
linktitle: "値を設定する"
type: docs
url: /ja/ranges/update/values/
aliases: [  /ja/set-range-value-in-excel-worksheet/ ]
keywords: "Aspose.Cells, Excel API, 範囲の値を設定する, REST API, クラウドSDK, ワークシートの更新"
description: "Aspose.Cells Cloud REST API（v3.0）を使用してExcelワークブック内のセルまたは範囲の値を設定する方法を学びます。エンドポイント、パラメータ、cURLの例、SDKのコードサンプル、エラー処理を含みます。"
weight: 72
ArticleTitle: "Excelワークシートで範囲の値を設定する – Aspose.Cells Cloud API"
---

このREST APIを使用して、指定された範囲に値を設定します。適切な場合、値は別のデータ型に変換され、セルの数値書式がリセットされます。

**前提条件**  
- 有効なAspose Cloudアカウント。  
- `Cells.ReadWrite` スコープを含むJWTトークン。  
- ワークブックは、すでにターゲットのストレージ場所にアップロードされていること。

## PostWorksheetCellsRangeValue API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/value
```

リクエストパラメータは以下の通りです：

| パラメータ名 | 型      | 位置   | 説明                                      |
|--------------|---------|--------|-------------------------------------------|
| name         | string  | path   | ワークブック名                             |
| sheetName    | string  | path   | ワークシート名                             |
| value        | string  | query  | 入力値                                     |
| range        | object  | body   | ワークシート内の範囲オブジェクト           |
| isConverted  | boolean | query  | 入力値を変換するかどうかを示します         |
| setStyle     | boolean | query  | ターゲットセルにスタイルを適用するかどうかを示します |
| folder       | string  | query  | ワークブックフォルダ                       |
| storageName  | string  | query  | ストレージ名                               |

**リクエストボディに送信できる `range` オブジェクトの例**：

```json
{
  "range": {
    "FirstRow": 0,
    "FirstColumn": 0,
    "RowCount": 1,
    "ColumnCount": 1
  }
}
```

[OpenAPI仕様](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeValue)は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Webブラウザから直接REST通信を実行できるようにします。

cURLコマンドラインツールを使用して、Aspose.Cellsウェブサービスに簡単にアクセスできます。以下の例は、cURLでクラウドAPIを呼び出す方法を示しています。**`Authorization` ヘッダーに有効なJWTトークンを含めてください。**

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/value?value=25&isConverted=false&setStyle=false" \
  -X POST \
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

**レスポンススキーマ**

| フィールド | 型      | 説明                                      |
|-----------|---------|-------------------------------------------|
| Code      | integer | 操作のHTTPステータスコード。              |
| Status    | string  | 結果の短い説明（例: "OK"）。              |
| Message   | string  | リクエストが失敗した場合の詳細なエラーメッセージ（オプション）。|
| Result    | object  | 成功した呼び出しで返される追加データ（オプション）。|

**可能なHTTPステータスコード**

- **200 OK** – 範囲の値が正常に設定されました。  
- **400 Bad Request** – 無効なパラメータまたは不正な形式のリクエストボディ。  
- **401 Unauthorized** – JWTトークンが欠落しているか、無効です。  
- **403 Forbidden** – 要求された操作に対する権限が不足しています。  
- **404 Not Found** – 指定されたワークブック、ワークシート、または範囲が存在しません。  
- **500 Internal Server Error** – 予期しないサーバーエラーが発生しました。

*400 Bad Requestのエラーレスポンスの例：*

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "The 'range' object is missing required fields."
}
```

## クラウドSDKファミリー

SDKを使用すると、開発を最適化できます。SDKは低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDKの完全な一覧は[GitHubリポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまなSDKを使用してAspose.Cellsウェブサービスを呼び出す方法を示しています：

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-SetRangeValueWorksheet-1.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-SetRangeValueWorksheet-1.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-PostSetCellRangeValue-.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-set_cell_range_value-.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-SetRangeValueWorksheet-1.js" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SetRangeValueInExcelWorksheet.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-SetRangeValueWorksheet-1.pl" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "7dc9243752ac8a0e5d9c0f211a029cd9" >}}
{{< /tab >}}

{{< /tabs >}}