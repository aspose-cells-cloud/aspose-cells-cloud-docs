---
title: "Excel を JSON に変換"
second_title: "ドキュメント"
linktitle: "Excel を JSON に変換"
type: docs
url: /convert-excel-file-to-json-file/
keywords: "Aspose.Cells, Excel to JSON, Cloud API, spreadsheet conversion, REST API"
description: "Aspose.Cells Cloud REST API を使用して Excel スプレッドシートを JSON ファイルに変換する方法を学びます。cURL の例、SDK スニペット (C#、Java、Python)、必要なパラメータ、認証、レスポンス形式を含みます。"
weight: 100
ArticleTitle: "Aspose.Cells Cloud API を使用して Excel を JSON に変換する – クイックガイド"
---


## REST API

この REST API は、スプレッドシートファイルを JSON 形式のファイルに変換します。


```http
POST https://api.aspose.cloud/v3.0/cells/convert/json
```

### セキュリティと認証

Aspose.Cells Cloud API は安全であり、[JWT トークンベースの認証](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)が必要です。

### リクエスト

**クエリパラメータ**

| パラメータ名            | 型     | 説明                                                      |
| ----------------------- | ------ | --------------------------------------------------------- |
| `password`              | 文字列 | Excel ファイルを開くために必要なパスワード（オプション）。     |
| `storageName`           | 文字列 | ファイルが配置されているストレージの名前（オプション）。       |
| `checkExcelRestriction` | 真偽値 | セルを変更する際に Excel 固有の制限を適用するかどうか（オプション）。 |

**リクエストボディパラメータ**

| パラメータ名 | 型   | 説明                                                                                       |
| ------------ | ---- | ------------------------------------------------------------------------------------------ |
| `datafile`   | ファイル | アップロードする Excel ファイル。`multipart/form-data` リクエストの最初のパートとして送信する必要があります。 |

#### cURL の使用例

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/json" \
     -H "Authorization: Bearer $ACCESS_TOKEN" \
     -H "accept: application/json" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@myWorkbook.xlsx"
```

### レスポンス

サービスは **FileInfo** オブジェクトを返します。重要なフィールドは以下の通りです：

| フィールド       | 型      | 説明                                                       |
| --------------- | ------- | ---------------------------------------------------------- |
| `Filename`      | 文字列  | 生成された JSON ファイルの名前（例: `myWorkbook.json`）。   |
| `FileSize`      | 整数    | 生成されたファイルのサイズ（バイト単位）。                  |
| `FileContent`   | 文字列  | JSON ファイルの内容を Base64 エンコードした文字列。実際の JSON を取得するにはデコードしてください。 |

**レスポンスの例**

```json
{
  "Filename": "myWorkbook.json",
  "FileSize": 8423,
  "FileContent": "eyJmb3JtYXR0ZWRfZGF0YSI6IH ... (base64 文字列) ..."
}
```

#### エラー処理

リクエストが失敗した場合、API は以下の構造を持つエラーオブジェクトを返します：

| フィールド    | 型     | 説明                               |
| ----------- | ------ | ---------------------------------- |
| `Code`      | 文字列 | 機械可読なエラー識別子。               |
| `Message`   | 文字列 | エラーの読みやすい説明。              |

よくある HTTP ステータスコード：

- **400** – 不正なリクエスト（例: ファイルが不足している、無効なパラメータ）。
- **401** – 認証エラー（無効または不足しているアクセストークン）。
- **500** – サーバ内部エラー。

**HTTP ステータスコード**

| コード | 意味                | 説明                                             |
|------|---------------------|--------------------------------------------------|
| 200  | OK                  | フィルターが正常に適用され、レスポンスに操作の詳細が含まれます。 |
| 400  | Bad Request         | パラメータが不足または無効（例: サポートされていないファイル形式）。 |
| 401  | Unauthorized        | 無効または不足している JWT トークン。 |
| 413  | Payload Too Large   | アップロードされたファイルがサイズ制限を超えています。 |
| 500  | Internal Server Error | 予期しないサーバ内部エラー。 |
## SDK を使用して PostConvertWorkbookToJson API を利用する方法

### PostConvertWorkbookToJson API の仕様

<a href="https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToJson" rel="noopener noreferrer" title="Aspose.Cells OpenAPI Specification – Convert Workbook to JSON">OpenAPI 仕様</a> は、パブリックに利用可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST による操作を実行できるようにします。

**cURL** コマンドラインツールを使用して、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用して Cloud API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/json" \
     -H "Authorization: Bearer $ACCESS_TOKEN" \
     -H "accept: application/json" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@myWorkbook.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "myWorkbook.json",
  "FileSize": 8423,
  "FileContent": "eyJmb3JtYXR0ZWRfZGF0YSI6IH... (base64 文字列)"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK を使用する

SDK を使用すると、開発を迅速に進めることができます。SDK が低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全なリストについては、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer" title="Aspose.Cells Cloud SDKs on GitHub">GitHub リポジトリ</a> をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスにリクエストを送信する方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToJson.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToJson.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToJson.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToJson.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToJson.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToJson.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToJson.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToJson.go" >}}

{{< /tab >}}

{{< /tabs >}}

## 同様の機能を実装するその他の API

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – 追加設定で Excel ファイルを HTML ファイルとして保存し、結果を指定されたストレージに保存します。
- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – 追加設定で Excel ファイルを HTML ファイルに変換し、結果をレスポンスとして返します。
- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Excel ファイルを取得します。クエリパラメータを使用して、HTML 形式でファイルを取得できます。
---