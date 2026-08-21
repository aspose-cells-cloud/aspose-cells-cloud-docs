---
title: "Aspose.Cells Cloud – ExcelワークブックをPDF、CSV、HTMLなどに変換する（GET /cells/{name}）"
second_title: "ドキュメント"
linktitle: "Excelの変換"
type: docs
url: /ja/get-different-formats-files/
aliases:
  - /export-excel-workbook-to-different-file-formats/
  - /export-different-formats/
keywords: "Aspose.Cells, Excel変換, Excel変換, PDF, CSV, HTML, ODS, JSON, 画像形式, スプレッドシートエクスポート, API, REST"
description: "Aspose.Cells Cloud REST API を使用して、Excelワークブックを任意の形式（PDF、CSV、HTML、PNGなど）で取得する方法を学びます。cURL、SDKサンプル、認証、レスポンス詳細を含みます。"
weight: 10
ArticleTitle: "Aspose.Cells Cloud – ExcelワークブックをPDF、CSV、HTMLなどに変換する（GET /cells/{name}）"
---

このREST APIは、Excelワークブックを別の形式で取得します。

## GetWorkBook API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}
```

### **セキュリティと認証**

Aspose.Cells Cloud APIは安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWTトークンベースの認証</a>が必要です。

### **クエリパラメータ**

| パラメータ名          | 型     | 説明                                                                                                                                                                    | デフォルト値 |
| --------------------- | ------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ |
| format                | 文字列 | 変換先のファイル形式（例：CSV、XLS、HTML、MHTML、ODS、PDF、XML、TXT、TIFF、XLSB、XLSM、XLSX、XLTM、XLTX、XPS、PNG、JPG、GIF、EMF、BMP、MD、Numbers、WMF、SVGなど）。 | –            |
| password              | 文字列 | Excelファイルを開くために必要なパスワード。                                                                                                                             | –            |
| isAutoFit             | 真偽値 | 行と列の幅を自動調整します。                                                                                                                                            | false        |
| onlySaveTable         | 真偽値 | **true**の場合、テーブルデータのみを保存します。`true`または`false`を指定できます。                                                                                    | false        |
| outPath               | 文字列 | 結果を保存するパス。単一ファイルの場合はファイル名と拡張子を含め、複数ファイルの場合はフォルダのみを指定します。                                                         | –            |
| outStorageName        | 文字列 | 出力ファイルを保存するストレージの名前。                                                                                                                                | –            |
| checkExcelRestriction | 真偽値 | セルや関連オブジェクトを変更する際、Excelの制限をチェックします。                                                                                                        | false        |
| region                | 文字列 | ワークブックに適用される地域設定。                                                                                                                                      | –            |
| pageWideFitOnPerSheet | 真偽値 | PDF変換時に、各ワークシートのページ幅をフィットさせます。                                                                                                               | false        |
| pageTallFitOnPerSheet | 真偽値 | PDF変換時に、各ワークシートのページ高さをフィットさせます。                                                                                                             | false        |
| onePagePerSheet       | 真偽値 | 各ワークシートごとに1枚のPDFページを生成します。                                                                                                                        | false        |
| folder                | 文字列 | 元のワークブックが存在するフォルダのパス。                                                                                                                              | –            |
| storageName           | 文字列 | ソースファイルが保存されているストレージの名前。                                                                                                                        | –            |

### レスポンス

**成功 (200)**

- `format`クエリパラメータを省略した場合、APIはワークブック構造情報を含む**[Workbook](/cells/workbook/)**オブジェクトを返します。

- `format`クエリパラメータでファイル形式を指定した場合、APIは要求された形式で変換されたファイルを返します。

```http
HTTP/1.1 200 OK
Content-Type: application/pdf
Content-Disposition: attachment; filename="book1.pdf"
Content-Length: 123456

(バイナリPDFデータ)
```

**HTTPステータスコード**

| コード | 意味                     | 説明                                                                 |
| ------ | ------------------------ | -------------------------------------------------------------------- |
| 200    | OK                       | フィルターが正常に適用され、レスポンスには操作の詳細が含まれます。   |
| 400    | Bad Request              | パラメータが不足または無効（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized             | JWTトークンが無効または不足しています。                              |
| 413    | Payload Too Large        | アップロードされたファイルがサイズ制限を超えています。               |
| 500    | Internal Server Error    | 予期せぬサーバーエラーが発生しました。                               |

> **注意事項:**  
> - 大きなワークブックの変換には時間がかかる場合があります。その場合はリクエストのタイムアウト時間を延長することを検討してください。  
> - 一部の形式（例：`ODS`）は、マクロなどの特定のExcel機能をサポートしていません。

## SDK を使用して GetWorkBook API を利用する方法

> **前提条件:**  
> - Aspose.Cellsの認証フローを通じて取得した有効な**JWTアクセストークン**。  
> - ソースワークブックは、サポートされているAsposeストレージに保存されているか、リクエスト内で直接渡されていること。  
> - APIバージョン（`v3.0`）が最新リリースバージョンと一致していることを確認してください。

### GetWorkBook APIの仕様

<a href="https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook" rel="noopener noreferrer">OpenAPI仕様</a>はパブリックに利用可能なプログラミングインターフェースを定義し、ウェブブラウザから直接REST APIとやり取りできるようにします。

### 例：リクエスト

**cURL**コマンドラインツールを使用してAspose.Cellsウェブサービスにアクセスできます。以下の例は、必要な認証ヘッダーを含む正しいGETリクエストを示しています。

{{< tabs tabTotal="1" tabID="11" tabName11="Request" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=pdf" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger"
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDKの使用

SDKを使用すると、開発が最も迅速に行えます。SDKは低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDKの完全な一覧については、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHubリポジトリ</a>を確認してください。

以下のコード例は、さまざまなSDKを使用してAspose.Cellsウェブサービスを呼び出す方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}

**関連リンク**

- <a href="https://apireference.aspose.cloud/cells/#/Workbook/ConvertWorkbook" rel="noopener noreferrer">ワークブックの変換（POST）</a>  
- <a href="https://apireference.aspose.cloud/cells/#/Workbook/SaveAs" rel="noopener noreferrer">名前をつけて保存（GET）</a>

---

**最終更新日：2024-12-01**

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Aspose.Cells Cloud – ExcelワークブックをPDF、CSV、HTMLなどに変換する（GET /cells/{name}）",
  "description": "Aspose.Cells CloudのGET /cells/{name}エンドポイントに関するドキュメント。ExcelワークブックをPDF、CSV、HTMLなどさまざまな形式に変換します。",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2024-12-01",
  "keywords": "Aspose.Cells, Excel変換, PDF, CSV, HTML, API, REST, クラウド",
  "url": "https://docs.aspose.cloud/cells/get-different-formats-files/",
  "publisher": {
    "@type": "Organization",
    "name": "Aspose"
  }
}
</script>