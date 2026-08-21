---
title: "リモートスプレッドシートですべての変更を受け入れる"
ArticleTitle: "リモートスプレッドシートですべての変更を受け入れる – Aspose.Cells Cloud"
second_title: "ドキュメント"
linktype: "docs"
url: /ja/cells/accept-all-revisions
aliases: [  /ja/cells/accept-all-revisions ]
keywords: "Aspose.Cells, AcceptAllRevisions, リモートスプレッドシート"
description: "リモートスプレッドシートですべての変更履歴（リビジョン）を受け入れ、更新されたワークブックファイルを返します。"
weight: 1000
---

## Aspose.Cells Cloud Web サービスのリモートスプレッドシートですべての変更を受け入れる機能

リモートストレージに保存された指定されたワークブック内の、追跡されたすべての変更（リビジョン）を受け入れます。この操作は、結果のワークブックを別の場所またはストレージにオプションで書き込むことができ、更新されたファイルをバイナリストリームとして返します。

### Web API エンドポイント

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/accept-all-revisions
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名 | 型 | パス／クエリ文字列／HTTP ボディ | 説明 |
|----------------|------|-----------------------------|-------------|
| name | string | パス | リモートストレージに保存されたワークブックファイルの名前。 |
| folder | string | クエリ | （オプション）ワークブックが配置されているストレージ内のフォルダ。 |
| storageName | string | クエリ | （オプション）カスタムクラウドストレージを使用する場合のストレージ名。省略した場合はデフォルトストレージを使用します。 |
| outPath | string | クエリ | （オプション）更新されたワークブックを保存するフォルダパス。デフォルトは null です。 |
| outStorageName | string | クエリ | （オプション）出力ファイルのストレージ名。 |
| fontsLocation | string | クエリ | （オプション）カスタムフォントの場所へのパス。 |
| region | string | クエリ | （オプション）スプレッドシートの地域／言語設定（例: `en-US`, `fr-FR`）。数値書式、日付解析、ロケール固有の動作に影響します。 |
| password | string | クエリ | （オプション）スプレッドシートファイルを開くためのパスワード。 |

### リクエストボディパラメータ

| パラメータ名 | 型 | 説明 |
| -------------- | ---- | ----------- |
| *なし* | *なし* | この操作にはリクエストボディは必要ありません。 |

### **レスポンス**

```json
{
  "File": "更新されたワークブック（例: .xlsx）のバイナリストリーム。レスポンスボディとして返されます。"
}
```

**レスポンスステータスコード**

| コード | 意味 | 説明 |
|------|---------|-------------|
| 200 | OK | すべてのリビジョンを受け入れたワークブックがバイナリファイルストリームとして返されます。 |
| 400 | Bad Request | 必須パラメータが不足している、またはリクエスト形式が無効です。 |
| 401 | Unauthorized | JWT トークンが無効または不足しています。 |
| 413 | Payload Too Large | リクエストが許容されるサイズ制限を超えています。 |
| 500 | Internal Server Error | サーバー上で予期しないエラーが発生しました。 |

## SDK を使用したリモートスプレッドシートでのすべての変更を受け入れる方法

### リモートスプレッドシートですべての変更を受け入れる仕様

[リモートスプレッドシートですべての変更を受け入れる API 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/AcceptAllRevisionsInRemoteSpreadsheet) は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST アクセスを実行できるようにします。

cURL コマンドラインツールを使用して、Aspose Cells Cloud Web サービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API に呼び出しを行う方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
# 安全な接続には HTTPS を使用
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/accept-all-revisions?folder=myFolder&storageName=MyStorage&outPath=output%2Fupdated.xlsx&outStorageName=OutStorage&fontsLocation=%2Fcustom%2Ffonts&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "File": "更新されたワークブック（例: .xlsx）のバイナリストリーム。"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose Cells Cloud SDK の使用

SDK を使用すると、開発を最も迅速に加速できます。SDK は低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストについては、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose Cells Cloud Web サービスを呼び出す方法を示しています：
 `[TBD]`
---