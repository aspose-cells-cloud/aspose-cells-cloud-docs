---
title: "Excel から PNG へ"
second_title: "Document"
linktitle: "Excel から PNG へ"
type: docs
url: convert-excel-file-to-png-file/
keywords: "Excel から PNG へ, Aspose.Cells Cloud, REST API, スプレッドシート変換, PNG 形式"
description: "Aspose.Cells Cloud REST API を使用して Excel スプレッドシートを PNG 画像に変換します。複数の SDK をサポートし、さまざまなプログラミング言語向けの詳細な例を提供します。"
weight: 90
---

この REST API は、スプレッドシートファイルを PNG 形式に変換します。

## REST API の仕様

```
POST https://api.aspose.cloud/v3.0/cells/convert/png
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全で、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を必要とします。

### **クエリパラメータ**

| パラメータ名          | タイプ   | 説明                                                                 |
| --------------------- | ------ | ------------------------------------------------------------------- |
| password              | string | Excel ファイルを開くために必要なパスワード。                           |
| storageName           | string | ファイルが配置されているストレージの名前。                              |
| checkExcelRestriction | bool   | セルや関連オブジェクトを変更する際に Excel ファイルの制限をチェックするかどうかを指定します。 |

### **リクエストボディパラメータ**

| パラメータ名 | タイプ      | 説明                                                       |
| ------------ | --------- | --------------------------------------------------------- |
| datafile     | data file | マルチパートリクエストの最初のパートに含まれるスプレッドシートファイル。 |

### **レスポンス**

API は、生成された PNG ファイルを含む **FileInfo** オブジェクトを返します。

| フィールド名      | タイプ   | 説明                                          |
| --------------- | ------ | -------------------------------------------- |
| **Filename**    | string | PNG ファイル名（例: `example.png`）          |
| **FileSize**    | int    | ファイルサイズ（バイト単位）。                 |
| **FileContent** | string | PNG ファイルの Base64 エンコードされた内容。   |

[FileInfo](/cells/file-info/)


**HTTP ステータスコード**

| コード | 意味                        | 説明                                               |
|------|-----------------------------|---------------------------------------------------|
| 200  | OK                          | フィルターが正常に適用され、レスポンスに操作の詳細が含まれます。 |
| 400  | Bad Request                 | パラメータが不足している、または無効です（例: 未対応のファイル形式）。 |
| 401  | Unauthorized                | JWT トークンが無効または不足しています。                |
| 413  | Payload Too Large           | アップロードされたファイルがサイズ制限を超えています。       |
| 500  | Internal Server Error       | 予期しないサーバーエラーが発生しました。                |

## SDK を使用した PostConvertWorkbookToPNG API の使用方法

### PostConvertWorkbookToPNG API の仕様

[OpenAPI 仕様](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPNG) は、パブリックにアクセス可能なプログラミングインターフェースを定義し、ウェブブラウザから直接 REST アクセスを実行できるようにします。

**cURL** コマンドラインツールを使用すると、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用して Cloud API にリクエストを行う方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/png" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d {"File":{}}
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "xxxxxx.png",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK を使用する

SDK を使用すると、開発を最速で進めることができます。SDK が低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全なリストは [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPNG.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPNG.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPNG.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPNG.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPNG.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToPNG.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPNG.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPNG.go" >}}

{{< /tab >}}

{{< /tabs >}}

## 同様の機能を実装するその他の API

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – Excel ファイルを CSV（またはその他の形式）で保存し、追加設定を適用して結果を保存します。
- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – Excel ファイルを CSV（またはその他の形式）に変換し、オプションパラメータを指定してレスポンスで結果を返します。
- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Excel ファイルを取得し、必要に応じて CSV（またはその他の形式）に動的に変換します。