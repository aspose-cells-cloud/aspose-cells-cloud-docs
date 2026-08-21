---
title: "画像のエクスポート"
second_title: "ドキュメント"
linktitle: "画像"
type: docs
url: /ja/export-excel-picture-to-different-formats/
aliases: [  /ja/export/excel-picture-to-different-formats/ ]
keywords: "画像のエクスポート, Aspose.Cells Cloud, REST API, Excel, 画像形式, PNG, GIF, JPEG, BMP, SVG, TIFF, EMF, WMF"
description: "Aspose.Cells Cloud REST API を使用して、Excel の画像をさまざまな画像形式にエクスポートします。このサービスは、C#、Java、PHP、Ruby、Node.js、Python、Perl、Go、Swift など複数の言語向けの SDK をサポートしています。"
weight: 20
---

以下の形式で画像をエクスポートできます: [PNG](https://docs.fileformat.com/Image/png/), [GIF](https://docs.fileformat.com/image/gif/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), および [WMF](https://docs.fileformat.com/image/Wmf/)。

## REST API


```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を要求します。


### リクエストパラメータ

| パラメータ        | 位置        | 型     | 必須     | 説明                                                                 |
| ---------------- | ---------- | ------ | -------- | -------------------------------------------------------------------- |
| `file`           | フォームデータ | ファイル | はい      | OLE オブジェクトを含む Excel ワークブック (`.xlsx`、`.xls` など)。        |
| `outputFormat`   | クエリ       | 文字列   | はい      | エクスポートされたオブジェクトの出力形式 (`pdf`、`png`、`jpeg`、`docx`、`pptx`)。 |
| `objectType`     | クエリ       | 文字列   | はい      | 固定値 `oleobject`。                                                 |


### レスポンス

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet6_Pictures_0.tif",
      "FileSize": 21680,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet6_Pictures_1.tif",
      "FileSize": 21286,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet2_Pictures_0.tif",
      "FileSize": 130084,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet2_Pictures_1.tif",
      "FileSize": 120062,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

**HTTP ステータスコード**

| コード | 意味                         | 説明                                                   |
|-------|-----------------------------|--------------------------------------------------------|
| 200   | OK                          | フィルターが正常に適用され、レスポンスに操作の詳細が含まれます。 |
| 400   | Bad Request                 | パラメータが不足または無効です (例: 未サポートのファイル形式)。   |
| 401   | Unauthorized                | JWT トークンが無効または不足しています。                    |
| 413   | Payload Too Large           | アップロードされたファイルがサイズ制限を超えています。          |
| 500   | Internal Server Error       | 予期しないサーバーエラーが発生しました。                      |

## SDK を使用した PostExport API の使い方

### PostExport API の仕様

[OpenAPI 仕様書](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 通信を実行できるようにします。

**cURL** コマンドラインツールを使用することで、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、cURL を使用して Cloud API にリクエストを送信する方法を示しています。


```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=picture&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### Aspose.Cells Cloud SDK の使用

SDK を使用することが開発を最も効率的に進める方法です。SDK が低レベルの詳細を処理するため、プロジェクトのロジックに集中できます。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) を確認してください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportPicture.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportPicture.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportPicture.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportPicture.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportPicture.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportPicture.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportPicture.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportPicture.go" >}}
{{< /tab >}}

{{< /tabs >}}