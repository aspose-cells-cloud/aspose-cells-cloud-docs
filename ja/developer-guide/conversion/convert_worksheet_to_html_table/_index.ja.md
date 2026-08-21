---
title: "ワークシートをHTMLテーブルに変換する"
ArticleTitle: "ワークシートをHTMLテーブルに変換する – Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktitle: "ConvertWorksheetToHtmlTable"
type: docs
url: /ja/cells/convert/worksheet/html-table
aliases: []
keywords: "Aspose.Cells, ConvertWorksheetToHtmlTable, HTMLテーブル, API"
description: "ローカルドライブ上のスプレッドシートのワークシートをAspose.Cells Cloudを使用してHTMLテーブルファイルに変換します。"
weight: 100
---

## Aspose.Cells CloudウェブサービスのワークシートをHTMLテーブルに変換する機能

この操作は、ローカルファイルシステムからスプレッドシートファイルを読み取り、指定されたワークシートをHTMLテーブルに変換し、変換結果をファイルストリームとして返します。変換はクラウドサーバー上で完全に実行されるため、クラウドストレージへの中間アップロードは不要です。ロケール設定やパスワードで保護されたワークブックもサポートされます。

### Web APIエンドポイント

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/html-table
```

### **セキュリティと認証**

Aspose.Cells Cloud APIは安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWTトークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名 | 型 | パス/クエリ文字列/HTTPボディ | 説明 |
|--------------|----|-----------------------------|------|
| Spreadsheet | ファイル | FormData | スプレッドシートファイルをアップロードします。 |
| worksheet | 文字列 | クエリ | スプレッドシートのワークシート名。（必須） |
| region | 文字列 | クエリ | スプレッドシートの地域/言語設定（例: `en-US`、`fr-FR`）。数値の書式設定、日付の解析、地域固有の動作に影響を与えます。 |
| password | 文字列 | クエリ | スプレッドシートファイルを開くためのパスワード。 |

### リクエストボディパラメータ

| パラメータ名 | 型 | 説明 |
| ------------ | -- | --- |
| *なし* | *なし* | *JSONボディは不要です。ファイルは multipart/form-data として送信されます。* |

### **レスポンス**

```json
{
  "File": "生成されたHTMLテーブルのバイナリストリーム"
}
```

**レスポンスステータスコード**

| コード | 意味 | 説明 |
|------|------|------|
| 200 | OK | ワークシートがHTMLテーブルに正常に変換され、ファイルストリームとして返されました。 |
| 400 | Bad Request | 無効なリクエストURL、または必須パラメータが不足しています。 |
| 401 | Unauthorized | 認証に失敗したか、資格情報が提供されていません。 |
| 404 | Not Found | ソースファイルにアクセスできません。 |
| 500 | Internal Server Error | スプレッドシートの変換データ取得中に異常が発生しました。 |
| 413 | Payload Too Large | アップロードされたファイルが許容サイズ制限を超えています。 |

## SDKを使用してワークシートをHTMLテーブルに変換する方法

### ワークシートをHTMLテーブルに変換する仕様

[Convert Worksheet To Html Table API仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToHtmlTable)は、パブリックにアクセス可能なプログラミングインターフェースを定義し、ウェブブラウザから直接REST APIを操作できるようにします。

cURLコマンドラインツールを使用してAspose.Cellsウェブサービスに簡単にアクセスできます。以下の例では、cURLを使用してクラウドAPIを呼び出す方法を示しています。

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# セキュアな接続にはHTTPSを使用
curl -v "https://api.aspose.cloud/v4.0/cells/convert/worksheet/html-table?worksheet={worksheet}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "File": "生成されたHTMLテーブルのバイナリストリーム"
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDKの使用

SDKを使用すると、開発を最速で加速できます。SDKは低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDKの完全な一覧については、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHubリポジトリ</a>をご確認ください。

以下のコード例は、さまざまなSDKを使用してAspose.Cells Cloudウェブサービスを呼び出す方法を示しています：
`[TBD]`
---