---
title: "TransposeData"
ArticleTitle: "TransposeData – Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktitle: "TransposeData"
type: docs
url: /ja/cells/transpose
aliases: [  /ja/cells/transpose ]
keywords: "TransposeData, Aspose.Cells, Cloud API, スプレッドシート, 行列転置"
description: "スプレッドシート内の行と列を入れ替えます。"
weight: 1000
---

## Aspose.Cells Cloud Web サービスの TransposeData

スプレッドシート内の行と列を入れ替えます。

### Web API エンドポイント

```http
PUT https://api.aspose.cloud/v4.0/cells/transpose
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名   | 型     | パス/クエリ文字列/HTTP ボディ | 説明                                                                                                                                                        |
|----------------|--------|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet    | ファイル | FormData                      | スプレッドシートファイルをアップロードします。                                                                                                              |
| worksheet      | 文字列   | クエリ                        | シート名。                                                                                                                                                  |
| cellArea       | 文字列   | クエリ                        | 指定されたデータ範囲。                                                                                                                                      |
| outPath        | 文字列   | クエリ                        | (オプション) ワークブックが保存されるフォルダのパス。デフォルトは null です。                                                                               |
| outStorageName | 文字列   | クエリ                        | 出力ファイルのストレージ名。                                                                                                                                |
| region         | 文字列   | クエリ                        | スプレッドシートの地域/言語設定（例: `en-US`、`fr-FR`）。数値の書式設定、日付の解析、地域固有の動作に影響を与えます。                                          |
| password       | 文字列   | クエリ                        | スプレッドシートファイルを開くためのパスワード。                                                                                                            |

### リクエストボディパラメータ

| パラメータ名 | 型   | 説明 |
| ------------ | ---- | ---- |
| [TBD]        | [TBD]| [TBD]|

### **レスポンス**

```json
{
  "file": "行列転置されたスプレッドシートのバイナリストリーム"
}
```

**レスポンスステータスコード**

| コード | 意味             | 説明                                                                 |
|--------|------------------|----------------------------------------------------------------------|
| 200    | OK               | 行列転置されたスプレッドシートファイルが返されます。                |
| 400    | Bad Request      | 無効な入力パラメータまたは不正な形式のリクエストです。              |
| 401    | Unauthorized     | 認証に失敗した、または JWT トークンが不足している／無効です。        |
| 413    | Payload Too Large| アップロードされたファイルが許容サイズ上限を超えています。          |
| 500    | Internal Server Error | 予期しないサーバーエラーが発生しました。                          |

## SDK を使用した TransposeData の利用方法

### TransposeData の仕様

[TransposeData API 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{Transform}/{TransposeData}) はパブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 通信を実行できるようにします。

cURL コマンドラインツールを使用すると、Aspose Cells Cloud Web サービスに簡単にアクセスできます。以下の例では、cURL を使用して Cloud API にアクセスする方法を示しています。

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# セキュアな接続には HTTPS を使用します
curl -v "https://api.aspose.cloud/v4.0/cells/transpose?worksheet=Sheet1&cellArea=A1:C10&outPath=output%2Ffolder&outStorageName=MyStorage&region=en-US&password=MyPassword" \
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
  "file": "行列転置されたスプレッドシートのバイナリストリーム"
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK の使用

SDK を使用すると、開発を最速で加速できます。SDK は低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストについては、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例では、さまざまな SDK を使用して Aspose Cells Cloud Web サービスを呼び出す方法を示しています：
`[TBD]`
---