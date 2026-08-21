---
title: "CSVデータをExcelワークシートにインポートする"
second_title: "Document"
linktitle: "CSVデータのインポート"
type: docs
url: /import-CSV-data-into-excel/
aliases:
  - /import-CSV-data-into-worksheet/
  - /import-data/csv-data/
  - /import/csv-data/
keywords: "CSVデータのインポート、Excel、Aspose.Cells Cloud、REST API、スプレッドシート、CSVインポート"
description: "Aspose.Cells Cloud REST API を使用すると、ExcelワークシートにCSVデータをインポートできます。サポートされているSDKには、Android、.NET、Go、Java、Node.js、Perl、PHP、Python、Ruby、Swiftがあります。"
weight: 19
---

このREST APIは、**CSVデータをExcelワークシートにインポート**します。

リクエストは、マルチパート形式のHTTPリクエストです（[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) または [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html) を参照）。マルチパート本文の最初のパートには `ImportCSVDataOption` データが含まれ、2番目のパートにはCSVファイルが含まれます。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

重要なパラメータを以下の表に示します。

### ImportCSVDataOption

| パラメータ名       | 型                         | 説明                                                                 |
| ------------------ | -------------------------- | ------------------------------------------------------------------- |
| SeparatorString    | 文字列                     | CSVファイル内のフィールドを区切るために使用する文字（例: `,` または `;`） |
| ConvertNumericData | 文字列 (`true`/`false`)    | 数値として解釈可能な文字列を数値に変換するかどうかを示します           |
| FirstRow           | 整数                       | データを配置する最初の行の1始まりのインデックス                        |
| FirstColumn        | 整数                       | データを配置する最初の列の1始まりのインデックス                        |
| SourceFile         | 文字列                     | インポートするソースCSVファイルの名前                                  |
| CustomParsers      | List\<CustomParserConfig\> | 特定の列用のカスタムパーサ設定のコレクション                           |

### CustomParserConfig

| パラメータ名   | 型     | 説明                                                        |
| -------------- | ------ | ---------------------------------------------------------- |
| ColumnIndex    | 整数   | カスタムパーサを適用する列の0始まりのインデックス           |
| ParseMethod    | 文字列 | 列の解析方法（例: `ToString`、`ToDate`、`ToNumber`）         |
| CustomStyle    | 文字列 | 解析されたセルに適用されるカスタムスタイル（例: 数値書式）   |

**例**

```xml
<ImportCSVDataOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>true</IsInsert>
    <ImportDataType>CSVData</ImportDataType>
    <SeparatorString>;</SeparatorString>
    <ConvertNumericData>true</ConvertNumericData>
    <FirstRow>1</FirstRow>
    <FirstColumn>2</FirstColumn>
    <SourceFile>TestImportDataCSV.CSV</SourceFile>
    <CustomParsers>
        <CustomParserConfig>
            <ColumnIndex>0</ColumnIndex>
            <ParseMethod>ToString</ParseMethod>
            <CustomStyle>#</CustomStyle>
        </CustomParserConfig>
    </CustomParsers>
</ImportCSVDataOption>
```
### レスポンス

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTPステータスコード**

| コード | 意味                         | 説明                                                  |
|------|-----------------------------|------------------------------------------------------|
| 200  | OK                          | フィルターが正常に適用された。レスポンスには操作の詳細が含まれる。 |
| 400  | Bad Request                 | パラメータが不足している、または無効（例: サポートされていないファイル形式） |
| 401  | Unauthorized                | JWT トークンが無効または不足している                           |
| 413  | Payload Too Large           | アップロードされたファイルがサイズ制限を超えている               |
| 500  | Internal Server Error       | 予期しないサーバーエラーが発生しました                           |

## SDK を使用した PostImportData API の使い方

### PostImportData API の仕様

[OpenAPI仕様](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) は、Webブラウザから直接RESTインタラクションを実行できる公開可能なプログラミングインターフェースを定義しています。

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、開発を最も効率的に加速できます。SDK は低レベルの詳細を抽象化し、ビジネスロジックの開発に集中できるようにします。Aspose.Cells Cloud SDK の完全なリストについては、[GitHubリポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、PHP SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{< tabs tabTotal="1" tabID="1" tabName1="PHP" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportCSVData.php" >}}
{{< /tab >}}
{{< /tabs >}}