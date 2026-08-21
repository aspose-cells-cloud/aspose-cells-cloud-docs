---
title: "Excel を Markdown に変換する"
second_title: "Document"
linktitle: "Excel to Markdown"
type: docs
url: /ja/convert-excel-file-to-markdown-file/
keywords: "Excel, Markdown, 変換, Aspose.Cells Cloud, REST API, Excel から Markdown への変換, Aspose Cells Markdown API, Excel Markdown エクスポート"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークシートを Markdown に変換します。cURL の例、SDK スニペット、必要なパラメーター、認証詳細が含まれます。"
weight: 100
ArticleTitle: "Excel を Markdown に変換する – Aspose.Cells Cloud API ドキュメント"
---

この REST API は、スプレッドシート ファイルを Markdown 形式のファイルに変換します。

## セキュリティと認証
Aspose.Cells Cloud API は安全であり、[JWT トークンベースの認証](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)が必要です。

## REST API

```http
POST https://api.aspose.cloud/v3.0/cells/convert/markdown
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### クエリ パラメーター


| パラメーター名        | 型     | 位置   | 説明                                                                                       |
| --------------------- | ------ | ------ | ------------------------------------------------------------------------------------------ |
| password              | string | query  | Excel ファイルを開くために必要なパスワード。                                               |
| storageName           | string | query  | ファイルが配置されているストレージの名前。                                                 |
| checkExcelRestriction | bool   | query  | セルまたは関連オブジェクトを変更する際に Excel 固有の制限を強制するかどうかを示します。 |
| datafile              | file   | body   | マルチパート コンテンツの最初のパートとしてアップロードされる Excel ファイル。           |

### レスポンス

API は **FileInfo** 型の JSON オブジェクトを返します。

- **FileInfo** – 生成された Markdown ファイルの名前、サイズ、Base64 エンコードされた内容を含むオブジェクト。

```json
{
  "Filename": "example.md",
  "FileSize": 12345,
  "FileContent": "base64_encoded_string"
}
```

### エラー レスポンス

| HTTP コード | 説明                                                       | 例 JSON ボディ                                  |
| ----------- | ---------------------------------------------------------- | ----------------------------------------------- |
| 401         | 認証されていません – トークンが欠落しているか無効です。   | `{"error":"Invalid access token."}`             |
| 400         | 不正なリクエスト – 必須パラメーターが欠落しているか、ファイル形式が無効です。 | `{"error":"The 'datafile' field is required."}` |
| 500         | サーバー内部エラー – 予期せぬサーバーの問題。              | `{"error":"An unexpected error occurred."}`     |



## SDK を使用した PostConvertWorkbookToMarkdown API の使用方法

### PostConvertWorkbookToMarkdown API の仕様

[OpenAPI 仕様](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToMarkdown) はパブリックにアクセス可能なプログラミング インターフェースを定義し、ウェブ ブラウザから直接 REST のやり取りを実行できるようにします。

**cURL** コマンドライン ツールを使用すると、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```shell
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/markdown" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <access_token>" \
     -F "File=@your_excel_file.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.md",
  "FileSize": 12345,
  "FileContent": "base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、開発が最も迅速に行えます。SDK が低レベルの詳細を処理するため、ビジネスロジックに集中できます。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) を参照してください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToMarkdown.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToMarkdown.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToMarkdown.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToMarkdown.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToMarkdown.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToMarkdown.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToMarkdown.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToMarkdown.go" >}}

{{< /tab >}}

{{< /tabs >}}

## この機能を実装するその他の API

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – 追加設定を使用して Excel ファイルを HTML として保存し、結果を保存します。
- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – Excel ファイルを追加オプション付きで HTML に変換し、結果をレスポンスとして返します。
- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Excel ファイルを取得し、オプション設定を使用して HTML に変換できます。
---