---
title: "ワークシートページのエクスポート – Aspose.Cells Cloud API リファレンス"
articleTitle: "ワークシートページのエクスポート – Aspose.Cells Cloud API リファレンス"
secondTitle: "ドキュメント"
linkTitle: "ページ"
type: docs
url: /ja/worksheets/page-to-different-formats/
aliases: [  /ja/get-worksheet-for-page-index/ ]
keywords: "Aspose.Cells Cloud, ワークシートページのエクスポート, PDF, PNG, CSV, REST API, JWT 認証, ファイル形式"
description: "Aspose.Cells Cloud REST API を使用して、特定のワークシートページを PDF、PNG、CSV などにエクスポートする方法を学習します。cURL リクエスト、パラメータガイド、および複数の言語向けの SDK サンプルを含みます。"
weight: 240
---

特定のワークシートページをエクスポートする機能は、ワークブック全体をダウンロードすることなく、レポートの印刷用スナップショット、チャート画像、またはデータ抽出を取得したい場合に役立ちます。このエンドポイントを使用すると、単一ページを下流ワークフローに最適な形式で取得できます。

[GET /cells/{name}/worksheets/{sheetName}](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet) API を使用すると、ワークシートの指定されたページをさまざまなファイル形式に変換できます。サポートされている形式：[XLS](https://docs.fileformat.com/spreadsheet/xls/)、[XLSX](https://docs.fileformat.com/spreadsheet/xlsx/)、[XLSB](https://docs.fileformat.com/spreadsheet/xlsb/)、[CSV](https://docs.fileformat.com/spreadsheet/csv/)、[TSV](https://docs.fileformat.com/spreadsheet/tsv/)、[XLSM](https://docs.fileformat.com/spreadsheet/xlsm/)、[ODS](https://docs.fileformat.com/spreadsheet/ods/)、[TXT](https://docs.fileformat.com/word-processing/txt/)、[PDF](https://docs.fileformat.com/pdf/)、[OTS](https://docs.fileformat.com/spreadsheet/ots/)、[XPS](https://docs.fileformat.com/page-description-language/xps/)、[DIF](https://docs.fileformat.com/spreadsheet/dif/)、[PNG](https://docs.fileformat.com/Image/png/)、[JPEG](https://docs.fileformat.com/image/jpeg/)、[GIF](https://docs.fileformat.com/image/gif/)、[BMP](https://docs.fileformat.com/image/bmp/)、[WMF](https://docs.fileformat.com/image/wmf/)、[TIFF](https://docs.fileformat.com/image/tiff/)、[EMF](https://docs.fileformat.com/image/emf/)、[NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/)、[FODS](https://docs.fileformat.com/spreadsheet/fods/)。

## REST API

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet) はパブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 操作を実行できるようにします。

> **前提条件** – 有効な JWT 認証トークンと、`folder` パラメータで指定したクラウドフォルダーに保存されたワークブックが必要です。

cURL コマンドラインツールを使用すると、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例では、cURL を使用してクラウド API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1?format=png&verticalResolution=100&horizontalResolution=90&pageIndex=1&folder=DotnetFiles" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

**レスポンス** – サービスは、選択した形式でリクエストされたページを返します。画像形式（png、jpeg、gif など）の場合、本文にはバイナリ画像が含まれます。ドキュメント形式（pdf、xls、csv など）の場合、本文にはファイルの内容が含まれます。成功した呼び出しは HTTP 200 を返します。

*PNG レスポンスの例（base64 サンプルを一部省略）：*

```text
iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAABG0lEQVR42mNkYGBg+M+ABbJw
...
```

{{< /tab >}}

{{< /tabs >}}

**パラメータ**

| パラメータ               | 型      | 説明                                                             | デフォルト値 |
| ------------------------ | ------- | ----------------------------------------------------------------- | ------------ |
| `format`                 | 文字列  | 出力ファイル形式（例：`pdf`、`png`、`csv`）。                     | `pdf`        |
| `verticalResolution`     | 整数    | 描画画像の垂直 DPI。                                              | `100`        |
| `horizontalResolution`   | 整数    | 描画画像の水平 DPI。                                              | `100`        |
| `pageIndex`              | 整数    | エクスポートするワークシートページの 0 から始まるインデックス（`0` = 最初のページ）。 | `0`          |
| `folder`                 | 文字列  | ソースワークブックが配置されているクラウドストレージフォルダー。 | —            |

**HTTP ステータスコード**

| コード | 意味                   | 説明                                         |
| ------ | ---------------------- | -------------------------------------------- |
| 200    | OK（成功）             | フィルターが正常に適用され、レスポンスに操作の詳細が含まれます。 |
| 400    | Bad Request（不正なリクエスト） | パラメータが不足または不正（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized（認証エラー）     | JWT トークンが不正または不足しています。     |
| 413    | Payload Too Large（ペイロードが大きすぎます） | アップロードされたファイルがサイズ制限を超えています。 |
| 500    | Internal Server Error（内部サーバーエラー） | 予期せぬサーバーエラーが発生しました。       |

**発生する可能性のあるエラー**

- **401 Unauthorized** – 無効または不足している JWT トークン。
- **404 Not Found** – 指定されたワークブックまたはワークシートが存在しません。
- **400 Bad Request** – 不正なパラメータ値（例：サポートされていない `format`）。
- **500 Internal Server Error** – 予期しないサーバー側の問題。

## クラウド SDK ファミリー

SDK を使用すると、開発を迅速化できます。SDK は低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) を確認してください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}