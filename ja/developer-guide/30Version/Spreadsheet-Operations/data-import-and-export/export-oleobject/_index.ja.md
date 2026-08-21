---
title: "OLE オブジェクトのエクスポート – Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktitle: "OLE オブジェクト"
type: docs
url: /export-excel-ole-object/
aliases: [/export/excel-ole-object/]
keywords: "Aspose.Cells, OLE オブジェクト, エクスポート, Excel, クラウド API, PDF, PNG, DOCX, PPTX"
description: "Aspose.Cells Cloud API を使用して Excel ワークブックから OLE オブジェクトをエクスポートします。リクエスト形式、パラメーター、cURL のサンプル、エラーハンドリングについて学びます。"
weight: 20
ArticleTitle: "OLE オブジェクトのエクスポート – Aspose.Cells Cloud API"
---

## **REST API**

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。


### リクエストパラメーター

| パラメーター       | 位置         | 型     | 必須 | 説明                                                                                      |
| ----------------- | ------------ | ------ | ---- | ----------------------------------------------------------------------------------------- |
| `file`            | Form‑data    | file   | はい  | OLE オブジェクトを含む Excel ワークブック (`.xlsx`、`.xls` など)。                          |
| `outputFormat`    | Query        | string | はい  | エクスポートされたオブジェクトの出力形式 (`pdf`、`png`、`jpeg`、`docx`、`pptx`)。           |
| `objectType`      | Query        | string | はい  | 固定値 `oleobject`。                                                                      |


### レスポンス

正常なリクエストは、エクスポートされたファイルの一覧を含む JSON オブジェクトを返します：

```json
{
  "Files": [
    {
      "Filename": "OLESlide.ppt",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "OLEDoc.docx",
      "FileSize": 382,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

**HTTP ステータスコード**

| コード | 意味                      | 説明                                                |
| ------ | ------------------------- | --------------------------------------------------- |
| 200    | OK                        | フィルターが正常に適用され、レスポンスに操作の詳細が含まれます。 |
| 400    | Bad Request               | パラメーターが不足している、または無効です (例: サポートされていないファイル形式)。 |
| 401    | Unauthorized              | JWT トークンが無効または不足しています。               |
| 413    | Payload Too Large         | アップロードされたファイルがサイズ制限を超えています。   |
| 500    | Internal Server Error     | 予期しないサーバーエラーが発生しました。               |
## SDK を使用した PostExport API の使用方法

### PostExport API 仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) はパブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザーから直接 REST 操作を実行できるようにします。

**cURL** コマンドラインツールを使用して、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使ってクラウド API にリクエストを送信する方法を示しています。


```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=oleobject&format=pdf" \
  -H "Authorization: Bearer $ACCESS_TOKEN" \
  -F "file=@MyWorkbook.xlsx" \
  -F "outputFormat=pdf"
```

### OLE オブジェクトとは

**OLE (Object Linking and Embedding)** オブジェクトは、Word ドキュメント、PowerPoint スライド、画像、その他のファイルなどの外部コンテンツを Excel ワークブック内に埋め込むものです。エクスポートすると、埋め込まれたコンテンツが抽出され、要求された出力形式で保存されます。

### エンドポイント概要

`POST https://api.aspose.cloud/v3.0/cells/export?objectType=oleobject&format={outputFormat}`

- `objectType` – `oleobject` に設定する必要があります。
- `format` – 目的の出力形式 (例: `pdf`、`png`、`jpeg`、`docx`、`pptx`)。

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、開発を最も効率的に進められます。SDK は低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}
---