---
title: "GetSpreadsheetStructure"
ArticleTitle: "GetSpreadsheetStructure – Aspose.Cells Cloud"
second_title: "ドキュメント"
linktitle: "GetSpreadsheetStructure"
type: docs
url: /cells/spreadsheet/structure
aliases: []
keywords: "Aspose.Cells, スプレッドシート構造, API"
description: "Excel ブックのコアメタデータ、ワークシート、テーブル、ピボットテーブル、チャート、図形などに関する情報を、JObject 型の JSON オブジェクトとして構造化変換します。"
weight: 1000
---

## Aspose.Cells Cloud Web サービスの GetSpreadsheetStructure

Excel ブックのコアメタデータ、ワークシート、テーブル、ピボットテーブル、チャート、図形などに関する情報を、JObject 型の JSON オブジェクトとして構造化変換し、データエクスポート、API 応答、ログ記録などのシナリオに活用します。

### Web API エンドポイント

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/structure
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名 | 型     | パス/クエリ文字列/HTTP ボディ | 説明 |
|--------------|--------|-------------------------------|------|
| Spreadsheet  | ファイル | FormData (body)               | スプレッドシートファイルをアップロードします。 |
| region       | 文字列   | クエリ                         | スプレッドシートの地域/言語設定（例: `en-US`, `fr-FR`）。数値の書式設定、日付の解析、ロケール固有の動作に影響します。 |
| password     | 文字列   | クエリ                         | スプレッドシートファイルを開くためのパスワードです。 |

### リクエストボディパラメータ

| パラメータ名 | 型   | 説明                 |
|--------------|------|----------------------|
| Spreadsheet  | ファイル | スプレッドシートファイルをアップロードします。 |

### **応答**

```json
{
  "Worksheets": [
    {
      "Name": "Sheet1",
      "Tables": [],
      "PivotTables": [],
      "Charts": [],
      "Shapes": []
    }
  ],
  "DocumentProperties": {
    "Author": "John Doe",
    "Created": "2023-01-01T12:00:00Z"
  }
}
```

**応答ステータスコード**

| コード | 意味             | 説明 |
|--------|------------------|------|
| 200    | OK               | スプレッドシート構造の取得に成功しました。 |
| 400    | Bad Request      | 無効なリクエストパラメータまたはファイル形式です。 |
| 401    | Unauthorized     | 認証に失敗したか、JWT トークンがありません。 |
| 413    | Payload Too Large | アップロードされたファイルが許容サイズ制限を超えています。 |
| 500    | Internal Server Error | サーバー上で予期せぬエラーが発生しました。 |

## SDK を使用して GetSpreadsheetStructure を利用する方法

### GetSpreadsheetStructure の仕様

[GetSpreadsheetStructure API 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetSpreadsheetStructure) は、公開可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 相互通信を実行できるようにします。

cURL コマンドラインツールを使用して、Aspose Cells Cloud Web サービスに簡単にアクセスできます。以下の例では、cURL を使って Cloud API にアクセスする方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="応答" >}}

{{< tab tabNum="1" >}}

```bash
# セキュアな接続に HTTPS を使用
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/structure?region=en-US&password=yourPassword" \
  -X PUT \
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
      "Tables": [],
      "PivotTables": [],
      "Charts": [],
      "Shapes": []
    }
  ],
  "DocumentProperties": {
    "Author": "John Doe",
    "Created": "2023-01-01T12:00:00Z"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose Cells Cloud SDK を使用する

SDK を使用すると、開発を最速で加速できます。SDK は低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧については、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose Cells Cloud Web サービスを呼び出す方法を示しています：
`[TBD]`
---