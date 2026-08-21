---
title: "CSVデータをスプレッドシートにインポート"
ArticleTitle: "CSVデータをスプレッドシートにインポート – Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktitle: "CSVデータをスプレッドシートにインポート"
type: docs
url: /ja/cells/import/data/csv
aliases: []
keywords: "Aspose.Cells, CSVインポート, スプレッドシート, API"
description: "Aspose.Cells Cloud API を使用して、CSVデータファイルをローカルのスプレッドシートにインポートします。"
weight: 100
---

## Aspose.Cells Cloud Web サービスの CSV データをスプレッドシートにインポート

CSV データファイルをローカルのスプレッドシートにインポートします。このメソッドは CSV を解析し、データをスプレッドシートのセル構造にマッピングして、ファイルをローカルに保存します。サポートされているスプレッドシート形式は .xlsx および .ods です。

### Web API エンドポイント

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data/csv
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を必要とします。

### リクエストパラメータ

| パラメータ名        | 型      | パス/クエリ文字列/HTTP ボディ | 説明                                                                                                                          |
|---------------------|---------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| datafile            | ファイル | FormData                      | データファイルをアップロードします。                                                                                          |
| Spreadsheet         | ファイル | FormData                      | スプレッドシートファイルをアップロードします。                                                                                |
| worksheet           | 文字列  | クエリ                        | CSV データをインポートするワークシートを指定します。（必須）                                                                  |
| startcell           | 文字列  | クエリ                        | データインポートの開始位置を指定します。（必須）                                                                             |
| insert              | 真偽値 | クエリ                        | 挿入動作を制御します。true: データを挿入; false: 既存のデータを上書き。デフォルト: true（任意）                               |
| convertNumericData  | 真偽値 | クエリ                        | テキストファイル内の文字列を数値データに変換するかどうかを指定します。デフォルト: true（任意）                               |
| splitter            | 文字列  | クエリ                        | CSV フィールドを分割するために使用される区切り文字を指定します。デフォルト: ","（任意）                                       |
| outPath             | 文字列  | クエリ                        | （任意）ワークブックを保存するフォルダパス。デフォルトは null です。（任意）                                                 |
| outStorageName      | 文字列  | クエリ                        | 出力ファイルのストレージ名。（任意）                                                                                          |
| fontsLocation       | 文字列  | クエリ                        | カスタムフォントを使用します。（任意）                                                                                        |
| region              | 文字列  | クエリ                        | スプレッドシートの地域/言語設定（例: `en-US`, `fr-FR`）。数値の書式設定、日付の解析、ロケール固有の動作に影響を与えます。（任意） |
| password            | 文字列  | クエリ                        | スプレッドシートファイルを開くためのパスワード。（任意）                                                                      |

### リクエストボディパラメータ

| パラメータ名 | 型 | 説明 |
| ------------ | -- | ---- |
| [TBD] | [TBD] | [TBD] |

### **レスポンス**

```json
{
  "file": "<生成されたスプレッドシートのバイナリストリーム>"
}
```

**レスポンスのHTTPステータスコード**

| コード | 意味 | 説明 |
|------|------|------|
| 200 | OK | CSV データが正常にインポートされ、生成されたスプレッドシートファイルが返されます。 |
| 400 | 不正なリクエスト | 無効なリクエストパラメータまたは不正な形式の URL。 |
| 401 | 認証エラー | 認証に失敗したか、資格情報が提供されていません。 |
| 404 | 見つかりません | ソースファイルにアクセスできません。 |
| 413 | ペイロードが大きすぎます | アップロードされたファイルが許可されたサイズ制限を超えています。 |
| 500 | サーバー内部エラー | スプレッドシートでデータ取得中に異常が発生しました。 |

## SDK を使用した CSV データをスプレッドシートにインポートする方法

### CSV データをスプレッドシートにインポートする仕様

[Import CSV Data Into Spreadsheet API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/ImportCSVDataIntoSpreadsheet) は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST アクセスを実行できるようにします。

cURL コマンドラインツールを使用して Aspose.Cells Web サービスに簡単にアクセスできます。以下の例では、cURL を使用して Cloud API にリクエストを送信する方法を示しています。

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# セキュアな接続には HTTPS を使用
curl -v "https://api.aspose.cloud/v4.0/cells/import/data/csv?worksheet=Sheet1&startcell=A1&insert=true&convertNumericData=true&splitter=,&outPath=outputFolder&outStorageName=MyStorage&fontsLocation=/custom/fonts&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F "datafile=@sample.csv" \
  -F "Spreadsheet=@workbook.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<生成されたスプレッドシートのバイナリストリーム>"
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK を使用する

SDK を使用すると、開発を最も迅速に進めることができます。SDK は低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧については、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose Cells Cloud Web サービスを呼び出す方法を示しています:
 `[TBD]`
---