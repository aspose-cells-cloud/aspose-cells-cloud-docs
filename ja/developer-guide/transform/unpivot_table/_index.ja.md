---
title: "テーブルのアンピボット"
ArticleTitle: "テーブルのアンピボット – Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktype: "docs"
url: /ja/cells/unpivot/table
aliases: []
keywords: "Aspose.Cells, アンピボット, 変換"
description: "スプレッドシート内の行と列を切り替えます。"
weight: 1
---

## Aspose.Cells Cloud Web サービスのテーブルアンピボット機能

スプレッドシート内の行と列を切り替えます。

### Web API エンドポイント

```http
PUT https://api.aspose.cloud/v4.0/cells/unpivot/table
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名     | 型      | パス/クエリ文字列/HTTP ボディ | 説明                                                                                                    |
|------------------|---------|-----------------------------|----------------------------------------------------------------------------------------------------------|
| Spreadsheet      | ファイル  | FormData                    | スプレッドシートファイルをアップロードします。                                                          |
| worksheet        | 文字列    | クエリ                      | シート名。                                                                                               |
| index            | 整数     | クエリ                      | 指定されたデータ範囲。                                                                                   |
| skipEmptyValue   | 真偽値   | クエリ                      | 空の値をスキップするかどうか（デフォルト: true）。                                                       |
| outPath          | 文字列    | クエリ                      | （オプション）ワークブックが保存されるフォルダパス。デフォルトは null です。                            |
| outStorageName   | 文字列    | クエリ                      | 出力ファイルのストレージ名。                                                                             |
| region           | 文字列    | クエリ                      | スプレッドシートの地域/言語設定（例: `en-US`, `fr-FR`）。数値の書式設定、日付の解析、地域固有の動作に影響します。 |
| password         | 文字列    | クエリ                      | スプレッドシートファイルを開くためのパスワード。                                                         |

### リクエストボディパラメータ

| パラメータ名 | 型   | 説明 |
| ------------ | ---- | ---- |
| N/A          | N/A  | リクエストボディパラメータはありません。 |

### **レスポンス**

```json
{
  "File": "アンピボットされたスプレッドシートのバイナリストリーム"
}
```

**レスポンスのステータスコード**

| コード | 意味     | 説明                             |
|--------|----------|----------------------------------|
| 200    | OK       | アンピボットされたスプレッドシートファイルが返されます。 |
| 400    | Bad Request | 無効なリクエストパラメータです。         |
| 401    | Unauthorized | 認証に失敗しました、または JWT トークンが不足・無効です。 |
| 413    | Payload Too Large | アップロードされたファイルが許容サイズ上限を超えています。 |
| 500    | Internal Server Error | サーバーで予期しないエラーが発生しました。 |

## SDK を使用したテーブルアンピボットの使用方法

### テーブルアンピボットの仕様

[テーブルアンピボット API 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4# /Transform/UnpivotTable) は、公開可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 通信を実行できるようにします。

cURL コマンドラインツールを使用して Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API にリクエストを行う方法を示しています。

{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}

{< tab tabNum="1" >}

```bash
# 安全な接続には HTTPS を使用します
curl -v "https://api.aspose.cloud/v4.0/cells/unpivot/table?worksheet={worksheet}&index={index}&skipEmptyValue={skipEmptyValue}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}" \
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
  "File": "アンピボットされたスプレッドシートのバイナリストリーム"
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK の使用

SDK を使用すると、開発を最速で加速できます。SDK は低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧については、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose Cells Cloud Web サービスを呼び出す方法を示しています：
`[TBD]`
---