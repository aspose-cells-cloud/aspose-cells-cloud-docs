---
title: "2 次元文字列配列を Excel ワークシートにインポートする"
second_title: "Document"
linktitle: "2 次元文字列配列のインポート"
type: docs
url: /import-a-2d-string-array-into-excel-worksheet/
aliases:
  [
    "/import-2dimension-string-array-into-excel-worksheet/",
    "/import-2dimension-string-array-into-worksheet/",
    "/import-data/-2dimension-string-array/",
    "/import-data/2dimension-string-array/",
    "/import/2dimension-string-array/",
  ]
keywords: "Aspose.Cells Cloud, 2 次元文字列配列のインポート, Excel, REST API, SDK"
description: "Aspose.Cells Cloud REST API を使用して 2 次元文字列配列を Excel ワークシートにインポートする方法を学びます。リクエスト形式、パラメーターの詳細、および C#、PHP、Ruby 用の SDK コード例を含みます。"
weight: 20
---

この REST API は、**2 次元文字列配列を Excel ワークシートにインポート**します。

リクエストは、マルチパートコンテンツを含む HTTP リクエストです（[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) または [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html) を参照）。マルチパートコンテンツの最初の部分には `Import2DimensionStringArrayOption` データが含まれ、2 番目の部分にはデータファイルが含まれます。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

重要なパラメーターは以下の表に示します。

### **Import2DimensionStringArrayOption**

| パラメーター名         | 型                  | 説明                                                                 |
| ---------------------- | ------------------- | ------------------------------------------------------------------- |
| FirstRow              | int                 | インポートを開始する行の 0 から始まるインデックス。                   |
| FirstColumn           | int                 | インポートを開始する列の 0 から始まるインデックス。                   |
| Data                  | string[,]           | インポートする文字列値を含む 2 次元配列。                             |
| DestinationWorksheet  | string              | インポートされたデータを受け取るワークシートの名前。                 |
| IsInsert              | string (true/false) | **true** の場合、データは挿入され、既存のセルはそれに応じてシフトされます。 |
| ImportDataType        | string              | データ型を指定します。この操作では `TwoDimensionStringArray` を使用します。 |
| Source                | FileSource          | `BatchData` パラメーターが null の場合のデータファイルの場所を示します。   |

### 例：リクエストボディ

```json
{
  "Data": [
    ["1.0", "2.9"],
    ["2.0", "2.1"]
  ],
  "DestinationWorksheet": "Sheet2",
  "FirstRow": 1,
  "FirstColumn": 1,
  "ImportDataType": "TwoDimensionStringArray"
}
```

### 応答

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP ステータスコード**

| コード | 意味                         | 説明                                                    |
|-------|------------------------------|---------------------------------------------------------|
| 200   | OK                           | フィルターが正常に適用され、応答に操作の詳細が含まれます。 |
| 400   | Bad Request                  | パラメーターが不足または無効（例：サポートされていないファイル形式）。 |
| 401   | Unauthorized                 | JWT トークンが無効または不足しています。                 |
| 413   | Payload Too Large            | アップロードされたファイルがサイズ制限を超えています。   |
| 500   | Internal Server Error        | 予期しないサーバーエラーが発生しました。                 |

## SDK を使用した PostImportData API の利用方法

### PostImportData API の仕様

[OpenAPI 仕様](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) は、Web ブラウザから直接 REST 操作を実行できるパブリックなプログラミングインターフェースを定義しています。

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、この機能を統合する最も速い方法です。SDK は低レベルの詳細を抽象化し、ビジネスロジックに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) を参照してください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2String.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}