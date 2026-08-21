---
title: "JSON データをスプレッドシートにインポートする"
ArticleTitle: "JSON データをスプレッドシートにインポートする – Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktitle: "JSON データをスプレッドシートにインポートする"
type: docs
url: /cells/import/data/json
aliases: []
keywords: "JSON のインポート, Aspose.Cells, スプレッドシート, API"
description: "ローカルのスプレッドシートに JSON データファイルをインポートします。"
weight: 1
---

## Aspose.Cells Cloud Web サービスによる JSON データのスプレッドシートへのインポート

ローカルのスプレッドシートに JSON データファイルをインポートします。このメソッドは JSON を解析し、データをスプレッドシートのセル構造にマッピングして、ローカルにファイルを保存します。サポートされているスプレッドシート形式は .xlsx および .ods です。

### Web API エンドポイント

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data/json
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名 | 型     | パス/クエリ文字列/HTTP リクエストボディ | 説明 |
|--------------|--------|----------------------------------------|------|
| datafile     | ファイル | FormData                              | データファイルをアップロードします。 |
| Spreadsheet  | ファイル | FormData                              | スプレッドシートファイルをアップロードします。 |
| worksheet    | 文字列   | クエリ                                | JSON データをインポートするワークシート。 |
| startcell    | 文字列   | クエリ                                | データインポートの開始位置 |
| insert       | 真偽値   | クエリ                                | 挿入動作を制御します。true: データを挿入する；false: 既存のデータを上書きする。（デフォルト: true） |
| outPath      | 文字列   | クエリ                                | (オプション) ワークブックが保存されるフォルダパス。デフォルトは null です。 |
| outStorageName | 文字列 | クエリ                              | 出力ファイルのストレージ名。 |
| fontsLocation | 文字列  | クエリ                                | カスタムフォントを使用します。 |
| region       | 文字列   | クエリ                                | スプレッドシートの地域/言語設定（例: `en-US`, `fr-FR`）。数値の書式設定、日付の解析、地域固有の動作に影響を与えます。 |
| password     | 文字列   | クエリ                                | スプレッドシートファイルを開くためのパスワード。 |

### リクエストボディパラメータ

| パラメータ名 | 型 | 説明 |
| ------------ | -- | ---- |
| [TBD] | [TBD] | [TBD] |

### **レスポンス**

```json
{
  "file": "バイナリストリーム"
}
```

**レスポンスステータスコード**

| コード | 意味 | 説明 |
|------|------|------|
| 200 | OK | ファイルが正常に生成され、返されました。 |
| 400 | 不正なリクエスト | 無効な URL です。 |
| 401 | 認証エラー | 認証に失敗したか、資格情報が提供されていません。 |
| 404 | 見つかりません | ソースファイルにアクセスできません。 |
| 413 | ペイロードが大きすぎます | [TBD] |
| 500 | サーバー内部エラー | スプレッドシートがデータ取得中に異常を検出しました。 |

## SDK を使用した JSON データのスプレッドシートへのインポートの方法

### JSON データのスプレッドシートへのインポート仕様

[JSON データのスプレッドシートへのインポート API 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/ImportJSONDataIntoSpreadsheet) は、公開可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST アクセスを実行できるようにします。

cURL コマンドラインツールを使用して、Aspose Cells Cloud Web サービスに簡単にアクセスできます。以下の例は、cURL を使用して Cloud API に呼び出しを行う方法を示しています。

{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}
{< tab tabNum="1" >}
```bash
# 安全な接続には HTTPS を使用
curl -v "https://api.aspose.cloud/v4.0/cells/import/data/json?worksheet=Sheet1&startcell=A1&insert=true&outPath=output%2F&outStorageName=MyStorage&fontsLocation=%2Ffonts&region=en-US&password=Secret" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "datafile=@data.json" \
  -F "Spreadsheet=@workbook.xlsx"
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "file": "バイナリストリーム"
}
```
{< /tab >}
{< /tabs >}

### Aspose Cells Cloud SDK の使用

SDK を使用すると、開発を最も迅速に加速できます。SDK は低レベルの詳細を抽象化し、プロジェクトタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストについては、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose Cells Cloud Web サービスを呼び出す方法を示しています：
 `[TBD]`
---