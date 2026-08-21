---
title: "JSON データを Excel にインポートする"
second_title: "ドキュメント"
linktitle: "JSON のインポート"
type: docs
url: /import-json-data-into-excel/
aliases: [/import/json/]
keywords: "Aspose.Cells Cloud, JSON インポート, Excel API, REST による JSON インポート, SDK サンプル"
description: "Aspose.Cells Cloud REST API を使用して Excel シートに JSON データをインポートする方法を学びます。エンドポイントの詳細、リクエスト/レスポンスの例、.NET、Java、Python 向けの SDK コードを含みます。"
weight: 40
---

この REST API は、**JSON データを Excel シートにインポート**します。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/importjson
```
### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### **リクエストパラメータ**

| パラメータ名          | 位置           | 型     | 説明                                                                                          |
| --------------------- | -------------- | ------ | -------------------------------------------------------------------------------------------- |
| name                  | パス           | 文字列 | ワークブックファイル名。                                                                      |
| importJsonRequest     | HTTP ボディ    | クラス | JSON インポートの詳細を含むリクエストペイロード。                                              |
| password              | クエリ文字列   | 文字列 | ワークブックを開くためのパスワード（保護されている場合）。                                      |
| folder                | クエリ文字列   | 文字列 | オリジナルのワークブックが格納されているフォルダ。                                              |
| storageName           | クエリ文字列   | 文字列 | ワークブックが存在するストレージ名。                                                            |
| outPath               | クエリ文字列   | 文字列 | インポート後の出力ファイルのパス。指定しない場合、更新されたワークブックがレスポンスとして返されます。 |
| outStorageName        | クエリ文字列   | 文字列 | 出力ファイル用のストレージ名。                                                                  |
| checkExcelRestriction | クエリ文字列   | 文字列 | Excel 固有の制限を適用するかどうかを示すフラグ (true/false)。                                   |

### **リクエスト本文の例**

```json
{
  "JsonFileSource": {
    "FilePath": "string"
  },
  "ImportPosition": {
    "SheetName": "string",
    "RowIndex": 0,
    "ColumnIndex": 0
  },
  "JsonContent": "string"
}
```

### レスポンス

成功したリクエストは、以下のような JSON ペイロードを含む **HTTP 200** を返します：

```json
{
  "Code": 200,
  "Status": "OK"
}
```

考えられるステータスコード：

| コード | 意味                                       |
| ------ | ------------------------------------------ |
| 200    | インポート成功                             |
| 400    | 不正なリクエスト – データが不足または無効  |
| 401    | 認証エラー – トークンが無効または不足      |
| 500    | サーバー内部エラー                         |


## SDK を使用した PostWorkbookImportJson API の利用方法

### PostWorkbookImportJson API 仕様

[OpenAPI 仕様](https://reference.aspose.cloud/cells/#/DataProcessing/PostWorkbookImportJson) は、公開可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST アクセスを実行できるようにします。

### Aspose.Cells Cloud SDK の使用

SDK を使用することは、開発を最効率的に進める最も良い方法です。SDK は低レベルの詳細を処理し、ビジネスロジックの開発に集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧は、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) を参照してください。

以下のコードサンプルは、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています：

---