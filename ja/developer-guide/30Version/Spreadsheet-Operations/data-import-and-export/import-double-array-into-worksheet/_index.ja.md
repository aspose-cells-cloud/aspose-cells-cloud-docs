---
title: "Excelワークシートへの二重配列のインポート"
second_title: "ドキュメント"
linktitle: "二重配列のインポート"
type: docs
url: /ja/import-double-array-into-excel-worksheet/
aliases:
  - /import-double-array-into-worksheet/
  - /import-data/double-array/
  - /import/double-array/
keywords: "Aspose.Cells, 二重配列のインポート, Excel API, クラウドSDK"
description: "Aspose.Cells Cloud REST APIを使用してExcelワークシートに二重配列をインポートする方法を学びます。認証、リクエスト形式、パラメータ、サンプルXML/JSON、およびレスポンスの詳細を含みます。"
weight: 20
ArticleTitle: "Excelワークシートへの二重配列のインポート – Aspose.Cells Cloudガイド"
---

このREST APIは、**二重配列データ**をExcelワークシートにインポートします。

> **前提条件:** このAPIを呼び出す前に、有効なJWTトークンが必要です。詳細については、認証ガイドを参照してください。

HTTPリクエストを**マルチパート**形式（[RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) または [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html) を参照）で送信します。  
マルチパート本文の最初の部分には **ImportDoubleArrayOption** データが含まれ、2番目の部分にはデータファイルが含まれます。

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **セキュリティと認証**

Aspose.Cells Cloud APIは安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWTトークンベースの認証</a>が必要です。

### リクエストパラメータ

#### **ImportDoubleArrayOption**

| パラメータ名         | 型         | 説明                                                                                             |
| -------------------- | ---------- | ------------------------------------------------------------------------------------------------ |
| FirstRow             | int        | データを配置する最初の行の0始まりのインデックス。                                                  |
| FirstColumn          | int        | データを配置する最初の列の0始まりのインデックス。                                                  |
| IsVertical           | boolean    | `true` / `false` – 配列を垂直方向（`true`）または水平方向（`false`）で挿入するかを決定します。      |
| Data                 | Double[]   | インポートする二重精度値の配列。                                                                   |
| DestinationWorksheet | string     | 対象ワークシートの名前。                                                                           |
| IsInsert             | boolean    | `true` / `false` – `true` の場合はデータを挿入し、`false` の場合は既存のセルを上書きします。       |
| ImportDataType       | string     | インポートするデータの種類（例: `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`）。 |
| Source               | FileSource | `BatchData` パラメータがnullの場合にデータファイルの場所を指定します。                              |

#### 例（XML）

```xml
<ImportDoubleArrayOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>DoubleArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Data>1.99,1.9,2.0</Data>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_double_xml.txt</FilePath>
    </Source>
</ImportDoubleArrayOption>
```

#### 例（JSON）

```json
{
  "Data": [1.99, 1.9, 2.0],
  "DestinationWorksheet": "Sheet1",
  "FirstRow": 0,
  "FirstColumn": 0,
  "IsVertical": false,
  "IsInsert": true,
  "ImportDataType": "DoubleArray"
}
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

| コード | 意味                         |
| ------ | ---------------------------- |
| 200    | インポート成功               |
| 400    | 不正なリクエスト – データ不足または無効 |
| 401    | 認証エラー – トークンが無効または不足 |
| 500    | サーバ内部エラー             |

### エラー処理

エラーが発生した場合、APIはエラーコードと説明的なメッセージを含むJSONオブジェクトを返します。認証エラーの例を以下に示します：

```json
{
  "Code": 401,
  "Status": "Error"
}
```

関連するインポート操作の詳細については、「2次元二重配列のインポート」と「整数配列のインポート」のドキュメントページをご覧ください。

## SDKを使用したPostImportData APIの利用方法

### PostImportData APIの仕様

[OpenAPI仕様](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)は、パブリックにアクセス可能なプログラミングインターフェースを定義し、ウェブブラウザから直接REST通信を実行できるようにします。

### Aspose.Cells Cloud SDKの利用

SDKを使用すると、開発を迅速化できます。SDKは低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDKの完全な一覧については、[GitHubリポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまなSDKを使用してAspose.Cellsウェブサービスを呼び出す方法を示しています：

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-Double.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}