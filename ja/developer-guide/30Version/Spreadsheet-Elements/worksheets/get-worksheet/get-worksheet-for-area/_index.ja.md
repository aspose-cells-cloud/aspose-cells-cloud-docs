---
title: "ワークシートの範囲を PNG、PDF、CSV にエクスポート – Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktitle: "範囲"
type: docs
url: /ja/worksheets/area-to-different-formats/
aliases: [  /ja/get-worksheet-for-area/ ]
keywords: "Aspose.Cells、ワークシート範囲のエクスポート、PNG、PDF、CSV、Excel 変換、REST API、SDK"
description: "Aspose.Cells Cloud REST API または SDK（C#、Java、Python など）を使用して、Excel ワークシートの特定のセル範囲を PNG、PDF、CSV、および 20 以上のその他の形式にエクスポートする方法を学びます。"
weight: 230
ArticleTitle: "Aspose.Cells Cloud API を使用してワークシート範囲を PNG、PDF、CSV にエクスポート – 完全ガイド"
---

[GET /cells/{name}/worksheets/{sheetName}](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet) API を使用すると、ワークシートの指定された範囲をさまざまなファイル形式に変換できます。サポートされている形式: [XLS](https://docs.fileformat.com/spreadsheet/xls/)、[XLSX](https://docs.fileformat.com/spreadsheet/xlsx/)、[XLSB](https://docs.fileformat.com/spreadsheet/xlsb/)、[CSV](https://docs.fileformat.com/spreadsheet/csv/)、[TSV](https://docs.fileformat.com/spreadsheet/tsv/)、[XLSM](https://docs.fileformat.com/spreadsheet/xlsm/)、[ODS](https://docs.fileformat.com/spreadsheet/ods/)、[TXT](https://docs.fileformat.com/word-processing/txt/)、[PDF](https://docs.fileformat.com/pdf/)、[OTS](https://docs.fileformat.com/spreadsheet/ots/)、[XPS](https://docs.fileformat.com/page-description-language/xps/)、[DIF](https://docs.fileformat.com/spreadsheet/dif/)、[PNG](https://docs.fileformat.com/Image/png/)、[JPEG](https://docs.fileformat.com/image/jpeg/)、[GIF](https://docs.fileformat.com/image/gif/)、[BMP](https://docs.fileformat.com/image/bmp/)、[WMF](https://docs.fileformat.com/image/wmf/)、[TIFF](https://docs.fileformat.com/image/tiff/)、[EMF](https://docs.fileformat.com/image/emf/)、[NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/)、[FODS](https://docs.fileformat.com/spreadsheet/fods/)。

このガイドでは、Aspose.Cells Cloud API を使用して、Excel ワークシートの**特定のセル範囲**を PNG、PDF、CSV、および 20 以上の追加形式にエクスポートする方法を示します。関連する操作（ワークシート全体のエクスポートやワークブックの変換など）については、**[ワークシート全体をエクスポート](https://docs.aspose.cloud/cells/worksheets/worksheet-to-different-formats/)** および **[ワークブックを PDF に変換](https://docs.aspose.cloud/cells/workbook/convert-to-pdf/)** のページをご参照ください。

## REST API

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetWithFormat)は、パブリックにアクセス可能なプログラミングインターフェースを定義し、ウェブブラウザから直接 REST アクセスを実行できるようにします。

### リクエストパラメータ

| パラメータ             | タイプ   | 必須   | 説明                                    |
|----------------------|--------|--------|-------------------------------------------|
| `name`               | 文字列   | はい     | ワークブックファイル名。                   |
| `sheetName`          | 文字列   | はい     | 対象ワークシート名。                       |
| `format`             | 文字列   | はい     | 出力形式（png、pdf、csv など）。            |
| `area`               | 文字列   | いいえ    | エクスポートするセル範囲（例: `B3:K8`）。   |
| `verticalResolution`| 整数    | いいえ    | ラスタ形式の垂直 DPI。                      |
| `horizontalResolution`| 整数  | いいえ    | ラスタ形式の水平 DPI。                      |
| `folder`             | 文字列   | いいえ    | ファイルを含むクラウドストレージフォルダ。  |
| `storage`            | 文字列   | いいえ    | ストレージサービスの名前。                  |

### 成功レスポンス

* **200 OK** – リクエストされたファイルをバイナリ形式（PNG、PDF、CSV など）で返します。

### エラーレスポンス

| ステータスコード | 説明                                      |
|------------------|-------------------------------------------|
| 400              | 不正なリクエスト – パラメータが不足しているか、無効です。 |
| 401              | 認証エラー – 認証トークンが不足しているか、無効です。     |
| 404              | 見つかりません – 指定されたワークブックまたはワークシートが存在しません。 |
| 500              | サーバーエラー – サーバー上で予期しない状態が発生しました。 |

**エラーペイロードの例**

```json
{
  "error": {
    "code": "InvalidParameter",
    "message": "The 'area' parameter is malformed. Expected format: B3:K8."
  }
}
```

cURL コマンドラインツールを使用すると、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1?format=png&verticalResolution=100&horizontalResolution=90&area=B3%3AK8&folder=DotnetFiles" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

変換された画像（バイナリ PNG）

{{< /tab >}}

{{< /tabs >}}

## クラウド SDK ファミリー

SDK を使用すると、開発が最も迅速に行えます。SDK は低レベルの詳細を抽象化し、プロジェクトのロジックに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCellAreaWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCellAreaWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCellAreaWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCellAreaWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCellAreaWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCellAreaWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCellAreaWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCellAreaWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}
---