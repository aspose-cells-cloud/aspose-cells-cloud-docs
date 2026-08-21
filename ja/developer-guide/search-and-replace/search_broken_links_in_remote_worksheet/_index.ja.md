---
title: "SearchBrokenLinksInRemoteWorksheet"
ArticleTitle: "リモートワークシート内のBroken Linksを検索 – Aspose.Cells Cloud API"
second_title: "Document"
linktype: "docs"
url: /cells/{name}/worksheets/{worksheet}/search/broken-links
aliases: []
keywords: "Aspose.Cells, Broken Linksの検索, リモートワークシート"
description: "リモートスプレッドシートのワークシート内に存在するBroken Linksを検索します。"
weight: 100
---

## Aspose.Cells Cloud Webサービスのリモートワークシート内Broken Links検索

このメソッドは、リモートクラウドストレージに保存されたスプレッドシートファイルのワークシート内に存在するBroken Linksを検索します。すべてのシートとセルをスキャンし、無効なURLや欠落した外部参照などを指しているハイパーリンクを特定します。この操作はクラウド環境内でリモートで実行され、ファイルをローカルマシンにダウンロードする必要はありません。

### Web APIエンドポイント

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/broken-links
```

### **セキュリティと認証**

Aspose.Cells Cloud APIは安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWTトークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名 | 型 | Path/Query String/HTTP Body | 説明 |
|----------------|------|-----------------------------|-------------|
| name | string | Path | 検索対象のワークブックファイルの名前。 |
| worksheet | string | Path | 検索対象のワークシートを指定。 |
| folder | string | Query | ワークブックが保存されているフォルダのパス。（オプション） |
| storageName | string | Query | （オプション）カスタムクラウドストレージを使用する場合のストレージ名。省略した場合はデフォルトストレージが使用されます。 |
| region | string | Query | スプレッドシートの地域/言語設定（例: `en-US`, `fr-FR`）。数値書式、日付解析、ロケール固有の動作に影響を与えます。 |
| password | string | Query | スプレッドシートファイルを開くためのパスワード。 |

### リクエストボディパラメータ

| パラメータ名 | 型 | 説明 |
| -------------- | ---- | ----------- |
| — | — | この操作にはリクエストボディは不要です。 |

### **レスポンス**

```json
{
  "Links": [
    {
      "SheetName": "Sheet1",
      "CellName": "A1",
      "Url": "http://invalid.example.com"
    }
  ],
  "Count": 1
}
```

**レスポンスステータスコード**

| コード | 意味 | 説明 |
|------|---------|-------------|
| 200 | OK | Broken Linksのリストを正常に取得しました。 |
| 400 | Bad Request | 無効なリクエストパラメータ、または不正なURLです。 |
| 401 | Unauthorized | 認証に失敗したか、資格情報が提供されていません。 |
| 404 | Not Found | ソースファイルにアクセスできません。 |
| 413 | Payload Too Large | リクエストエンティティが大きすぎます。 |
| 500 | Internal Server Error | スプレッドシートでデータ取得中に異常が発生しました。 |

## SDKを使用したリモートワークシート内Broken Links検索の使用方法

### リモートワークシート内Broken Links検索の仕様

[リモートワークシート内Broken Links検索API仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchBrokenLinksInRemoteWorksheet)は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Webブラウザから直接REST APIを実行できます。

cURLコマンドラインツールを使用して、Aspose.Cells Webサービスに簡単にアクセスできます。以下の例は、cURLでCloud APIを呼び出す方法を示しています。

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# セキュアな接続にHTTPSを使用
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/broken-links?folder={folder}&storageName={storageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "Links": [
    {
      "SheetName": "Sheet1",
      "CellName": "A1",
      "Url": "http://invalid.example.com"
    }
  ],
  "Count": 1
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDKの使用

SDKを使用することで、開発を最速で加速できます。SDKは低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDKの完全なリストについては、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHubリポジトリ</a>をご確認ください。

以下のコード例は、さまざまなSDKを使用してAspose Cells Cloud Webサービスを呼び出す方法を示しています：
`[TBD]`
---