---
title: "2次元double配列をExcelワークシートにインポートする"
second_title: "Document"
linktitle: "2次元double配列のインポート"
type: docs
url: /ja/import-a-2D-double-array-into-excel-worksheet/
aliases:
  [
    "/import-2dimension-double-array-into-excel-worksheet/",
    "/import-2dimension-double-array-into-worksheet/",
    "/import-data/2dimension-double-array/",
    "/import/2dimension-double-array/",
  ]
keywords: "2次元double配列のインポート, Excel, Aspose Cells Cloud, REST API, スプレッドシート, データインポート"
description: "Aspose.Cells Cloud REST API を使用して2次元double配列をExcelワークシートにインポートする方法を学びます。リクエスト形式、パラメーター、SDKコードサンプルを含みます。"
weight: 20
---

この REST API は、**2次元double配列**をExcelワークシートにインポートします。

このリクエストは、HTTPの`POST`リクエストで、マルチパート形式のコンテンツ（[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) または [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html) を参照）を使用します。マルチパート本文の第1パートには **Import2DimensionDoubleArrayOption** データが含まれ、第2パートにはソースデータファイルが含まれます。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

主なパラメーターを以下の表に示します：

### Import2DimensionDoubleArrayOption

| パラメーター名           | 型           | 説明                                                                                                             |
| ------------------------ | ------------ | ----------------------------------------------------------------------------------------------------------------------- |
| **FirstRow**             | `int`        | インポートを開始する行インデックス（1から始まる）。                                                                            |
| **FirstColumn**          | `int`        | インポートを開始する列インデックス（1から始まる）。                                                                         |
| **Data**                 | `Double[,]`  | インポートする2次元double値配列。                                                                  |
| **DestinationWorksheet** | `string`     | データを受信するワークシートの名前。                                                                       |
| **IsInsert**             | `string`     | 行を挿入する場合は `"true"`、既存のセルを上書きする場合は `"false"`。                                                         |
| **ImportDataType**       | `string`     | インポートするデータのタイプ（例：`IntArray`、`DoubleArray`、`TwoDimensionDoubleArray`、`BatchData`、`csvData` など）。 |
| **Source**               | `FileSource` | `BatchData` パラメーターが null の場合にデータファイルの場所を示します。                                                |

**例**

```json
{
  "Data": [
    [1.0, 2.9, 3.1],
    [2.0, 2.1, 3.1]
  ],
  "DestinationWorksheet": "Sheet2",
  "FirstRow": 4,
  "FirstColumn": 1,
  "importDataType": "TwoDimensionDoubleArray"
}
```

### レスポンス

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP ステータスコード**

| コード | 意味                         | 説明                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | フィルターが正常に適用された。レスポンスには操作の詳細が含まれます。 |
| 400  | Bad Request                 | 必須パラメーターが不足している、または無効なパラメーター（例：サポートされていないファイル形式）があります。 |
| 401  | Unauthorized                | JWT トークンが無効または不足しています。 |
| 413  | Payload Too Large           | アップロードされたファイルがサイズ制限を超えています。 |
| 500  | Internal Server Error       | 予期しないサーバーエラーが発生しました。 |

## SDK を使用した PostImportData API の使用方法

### PostImportData API の仕様

[OpenAPI 仕様](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) は、ウェブブラウザから直接 REST 通信を実行できる、パブリックにアクセス可能なプログラミングインターフェースを定義しています。

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、この機能を最速で統合できます。SDK は低レベルの詳細を処理するため、ビジネスロジックに集中できます。Aspose.Cells Cloud SDK の完全なリストは [GitHub リポジトリ](https://github.com/aspose-cells-cloud) を参照してください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています：

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2Double.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}