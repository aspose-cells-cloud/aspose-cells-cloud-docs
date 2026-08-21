---
title: "Excel ファイルをさまざまな形式に変換する"
second_title: "ドキュメント"
linktitle: "スプレッドシートの変換"
type: docs
url: /ja/convert-a-spread-file-to-different-formats/
keywords: "Excel 変換、スプレッドシート変換、Aspose.Cells Cloud、REST API、PDF、CSV、JSON、Markdown、ファイル形式変換"
description: "Aspose.Cells Cloud REST API を使用して、Excel ワークブックを PDF、CSV、JSON、Markdown などのさまざまな形式に変換します。この API は、C#、Java、Python などの言語用の複数の SDK をサポートしています。"
weight: 10
ArticleTitle: "Excel ファイルをさまざまな形式に変換する – Aspose.Cells Cloud API ガイド"
---

この REST API は、Excel ファイルを別の形式に変換します。幅広い出力形式をサポートしており、変換前にページ設定や保存オプションを設定できます。

## PostConvertWorkBook API

```http
POST https://api.aspose.cloud/v3.0/cells/convert
```

この API を使用する前に、有効な JWT トークンを取得し、使用しているプログラミング言語向けの適切な Aspose.Cells Cloud SDK をインストールしてください。

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を必要とします。

## SDK を使用して PostConvertWorkBook API を利用する方法

### PostConvertWorkBook API の仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Workbook/PostConvertWorkBook) は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST による操作を実行できるようにします。

**cURL** コマンドラインツールを使用して、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d {}
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "filename",
  "FileSize": 12345,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK を使用する

SDK を使用すると、開発が最も迅速になります。SDK は低レベルの詳細を抽象化し、プロジェクトの本質的な部分に集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

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
---