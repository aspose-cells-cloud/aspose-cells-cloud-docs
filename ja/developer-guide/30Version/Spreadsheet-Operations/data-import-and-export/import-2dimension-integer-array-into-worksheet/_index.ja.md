---
title: "2次元整数配列をExcelワークシートにインポートする"
second_title: "Document"
linktitle: "2次元整数配列のインポート"
type: docs
url: /ja/import-a-2D-integer-array-into-excel-worksheet/
aliases:
  [
    "/import-2dimension-integer-array-into-excel-worksheet/",
    "/import-2dimension-integer-array-into-worksheet/",
    "/import-data/2dimension-integer-array/",
    "/import/2dimension-integer-array/",
  ]
keywords: "Aspose.Cells Cloud, 2次元整数配列のインポート, Excelワークシート, REST API, SDK, Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby, Swift"
description: "Aspose.Cells Cloud REST API を使用すると、2次元整数配列を Excel ワークシートにインポートできます。Android、C#、Go、Java、Node.js、Perl、PHP、Python、Ruby、Swift 用の SDK が提供されています。"
weight: 20
---

この REST API は、**2次元整数配列**を Excel ワークシートにインポートします。

リクエストは multipart コンテンツを含む HTTP リクエストです（[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) または [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html) を参照）。multipart コンテンツの第1パートには `Import2DimensionIntegerArrayOption` データが含まれ、第2パートにはデータファイルが含まれます。

重要なパラメータを以下の表に示します。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### **Import2DimensionIntegerArrayOption**

| パラメータ名         | 型         | 説明                                                                                                                                   |
| ------------------- | ---------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| FirstRow            | int        | データを配置する最初の行の 1 から始まるインデックス。                                                                                   |
| FirstColumn         | int        | データを配置する最初の列の 1 から始まるインデックス。                                                                                   |
| Data                | Integer[,] | インポートする値を含む 2次元整数配列。                                                                                                   |
| DestinationWorksheet | string     | 送信先ワークシート名。                                                                                                                  |
| IsInsert            | string     | データを挿入する場合は `"true"`（既存のセルをずらす）、上書きする場合は `"false"`。                                                      |
| ImportDataType      | string     | データ形式を指定します。サポートされる値: `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`。 |
| Source              | FileSource | `BatchData` パラメータが `null` の場合にデータファイルの場所を示します。                                                                 |

### **例**

```json
{
  "Data": [
    [1, 2],
    [3, 4]
  ],
  "DestinationWorksheet": "Sheet2",
  "FirstRow": 4,
  "FirstColumn": 1,
  "ImportDataType": "TwoDimensionIntArray"
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

| コード | 意味                   | 説明                                                  |
|------|------------------------|-------------------------------------------------------|
| 200  | OK                     | フィルターが正常に適用され、レスポンスに操作の詳細が含まれます。 |
| 400  | Bad Request            | パラメータが不足または無効（例: サポートされていないファイル形式） |
| 401  | Unauthorized           | JWT トークンが無効または不足しています。                  |
| 413  | Payload Too Large      | アップロードされたファイルがサイズ制限を超えています。        |
| 500  | Internal Server Error  | 予期しないサーバーエラーが発生しました。                   |

## SDK を使用した PostImportData API の利用方法

### PostImportData API 仕様

[OpenAPI 仕様](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) は、ウェブブラウザから直接 REST 操作を実行できるパブリックなプログラミングインタフェースを定義しています。

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、開発 speed up が最適な方法です。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧については [GitHub リポジトリ](https://github.com/aspose-cells-cloud) を確認してください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています：

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}