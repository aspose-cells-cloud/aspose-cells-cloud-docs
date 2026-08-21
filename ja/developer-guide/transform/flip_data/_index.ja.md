---
title: "FlipData"
ArticleTitle: "FlipData – Aspose.Cells Cloud"
second_title: "ドキュメント"
linktype: "docs"
url: /ja/cells/flip
aliases: []
keywords: "FlipData, 並べ替え, Aspose.Cells"
description: "スプレッドシートファイル内の指定されたデータ範囲を転置します。"
weight: 100
---

## Aspose.Cells Cloud Web サービスの FlipData

この API は、指定されたデータ行列の向きを反転させます。たとえば、3行×2列（3行2列）の範囲は、出力時に2行×3列（2行3列）の範囲になります。これは、さまざまなチャート、レポート、データモデルの入力要件に合わせてデータ構造を再編成する際に一般的に使用されます。

### Web API エンドポイント

```http
PUT https://api.aspose.cloud/v4.0/cells/flip
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメーター

| パラメーター名 | 型      | パス/クエリ文字列/HTTP ボディ | 説明 |
|----------------|---------|-----------------------------|-------------|
| Spreadsheet    | ファイル | FormData                    | スプレッドシートファイルをアップロードします。 |
| worksheet      | 文字列  | クエリ                      | シート名。 |
| cellArea       | 文字列  | クエリ                      | 指定されたデータ範囲。 |
| Horizontal     | 真偽値  | クエリ                      | 水平/垂直反転。既定値: true |
| outPath        | 文字列  | クエリ                      | （オプション）ワークブックが保存されるフォルダーのパス。既定値は null です。 |
| outStorageName | 文字列  | クエリ                      | 出力ファイルのストレージ名。 |
| region         | 文字列  | クエリ                      | スプレッドシートの地域/言語設定（例: `en-US`, `fr-FR`）。数値の書式設定、日付の解析、ロケール固有の動作に影響します。 |
| password       | 文字列  | クエリ                      | スプレッドシートファイルを開くためのパスワード。 |

### リクエストボディパラメーター

| パラメーター名 | 型 | 説明 |
| -------------- | ---- | ----------- |
| *なし* | *該当なし* | *追加の JSON ボディは不要です。ファイルは multipart/form-data として送信されます。* |

### **レスポンス**

```json
{
  "File": "<変換されたワークブックのバイナリストリーム>"
}
```

**レスポンスステータスコード**

| コード | 意味 | 説明 |
|------|---------|-------------|
| 200 | OK | 処理が正常に完了し、変換されたスプレッドシートファイルが返されます。 |
| 400 | Bad Request | 必須パラメーターのいずれかが不足しているか、無効です。 |
| 401 | Unauthorized | 認証に失敗しました。JWT トークンが不足しているか、無効です。 |
| 413 | Payload Too Large | アップロードされたファイルが許容サイズ制限を超えています。 |
| 500 | Internal Server Error | サーバー上で予期しないエラーが発生しました。 |

## SDK を使用した FlipData の利用方法

### FlipData の仕様

[FlipData API 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TransformController/FlipData) は、公開可能なプログラミングインターフェースを定義し、Web ブラウザーから直接 REST 操作を実行できるようにします。

cURL コマンドラインツールを使用して、Aspose.Cells Cloud Web サービスに簡単にアクセスできます。以下の例は、cURL を使ってクラウド API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
# 安全な接続に HTTPS を使用
curl -v "https://api.aspose.cloud/v4.0/cells/flip?worksheet=Sheet1&cellArea=A1:B3&Horizontal=true&outPath=output%2Ffolder&outStorageName=MyStorage&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "File": "<変換されたワークブックのバイナリストリーム>"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose Cells Cloud SDK の使用

SDK を使用すると、開発を最速で加速できます。SDK は低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧については、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリー</a>をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose Cells Cloud Web サービスを呼び出す方法を示しています：
 `[TBD]`
---