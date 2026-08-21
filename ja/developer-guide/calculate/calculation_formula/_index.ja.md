---
title: "計算式の計算"
ArticleTitle: "計算式の計算 – Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktitle: "計算式の計算"
type: docs
url: /cells/calculate/formula
aliases: []
keywords: "Aspose Cells, 計算式, スプレッドシート, API"
description: "Aspose.Cells Cloud API を使用してスプレッドシート内の計算式を計算します。"
weight: 100
---

## Aspose.Cells Cloud Web サービスの計算式の計算

アップロードされたスプレッドシートファイルの指定されたワークシート内の計算式を計算し、結果のスプレッドシートをファイルストリームとして返します。この操作は、**region** パラメーターを通じてロケール固有の処理をサポートし、パスワードで保護されたファイルを開くことも可能です。

### Web API エンドポイント

```http
PUT https://api.aspose.cloud/v4.0/cells/calculate/formula
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメーター

| パラメーター名 | 型     | パス/クエリ文字列/HTTP ボディ | 説明 |
|----------------|--------|-----------------------------|-------------|
| Spreadsheet    | ファイル | FormData                    | スプレッドシートファイルをアップロードします。 |
| worksheet      | 文字列 | クエリ                      | 計算式を含むワークシートの名前。 |
| formula        | 文字列 | クエリ                      | 計算する計算式（例: `=SUM(A1:B2)`）。 |
| region         | 文字列 | クエリ                      | スプレッドシートの地域/言語設定（例: `en-US`, `fr-FR`）。数値の書式設定、日付の解析、ロケール固有の動作に影響します。 |
| password       | 文字列 | クエリ                      | スプレッドシートファイルを開くためのパスワード。 |

### リクエストボディパラメーター

| パラメーター名 | 型 | 説明 |
| -------------- | ---- | ----------- |
| [TBD] | [TBD] | [TBD] |

### **レスポンス**

```json
{
  "File": "<結果のスプレッドシートのバイナリストリーム>"
}
```

**レスポンスステータスコード**

| コード | 意味 | 説明 |
|------|---------|-------------|
| 200 | OK | 計算に成功し、結果のスプレッドシートファイルが返されます。 |
| 400 | Bad Request | 1つ以上のリクエストパラメーターが不足しているか、無効です。 |
| 401 | Unauthorized | 認証に失敗したか、JWT トークンが不足しているか無効です。 |
| 413 | Payload Too Large | アップロードされたファイルが許可されたサイズ制限を超えています。 |
| 500 | Internal Server Error | サーバー上で予期せぬエラーが発生しました。 |

## SDK を使用した計算式の計算方法

### 計算式の計算仕様

[計算式の計算 API 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Calculate/CalculationFormula) は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザーから直接 REST アクセスを実行できるようにします。

cURL コマンドラインツールを使用して、Aspose Cells Cloud Web サービスに簡単にアクセスできます。以下の例は、cURL を使用して Cloud API にアクセスする方法を示しています。

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# セキュアな接続には HTTPS を使用
curl -v "https://api.aspose.cloud/v4.0/cells/calculate/formula?worksheet=Sheet1&formula=%3DSUM(A1%3AB2)&region=en-US&password=MyPassword" \
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
  "File": "<結果のスプレッドシートのバイナリストリーム>"
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK の使用

SDK を使用すると、開発を最も速く加速できます。SDK は低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストについては、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリー</a>をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose Cells Cloud Web サービスを呼び出す方法を示しています：
`[TBD]`
---