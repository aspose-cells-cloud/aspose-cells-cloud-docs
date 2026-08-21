---
title: "GetMergedCellsInWorksheet"
ArticleTitle: "ワークシート内の結合セルを取得する – Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktype: "GetMergedCellsInWorksheet"
type: docs
url: /cells/spreadsheet/mergedcells
aliases: []
keywords: "Aspose Cells, 結合セル, ワークシート, API"
description: "ローカルのスプレッドシートワークシートからすべての結合セル領域を取得します。"
weight: 1000
---

## Aspose.Cells Cloud Web サービスのワークシート内の結合セルを取得する機能

ローカルのスプレッドシートワークシートからすべての結合セル領域を取得します。

### Web API エンドポイント

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/mergedcells
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全で、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名 | 型 | パス／クエリ文字列／HTTP ボディ | 説明 |
|--------------|----|-------------------------------|------|
| Spreadsheet | ファイル | FormData | スプレッドシートファイルをアップロードします。 |
| worksheet | 文字列 | クエリ | ワークシート名。 |
| region | 文字列 | クエリ | スプレッドシートの地域／言語設定（例：`en-US`, `fr-FR`）。数値の書式設定、日付の解析、ロケール固有の動作に影響します。 |
| password | 文字列 | クエリ | スプレッドシートファイルを開くためのパスワード。 |

### リクエストボディパラメータ

| パラメータ名 | 型 | 説明 |
| ------------ | -- | ---- |
| N/A | N/A | 本操作では JSON ボディを受け付けません。スプレッドシートファイルは `multipart/form-data` 経由で送信されます。 |

### **レスポンス**

```json
[
  {
    "Column": 1,
    "ColumnCount": 3,
    "Row": 5,
    "RowCount": 2
  },
  {
    "Column": 6,
    "ColumnCount": 2,
    "Row": 10,
    "RowCount": 4
  }
]
```

**レスポンスのステータスコード**

| コード | 意味 | 説明 |
|------|------|------|
| 200 | OK | 結合セル領域の取得に成功しました。 |
| 400 | Bad Request | 1 つ以上のリクエストパラメータが無効または不足しています。 |
| 401 | Unauthorized | 認証に失敗しました。JWT トークンが無効または不足しています。 |
| 413 | Payload Too Large | アップロードされたスプレッドシートが許可されたサイズ制限を超えています。 |
| 500 | Internal Server Error | サーバー上で予期せぬエラーが発生しました。 |

## SDK を使用してワークシート内の結合セルを取得する方法

### ワークシート内の結合セル仕様

[Get Merged Cells In Worksheet API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetMergedCellsInWorksheet) は公開可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 操作を実行できるようにします。

cURL コマンドラインツールを使用して Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、cURL を使って Cloud API にリクエストを行う方法を示しています。

{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}

{< tab tabNum="1" >}

```bash
# セキュアな接続に HTTPS を使用
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/mergedcells?worksheet=Sheet1&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@example.xlsx'
```

{< /tab >}

{< tab tabNum="2" >}

```json
[
  {
    "Column": 1,
    "ColumnCount": 3,
    "Row": 5,
    "RowCount": 2
  },
  {
    "Column": 6,
    "ColumnCount": 2,
    "Row": 10,
    "RowCount": 4
  }
]
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK を使用する

SDK を使用すると、開発を最速で加速できます。SDK は低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧は <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a> をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose Cells Cloud Web サービスを呼び出す方法を示しています：
`[TBD]`
---