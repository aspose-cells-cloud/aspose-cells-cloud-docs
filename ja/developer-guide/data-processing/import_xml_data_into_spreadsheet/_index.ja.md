---
title: "XML データをスプレッドシートにインポート"
ArticleTitle: "XML データをスプレッドシートにインポート – Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktype: "docs"
url: /cells/import/data/xml
aliases: []
keywords: "XML インポート、Aspose.Cells、API"
description: "Aspose.Cells Cloud を使用して、ローカルのスプレッドシートに XML データファイルをインポートします。"
weight: 1000
---

## Aspose.Cells Cloud Web サービスの XML データをスプレッドシートにインポート

ローカルのスプレッドシートに XML データファイルをインポートします。このメソッドは XML を解析し、データをスプレッドシートのセル構造にマッピングして、ローカルにファイルを保存します。サポートされているスプレッドシート形式は .xlsx および .ods です。

### Web API エンドポイント

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data/xml
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名     | タイプ    | パス/クエリ文字列/HTTP ボディ | 説明                                                                                                                            |
|------------------|---------|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| datafile         | ファイル  | FormData                    | データファイルをアップロードします。                                                                                                                      |
| Spreadsheet      | ファイル  | FormData                    | スプレッドシートファイルをアップロードします。                                                                                                               |
| worksheet        | 文字列    | クエリ                        | XML データをインポートするワークシートを指定します。                                                                                            |
| startcell        | 文字列    | クエリ                        | データのインポート開始位置                                                                                                      |
| insert           | 真偽値    | クエリ                        | 挿入動作を制御します。true: データを挿入します; false: 既存のデータを上書きします。デフォルト: **true**                               |
| outPath          | 文字列    | クエリ                        | (オプション) ワークブックが保存されるフォルダーパス。デフォルトは null です。                                                         |
| outStorageName   | 文字列    | クエリ                        | 出力ファイルのストレージ名。                                                                                                              |
| fontsLocation    | 文字列    | クエリ                        | カスタムフォントを使用します。                                                                                                                      |
| region           | 文字列    | クエリ                        | スプレッドシートの地域/言語設定（例: `en-US`、`fr-FR`）。数値の書式設定、日付の解析、ロケール固有の動作に影響します。 |
| password         | 文字列    | クエリ                        | スプレッドシートファイルを開くためのパスワード。                                                                                             |

### リクエストボディパラメータ

| パラメータ名 | タイプ | 説明 |
|--------------|------|-------------|
| *なし*         | -    | -           |

### **レスポンス**

```json
{
  "file": "<更新されたスプレッドシートのバイナリストリーム>"
}
```

**レスポンスステータスコード**

| コード | 意味                    | 説明                                                                                           |
|------|-------------------------|-------------------------------------------------------------------------------------------------------|
| 200  | OK                      | XML データが正常にインポートされ、更新されたスプレッドシートファイルが返されます。                        |
| 400  | Bad Request             | 無効なリクエスト URL または不足している必須パラメータ。                                                   |
| 401  | Unauthorized            | 認証に失敗したか、資格情報が提供されていません。                                          |
| 404  | Not Found               | ソースファイルにアクセスできません。                                                                           |
| 413  | Payload Too Large       | アップロードされたファイルが許可されたサイズ制限を超えています。                                                          |
| 500  | Internal Server Error   | スプレッドシートでデータ取得中に異常が発生しました。                                         |

## SDK を使用して XML データをスプレッドシートにインポートする方法

### XML データをスプレッドシートにインポートする仕様

[XML データをスプレッドシートにインポートする API 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{DataProcessingController}/ImportXMLDataIntoSpreadsheet) は、公開可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 操作を実行できるようにします。

cURL コマンドラインツールを使用して、Aspose.Cells Cloud Web サービスに簡単にアクセスできます。以下の例は、cURL を使用して Cloud API に呼び出しを行う方法を示しています。

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# 安全な接続に HTTPS を使用
curl -v "https://api.aspose.cloud/v4.0/cells/import/data/xml?worksheet={worksheet}&startcell={startcell}&insert={insert}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "datafile=@{DataFileName}" \
  -F "Spreadsheet=@{SpreadsheetFileName}"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<更新されたスプレッドシートのバイナリストリーム>"
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK を使用する

SDK を使用すると、開発を最も迅速に加速できます。SDK は低レベルの詳細を抽象化し、プロジェクトタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストについては、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose Cells Cloud Web サービスを呼び出す方法を示しています：
`[TBD]`
---