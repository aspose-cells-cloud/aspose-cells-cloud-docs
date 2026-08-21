---
title: "テーブルの分割"
ArticleTitle: "Split Table – Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktitle: "テーブルの分割"
type: docs
url: /cells/split/table
aliases: []
keywords: "Aspose.Cells, テーブルの分割, API"
description: "スプレッドシート内のテーブルを列の値に基づいて分割するためのAPI。"
weight: 1
---

## Aspose.Cells Cloud WebサービスのSplitTable

このメソッドは、指定された列の固有値に基づいて行をグループ化し、ソーステーブルに対して分割操作を実行します。各データグループ（各一意の分割値ごと）は、個別のデータ単位として処理されます。エクスポート先は、以下の2つの重要なブール型パラメータによって制御されます。
- **ワークブック構造の決定**: `true` の場合、各分割単位は個別のワークブックファイルとして保存されます。`false` の場合、各単位は現在のワークブック内に新しいワークシートとして追加されます。
- **出力パッケージングの決定**: `true` に設定され、かつ `toNewWorkbook` = `true` の場合、このメソッドは複数の個別ファイルを生成し、ZIPアーカイブとして返します。`false` の場合、すべてのデータは単一のファイル（複数シートのワークブックまたは他の設定に応じた単一ファイル）に統合されます。

### Web API エンドポイント

```http
PUT https://api.aspose.cloud/v4.0/cells/split/table
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名       | タイプ    | Path/クエリ文字列/HTTP本文 | 説明                                                                                                                                                                   |
|------------------|---------|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | ファイル  | FormData                    | スプレッドシートファイルをアップロードします。                                                                                                                                                      |
| worksheet        | 文字列    | クエリ                      | テーブルを含むワークシート。                                                                                                                                               |
| tableName        | 文字列    | クエリ                      | 分割対象のデータテーブル。                                                                                                                                           |
| splitColumnName  | 文字列    | クエリ                      | 分割に使用する列名。                                                                                                                                                      |
| saveSplitColumn  | ブール値  | クエリ                      | 分割対象の列のデータを保持するかどうか。                                                                                                                                 |
| splitRowNumber   | 整数    | クエリ                      | [TBD]                                                                                                                                                                          |
| toNewWorkbook    | ブール値  | クエリ                      | エクスポート先の制御: true - 分割されたデータを含む新しいワークブックファイルを作成；false - 現在のワークブックに新しいワークシートを追加。                              |
| toMultipleFiles  | ブール値  | クエリ                      | true - テーブルデータを**複数の個別ファイル**としてエクスポート（ZIPアーカイブとして返される）；false - 複数シートを含む**単一ファイル**にすべてのデータを保存。既定値: false. |
| outPath          | 文字列    | クエリ                      | （オプション）ワークブックを保存するフォルダのパス。既定値は null です。                                                                                                 |
| outStorageName   | 文字列    | クエリ                      | 出力ファイルのストレージ名。                                                                                                                                                     |
| fontsLocation    | 文字列    | クエリ                      | カスタムフォントを使用します。                                                                                                                                                              |
| region           | 文字列    | クエリ                      | スプレッドシートの地域/言語設定（例: `en-US`, `fr-FR`）。数値の書式設定、日付の解析、ロケール固有の動作に影響します。                                      |
| password         | 文字列    | クエリ                      | スプレッドシートファイルを開くためのパスワード。                                                                                                                                   |

### リクエストボディパラメータ

| パラメータ名 | タイプ | 説明 |
| ------------ | ---- | ----------- |
| Spreadsheet  | ファイル | スプレッドシートファイルをアップロードします。 |

### **レスポンス**

```json
{
  "file": "バイナリストリーム（ZIPアーカイブまたはワークブック、パラメータによって異なります）"
}
```

**レスポンスステータスコード**

| コード | 意味           | 説明 |
|------|----------------|------|
| 200  | OK             | 分割操作が正常に完了しました。レスポンスには生成されたファイル（ZIPアーカイブまたはワークブック）が含まれます。 |
| 400  | Bad Request    | URL またはリクエストパラメータが無効です。 |
| 401  | Unauthorized   | 認証に失敗したか、資格情報が提供されていません。 |
| 404  | Not Found      | ソースファイルにアクセスできません。 |
| 413  | Payload Too Large | リクエストペイロードが許容サイズを超えています。 |
| 500  | Internal Server Error | スプレッドシートでデータ取得中に異常が発生しました。 |

## SDK を使用した SplitTable の使い方

### SplitTable の仕様

[SplitTable API 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/SplitTable) は、公開可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 操作を実行できるようにします。

cURL コマンドラインツールを使用することで、Aspose.Cells Cloud Web サービスに簡単にアクセスできます。以下の例は、cURL を使用して Cloud API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
# セキュアな接続には HTTPS を使用
curl -v "https://api.aspose.cloud/v4.0/cells/split/table?worksheet=Sheet1&tableName=MyTable&splitColumnName=Category&saveSplitColumn=true&splitRowNumber=1&toNewWorkbook=true&toMultipleFiles=true&outPath=output%2Ffolder&outStorageName=MyStorage&fontsLocation=%2Fcustom%2Ffonts&region=en-US&password=SecretPassword" \
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
  "file": "バイナリストリーム（ZIPアーカイブまたはワークブック、パラメータによって異なります）"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose Cells Cloud SDK の使用

SDK を使用すると、開発を最速で加速できます。SDK は低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストについては、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose Cells Cloud Web サービスを呼び出す方法を示しています：
`[TBD]`
---