---
title: "ExcelファイルへのデータのインポートとExcelファイルからのデータのエクスポート"
second_title: "Document"
linktitle: "データのインポートとエクスポート"
type: docs
url: /ja/data-import-and-export/
keywords: "Aspose.Cells Cloud, データのインポート, Excelのエクスポート, API, CSV, JSON, 画像, 配列"
description: "CSV、JSON、配列、画像からExcelファイルへデータをインポートし、ワークブック、チャート、図形をPDF、PNGなどにエクスポートする方法をAspose.Cells Cloud API（v3.0）を使って学びます。"
weight: 25
---

Aspose.Cells Cloud APIは、多様なソースからのデータインポートをサポートし、**XLSX**、**CSV**、**PDF**、**HTML**、**PNG**などの異なる形式へExcelワークブック、チャート、その他のオブジェクトをエクスポートできます。これにより、データの管理と共有がシンプルかつ効率的になります。

**API version:** **v3.0** – 最終更新日：**2024‑03‑15**

### クイックスタートガイド

1. **ペイロードの準備** – インポートまたはエクスポートのオプションを記述するJSON本文（例：`ImportCSVDataOption`、`ExportOptions`）を構築します。
2. **リクエストの送信** – `curl`、Postman、またはSDKを使用して適切なエンドポイント（`POST /cells/import` または `POST /cells/export`）を呼び出します。
3. **レスポンスの処理** – 成功した場合は処理済みファイル（バイナリまたはBase64）が返されます。エラーの場合は、HTTPステータスコードとJSON本文で返されたエラーメッセージを確認します。

#### 必要条件

- 有効なAspose Cloudアカウントと有効なJWTトークン。
- 対象のワークブックは、指定されたストレージの場所に存在している必要があります（ストレージベースのAPIの場合）。
- 正しい`Content-Type`ヘッダー（ファイルアップロードの場合は`multipart/form-data`、JSON本文の場合は`application/json`）。

## さまざまなデータソースからのデータのインポート方法

Excelファイルへのデータのインポートには、処理中に考慮すべき複数の要素があります。多様なフォーマットやデータタイプを高品質でインポートできる機能は、Aspose.Cells Cloudの主要な機能の一つです。

### データインポートAPIの情報

以下のAPIが提供されており、1つまたは複数のExcelファイルへデータをインポートできます：

| API                                                                                                | 説明                                                         |
| :------------------------------------------------------------------------------------------------- | :----------------------------------------------------------- |
| [POST /cells/import](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)              | ストレージを使わずにExcelファイルへデータをインポートします。 |
| [POST /cells/{name}/importdata](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) | クラウド上に保存されたExcelファイルへデータをインポートします。 |

### リクエストパラメーター

#### ストレージを使わない場合

| パラメーター名 | 種別    | 位置       | 説明                                     |
| :------------- | :------ | :--------- | :--------------------------------------- |
| file           | file    | formData   | アップロードするファイル                 |
| ImportOption   | ImportOptions | body   | インポート形式（IntArray, DoubleArray, StringArray, TwoDimensionIntArray, TwoDimensionDoubleArray, TwoDimensionStringArray, BatchData, csvData, Picture）を指定 |

#### ストレージを使う場合

| パラメーター名 | 種別    | 位置       | 説明                   |
| :------------- | :------ | :--------- | :--------------------- |
| name           | string  | path       | Excelファイルの名前    |
| folder         | string  | query      | ストレージ内のフォルダーパス |
| storageName    | string  | query      | ストレージ名           |
| importData     | ImportOptions | body   | データインポートペイロード |

#### データインポートオプションパラメーター

**重要なパラメーターは以下の表に示します：**

{{< tabs tabTotal="11" tabID="1" tabName1="ImportBatchDataOption"  tabName2="ImportCSVDataOption"   tabName3="ImportPictureOption" tabName4="Import2DimensionIntArrayOption" tabName5="Import2DimensionDoubleArrayOption" tabName6="Import2DimensionStringArrayOption" tabName7="ImportIntegerArrayOption" tabName8="ImportDoubleArrayOption" tabName9="ImportStringArrayOption" tabName10="CellValue" tabName11="FileSource" >}}

{{< tab tabNum="1" >}}

<table class="table">
  <thead>
    <tr><th>パラメーター</th><th>種別</th><th>説明</th></tr>
  </thead>
  <tbody>
    <tr><td>BatchData</td><td>List&lt;CellValue&gt;</td><td>インポートするバッチデータ</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>宛先ワークシート名</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>データを挿入するかどうか（true/false）</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionStringBatchDataArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>BatchDataがnullの場合のデータファイルの場所</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="2" >}}

<table class="table">
  <thead>
    <tr><th>パラメーター</th><th>種別</th><th>説明</th></tr>
  </thead>
  <tbody>
    <tr><td>ConvertNumericData</td><td>boolean</td><td>数値データを変換するかどうか（true/false）</td></tr>
    <tr><td>FirstRow</td><td>int</td><td>最初の行のインデックス</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>最初の列のインデックス</td></tr>
    <tr><td>SeparatorString</td><td>string</td><td>列の区切り文字</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>宛先ワークシート名</td></tr>
    <tr><td>CustomParsers</td><td>List&lt;CustomParserConfig&gt;</td><td>カスタムパーサー設定</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>CSVData</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>BatchDataがnullの場合のデータファイルの場所</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="3" >}}

<table class="table">
  <thead>
    <tr><th>パラメーター</th><th>種別</th><th>説明</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>最初の行のインデックス</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>最初の列のインデックス</td></tr>
    <tr><td>IsVertical</td><td>boolean</td><td>画像を垂直に配置するかどうか（true/false）</td></tr>
    <tr><td>Data</td><td>string[]</td><td>画像データ（Base64文字列）</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>宛先ワークシート名</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>データを挿入するかどうか（true/false）</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>Picture</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>BatchDataがnullの場合のデータファイルの場所</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="4" >}}

<table class="table">
  <thead>
    <tr><th>パラメーター</th><th>種別</th><th>説明</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>最初の行のインデックス</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>最初の列のインデックス</td></tr>
    <tr><td>Data</td><td>int[,] </td><td>2次元整数配列</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>宛先ワークシート名</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>データを挿入するかどうか（true/false）</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionIntArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>BatchDataがnullの場合のデータファイルの場所</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="5" >}}

<table class="table">
  <thead>
    <tr><th>パラメーター</th><th>種別</th><th>説明</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>最初の行のインデックス</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>最初の列のインデックス</td></tr>
    <tr><td>Data</td><td>double[,] </td><td>2次元倍精度浮動小数点数配列</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>宛先ワークシート名</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>データを挿入するかどうか（true/false）</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionDoubleArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>BatchDataがnullの場合のデータファイルの場所</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="6" >}}

<table class="table">
  <thead>
    <tr><th>パラメーター</th><th>種別</th><th>説明</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>最初の行のインデックス</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>最初の列のインデックス</td></tr>
    <tr><td>Data</td><td>string[,] </td><td>2次元文字列配列</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>宛先ワークシート名</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>データを挿入するかどうか（true/false）</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionStringArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>BatchDataがnullの場合のデータファイルの場所</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="7" >}}

<table class="table">
  <thead>
    <tr><th>パラメーター</th><th>種別</th><th>説明</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>最初の行のインデックス</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>最初の列のインデックス</td></tr>
    <tr><td>IsVertical</td><td>boolean</td><td>配列を垂直に配置するかどうか（true/false）</td></tr>
    <tr><td>Data</td><td>int[] </td><td>1次元整数配列</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>宛先ワークシート名</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>データを挿入するかどうか（true/false）</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>IntegerArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>BatchDataがnullの場合のデータファイルの場所</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="8" >}}

<table class="table">
  <thead>
    <tr><th>パラメーター</th><th>種別</th><th>説明</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>最初の行のインデックス</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>最初の列のインデックス</td></tr>
    <tr><td>IsVertical</td><td>boolean</td><td>配列を垂直に配置するかどうか（true/false）</td></tr>
    <tr><td>Data</td><td>double[] </td><td>1次元倍精度浮動小数点数配列</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>宛先ワークシート名</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>データを挿入するかどうか（true/false）</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>DoubleArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>BatchDataがnullの場合のデータファイルの場所</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="9" >}}

<table class="table">
  <thead>
    <tr><th>パラメーター</th><th>種別</th><th>説明</th></tr>
  </thead>
  <tbody>
    <tr><td>UpperLeftRow</td><td>int</td><td>左上行インデックス</td></tr>
    <tr><td>UpperLeftColumn</td><td>int</td><td>左上列インデックス</td></tr>
    <tr><td>LowerRightRow</td><td>int</td><td>右下行インデックス</td></tr>
    <tr><td>LowerRightColumn</td><td>int</td><td>右下列インデックス</td></tr>
    <tr><td>Filename</td><td>string</td><td>ソースファイル名</td></tr>
    <tr><td>Data</td><td>string</td><td>インポートする文字列データ</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>宛先ワークシート名</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>データを挿入するかどうか（true/false）</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>StringArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>BatchDataがnullの場合のデータファイルの場所</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="10" >}}

<table class="table">
  <thead>
    <tr><th>パラメーター</th><th>種別</th><th>説明</th></tr>
  </thead>
  <tbody>
    <tr><td>rowIndex</td><td>int</td><td>セルの行インデックス</td></tr>
    <tr><td>columnIndex</td><td>int</td><td>セルの列インデックス</td></tr>
    <tr><td>type</td><td>string</td><td>セル値のデータタイプ</td></tr>
    <tr><td>value</td><td>string</td><td>セル値</td></tr>
    <tr><td>style</td><td>Style (object)</td><td>セルスタイル定義</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="11" >}}

<table class="table">
  <thead>
    <tr><th>パラメーター</th><th>種別</th><th>説明</th></tr>
  </thead>
  <tbody>
    <tr><td>FileSourceType</td><td>string</td><td>InMemoryFiles、CloudFileSystem、またはRequestFiles</td></tr>
    <tr><td>FilePath</td><td>string</td><td>ソースファイルのパス</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< /tabs >}}

## Excelオブジェクトをさまざまなファイル形式にエクスポートする方法

もしあなたが元のExcelファイルを**XLS**、**XLSX**、**XLSB**、**CSV**などの形式で作成している場合、特定の機能を活用するために他の形式に変換したいと感じるかもしれません。たとえば、**PDF**にエクスポートすると、不正な変更からコンテンツを保護しながら、読みやすく共有しやすい形式になります。

Excelオブジェクトのエクスポートにはいくつか考慮すべき点があります。Aspose.Cells Cloudは、ワークブック、チャート、図形、画像を多様な形式へ高品質でエクスポートできます：

_エクスポート専用形式_: PDF、OTS、XPS、DIF、PNG、JPEG、BMP、SVG、TIFF、EMF、NUMBERS、FODS。  
_インポートとエクスポートの両方対応_: XLS、XLSX、XLSB、CSV、TSV、XLSM、ODS、TXT。

このリクエストは[RFC 2046]および[RFC 1341]で定義されたマルチパートコンテンツを使用します。最初のパートにはデータファイルが含まれ、2番目のパートには保存オプションが含まれます。

### エクスポートAPIの情報

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

#### リクエストパラメーター

| パラメーター名 | 種別   | 位置       | 説明                                                                                   |
| :------------- | :----- | :--------- | :------------------------------------------------------------------------------------- |
| file           | file   | formData   | アップロードするファイル                                                               |
| objectType     | string | query      | オブジェクトタイプ（`workbook`、`worksheet`、`chart`、`shape`、`picture`、`listobject`、`oleobject`） |
| format         | string | query      | 出力ファイル形式（[サポートされているファイル形式](/cells/supported-file-formats/)を参照）     |

[OpenAPI仕様](https://apireference.aspose.cloud/cells/#/LightCells/PostExport)は、Webブラウザから直接RESTインタラクションを実行できるパブリックAPIインタフェースを定義しています。

cURLコマンドラインツールを使用してAPIを呼び出すことができます。以下の例では、リクエストとそのJSONレスポンスを示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/export" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'file1=@example1.xlsx' \
  -F 'file2=@example2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "example1.pdf",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "example2.pdf",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}

#### 一般的なHTTPステータスコード

| ステータス | 意味                                                           | 推奨アクション                               |
| ---------- | -------------------------------------------------------------- | -------------------------------------------- |
| 200        | 成功 – ファイルがエクスポートされました                         | 返されたファイルを処理します                 |
| 400        | 不正なリクエスト – パラメーターが不足しているか無効です         | リクエストペイロードとクエリ文字列を確認します |
| 401        | 認証エラー – 無効または期限切れのJWTトークン                    | トークンを更新して再試行します                 |
| 404        | 見つかりません – 指定されたワークブックまたはワークシートが存在しません | ファイル名とストレージパスを確認します         |
| 500        | サーバー内部エラー – サーバー上で予期しない状態が発生しました     | リクエストIDとともにAsposeのサポートに連絡します |

## インポートAPIとエクスポートAPIの呼び出し方法

以下の記事では、各APIを詳しく説明し、cURLおよびSDKの例を含んでいます：

- [ストレージを使わずにExcelファイルへデータをインポートする方法](/cells/import/without-using-storage)
- [ストレージを使ってExcelファイルへデータをインポートする方法](/cells/import/with-using-storage)
- [Excelワークシートへバッチデータをインポートする方法](/cells/import-batch-data-into-excel-worksheet/)
- [ExcelワークシートへCSVデータをインポートする方法](/cells/import-CSV-data-into-excel-worksheet/)
- [Excelワークシートへ画像をインポートする方法](/cells/import-picture-into-excel-worksheet/)
- [Excelワークシートへ整数配列をインポートする方法](/cells/import-integer-array-into-excel-worksheet/)
- [Excelワークシートへ倍精度浮動小数点数配列をインポートする方法](/cells/import-double-array-into-excel-worksheet/)
- [Excelワークシートへ文字列配列をインポートする方法](/cells/import-string-array-into-excel-worksheet/)
- [Excelワークシートへ2次元整数配列をインポートする方法](/cells/import-a-2D-integer-array-into-excel-worksheet/)
- [Excelワークシートへ2次元倍精度浮動小数点数配列をインポートする方法](/cells/import-a-2D-double-array-into-excel-worksheet/)
- [Excelワークシートへ2次元文字列配列をインポートする方法](/cells/import-a-2D-string-array-into-excel-worksheet/)
- [Excelチャートを別のファイル形式にエクスポートする方法](/cells/export-excel-chart-to-different-formats/)
- [Excelリストオブジェクトを別のファイル形式にエクスポートする方法](/cells/export-excel-listobject-to-different-formats/)
- [ExcelOLEオブジェクトを別のファイル形式にエクスポートする方法](/cells/export-excel-ole-object/)
- [Excel画像を別のファイル形式にエクスポートする方法](/cells/export-excel-picture-to-different-formats/)
- [Excel図形を別のファイル形式にエクスポートする方法](/cells/export-excel-shape-to-different-formats/)
- [Excelワークブックを別のファイル形式にエクスポートする方法](/cells/export-excel-to-different-formats/)
- [Excelワークシートを別のファイル形式にエクスポートする方法](/cells/export-excel-worksheet-to-different-formats/)

---