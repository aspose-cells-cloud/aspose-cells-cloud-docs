---
title: "テーブルを CSV に変換"
ArticleTitle: "テーブルを CSV に変換 – Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktitle: "テーブルを CSV に変換"
type: docs
url: /ja/cells/convert/table/csv
aliases: []
keywords: "テーブル CSV 変換, Aspose.Cells, クラウド API"
description: "ローカルドライブ上のスプレッドシートのテーブルを CSV ファイルに変換します。"
weight: 1
---

## Aspose.Cells Cloud Web サービスによるテーブルから CSV への変換

このメソッドは、ローカルファイルシステムからスプレッドシートファイルを読み込み、指定されたテーブルを CSV ファイルに変換して、変換結果を返します。この処理は完全にクラウドサーバー上で実行されるため、事前のクラウドストレージへのアップロードは不要です。変換を正しく実行するには、ソースファイルのパスと出力形式を適切に指定し、ソースファイルを読み取るための適切な権限が必要です。ファイルが存在しない、パスにアクセスできない、または変換中にエラーが発生した場合などは、適切な例外が発生します。

### Web API エンドポイント

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/csv
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名   | 型     | Path / クエリ文字列 / HTTP ボディ | 説明 |
|----------------|--------|-----------------------------------|------|
| Spreadsheet    | ファイル | FormData                          | スプレッドシートファイルをアップロードします。 |
| worksheet      | 文字列   | クエリ                            | スプレッドシートのワークシート名。 |
| tableName      | 文字列   | クエリ                            | テーブル名。 |
| outPath        | 文字列   | クエリ                            | (オプション) ワークブックが保存されるフォルダのパス。デフォルトは null です。 |
| outStorageName | 文字列   | クエリ                            | 出力ファイルのストレージ名。 |
| fontsLocation  | 文字列   | クエリ                            | カスタムフォントを使用します。 |
| AutoRowsFit    | 真偽値   | クエリ                            | (オプション) すべてのワークシートの行を自動的に調整します。 |
| AutoColumnsFit | 真偽値   | クエリ                            | (オプション) すべてのワークシートの列を自動的に調整します。 |
| region         | 文字列   | クエリ                            | スプレッドシートの地域/言語設定 (例: `en-US`, `fr-FR`)。数値の書式設定、日付の解析、ロケール固有の動作に影響します。 |
| password       | 文字列   | クエリ                            | スプレッドシートファイルを開くためのパスワード。 |

### リクエストボディパラメータ

| パラメータ名 | 型     | 説明 |
| ------------ | ---- | ---- |
| *なし*       | *なし* | *リクエストボディは不要です。ファイルは multipart/form-data として送信されます。* |

### **レスポンス**

```json
{
  "file": "生成された CSV ファイルのバイナリストリーム"
}
```

**レスポンスステータスコード**

| コード | 意味 | 説明 |
|------|------|------|
| 200 | OK | テーブルの変換が成功し、CSV ファイルが返されました。 |
| 400 | Bad Request | 無効なリクエストパラメータ、または不正な形式の URL。 |
| 401 | Unauthorized | 認証に失敗したか、資格情報が提供されていません。 |
| 404 | Not Found | ソースファイルにアクセスできない、またはファイルが存在しません。 |
| 413 | Payload Too Large | アップロードされたファイルが許容サイズ制限を超えています。 |
| 500 | Internal Server Error | 変換中にスプレッドシートで異常が発生しました。 |

## SDK を使用したテーブルから CSV への変換の使用方法

### テーブルから CSV への変換の仕様

[Convert Table to CSV API 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToCsv) は、パブリックにアクセス可能なプログラミングインターフェースを定義し、ウェブブラウザから直接 REST アクセスを実行できるようにします。

cURL コマンドラインツールを使用すると、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API にリクエストを送信する方法を示しています。

{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}

{< tab tabNum="1" >}

```bash
# セキュアな接続には HTTPS を使用
curl -v "https://api.aspose.cloud/v4.0/cells/convert/table/csv?worksheet={worksheet}&tableName={tableName}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&AutoRowsFit={AutoRowsFit}&AutoColumnsFit={AutoColumnsFit}&region={region}&password={password}" \
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
  "file": "生成された CSV ファイルのバイナリストリーム"
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK の使用

SDK を使用すると、開発を最も迅速に加速できます。SDK は低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストについては、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Cloud Web サービスを呼び出す方法を示しています：
`[TBD]`
---