---
title: "文字列配列をExcelワークシートにインポート – Aspose.Cells Cloud"
second_title: "ドキュメント"
linktitle: "文字列配列のインポート"
type: docs
url: /ja/import-string-array-into-excel-worksheet/
aliases:
  - /import-string-array-into-worksheet/
  - /import-data/string-array/
  - /import/string-array/
keywords: "Aspose.Cells Cloud, 文字列配列のインポート, Excel REST API, マルチパートアップロード, ワークシートデータのインポート, クラウドSDK"
description: "Aspose.Cells Cloud REST API (v3.0) を使用して文字列配列をExcelワークシートにインポートする方法を学びます。リクエスト形式、パラメータ、SDKサンプルを含みます。"
weight: 40
ArticleTitle: "文字列配列をExcelワークシートにインポート – Aspose.Cells Cloud"
---

文字列配列をExcelワークシートにインポートする操作は、リスト形式のデータでスプレッドシートを入力する際によく行われます。この操作は、設定値の読み込み、外部ソースからのデータ転送、または事前に定義された文字列コレクションでワークシートを初期化するなどのシナリオに役立ちます。

**前提条件:**  
- Aspose.Cells Cloudの認証フローを通じて取得した有効なJWTトークン。  
- Aspose Cloudストレージ内に存在するワークブック（または新規作成可能であること）。  
- `ImportStringArrayOption`モデルをサポートする適切なSDKバージョン。

このREST APIは、文字列配列データをExcelワークシートにインポートします。

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **セキュリティと認証**

Aspose.Cells Cloud APIはセキュアであり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWTトークンによる認証</a>が必要です。

### **リクエストパラメータ**

リクエストはマルチパートHTTPコンテンツを使用します（参照：[RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) または [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)）。  
マルチパート本体の最初のパートには **ImportStringArrayOption** ペイロードが含まれ、2番目のパートにはソースデータファイルが含まれます。

重要なパラメータを以下の表に示します：

<caption>ImportStringArrayOption パラメータ</caption>
### **ImportStringArrayOption**

| パラメータ名             | 型         | 説明                                                                                                                                                                         |
| ----------------------- | ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| FirstRow                | int        | データを配置する開始行のインデックス（1始まり）。                                                                                                                            |
| FirstColumn             | int        | データを配置する開始列のインデックス（1始まり）。                                                                                                                            |
| IsVertical              | boolean    | `true` は垂直方向にデータを挿入、`false` は水平方向に挿入します。                                                                                                             |
| Data                    | String[]   | インポートする文字列配列。                                                                                                                                                   |
| DestinationWorksheet    | string     | データを受信するワークシート名。                                                                                                                                             |
| IsInsert                | boolean    | `true` は行／列を挿入（既存のセルをシフト）、`false` は既存のセルを上書きします。                                                                                            |
| ImportDataType          | string     | インポートするデータの種類（例：`IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`）。 |
| Source                  | FileSource | **BatchData** が null の場合にデータファイルの場所を示します（例：`CloudFileSystem`, `LocalFile`）。`BatchData` が指定されていない場合は必須です。                         |

### 例

```xml
<ImportStringArrayOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>StringArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_string_xml.txt</FilePath>
    </Source>
</ImportStringArrayOption>
```

### レスポンス

成功したリクエストは、以下のようなJSONペイロードを含む **HTTP 200** を返します：

```json
{
  "Code": 200,
  "Status": "OK"
}
```

可能なステータスコード：

| コード | 意味                                 |
| ------ | ------------------------------------ |
| 200    | インポート成功                       |
| 400    | 不正なリクエスト – データ不足または不正 |
| 401    | 認証エラー – トークンが無効または不足   |
| 500    | サーバー内部エラー                   |


## SDKを使用したPostImportData APIの利用方法

### PostImportData API仕様

[OpenAPI仕様](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) は、パブリックにアクセス可能なプログラミングインターフェースを定義し、ウェブブラウザから直接RESTインタラクションを実行できるようにします。

### Aspose.Cells Cloud SDKの使用

SDKを使用すると、開発速度が大幅に向上します。SDKが低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDKの完全なリストは [GitHubリポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまなSDKを使用してAspose.Cellsウェブサービスを呼び出す方法を示しています：

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-String.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}