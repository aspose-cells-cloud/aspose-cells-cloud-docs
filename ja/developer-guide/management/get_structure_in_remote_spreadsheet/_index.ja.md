---
title: "GetStructureInRemoteSpreadsheet"
ArticleTitle: "リモートスプレッドシートの構造を取得する – Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktype: "docs"
url: /cells/{name}/structure
aliases: []
keywords: "Aspose.Cells, GetStructure, スプレッドシート, 構造"
description: "リモートのExcelワークブックの構造メタデータ（ワークシート、テーブル、ピボットテーブル、チャート、図形、その他の主要情報）を取得します。"
weight: 100
---

## Aspose.Cells Cloud Web サービスのリモートスプレッドシートの構造を取得する機能

Excelワークブックのコアメタデータ、ワークシート、テーブル、ピボットテーブル、チャート、図形などの情報を、JObject型のJSONオブジェクトとして構造化し、データエクスポート、APIレスポンス、ログ記録などの用途に使用します。

### Web API エンドポイント

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/structure
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名 | 型 | パス / クエリ文字列 / HTTP ボディ | 説明 |
|--------------|----|----------------------------------|------|
| name | string | Path | スプレッドシートファイルの名前。 |
| folder | string | Query | ファイルが配置されているフォルダ。（オプション） |
| storageName | string | Query | （オプション）カスタムクラウドストレージを使用する場合のストレージ名。省略した場合、デフォルトストレージが使用されます。 |
| region | string | Query | スプレッドシートの地域/言語設定（例: `en-US`, `fr-FR`）。数値書式、日付解析、ロケール固有の動作に影響します。 |
| password | string | Query | スプレッドシートファイルを開くためのパスワード。 |

### リクエストボディパラメータ

| パラメータ名 | 型 | 説明 |
| ------------ | -- | ---- |
| [TBD] | [TBD] | [TBD] |

### **レスポンス**

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
  "WorkbookProperties": {
    "Author": "string",
    "Created": "string",
    "Version": "string"
  },
  "DocumentProperties": {
    "Title": "string",
    "Subject": "string",
    "Keywords": "string"
  }
}
```

**レスポンスステータスコード**

| コード | 意味 | 説明 |
|------|------|------|
| 200 | OK | ワークブックの構造の取得に成功しました。 |
| 400 | Bad Request | 無効なリクエストパラメータです。 |
| 401 | Unauthorized | 認証に失敗したか、トークンがありません。 |
| 413 | Payload Too Large | リクエストペイロードが許容サイズを超えています。 |
| 500 | Internal Server Error | 予期しないサーバーエラーが発生しました。 |

## SDK を使用したリモートスプレッドシートの構造を取得する方法

### リモートスプレッドシートの構造を取得する仕様

[リモートスプレッドシートの構造を取得する API 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetStructureInRemoteSpreadsheet)は、パブリックにアクセス可能なプログラミングインターフェースを定義し、ウェブブラウザから直接 REST 通信を実行できるようにします。

cURL コマンドラインツールを使用して Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例では、cURL を使用してクラウド API に呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
# セキュアな接続に HTTPS を使用
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/structure?folder=myFolder&storageName=MyStorage&region=en-US&password=SecretPwd" \
  -X GET \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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
  "WorkbookProperties": {
    "Author": "John Doe",
    "Created": "2023-01-01T12:00:00Z",
    "Version": "16.0"
  },
  "DocumentProperties": {
    "Title": "SalesReport",
    "Subject": "Quarterly Sales",
    "Keywords": "sales,report,2023"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose Cells Cloud SDK を使用する

SDK を使用すると、開発を最速で加速できます。SDK は低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストについては、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例では、さまざまな SDK を使用して Aspose Cells Cloud ウェブサービスを呼び出す方法を示しています：
`[TBD]`
---