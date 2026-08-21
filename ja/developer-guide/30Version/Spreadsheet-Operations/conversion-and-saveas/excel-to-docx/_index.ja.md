---
title: "Excel から Docx へ変換"
second_title: "ドキュメント"
linktitle: "Excel から Docx へ変換"
type: docs
url: /ja/jaconvert-excel-file-to-docx-file/
keywords: "Excel から Docx への変換、Aspose.Cells Cloud、REST API、スプレッドシート変換、ドキュメント生成"
description: "Aspose.Cells Cloud REST API を使用して Excel スプレッドシートを DOCX ドキュメントに変換します。複数の SDK とプログラミング言語をサポートし、シームレスな統合を実現します。"
weight: 90
---

この REST API は、スプレッドシートファイルを DOCX 形式のファイルに変換します。

## REST API

```http
POST https://api.aspose.cloud/v3.0/cells/convert/docx
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

**クエリパラメータ**

| パラメータ名              | 型     | 説明                                                                                       |
| ------------------------ | ------ | ------------------------------------------------------------------------------------------ |
| password                 | string | Excel ファイルを開くために必要なパスワード。                                                 |
| storageName              | string | ファイルが配置されているストレージの名前。                                                   |
| checkExcelRestriction    | bool   | ユーザーがセル関連オブジェクトを変更する際に、Excel ファイルの制限をチェックするかどうかを示します。 |

**リクエストボディパラメータ**

| パラメータ名 | 型        | 説明                                                     |
| ----------- | --------- | -------------------------------------------------------- |
| datafile    | data file | マルチパートリクエストボディの最初のパートに保存されたデータファイル。 |

**レスポンス**

API は、生成された Word ファイルを含む **FileInfo** オブジェクトを返します。

| フィールド          | 型     | 説明                                           |
| ------------------ | ------ | ---------------------------------------------- |
| **Filename**       | string | Word ファイルの名前 (例: `example.docx`)。     |
| **FileSize**       | int    | ファイルサイズ（バイト単位）。                 |
| **FileContent**    | string | Word ファイルの Base64 エンコードされた内容。   |


[FileInfo](/cells/file-info/)

**HTTP ステータスコード**

| コード | 意味                         | 説明                                                                 |
| ------ | ---------------------------- | -------------------------------------------------------------------- |
| 200    | OK                           | フィルターが正常に適用され、レスポンスに操作の詳細が含まれます。     |
| 400    | Bad Request                  | パラメータが不足または無効（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized                 | JWT トークンが無効または不足しています。                             |
| 413    | Payload Too Large            | アップロードされたファイルがサイズ制限を超えています。               |
| 500    | Internal Server Error        | 予期しないサーバーエラーが発生しました。                             |

## SDK を使用した PostConvertWorkbookToDocx API の利用方法

### PostConvertWorkbookToDocx API 仕様

[OpenAPI 仕様](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToDocx) はパブリックにアクセス可能なプログラミングインターフェースを定義し、ウェブブラウザから直接 REST 操作を実行できるようにします。

**cURL** コマンドラインツールを使用して Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例では、cURL を使用してクラウド API にアクセスする方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/docx" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d '{"File":{}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.docx",
  "FileSize": 12345,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK の利用

SDK を使用すると、開発を迅速化できます。SDK が低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToDocx.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToDocx.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToDocx.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToDocx.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToDocx.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToDocx.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToDocx.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToDocx.go" >}}

{{< /tab >}}

{{< /tabs >}}

## この機能を実装するその他の API

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – Excel ファイルを追加設定付きで DOCX ファイルとして保存し、結果を指定されたストレージに保存します。

- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – Excel ファイルをオプション設定付きで DOCX ファイルに変換し、結果をレスポンスとして返します。

- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Excel ワークブックを取得し、オプションパラメータ付きで DOCX ファイルに変換します。

---