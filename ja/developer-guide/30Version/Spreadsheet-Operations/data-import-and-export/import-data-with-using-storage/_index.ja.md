---
title: "ストレージを使用したデータのインポート"
second_title: "ドキュメント"
linktitle: "ストレージを使用したデータのインポート"
type: docs
url: /import-data-with-using-storage/
aliases:
  - /import-data-into-excel-worksheet/
  - /import-data-into-worksheet/
  - /import-data-in-excel-worksheet/
  - /import-data/
  - /import/with-using-storage/
description: "ストレージを使用したデータのインポート: Aspose.Cells Cloud APIを使用して、さまざまなストレージソースからExcelワークシートにデータをインポートします。HTTPS経由でJSON、CSV、およびその他の形式をサポートします。"
keywords: "Aspose.Cells Cloud, Excel, データのインポート, REST API, クラウドストレージ, JSON, CSV, PDF, Markdown, HTTPS"
weight: 10
ArticleTitle: "ストレージを使用したデータのインポート - Aspose.Cells Cloud API ドキュメント"
---

このREST APIは、Excelファイルにデータをインポートします。

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **セキュリティと認証**

Aspose.Cells Cloud APIは安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWTトークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名   | 型     | 位置   | 説明                                                  |
| -------------- | ------ | ------ | ----------------------------------------------------- |
| name           | string | path   | Excelファイルの名前。                                 |
| folder         | string | query  | ファイルが存在するストレージ内のフォルダーパス。     |
| storageName    | string | query  | ストレージサービスの名前。                            |
| importData     | object | body   | インポートするデータを含むJSONオブジェクト。          |

**import-dataオプションパラメータ**については、[リファレンスリンク](/cells/import/#import-data-option-parameter)をご覧ください。

**前提条件:** `Authorization` ヘッダーに有効なJWTトークンを提供し、対象のワークブックが指定されたストレージの場所に既に存在することを確認する必要があります。

### レスポンス

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTPステータスコード**

| コード | 意味           | 説明                                               |
|--------|----------------|----------------------------------------------------|
| 200    | OK             | フィルターが正常に適用されました。レスポンスには操作の詳細が含まれます。 |
| 400    | Bad Request    | パラメータが不足または無効です（例：サポートされていないファイルタイプ）。 |
| 401    | Unauthorized   | JWTトークンが無効または不足しています。            |
| 413    | Payload Too Large | アップロードされたファイルがサイズ制限を超えています。 |
| 500    | Internal Server Error | サーバーで予期しないエラーが発生しました。         |

## SDKを使用したPostImportData APIの利用方法

### PostImportData API仕様

<a href="https://apireference.aspose.cloud/cells/#/Workbook/PostImportData" rel="noopener noreferrer">OpenAPI仕様</a>はパブリックにアクセス可能なプログラミングインターフェースを定義し、Webブラウザから直接REST通信を実行できるようにします。

cURLコマンドラインツールを使用してAspose.Cellsウェブサービスに簡単にアクセスできます。以下の例は、cURLを使用してクラウドAPIを呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/importdata" \
     -X POST \
     -d '{"Data":[1,2,4],"DestinationWorksheet":"Sheet1","FirstRow":1,"FirstColumn":2,"IsVertical":true,"IsInsert":true,"importDataType":"IntArray"}' \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDKの使用

SDKを使用することで、開発を最も効率的に進めることができます。SDKは低レベルの詳細を抽象化し、ビジネスロジックに集中できるようにします。Aspose.Cells Cloud SDKの完全なリストについては、[GitHubリポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、PHP SDKを使用してAspose.Cellsウェブサービスを呼び出す方法を示しています。