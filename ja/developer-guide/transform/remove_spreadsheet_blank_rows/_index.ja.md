---
title: "スプレッドシートの空白行を削除する"
ArticleTitle: "スプレッドシートの空白行を削除する – Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktitle: "スプレッドシートの空白行を削除する"
type: docs
url: /ja/cells/remove/blank-rows
aliases: []
keywords: "Aspose.Cells, 空白行の削除, スプレッドシート, API"
description: "スプレッドシートファイルからすべての空白行を削除します。"
weight: 100
---

## Aspose.Cells Cloud Web サービスによるスプレッドシートの空白行削除

このメソッドは、データやオブジェクトが一切含まれていない完全に空の行をスプレッドシートから削除します。すべてのシートをスキャンし、すべてのセルが空である行を特定します。この操作はスプレッドシートに対して直接実行されるため、コンテンツが一切ない行のみが削除されます。これによりスプレッドシートをクリーンアップし、不要な空白行を除去して、データをより整理され、管理しやすい状態に保つことができます。この操作を実行する前に、削除された行は復元できないため、スプレッドシートをバックアップしておくことを推奨します。

### Web API エンドポイント

```http
PUT https://api.aspose.cloud/v4.0/cells/remove/blank-rows
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名 | 型     | パス/クエリ文字列/HTTP リクエストボディ | 説明 |
|--------------|--------|-----------------------------------------|------|
| Spreadsheet  | ファイル | FormData                                | スプレッドシートファイルをアップロードします。 |
| outPath      | 文字列   | クエリ                                  | (オプション) ワークブックが保存されるフォルダーパス。デフォルトは null です。 |
| outStorageName | 文字列 | クエリ                              | 出力ファイルのストレージ名。 |
| region       | 文字列   | クエリ                                  | スプレッドシートの地域/言語設定（例: `en-US`、`fr-FR`）。数値の書式設定、日付の解析、地域固有の動作に影響します。 |
| password     | 文字列   | クエリ                                  | スプレッドシートファイルを開くためのパスワード。 |

### リクエストボディパラメータ

| パラメータ名 | 型     | 説明 |
|--------------|--------|------|
| Spreadsheet  | ファイル | スプレッドシートファイルをアップロードします。 |

### **レスポンス**

```json
{
  "ResponseFile": "バイナリファイルストリーム"
}
```

**レスポンスステータスコード**

| コード | 意味 | 説明 |
|--------|------|------|
| 200 | OK | 空白行を削除した処理済みスプレッドシートファイルが返されます。 |
| 400 | Bad Request | URL またはリクエストパラメータが無効です。 |
| 401 | Unauthorized | 認証に失敗したか、認証情報が提供されていません。 |
| 404 | Not Found | ソースファイルにアクセスできません。 |
| 413 | Payload Too Large | リクエストペイロードが許容サイズを超えています。 |
| 500 | Internal Server Error | データの取得中にスプレッドシートに異常が発生しました。 |

## SDK を使用したスプレッドシートの空白行削除の方法

### スプレッドシートの空白行削除の仕様

[スプレッドシートの空白行削除 API 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Transform/RemoveSpreadsheetBlankRows) は、公開可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 通信を実行できるようにします。

cURL コマンドラインツールを使用して、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、cURL を使って Cloud API にリクエストを送信する方法を示しています。

{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}
{< tab tabNum="1" >}
```bash
# 安全な接続には HTTPS を使用
curl -v "https://api.aspose.cloud/v4.0/cells/remove/blank-rows?outPath=outputFolder&outStorageName=MyStorage&region=en-US&password=12345" \
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
  "ResponseFile": "バイナリファイルストリーム"
}
```
{< /tab >}
{< /tabs >}

### Aspose Cells Cloud SDK の使用

SDK を使用すると、開発を最速で加速できます。SDK は低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストについては、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a> をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose Cells Cloud Web サービスを呼び出す方法を示しています：
`[TBD]`
---