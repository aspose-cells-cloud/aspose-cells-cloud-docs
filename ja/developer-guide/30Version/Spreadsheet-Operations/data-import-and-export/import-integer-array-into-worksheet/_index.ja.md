---
title: "Excelワークシートへの整数配列のインポート"
linktitle: "整数配列のインポート"
type: docs
url: /ja/import-integer-array-into-excel-worksheet/
aliases:
  - /import-integer-array-into-excel-worksheet/
  - /import-integer-array-into-worksheet/
  - /import-data/integer-array/
  - /import/integer-array/
keywords: "Aspose.Cells Cloud, Excel, 整数配列のインポート, REST API, SDK, C#, PHP, Ruby, Java, Python"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークシートに整数配列をインポートする方法を学びます。リクエスト構文、パラメーター、複数の SDK 用のサンプルコード、および応答の詳細を含みます。"
weight: 30
ArticleTitle: "Excelワークシートへの整数配列のインポート – Aspose.Cells Cloud API"
---

この REST API は、整数配列を Excel ワークシートにインポートします。

リクエストは、マルチパート・コンテンツを含む HTTP **POST** である必要があります（[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) または [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html) を参照）。マルチパート本文の最初のパートには **ImportIntegerArrayOption** の JSON ペイロードが含まれ、2 番目のパートにはソースデータ・ファイル（例：CSV またはバイナリ Excel ファイル）が含まれます。

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

両方のエンドポイントは、同じマルチパート・ペイロードを受け入れます。1 つ目のエンドポイントは汎用的なインポート操作を実行し、2 つ目は `{name}` で識別される特定のワークブックを対象とします。

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### **リクエストパラメーター**

### ImportIntegerArrayOption

| パラメーター名           | 型         | 説明                                                                                                                                                                                    |
| ------------------------ | ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **FirstRow**             | int        | データを配置する最初の行の 0 から始まるインデックス。                                                                                                                               |
| **FirstColumn**          | int        | データを配置する最初の列の 0 から始まるインデックス。                                                                                                                            |
| **IsVertical**           | boolean    | 配列を垂直方向（列方向）に挿入する場合は `true`、水平方向（行方向）に挿入する場合は `false`。                                                                                       |
| **Data**                 | Integer[]  | インポートする整数配列。                                                                                                                                                              |
| **DestinationWorksheet** | string     | データを受信するワークシートの名前。                                                                                                                                              |
| **IsInsert**             | boolean    | データを書き込む前に行/列を挿入する場合は `true`、既存のセルを上書きする場合は `false`。                                                                                                    |
| **ImportDataType**       | string     | インポートされるデータのタイプ。有効な値: `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`. |
| **Source**               | FileSource | **BatchData** パラメーターが `null` の場合にデータファイルの位置を示します。                                                                                                            |

#### リクエスト本文の例

```json
{
  "Data": [1, 2, 4],
  "DestinationWorksheet": "Sheet1",
  "FirstRow": 1,
  "FirstColumn": 2,
  "IsVertical": true,
  "IsInsert": true,
  "ImportDataType": "IntArray"
}
```

### 応答

成功したリクエストは、JSON ペイロードを含む **HTTP 200** を返します：

```json
{
  "Code": 200,
  "Status": "OK"
}
```

考えられるステータス・コード：

| コード | 意味                                     |
| ---- | --------------------------------------- |
| 200  | インポート成功                           |
| 400  | 不正なリクエスト – データが不足または無効   |
| 401  | 認証エラー – トークンが無効または不足      |
| 500  | サーバー内部エラー                   |

## SDK を使用した PostImportData API の利用方法

### PostImportData API の仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) は、パブリックにアクセス可能なプログラミング・インターフェースを定義し、Web ブラウザから直接 REST 操作を実行できるようにします。

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、この機能を最速で統合できます。SDK は低レベルの詳細を抽象化し、ビジネスロジックに集中できます。Aspose.Cells Cloud SDK の完全なリストは [GitHub リポジトリ](https://github.com/aspose-cells-cloud) を参照してください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています：

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}