---
title: "Aspose.Cells Cloud Web API - スプレッドシートを他の形式に変換する - 無料オンラインツール"
second_title: "ドキュメント"
ArticleTitle: "スプレッドシートを他の形式に変換する方法：ステップ・バイ・ステップ・ガイド"
linktitle: "スプレッドシートの変換"
type: docs
url: /ja/convert-spreadsheet/
keywords: "Aspose, Aspose.Cells, スプレッドシート変換, ExcelからPDF, Excel API, クラウドファイル変換"
description: "Aspose.Cells Cloud API を使用してスプレッドシートファイルを他の形式に変換します。"
weight: 100
---

Aspose.Cells Cloud Web API を使用して、ローカルのスプレッドシート／Excel ファイルを他の形式に変換します。

## **スプレッドシート変換 API**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### **リクエストパラメータ**

| パラメータ名 | 型     | パス／クエリ文字列／HTTP ボディ | 説明                                                                 |
| :----------- | :----- | :------------------------------ | :------------------------------------------------------------------- |
| Spreadsheet  | ファイル | FormData                        | 変換対象のスプレッドシートファイルをアップロードします。             |
| format       | 文字列 | クエリ                          | （必須）出力形式（例："XLSX"、"PDF"、"CSV"）を指定します。           |
| outPath      | 文字列 | クエリ                          | （オプション）変換後のワークブックを保存するフォルダパス。既定値は null。 |
| outStorageName | 文字列 | クエリ                        | 出力ファイルのストレージ名を指定します。                             |
| fontsLocation | 文字列 | クエリ                         | スプレッドシートにカスタムフォントを使用します。                     |
| region       | 文字列 | クエリ                          | スプレッドシートの地域設定を指定します。                             |
| password     | 文字列 | クエリ                          | パスワードで保護されたスプレッドシートファイルを開くためのパスワード。 |

### **レスポンス**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**成功ステータス**

- **200 OK** – 変換が成功し、レスポンスボディに変換後のファイルストリームが含まれます。
- `Content-Type` ヘッダーは、リクエストされた出力形式の MIME タイプ（例：PDF の場合は `application/pdf`）を反映します。

**HTTP ステータスコード**

| コード | 意味               | 説明                                                       |
| ---- | ----------------- | --------------------------------------------------------- |
| 200  | OK                | フィルターが正常に適用され、レスポンスに操作の詳細が含まれます。 |
| 400  | Bad Request       | パラメータが不足または不正（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized      | JWT トークンが不正または不足しています。                     |
| 413  | Payload Too Large | アップロードされたファイルがサイズ制限を超えています。       |
| 500  | Internal Server Error | サーバーで予期しないエラーが発生しました。                 |

## 形式

| **出力形式**                                                                                           | **説明**                                                                                                             |
| :----------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------- |
| <a href="https://docs.fileformat.com/spreadsheet/xls/" rel="noopener noreferrer">XLS</a>               | Excel 95/5.0 - 2003 ワークブック。                                                                                   |
| <a href="https://docs.fileformat.com/spreadsheet/xlsx/" rel="noopener noreferrer">XLSX</a>             | Office Open XML SpreadsheetML ファイル形式。                                                                         |
| <a href="https://docs.fileformat.com/spreadsheet/xlsb/" rel="noopener noreferrer">XLSB</a>             | Excel バイナリワークブック。                                                                                         |
| <a href="https://docs.fileformat.com/spreadsheet/xlsm/" rel="noopener noreferrer">XLSM</a>             | Excel マクロ有効ワークブック。                                                                                       |
| <a href="https://docs.fileformat.com/spreadsheet/xlt/" rel="noopener noreferrer">XLT</a>               | Excel 97 - Excel 2003 テンプレート。                                                                                 |
| <a href="https://docs.fileformat.com/spreadsheet/xltx/" rel="noopener noreferrer">XLTX</a>             | Excel テンプレート。                                                                                                 |
| <a href="https://docs.fileformat.com/spreadsheet/xltm/" rel="noopener noreferrer">XLTM</a>             | Excel マクロ有効テンプレート。                                                                                       |
| <a href="https://docs.fileformat.com/spreadsheet/xlam/" rel="noopener noreferrer">XLAM</a>             | Excel に新しい関数を追加するために使用される、Excel マクロ有効アドインファイル。                                       |
| <a href="https://docs.fileformat.com/spreadsheet/csv/" rel="noopener noreferrer">CSV</a>               | CSV（コンマ区切り値）ファイル。                                                                                      |
| <a href="https://docs.fileformat.com/spreadsheet/tsv/" rel="noopener noreferrer">TSV</a>               | TSV（タブ区切り値）ファイル。                                                                                        |
| <a href="https://docs.fileformat.com/word-processing/txt/" rel="noopener noreferrer">TXT</a>           | 区切り文字付きプレーンテキストファイル。                                                                             |
| <a href="https://docs.fileformat.com/web/html/" rel="noopener noreferrer">HTML</a>                     | HTML 形式。                                                                                                          |
| <a href="https://docs.fileformat.com/web/mhtml/" rel="noopener noreferrer">MHTML</a>                   | MHTML ファイル。                                                                                                     |
| <a href="https://docs.fileformat.com/spreadsheet/ods/" rel="noopener noreferrer">ODS</a>               | ODS（OpenDocument スプレッドシート）。                                                                               |
| SpreadsheetML                                                                                          | Excel 2003 XML ファイル。                                                                                            |
| <a href="https://docs.fileformat.com/spreadsheet/numbers/" rel="noopener noreferrer">Numbers</a>       | Apple の「Numbers」アプリケーション（macOS および iOS 向け iWork スイートの一部）で作成されたドキュメント。             |
| <a href="https://docs.fileformat.com/web/json/" rel="noopener noreferrer">JSON</a>                     | JavaScript オブジェクト表記（JavaScript Object Notation）。                                                           |
| <a href="https://docs.fileformat.com/spreadsheet/dif/" rel="noopener noreferrer">DIF</a>               | データ交換形式（Data Interchange Format）。                                                                          |
| <a href="https://docs.fileformat.com/database/dbf/" rel="noopener noreferrer">DBF</a>                  | .dbf 拡張子のファイルは、dBASE データベース管理システムで使用されるデータベースファイル。                             |
| <a href="https://docs.fileformat.com/pdf/" rel="noopener noreferrer">PDF</a>                           | Adobe ポータブルドキュメントフォーマット（Adobe Portable Document Format）。                                         |
| <a href="https://docs.fileformat.com/page-description-language/xps/" rel="noopener noreferrer">XPS</a> | XML Paper Specification 形式。                                                                                      |
| <a href="https://docs.fileformat.com/page-description-language/svg/" rel="noopener noreferrer">SVG</a> | スケーラブルベクターグラフィックス（Scalable Vector Graphics）形式。                                                 |
| <a href="https://docs.fileformat.com/image/tiff/" rel="noopener noreferrer">TIFF</a>                   | タグ付き画像ファイル形式（Tagged Image File Format）。                                                               |
| <a href="https://docs.fileformat.com/image/png/" rel="noopener noreferrer">PNG</a>                     | ポータブルネットワークグラフィックス（Portable Network Graphics）形式。                                              |
| <a href="https://docs.fileformat.com/image/bmp/" rel="noopener noreferrer">BMP</a>                     | ビットマップ画像形式（Bitmap Image）。                                                                               |
| <a href="https://docs.fileformat.com/image/emf/" rel="noopener noreferrer">EMF</a>                     | 拡張メタファイル形式（Enhanced Metafile）。                                                                          |
| <a href="https://docs.fileformat.com/image/jpeg/" rel="noopener noreferrer">JPEG</a>                   | JPEG は、可逆圧縮を使用して保存される画像形式の一種です。                                                             |
| <a href="https://docs.fileformat.com/image/gif/" rel="noopener noreferrer">GIF</a>                     | グラフィック交換フォーマット（Graphics Interchange Format）。                                                       |
| <a href="https://docs.fileformat.com/word-processing/md/" rel="noopener noreferrer">MARKDOWN</a>       | Markdown ドキュメントを表します。                                                                                    |
| <a href="https://docs.fileformat.com/spreadsheet/sxc/" rel="noopener noreferrer">SXC</a>               | OpenOffice および StarOffice で使用される XML ベースの形式。                                                        |
| <a href="https://docs.fileformat.com/spreadsheet/fods/" rel="noopener noreferrer">FODS</a>             | フラット XML として保存される Open Document 形式。                                                                   |
| <a href="https://docs.fileformat.com/word-processing/docx/" rel="noopener noreferrer">DOCX</a>         | Microsoft Word 文書用の代表的な形式で、XML とバイナリファイルを組み合わせています。                                   |
| <a href="https://docs.fileformat.com/presentation/pptx/" rel="noopener noreferrer">PPTX</a>            | PPTX 形式は、Microsoft PowerPoint の Open XML プレゼンテーションファイル形式に基づいています。                        |
| <a href="https://docs.fileformat.com/database/sql/" rel="noopener noreferrer">SqlScript</a>            | 構造化クエリ言語（Structured Query Language）。                                                                      |
| <a href="https://docs.fileformat.com/web/xhtml/" rel="noopener noreferrer">XHtml</a>                   | XHTML は、XML のマークアップを使用したテキストベースのファイル形式で、HTML 4.0 の再定義を使用します。                  |
| <a href="https://docs.fileformat.com/ebook/epub/" rel="noopener noreferrer">Epub</a>                   | .epub 拡張子のファイルは、出版社および読者向けの標準的な電子書籍形式です。                                              |
| <a href="https://docs.fileformat.com/web/xml/" rel="noopener noreferrer">Xml</a>                       | XML（Extensible Markup Language）は、HTML に似ていますが、タグを使用してオブジェクトを定義します。                     |
| <a href="https://docs.fileformat.com/spreadsheet/ots/" rel="noopener noreferrer">Ots</a>               | Open Document Template Sheet（OTS）ファイル。                                                                       |
| <a href="https://docs.fileformat.com/ebook/azw3/" rel="noopener noreferrer">AZW3</a>                   | AZW は、Amazon が Kindle 端末向けに開発したデジタル電子書籍ファイル形式です。AZW3 は、Kindle Format 8（KF8）としても知られています。 |

## スプレッドシート変換 API の使用例

- **レガシーシステムの移行**：多数のレガシー XLS ファイルを現代的なシステム向けに XLSX に変換します。
- **アーカイブ標準化**：XLS、XLSM、ODS、CSV など、さまざまなスプレッドシート形式をアーカイブ用に単一の形式に正規化します。
- **オフィススイート間の相互運用性**：Excel ファイルを LibreOffice、Google スプレッドシート、Apple Numbers と互換性のある形式に変換します。
- **データソースの正規化**：さまざまなスプレッドシート形式を CSV または JSON に変換し、データベースに取り込みます。
- **ウェブ公開**：財務モデルを HTML に変換し、ウェブで表示します。

## スプレッドシート変換 API を使用する理由

- **開発者に優しい**：Aspose.Cells Cloud は複数の言語向けの SDK ライブラリを提供しており、迅速な開発が可能です。また、包括的なドキュメントも整っています。独自のチャート描画ソリューションを構築する場合と比べ、開発工数が大幅に削減されます。
- **コスト効率が高い**：ワークブックをアップロードせずにテーブルデータを変換できるため、ストレージ容量を節約し、コストを削減できます。
- **幅広い形式対応**：20種類以上のスプレッドシート形式間で変換が可能です。
- **データの正確性と書式を保持**：変換後もデータの正確性と書式を維持します。

## SDK を使用してスプレッドシート変換 API を利用する方法

以下のコード例は、さまざまな SDK を使用してスプレッドシート変換 API を利用する方法を示しています。

### スプレッドシート変換 API の仕様

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertSpreadsheet" rel="noopener noreferrer">スプレッドシート変換 API の仕様</a> はパブリックにアクセス可能なプログラミングインターフェースを定義しており、Web ブラウザから直接 REST API を利用できます。

cURL コマンドラインツールを使用して、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例では、cURL を使用してクラウド API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert?format=pdf \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/file.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="file.pdf"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK を使用する

SDK を使用すると、低レベルの詳細を抽象化できるため、最も迅速に開発が可能です。簡潔なコードでスプレッドシートファイルを他の形式に変換できます。Aspose.Cells Cloud SDK の完全なリストは、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorkbook.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorkbook.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorkbook.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorkbook.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorkbook.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorkbook.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorkbook.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorkbook.go" >}}
{{</tab>}}
{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebAPI",
  "name": "Convert Spreadsheet",
  "description": "Aspose.Cells Cloud を使用してスプレッドシートファイルを他の形式に変換します。",
  "url": "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet",
  "documentation": "https://docs.aspose.cloud/cells/convert-spreadsheet/",
  "targetPlatform": "Web",
  "authenticationType": "OAuth2",
  "operation": [
    {
      "@type": "HttpOperation",
      "httpMethod": "PUT",
      "urlTemplate": "/cells/convert/spreadsheet",
      "description": "スプレッドシートを指定された形式に変換します。"
    }
  ]
}
</script>

---