---
title: "Excel ワークブックの保存 – Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktitle: "別名で保存"
type: docs
url: /save-an-excel-file-as-other-formats-files/
aliases:
  - /convert-excel-workbook-to-different-file-formats/
  - /saveas-other-formats/
keywords: "Aspose Cells, Excel, 名前をつけて保存, PDF, CSV, JSON, Markdown, REST API"
description: "Aspose.Cells Cloud REST API を使用して、Excel ワークブックを PDF、CSV、JSON、Markdown およびその他の形式で保存します。"
weight: 30
---

この REST API を使用すると、Excel ファイルをさまざまな形式で**保存**できます。  
このエンドポイントを呼び出す前に、有効な OAuth 2.0 アクセストークンを取得し、ソースワークブックが Aspose Cloud ストレージに保存されていることを確認してください。

**前提条件**  
1. JWT アクセストークンを取得し、すべてのリクエストの `Authorization: Bearer <token>` ヘッダーに含めます。  
2. ソースワークブックを Aspose Cloud ストレージにアップロードする（または、既に存在することを確認します）。  
3. ワークブックが配置されているストレージ名とフォルダーパスを把握します。

## PostWorkbookSaveAs API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/saveAs
```

### **セキュリティと認証**

Aspose.Cells Cloud API はセキュアであり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### **パスパラメータ**

| パラメータ名 | タイプ   | 説明                       |
| ------------ | ------ | --------------------------- |
| name         | string | Excel ファイルの名前です。 |

### **クエリパラメータ**

| パラメータ名            | タイプ   | 説明                                                                                      |
| ----------------------- | ------ | ----------------------------------------------------------------------------------------- |
| newfilename             | string | 保存されたドキュメントの新しいファイル名です。                                            |
| isAutoFitRows           | string | true の場合、ワークブック内のすべての行を自動的に調整します。既定値は `false` です。        |
| isAutoFitColumns        | string | true の場合、ワークブック内の列幅を自動的に調整します。既定値は `false` です。             |
| folder                  | string | 元のワークブックが含まれているフォルダーです。                                            |
| storageName             | string | ソースファイルが配置されているストレージの名前です。                                      |
| outStorageName          | string | 出力ファイルを保存するストレージの名前です。                                              |
| checkExcelRestriction   | bool   | セルまたは関連オブジェクトを変更する際に、Excel の制限を強制するかどうかを指定します。       |
| region                  | string | ワークブックに適用される地域設定です。                                                    |
| pageWideFitOnPerSheet   | bool   | 変換時に各ワークシートのページ幅を調整します。                                            |
| pageTallFitOnPerSheet   | bool   | 変換時に各ワークシートのページ高さを調整します。                                          |
| sheetName               | string | 変換するワークシートの名前です。                                                          |
| pageIndex               | string | 指定されたワークシート内での変換対象ページのインデックスです（`sheetName` が必要です）。   |
| onePagePerSheet         | bool   | PDF に変換する際に、ワークシートごとに 1 ページを生成します。                             |

### **リクエストボディパラメータ**

| パラメータ名 | タイプ   | 説明                                                       |
| ------------ | ------ | ---------------------------------------------------------- |
| SaveOptions  | Object | マルチパートリクエストの 2 番目の部分で提供される保存オプションです。 |

**リクエストボディのサンプル（マルチパートリクエストの JSON 部分）**

```json
{
  "SaveOptions": {
    "SaveFormat": "pdf",
    "CompressionLevel": 9
  }
}
```

### レスポンス

API は `SaveResponse` オブジェクトを返します。

```json
{
  "Status": "OK",
  "Code": 200,
  "SaveResult": {
    "Documents": [
      {
        "Name": "sample.pdf",
        "Size": 10240,
        "Folder": "output",
        "Storage": "MyStorage"
      }
    ]
  }
}
```

**HTTP ステータスコード**

| コード | 意味                      | 説明                                             |
|------|---------------------------|--------------------------------------------------|
| 200  | OK                        | フィルターが正常に適用され、レスポンスに操作の詳細が含まれます。 |
| 400  | Bad Request               | パラメータが不足または無効です（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized              | JWT トークンが無効または不足しています。          |
| 413  | Payload Too Large         | アップロードされたファイルがサイズ制限を超えています。 |
| 500  | Internal Server Error     | 予期しないサーバーエラーが発生しました。          |

## SDK を使用した PostWorkbookSaveAs API の利用方法

### PostWorkbookSaveAs API の仕様

[OpenAPI 仕様](https://reference.aspose.cloud/cells/#/Conversion/PostWorkbookSaveAs) は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST による操作を実行できるようにします。

**cURL** を使用して Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/sampleBook.xlsx/SaveAs?newfilename=sample.pdf&isAutoFitRows=true&isAutoFitColumns=true" \
  -H "accept: multipart/form-data" \
  -H "Authorization: Bearer <your_jwt_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "SaveResult": {
    "Documents": [
      {
        "Name": "sample.pdf",
        "Size": 10240,
        "Folder": "output",
        "Storage": "MyStorage"
      }
    ]
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、開発を高速化できます。SDK は低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全なリストについては、<a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookSaveAs.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookSaveAs.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookSaveAs.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookSaveAs.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookSaveAs.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookSaveAs.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookSaveAs.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbookSaveAs.go" >}}

{{< /tab >}}

{{< /tabs >}}

その他の変換シナリオについては、[Excel を PDF に変換する](/convert-excel-to-pdf/) および [Excel を CSV にエクスポートする](/export-excel-to-csv/) ガイドをご参照ください。