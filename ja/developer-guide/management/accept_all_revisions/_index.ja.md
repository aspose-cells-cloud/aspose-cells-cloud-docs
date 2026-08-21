---
title: "すべての変更を承認する"
ArticleTitle: "すべての変更を承認する – Aspose.Cells Cloud"
second_title: "ドキュメント"
linktype: "すべての変更を承認する"
type: docs
url: /ja/cells/spreadsheet/accept-all-revisions
aliases: []
keywords: "Aspose.Cells, AcceptAllRevisions, スプレッドシート, 変更履歴"
description: "Aspose.Cells Cloud API を使用してスプレッドシートファイル内のすべての変更を承認します。"
weight: 100
---

## Aspose.Cells Cloud Web サービスの AcceptAllRevisions

アップロードされたスプレッドシートファイル内のすべての変更を承認し、処理済みのワークブックを返します。

### Web API エンドポイント

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/accept-all-revisions
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名 | 型     | パス / クエリ文字列 / HTTP ボディ | 説明 |
|--------------|--------|-----------------------------------|------|
| Spreadsheet  | ファイル | FormData (HTTP ボディ)            | スプレッドシートファイルをアップロードします。 |
| outPath      | 文字列   | クエリ                            | (オプション) ワークブックが保存されるフォルダーパス。既定値は null です。 |
| outStorageName | 文字列 | クエリ                            | 出力ファイルのストレージ名。 |
| fontsLocation | 文字列  | クエリ                            | カスタムフォントを使用します。 |
| region       | 文字列   | クエリ                            | スプレッドシートの地域/言語設定（例: `en-US`, `fr-FR`）。数値の書式設定、日付の解析、ロケール固有の動作に影響を与えます。 |
| password     | 文字列   | クエリ                            | スプレッドシートファイルを開くためのパスワード。 |

### リクエストボディパラメータ

| パラメータ名 | 型   | 説明 |
|--------------|------|------|
| Spreadsheet  | ファイル | スプレッドシートファイルをアップロードします。 |

### **レスポンス**

```json
{
  "File": "処理されたスプレッドシートのバイナリストリーム"
}
```

**レスポンスステータスコード**

| コード | 意味 | 説明 |
|--------|------|------|
| 200 | OK | 変更が正常に承認され、処理済みファイルが返されました。 |
| 400 | Bad Request | リクエストが無効です（例: 必須ファイルが欠落している、または無効なパラメータを含む）。 |
| 401 | Unauthorized | 認証に失敗したか、JWT トークンが欠落または無効です。 |
| 413 | Payload Too Large | アップロードされたファイルが許容サイズ制限を超過しています。 |
| 500 | Internal Server Error | サーバー上で予期しないエラーが発生しました。 |

## SDK を使用して AcceptAllRevisions を利用する方法

### AcceptAllRevisions の仕様

[AcceptAllRevisions API 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/AcceptAllRevisions) は公開可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST アクセスを実行できるようにします。

cURL コマンドラインツールを使用して、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例では、cURL を使って Cloud API にリクエストを送信する方法を示しています。

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# セキュアな接続に HTTPS を使用
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/accept-all-revisions?outPath=outputFolder&outStorageName=MyStorage&fontsLocation=/fonts&region=en-US&password=12345" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@sample.xlsx'
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "File": "処理されたスプレッドシートのバイナリストリーム"
}
```

{< /tab >}

{< /tabs >}

### Aspose.Cells Cloud SDK を使用する

SDK を使用すると、開発を最速で加速できます。SDK は低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストについては、<a href="[TBD]" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例は、さまざまな SDK を使って Aspose.Cells Cloud Web サービスを呼び出す方法を示しています：
`[TBD]`
---