---
title: "GetMergedCellsInRemotedWorksheet"
ArticleTitle: "リモートワークシート内の結合セルを取得 – Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktitle: "リモートワークシート内の結合セルを取得"
type: docs
url: /cells/mergedcells/get
aliases: []
keywords: "Aspose Cells, 結合セルの取得, リモートワークシート, API"
description: "スプレッドシート内のリモートワークシートからすべての結合セル領域を取得します。"
weight: 10
---

## Aspose.Cells Cloud Web サービスの GetMergedCellsInRemotedWorksheet

リモートスプレッドシートのワークシートからすべての結合セル領域を取得します。

### Web API エンドポイント

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/mergedcells
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名 | 型     | パス / クエリ文字列 / HTTP ボディ | 説明 |
|--------------|--------|-----------------------------------|------|
| name | string | パス | スプレッドシートのファイル名 |
| worksheet | string | パス | ワークシート名 |
| folder | string | クエリ | スプレッドシートのクラウドストレージ内のパス |
| storageName | string | クエリ | （オプション）カスタムクラウドストレージを使用する場合のストレージ名。省略された場合はデフォルトストレージを使用します。 |
| region | string | クエリ | スプレッドシートの地域/言語設定（例: `en-US`, `fr-FR`）。数値の書式設定、日付の解析、ロケール固有の動作に影響します。 |
| password | string | クエリ | スプレッドシートファイルを開くためのパスワード |

### リクエストボディパラメータ

| パラメータ名 | 型 | 説明 |
| ------------ | -- | --- |
| — | — | *なし* |

### **レスポンス**

```json
[
  {
    "FirstRow": 0,
    "FirstColumn": 0,
    "TotalRows": 2,
    "TotalColumns": 3
  },
  {
    "FirstRow": 5,
    "FirstColumn": 1,
    "TotalRows": 1,
    "TotalColumns": 4
  }
]
```

**レスポンスのステータスコード**

| コード | 意味 | 説明 |
|------|------|------|
| 200 | OK | リクエストは成功し、結合セル領域のリストが返されます。 |
| 400 | Bad Request | URL が無効、またはリクエストパラメータの形式が不正です。 |
| 401 | Unauthorized | 認証に失敗したか、資格情報が提供されていません。 |
| 413 | Payload Too Large | リクエストペイロードが許容サイズを超えています。 |
| 500 | Internal Server Error | スプレッドシートでデータ取得中に異常が発生しました。 |

## SDK を使った GetMergedCellsInRemotedWorksheet の使用方法

### GetMergedCellsInRemotedWorksheet の仕様

[GetMergedCellsInRemotedWorksheet API 仕様書](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetMergedCellsInRemotedWorksheet) はパブリックに公開されたプログラミングインターフェースを定義し、Web ブラウザから直接 REST 操作を実行できるようにします。

cURL コマンドラインツールを使用して Aspose.Cells Web サービスに簡単にアクセスできます。以下の例では、cURL を使って Cloud API にリクエストを送る方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
# 安全な接続には HTTPS を使用
curl -v "https://api.aspose.cloud/v4.0/cells/Sample.xlsx/worksheets/Sheet1/mergedcells?folder=MyFolder&storageName=MyStorage&region=en-US&password=1234" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
[
  {
    "FirstRow": 0,
    "FirstColumn": 0,
    "TotalRows": 2,
    "TotalColumns": 3
  },
  {
    "FirstRow": 5,
    "FirstColumn": 1,
    "TotalRows": 1,
    "TotalColumns": 4
  }
]
```

{{< /tab >}}

{{< /tabs >}}

### Aspose Cells Cloud SDK の使用

SDK を使用すると、開発を最速で加速できます。SDK は低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧については、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例では、さまざまな SDK を使って Aspose Cells Cloud Web サービスを呼び出す方法を示しています：
`[TBD]`
---