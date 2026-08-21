---
title: "ローカルスプレッドシートからワークシートを取得する"
ArticleTitle: "ローカルスプレッドシートからワークシートを取得する – Aspose.Cells Cloud"
second_title: "ドキュメント"
linktitle: "ローカルスプレッドシートからワークシートを取得する"
type: docs
url: /cells/spreadsheet/worksheets
aliases: []
keywords: "Aspose.Cells, ワークシート, ローカルスプレッドシート, API"
description: "現在アクティブなローカルスプレッドシートからワークシートの完全な一覧を取得します。"
weight: 1000
---

## Aspose.Cells Cloud Web サービスの「ローカルスプレッドシートからワークシートを取得する」機能

このエンドポイントは、インタープロセス通信（interop）またはローカル API を介してローカルスプレッドシートアプリケーション（例：Excel）にアクセスし、各ワークシートの名前と種類（例：標準、チャート、マクロ）を収集して、構造化された JSON 配列として返します。通常、ワークシート選択用 UI を構築したり、スプレッドシートの内容を監査する目的で使用されます。

### Web API エンドポイント

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/worksheets
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名 | 種別 | パス／クエリ文字列／HTTP ボディ | 説明 |
|--------------|------|-------------------------------|------|
| Spreadsheet  | ファイル | FormData (HTTP ボディ)        | スプレッドシートファイルをアップロードします。 |
| region       | 文字列 | クエリ                        | スプレッドシートの地域／言語設定（例：`en-US`、`fr-FR`）。数値の書式設定、日付の解析、ロケール固有の動作に影響します。（*省略可*） |
| password     | 文字列 | クエリ                        | スプレッドシートファイルを開くためのパスワード。（*省略可*） |

### リクエストボディパラメータ

| パラメータ名 | 種別 | 説明 |
|--------------|------|------|
| Spreadsheet  | ファイル | スプレッドシートファイルをアップロードします。 |

### **レスポンス**

```json
{
  "Worksheets": [
    {
      "Name": "Sheet1",
      "Id": 0,
      "Type": "Standard"
    },
    {
      "Name": "Chart1",
      "Id": 1,
      "Type": "Chart"
    }
    // ... その他のワークシート
  ]
}
```

**レスポンスステータスコード**

| コード | 意味 | 説明 |
|--------|------|------|
| 200 | OK | ワークシート一覧の取得に成功しました。 |
| 400 | Bad Request | 不正なリクエスト（例：不正な URL 形式、必須データの欠如） |
| 401 | Unauthorized | 認証に失敗した、または認証情報が提供されていません。 |
| 404 | Not Found | ソースファイルにアクセスできません。 |
| 413 | Payload Too Large | アップロードされたファイルが許容サイズ上限を超えています。 |
| 500 | Internal Server Error | スプレッドシートのデータ取得中に異常が発生しました。 |

## SDK を使用した「ローカルスプレッドシートからワークシートを取得する」の使用方法

### ローカルスプレッドシートからワークシートを取得する API 仕様

[「ローカルスプレッドシートからワークシートを取得する」API 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetWorksheetsWithLocalSpreadsheet) は、パブリックに利用可能なプログラミングインタフェースを定義し、Web ブラウザから直接 REST API を利用できます。

cURL コマンドラインツールを使用して Aspose.Cells Cloud Web サービスに簡単にアクセスできます。以下の例は、cURL を使って Cloud API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
# セキュアな接続には HTTPS を使用
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/worksheets?region=en-US&password=yourPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@example.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Worksheets": [
    {
      "Name": "Sheet1",
      "Id": 0,
      "Type": "Standard"
    },
    {
      "Name": "Chart1",
      "Id": 1,
      "Type": "Chart"
    }
    // ... その他のワークシート
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose Cells Cloud SDK の使用

SDK を使用すると、開発を最も迅速に進めることが可能です。SDK は低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようになります。Aspose.Cells Cloud SDK の完全な一覧については、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Cloud Web サービスを呼び出す方法を示しています：
`[TBD]`
---