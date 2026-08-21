---
title: "スプレッドシート内のすべてのテキスト項目を検索"
ArticleTitle: "スプレッドシート内のすべてのテキスト項目を検索 – Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktitle: "スプレッドシート内のすべてのテキスト項目を検索"
type: docs
url: /cells/search/content/all-textitems
aliases: []
keywords: "Aspose.Cells, 検索, テキスト項目, API"
description: "Aspose.Cells Cloud API を使用してスプレッドシートファイル内のすべてのテキスト項目を検索します。"
weight: 100
---

## Aspose.Cells Cloud Web サービスによるスプレッドシート内のすべてのテキスト項目の検索

このメソッドは、ローカルのスプレッドシートファイル内のすべてのテキスト項目を検索します。ワークブックのすべてのシートおよびセルを対象に検索を実行し、検索語の出現箇所を特定します。この処理はクラウド側で実行されるため、クラウドストレージは不要です。対象ファイルを読み取り可能な権限を持っていることを確認してください。対象ファイルにアクセスできない場合や、検索処理中にエラー（サポートされていないファイル形式など）が発生した場合は、適切な例外がスローされます。このメソッドは、実装の詳細に応じて、マッチ箇所の位置（シート名やセルの座標など）を返す場合があります。

### Web API エンドポイント

```http
PUT https://api.aspose.cloud/v4.0/cells/search/content/all-textitems
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名 | 種類 | パス/クエリ文字列/HTTP ボディ | 説明 |
|----------------|------|-----------------------------|-------------|
| Spreadsheet | ファイル | FormData | スプレッドシートファイルをアップロードします。 |
| region | 文字列 | クエリ | スプレッドシートの地域/言語設定（例: `en-US`, `fr-FR`）。数値の書式設定、日付の解析、ロケール固有の動作に影響します。 |
| password | 文字列 | クエリ | スプレッドシートファイルを開くためのパスワード。 |

### リクエストボディパラメータ

| パラメータ名 | 種類 | 説明 |
| -------------- | ---- | ----------- |
| [TBD] | [TBD] | [TBD] |

### **レスポンス**

```json
{
  "SearchResults": [
    {
      "SheetName": "Sheet1",
      "CellName": "A1",
      "Text": "Sample text"
    }
    // ... その他の項目
  ],
  "TotalCount": 42
}
```

**レスポンスのHTTPステータスコード**

| コード | 意味 | 説明 |
|------|---------|-------------|
| 200 | OK | リクエストは成功し、レスポンスには見つかったすべてのテキスト項目が含まれています。 |
| 400 | Bad Request | URL が無効、またはリクエストパラメータが不正な形式です。 |
| 401 | Unauthorized | 認証に失敗したか、資格情報が提供されていません。 |
| 404 | Not Found | ソースファイルにアクセスできません。 |
| 413 | Payload Too Large | アップロードされたファイルが許容サイズ上限を超えています。 |
| 500 | Internal Server Error | データ取得中にスプレッドシートで異常が発生しました。 |

## SDK を使用したスプレッドシート内のすべてのテキスト項目の検索の方法

### スプレッドシート内のすべてのテキスト項目を検索する仕様

[スプレッドシート内のすべてのテキスト項目を検索する API 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{SearchController}/{SearchSpreadsheetAllTextItems}) は、公開可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 通信を実行できるようにします。

cURL コマンドラインツールを使用すれば、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例では、cURL を使用してクラウド API にリクエストを送信する方法を示しています。

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# セキュアな接続に HTTPS を使用
curl -v "https://api.aspose.cloud/v4.0/cells/search/content/all-textitems?region=en-US&password=myPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "SearchResults": [
    {
      "SheetName": "Sheet1",
      "CellName": "A1",
      "Text": "Sample text"
    }
    // ... その他の項目
  ],
  "TotalCount": 42
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK の使用

SDK を使用すると、開発を最速で加速できます。SDK は低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧については、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例では、さまざまな SDK を使用して Aspose Cells Cloud Web サービスを呼び出す方法を示しています：
 `[TBD]`
---