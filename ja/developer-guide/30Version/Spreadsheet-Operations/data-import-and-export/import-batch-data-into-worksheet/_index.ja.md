---
title: "Excelワークシートにバッチデータをインポート"
second_title: "Document"
linktitle: "バッチデータのインポート"
type: docs
url: /ja/import-batch-data-into-excel/
aliases:
  - /import-batch-data-into-worksheet/
  - /import-data/batch-data/
  - /import/batch-data/
keywords: "Aspose.Cells, Cloud API, バッチデータのインポート, Excel, CSV, JSON, XML, 配列"
description: "Aspose.Cells Cloud REST API を使用して、Excelワークシートにバッチデータ（CSV、JSON、XML、配列）をインポートする方法を学びます。認証、リクエスト／レスポンスの例、SDKスニペット、エラーハンドリングを含みます。"
weight: 19
ArticleTitle: "Excelワークシートにバッチデータをインポート – Aspose.Cells Cloud ドキュメント"
---

この REST API は、Excelワークシートに**バッチデータ**をインポートします。この API はマルチパートリクエストを受け取り、最初のパートには **ImportBatchDataOption** オブジェクトを、2 番目のパートには実際のデータファイル（CSV、JSON、XML など）を含めます。

この操作は、マルチパートコンテンツを含む HTTP リクエストを使用します（[RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) または [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html) を参照）。

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を必要とします。

### ImportBatchDataOption

| パラメータ名           | 型                | 説明                                                                                                                                                                                   |
| ---------------------- | ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **BatchData**          | `List<CellValue>` | 直接書き込まれるセル値のコレクション。                                                                                                                                                |
| **DestinationWorksheet** | `string`          | データをインポートするワークシート名。                                                                                                                                                |
| **IsInsert**           | `bool`            | `true` の場合、データは挿入され、既存のセルはシフトされます。`false` の場合、データは既存のセルを上書きします。                                                                       |
| **ImportDataType**     | `string`          | インポートするデータの形式。許可される値: `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`。 |
| **Source**             | `FileSource`      | **BatchData** が `null` の場合、データファイルの場所を指定します。                                                                                                                     |

### CellValue

| パラメータ名    | 型       | 説明                                              |
| --------------- | -------- | ------------------------------------------------- |
| **rowIndex**    | `int`    | 対象セルのゼロベースの行インデックス。            |
| **columnIndex** | `int`    | 対象セルのゼロベースの列インデックス。            |
| **type**        | `string` | 値のデータ型（例: `int`, `double`, `string`）。   |
| **value**       | `string` | セルに書き込む実際の値。                          |
| **style**       | `Style`  | セルのオプションのスタイル情報。                  |

### FileSource

| パラメータ名       | 型       | 説明                                                           |
| ------------------ | -------- | -------------------------------------------------------------- |
| **FileSourceType** | `string` | ファイルのソース: `InMemoryFiles`, `CloudFileSystem`, `RequestFiles`。 |
| **FilePath**       | `string` | 選択されたソース内でのファイルのパスまたは識別子。             |

### 例（XML）

```xml
<ImportBatchDataOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>IntArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_int_xml.txt</FilePath>
    </Source>
</ImportBatchDataOption>
```

### レスポンス

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP ステータスコード**

| コード | 意味             | 説明                                               |
|------|------------------|----------------------------------------------------|
| 200  | OK               | フィルターが正常に適用された。レスポンスには操作の詳細が含まれます。 |
| 400  | Bad Request      | パラメータが不足または無効（例: 未サポートのファイル形式）。     |
| 401  | Unauthorized     | JWT トークンが無効または不足。                     |
| 413  | Payload Too Large | アップロードされたファイルがサイズ制限を超えています。          |
| 500  | Internal Server Error | 予期しないサーバーエラー。                         |

## SDK を使用した PostImportData API の使用方法

### PostImportData API の仕様

[OpenAPI 仕様](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) は、Web ブラウザから直接 REST 操作を実行できるパブリックなプログラミングインターフェースを定義しています。

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、この機能を最短で統合できます。SDK は低レベルの詳細を処理するため、ビジネスロジックに集中できます。Aspose.Cells Cloud SDK の完全なリストは [GitHub リポジトリ](https://github.com/aspose-cells-cloud) を参照してください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportBatchData.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}