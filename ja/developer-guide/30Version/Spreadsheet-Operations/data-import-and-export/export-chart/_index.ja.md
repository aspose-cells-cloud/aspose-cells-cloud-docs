---
title: "Excel チャートのエクスポート"
second_title: "ドキュメント"
linktitle: "チャート"
type: docs
url: /ja/export-excel-chart-to-different-formats/
aliases: [  /ja/export/excel-chart-to-different-formats/ ]
description: "Aspose.Cells Cloud REST API または SDK を使用して、Excel チャート オブジェクトを PNG、JPEG、PDF、SVG、TIFF、EMF、WMF など、人気のある形式にエクスポートします。認証、cURL の例、および複数の言語向けのコードサンプルが含まれます。"
keywords: "Aspose.Cells, チャートのエクスポート, Excel チャート エクスポート, REST API, cURL, PDF, PNG, JPEG, SVG, TIFF, EMF, WMF, SDK, チャート形式, Aspose Cells Cloud"
weight: 20
ArticleTitle: "Excel チャートのエクスポート – ドキュメント"
---

Excel ワークブックからチャート オブジェクトをさまざまな画像形式やドキュメント形式にエクスポートすることは、レポーティングや公開において一般的な要件です。Aspose.Cells Cloud は、チャートを PNG、JPEG、PDF、SVG、TIFF、EMF、WMF など、人気のある形式に直接変換するシンプルな REST エンドポイントを提供します。

以下の形式にチャートをエクスポートできます：[PNG](https://docs.fileformat.com/Image/png/)、[GIF](https://docs.fileformat.com/image/gif/)、[JPEG](https://docs.fileformat.com/image/jpeg/)、[BMP](https://docs.fileformat.com/image/bmp/)、[SVG](https://docs.fileformat.com/page-description-language/svg/)、[TIFF](https://docs.fileformat.com/image/tiff/)、[EMF](https://docs.fileformat.com/image/emf/)、[WMF](https://docs.fileformat.com/image/Wmf/)、および [PDF](https://docs.fileformat.com/pdf/)。

**前提条件：**  
- 有効なサブスクリプションを持つ Aspose.Cells Cloud アカウント  
- 認証フローによって取得した OAuth 2.0 Bearer トークン (JWT)  
- アップロードするワークブック ファイル（最大サイズ < 50 MB）  

## **REST API**

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエスト パラメータ

| パラメータ名 | 型     | パス/クエリ文字列/HTTP ボディ | 必須 | 説明                                                                                                                       |
|--------------|--------|-------------------------------|------|-----------------------------------------------------------------------------------------------------------------------------|
| file         | file   | formData                      | True | アップロードするファイル                                                                                                    |
| objectType   | string | query                         | True | エクスポートするオブジェクトの種類。チャートをエクスポートする場合は `chart` を指定します。その他の可能な値として `worksheet`、`picture` などがあります。 |
| format       | string | query                         | True | 出力フォーマット。サポートされる値：`png`、`jpeg`、`gif`、`bmp`、`svg`、`tiff`、`emf`、`wmf`、`pdf`。                         |

### **レスポンス**

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_0.tif",
      "FileSize": 10040,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_1.tif",
      "FileSize": 12978,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_2.tif",
      "FileSize": 7002,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_3.tif",
      "FileSize": 11532,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet6_Charts_0.tif",
      "FileSize": 8270,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3_Charts_0.tif",
      "FileSize": 42570,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3_Charts_1.tif",
      "FileSize": 12102,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3_Charts_2.tif",
      "FileSize": 8290,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

**HTTP ステータス コード**

| コード | 意味                         | 説明                                               |
|--------|------------------------------|----------------------------------------------------|
| 200    | OK                           | フィルターが正常に適用された。レスポンスには操作の詳細が含まれます。 |
| 400    | Bad Request                  | パラメータが不足または無効（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized                 | JWT トークンが無効または不足しています。             |
| 413    | Payload Too Large            | アップロードされたファイルがサイズ制限を超えています。 |
| 500    | Internal Server Error        | 予期せぬサーバーエラーが発生しました。               |

## SDK を使用した PostExport API の使い方

### PostExport API の仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) は、パブリックにアクセス可能なプログラミング インターフェースを定義し、ウェブブラウザから直接 REST アクセスを実行できるようにします。

すべてのリクエストには、`Authorization` ヘッダーに有効な OAuth 2.0 Bearer トークンを含める必要があります。以下の例では、**cURL** を使用して API を呼び出し、multipart/form-data を使用してワークブックをアップロードする方法を示しています。

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=chart&format=tiff" \
  -H "Authorization: Bearer {access_token}" \
  -H "Accept: multipart/form-data" \
  -H "Content-Type: multipart/form-data" \
  -H "x-aspose-client: Containerize.Swagger" \
  -F "File=@/path/to/your/workbook.xlsx"
```

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、開発を迅速に進めることができます。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストについては、[GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportChart.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportChart.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportChart.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportChart.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportChart.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportChart.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportChart.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportChart.go" >}}

{{< /tab >}}

{{< /tabs >}}