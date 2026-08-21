---
title: "高度な Excel ファイル変換"
second_title: "ドキュメント"
linktype: "高度な変換"
type: docs
url: /ja/advanced-convert-excel/
keywords: "Aspose.Cells, Excel 変換, クラウド API, SDK"
description: "Aspose.Cells Cloud REST API は、Excel ワークブックを幅広い形式 (PDF、HTML、CSV など) に変換する強力な機能を提供します。ページ設定、保存オプション、印刷設定の詳細な制御が可能です。SDK は Android、C#、Go、Java、Node.js、Perl、PHP、Python、Ruby、Swift で提供されており、複数のプラットフォーム間でシームレスな統合が実現できます。"
weight: 50
ArticleTitle: "高度な Excel ファイル変換 – Aspose.Cells Cloud API ガイド"
---

## Excel 変換のための高度なクラウド API

高度な変換操作 (Advanced Convert) を使用すると、Excel ワークブックをさまざまな出力形式 (PDF、HTML、CSV など) に変換しながら、ページ設定、保存オプション、印刷設定を細かく制御できます。

**前提条件 / 認証**  
このエンドポイントを使用するには、Aspose.Cells Cloud からアクセストークンを取得し、`Authorization` ヘッダーにベアラートークンとして含める必要があります。

**API リファレンス**  
- **メソッド:** `PUT`  
- **エンドポイント:** `/cells/convert`  
- **パラメーター:**  
  - `format` (文字列、必須) – 期待される出力形式 (例: `pdf`、`html`)  
  - `outPath` (文字列、オプション) – 変換後のファイルをクラウドストレージ内に保存するパス  
  - `options` (オブジェクト、オプション) – `pageSetup`、`saveOptions`、`printSettings` などの高度な変換オプションを含む JSON オブジェクト  
- **リクエスト本文の例:**  
  ```json
  {
    "format": "pdf",
    "outPath": "output/converted.pdf",
    "options": {
      "pageSetup": {
        "orientation": "Landscape",
        "paperSize": "A4"
      },
      "saveOptions": {
        "compress": true
      },
      "printSettings": {
        "printHeadings": false
      }
    }
  }
  ```  
- **レスポンス:**  
  - `200 OK` – 変換が成功し、レスポンスに変換されたファイルのストリームまたは保存されたファイルへの参照が含まれます  
  - `400 Bad Request` – 無効なパラメーターまたは不正な形式のリクエスト本文  
  - `401 Unauthorized` – 認証失敗またはトークンがありません  
  - `500 Internal Server Error` – 変換中のサーバーサイドエラー  

**HTTP ステータスコード**

| コード | 意味                         | 説明                                             |
|--------|------------------------------|--------------------------------------------------|
| 200    | OK                           | フィルターが正常に適用され、レスポンスに操作の詳細が含まれます |
| 400    | Bad Request                  | パラメーターが不足している、または無効です (例: サポートされていないファイル形式) |
| 401    | Unauthorized                 | JWT トークンが無効または不足しています |
| 413    | Payload Too Large            | アップロードされたファイルがサイズ制限を超えています |
| 500    | Internal Server Error        | 予期せぬサーバーエラーが発生しました |

**注意事項**  
* 一部の出力形式には固有の制限があります (例: HTML 変換ではマクロが保持されません)。詳細については、各形式のドキュメントを確認してください。

### スプレッドシートファイルを複数のデータソースから読み込む機能

### ページ設定と保存オプションの設定

## クラウド SDK ファミリー

SDK を使用すると、低レベルの詳細な処理が抽象化されるため、開発を加速し、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全な一覧については、<a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub リポジトリ</a>をご覧ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context":"https://schema.org",
  "@type":"WebAPI",
  "name":"Aspose.Cells Cloud 高度な変換",
  "description":"Excel ワークブックを PDF/HTML/CSV に高度なオプションで変換します。",
  "url":"https://api.aspose.cloud/v3.0/cells/convert",
  "documentation":"https://docs.aspose.cloud/cells/ja/advanced-convert-excel/",
  "endpointDescription":"PUT /cells/convert",
  "input":{
    "@type":"PropertyValueSpecification",
    "valueRequired":true,
    "valueName":"format",
    "description":"期待される出力形式 (pdf, html, csv, …)"
  },
  "target":{
    "@type":"EntryPoint",
    "urlTemplate":"https://api.aspose.cloud/v3.0/cells/convert?format={format}",
    "httpMethod":"PUT"
  }
}
</script>
---