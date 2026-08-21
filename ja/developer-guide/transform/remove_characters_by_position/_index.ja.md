---
title: "位置に基づいて文字を削除する"
ArticleTitle: "位置に基づいて文字を削除する – Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktitle: "位置に基づいて文字を削除する"
type: docs
url: /ja/cells/content/remove/characters-by-position
aliases: []
keywords: "Aspose.Cells, 文字削除, API"
description: "スプレッドシート内でセルから位置に基づいて文字を削除します。"
weight: 100
---

## Aspose.Cells Cloud Web サービスの「位置に基づいて文字を削除する」機能

ターゲット範囲内のすべてのセルから、位置（先頭/末尾の N 文字、特定の部分文字列の前/後、または2つの区切り文字の間）に基づいて文字を削除し、数式、書式設定、データ検証を保持します。

### Web API エンドポイント

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/characters-by-position
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名                | 型      | パス/クエリ文字列/HTTP ボディ | 説明                                                                                                    |
|----------------------------|---------|-------------------------------|--------------------------------------------------------------------------------------------------------|
| Spreadsheet                | ファイル | FormData                      | スプレッドシートファイルをアップロードします。                                                        |
| theFirstNCharacters        | 整数    | クエリ                        | 選択されたセルから先頭の n 文字を削除することを指定します。省略可能です。                             |
| theLastNCharacters         | 整数    | クエリ                        | 選択されたセルから末尾の n 文字を削除することを指定します。省略可能です。                             |
| allCharactersBeforeText    | 文字列  | クエリ                        | 指定された部分文字列の前にあるテキストを削除します。省略可能です。                                    |
| allCharactersAfterText     | 文字列  | クエリ                        | 指定された部分文字列の後のテキストを削除します。省略可能です。                                        |
| caseSensitive              | 真偽値  | クエリ                        | `Substring` モードおよび `CustomChars` を有効にした場合に影響します。省略可能です。                  |
| worksheet                  | 文字列  | クエリ                        | スプレッドシートのワークシートを指定します。省略可能です。                                            |
| range                      | 文字列  | クエリ                        | スプレッドシートのワークシート範囲を指定します（例: `A1:B10`）。省略可能です。                        |
| outPath                    | 文字列  | クエリ                        | (省略可能) ワークブックが保存されるフォルダパス。デフォルトは null です。省略可能です。              |
| outStorageName             | 文字列  | クエリ                        | 出力ファイルのストレージ名。省略可能です。                                                            |
| region                     | 文字列  | クエリ                        | スプレッドシートの地域/言語設定（例: `en-US`, `fr-FR`）。省略可能です。                               |
| password                   | 文字列  | クエリ                        | スプレッドシートファイルを開くためのパスワード。省略可能です。                                        |

### リクエストボディパラメータ

| パラメータ名 | 型     | 説明                   |
|-------------|--------|------------------------|
| Spreadsheet | ファイル | スプレッドシートファイルをアップロードします。 |

### **レスポンス**

```json
{
  "status": "OK",
  "message": "文字が正常に削除されました。",
  "downloadUrl": "https://api.aspose.cloud/v4.0/storage/file/sample_output.xlsx"
}
```

**レスポンスステータスコード**

| コード | 意味 | 説明 |
|--------|------|------|
| 200 | OK | 操作が正常に完了し、処理されたファイルが返されます。 |
| 400 | Bad Request | リクエストが不正な形式であるか、無効なパラメータを含んでいます。 |
| 401 | Unauthorized | 認証に失敗したか、JWT トークンが不足しているか無効です。 |
| 413 | Payload Too Large | アップロードされたファイルが許可されたサイズ制限を超えています。 |
| 500 | Internal Server Error | サーバー側で予期しないエラーが発生しました。 |

## SDK を使用した「位置に基づいて文字を削除する」の使用方法

### Remove Characters By Position の仕様

[Remove Characters By Position API 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveCharactersByPosition) は、パブリックにアクセス可能なプログラミングインタフェースを定義し、ウェブブラウザから直接 REST 操作を実行できるようにします。

cURL コマンドラインツールを使用して Aspose.Cells Cloud Web サービスに簡単にアクセスできます。以下の例は、cURL を使って Cloud API にリクエストを送信する方法を示しています。

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# セキュアな接続には HTTPS を使用
curl -v "https://api.aspose.cloud/v4.0/cells/content/remove/characters-by-position?theFirstNCharacters=5&worksheet=Sheet1&range=A1%3AB10" \
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
  "status": "OK",
  "message": "文字が正常に削除されました。",
  "downloadUrl": "https://api.aspose.cloud/v4.0/storage/file/sample_output.xlsx"
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK の使用

SDK を使用すると、開発を最速で加速できます。SDK は低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧については、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose Cells Cloud Web サービスを呼び出す方法を示しています：
`[TBD]`
---