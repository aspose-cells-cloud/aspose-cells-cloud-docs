---
title: "図形のエクスポート"
second_title: "Document"
linktitle: "Shape"
type: docs
url: /ja/export-excel-shape-to-different-formats/
aliases: [  /ja/export/excel-shape-to-different-formats/ ]
keywords: "図形のエクスポート, Aspose.Cells Cloud, Excel 図形エクスポート, 画像形式, REST API, SDK"
description: "Aspose.Cells Cloud REST API および SDK を使用して Excel 図形をさまざまな画像形式（PNG、GIF、JPEG、BMP、SVG、TIFF、EMF、WMF）にエクスポートする方法を学びます。"
weight: 20
ArticleTitle: "図形のエクスポート – Aspose.Cells Cloud"
---

Excel から図形をエクスポートすると、図解形式のコンテンツをさまざまなプラットフォームやアプリケーション間で再利用できるようになります。**前提条件:** 有効な JWT アクセストークンと、アップロードするソース Excel ファイル。

以下の形式で図形をエクスポートできます：**PNG**、**GIF**、**JPEG**、**BMP**、**SVG**、**TIFF**、**EMF**、**WMF**。

## PostExport API

```http
PUT https://api.aspose.cloud/v3.0/cells/export
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を必要とします。

### リクエストパラメータ

| パラメータ名 | 型     | パス/クエリ文字列/HTTP ボディ | 必須 | 説明 |
|--------------|--------|-------------------------------|------|------|
| file         | file   | formData                      | True | アップロードするファイル |
| objectType   | string | query                         | True | エクスポートするオブジェクトのタイプ。チャートのエクスポートには `chart` を使用します。有効な値には `shape`、`worksheet`、`picture` などがあります。 |
| format       | string | query                         | True | 期待される出力形式。サポートされる値: `png`、`jpeg`、`gif`、`bmp`、`svg`、`tiff`、`emf`、`wmf`、`pdf`。 |

### **リクエストの例**

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/export?objectType=shape&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### レスポンス

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet1_Shapes_0.tif",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    }
    // ... 追加のファイルオブジェクト ...
  ]
}
```

*Base64 エンコードされたファイルペイロードのサイズは、画像の寸法や形式によって数百バイトから数メガバイト程度まで変動します。*

**HTTP ステータスコード**

| コード | 意味                 | 説明 |
|--------|----------------------|------|
| 200    | OK                   | 図形が正常にエクスポートされ、レスポンスにファイル一覧が含まれます。 |
| 400    | Bad Request          | パラメータが不足しているか、無効です。 |
| 401    | Unauthorized         | アクセストークンが無効または不足しています。 |
| 413    | Payload Too Large    | アップロードされたファイルがサイズ制限を超えています。 |
| 500    | Internal Server Error | サーバー側で予期せぬエラーが発生しました。 |

## SDK を使用した PostExport API の利用方法

### PostExport API の仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) はパブリックにアクセス可能なプログラミングインターフェースを定義し、ウェブブラウザから直接 REST 操作を実行できるようにします。

**cURL** コマンドラインツールを使用して、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例では、cURL を使用してクラウド API を呼び出す方法を示しています。

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/export?objectType=shape&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、Aspose.Cells Cloud に対する開発を最速で行えます。SDK は低レベルの詳細を抽象化し、ビジネスロジックに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストについては [GitHub リポジトリ](https://github.com/aspose-cells-cloud) を参照してください。

以下のコード例では、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportShape.go" >}}

{{< /tab >}}

{{< /tabs >}}