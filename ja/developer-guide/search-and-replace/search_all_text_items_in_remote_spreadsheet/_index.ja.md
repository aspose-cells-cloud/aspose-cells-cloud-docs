---
title: "SearchAllTextItemsInRemoteSpreadsheet"
ArticleTitle: "SearchAllTextItemsInRemoteSpreadsheet – Aspose.Cells Cloud API"
second_title: "Document"
linktype: "docs"
url: /cells/{name}/search/content/all-textitems
aliases: []
keywords: "検索, テキスト項目, Aspose.Cells"
description: "Aspose.Cells Cloud を使用してリモートスプレッドシート内のすべてのテキスト項目を検索します。"
weight: 100
---

## Aspose.Cells Cloud Web サービスの SearchAllTextItemsInRemoteSpreadsheet

このメソッドは、リモートスプレッドシートファイル内のすべてのテキスト項目を検索します。ワークブックのすべてのシートおよびセルを対象に検索を実行し、検索語の出現箇所を特定します。この操作はクラウド上で実行されるため、ローカルストレージは不要です。ソースファイルを読み込む権限があることを確認してください。ソースファイルにアクセスできない場合や、検索プロセス中にエラー（サポートされていないファイル形式など）が発生した場合は、適切な例外がスローされます。このメソッドは、実装の詳細に応じて、一致箇所の場所（例：シート名、セル座標）を返すことがあります。

### Web API エンドポイント

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/search/content/all-textitems
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名 | 型     | パス/クエリ文字列/HTTP ボディ | 説明 |
|--------------|--------|-------------------------------|------|
| name         | string | パス                          | ワークブックファイルの名前 |
| folder       | string | クエリ                        | ワークブックが格納されているフォルダのパス |
| storageName  | string | クエリ                        | （オプション）カスタムクラウドストレージを使用する場合のストレージ名。省略された場合はデフォルトストレージが使用されます。 |
| region       | string | クエリ                        | スプレッドシートの地域/言語設定（例：`en-US`、`fr-FR`）。数値の書式、日付の解析、ロケール固有の動作に影響します。 |
| password     | string | クエリ                        | スプレッドシートファイルを開くためのパスワード |

### リクエストボディパラメータ

| パラメータ名 | 型   | 説明 |
| ------------ | ---- | ---- |
| [TBD]        |      | [TBD] |

### **レスポンス**

```json
{
  "TextItems": [
    {
      "SheetName": "string",
      "CellAddress": "string",
      "Text": "string"
    }
  ],
  "TotalCount": 0
}
```

**レスポンスステータスコード**

| コード | 意味 | 説明 |
|--------|------|------|
| 200 | OK | リクエストは成功し、レスポンスにはスプレッドシート内で見つかったすべてのテキスト項目が含まれます。 |
| 400 | Bad Request | 無効な URL またはリクエストパラメータ |
| 401 | Unauthorized | 認証に失敗したか、資格情報が提供されていません |
| 404 | Not Found | ソースファイルにアクセスできません |
| 413 | Payload Too Large | リクエストペイロードが許容サイズを超えています |
| 500 | Internal Server Error | スプレッドシートでデータ取得中に異常が発生しました |

## SearchAllTextItemsInRemoteSpreadsheet の SDK を使用する方法

### SearchAllTextItemsInRemoteSpreadsheet の仕様

[SearchAllTextItemsInRemoteSpreadsheet API 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchAllTextItemsInRemoteSpreadsheet) は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 操作を実行できるようにします。

cURL コマンドラインツールを使用して、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API にリクエストを送信する方法を示しています。

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# セキュアな接続に HTTPS を使用
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/search/content/all-textitems?folder={folder}&storageName={storageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "TextItems": [
    {
      "SheetName": "Sheet1",
      "CellAddress": "A1",
      "Text": "Sample text"
    }
  ],
  "TotalCount": 1
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK を使用する

SDK を使用すると、開発を最速で加速できます。SDK は低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストについては、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose Cells Cloud Web サービスを呼び出す方法を示しています：
`[TBD]`
---