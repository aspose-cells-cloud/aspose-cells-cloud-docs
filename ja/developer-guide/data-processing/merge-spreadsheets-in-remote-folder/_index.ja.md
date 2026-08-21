---
title: "リモートフォルダー内の一致するスプレッドシートを統合する"
description: "Aspose Cloud ストレージに保存されたスプレッドシートファイルを1つのファイルに統合します。PDF、CSV、JSON、XLSX、ODS、XPS など、30以上の出力形式をサポートします。"
keywords: "Aspose.Cells, スプレッドシート統合, リモートフォルダー, API, PDF, CSV, JSON, XLSX, ODS, XPS"
weight: 100
type: docs
url: /merge-spreadsheets-in-remote-folder/
---

リモートの Aspose Cloud ストレージフォルダー内にある複数のスプレッドシートファイルを、1つの出力ファイルに統合します。この処理はクラウド上で完全に実行されるため、ソースファイルをローカルにダウンロードする必要がありません。出力形式は30種類以上をサポートしています（PDF、CSV、JSON、XLSX、ODS、XPS など）。

## MergeSpreadsheetsInRemoteFolder API

```http
PUT https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメーター <a id="request-parameters"></a>

| 名前                    | 型      | 位置     | 必須     | 説明                                                                                     |
| ----------------------- | ------- | -------- | -------- | ----------------------------------------------------------------------------------------- |
| **folder**              | 文字列  | クエリ   | **はい**  | ソーススプレッドシートが格納されているクラウドストレージフォルダー。                       |
| **fileMatchExpression** | 文字列  | クエリ   | **はい**  | ファイルを選択するためのパターン（例: `*report*.xlsx`）。ワイルドカード `*` と `?` をサポートします。 |
| **outFormat**           | 文字列  | クエリ   | **はい**  | 期望する出力形式（`PDF`、`CSV`、`JSON`、`XLSX`、`ODS`、`XPS` など）。                       |
| **mergeInOneSheet**     | 真偽値  | クエリ   | **はい**  | `true` – すべてのデータを1つのワークシートに統合します。`false` – 各ソースファイルを別々のワークシートに配置します。 |
| **storageName**         | 文字列  | クエリ   | いいえ   | カスタムストレージ名；省略された場合はプライマリストレージが使用されます。                 |
| **outPath**             | 文字列  | クエリ   | いいえ   | 統合されたファイルの保存先フォルダー。省略された場合はソースフォルダーに保存されます。     |
| **outStorageName**      | 文字列  | クエリ   | いいえ   | 統合されたファイルを書き込むストレージ名。                                                 |
| **fontsLocation**       | 文字列  | クエリ   | いいえ   | カスタムフォントが格納されたフォルダーへのパス（PDF/画像出力に必要）。                     |
| **region**              | 文字列  | クエリ   | いいえ   | 数値・日付・通貨の書式設定に使用するロケール（例: `en-US`、`de-DE`）。                     |
| **password**            | 文字列  | クエリ   | いいえ   | 保護されたソーススプレッドシートを開くためのパスワード。                                   |

## リクエスト例（cURL）<a id="request-example"></a>

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets?folder=MyFolder&fileMatchExpression=*.xlsx&outFormat=PDF&mergeInOneSheet=true" \
     -H "Authorization: Bearer <access_token>" \
     -H "Accept: application/json"
```

### **レスポンス**

```json
{
  "Name": "ResponseFile",
  "DataType": {
    "Identifier": "File",
    "Reference": "Stream"
  }
}
```

ファイルは `FileUrl` から直接ダウンロードするか、`outPath` で指定された場所に保存できます。

**成功レスポンスの詳細**

| ステータスコード | コンテンツタイプ           | 説明                           |
| ---------------- | -------------------------- | ------------------------------ |
| 200 OK           | `application/octet-stream` | 統合されたワークブックファイルのバイナリストリーム。 |
| 202 Accepted     | `application/json`         | `FileUrl`、`FileName` などを含む JSON。 |

**HTTP ステータスコード**

| コード | 意味                 | 説明                                     |
| ------ | -------------------- | ---------------------------------------- |
| 200    | OK                   | フィルター適用が成功；レスポンスに操作の詳細が含まれます。 |
| 400    | Bad Request          | パラメーターが不足または無効（例: サポートされていないファイル形式）。 |
| 401    | Unauthorized         | JWT トークンが無効または不足しています。 |
| 413    | Payload Too Large    | アップロードされたファイルがサイズ制限を超えています。 |
| 500    | Internal Server Error | 予期しないサーバーエラーが発生しました。 |

## SDK を使用してスプレッドシート統合 API を利用する方法

### OpenAPI スペック

<a href="https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheetsInRemoteFolder" rel="noopener noreferrer">OpenAPI スペック</a> により、API の機械可読な記述が提供され、直接 REST リクエストを実行できるようになります。

cURL コマンドラインツールを使用して、Aspose.Cells ウェブサービスへ簡単にアクセスできます。以下の例では、cURL を使ってクラウド API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets?folder=MyFolder&fileMatchExpression=*.xlsx&outFormat=PDF&mergeInOneSheet=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/Book1.xlsx" \
  -F "Spreadsheet=@/path/to/Book2.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 エンコード)",
  "contentType": "MIME タイプ",
  "fileDownloadName": "オプションのファイル名"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK の利用

SDK を利用すると、低レベルの詳細を抽象化してくれるため、開発が最も迅速に行えます。短いコードでスプレッドシートワークシートへデータをインポートできます。Aspose.Cells Cloud SDK の完全な一覧については、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリー</a>をご確認ください。

---