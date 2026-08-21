---
title: "テーブルをピ벗表に変換する"
second_title: "Document"
linktitle: 変換
type: docs
url: /ja/pivot-tables/convert-table-to-pivottable/
aliases:
  [
    "/create-a-pivottable-with-table/",
    "/create-new-pivot-table-with-list-object-as-source-data/",
  ]
keywords: "ピ벗表、リスト オブジェクト、Aspose.Cells Cloud、REST API、テーブルをピ벗表に変換"
description: "Aspose.Cells Cloud REST API を使用してリスト オブジェクトからピ벗表を作成する方法を学びます。リクエストの詳細、cURL の例、SDK 参照を含みます。"
weight: 60
ArticleTitle: "テーブルをピ벗表に変換 – Aspose.Cells Cloud ドキュメント"
---

この REST API は、リスト オブジェクトから **ピ벗表** を作成します。

ピ벗表はリスト オブジェクトからのデータを要約し、ワークブック内で直接大規模なデータセットの分析とレポート作成を可能にします。

**前提条件:**  
- 認証用の有効な JWT ベアラートークン。  
- ワークブックは指定されたストレージの場所に存在している必要があります。  
- 対象のワークシートには、要約したいリスト オブジェクトが含まれている必要があります。

## PostWorksheetListObjectSummarizeWithPivotTable API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/SummarizeWithPivotTable
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### **リクエストパラメーター**

| パラメーター名    | 型      | 位置   | 説明                                      |
| ---------------- | ------- | ------ | ----------------------------------------- |
| name             | string  | path   | ワークブック ファイル名。                 |
| sheetName        | string  | path   | リスト オブジェクトを含むワークシート。   |
| listObjectIndex  | integer | path   | ワークシート内のリスト オブジェクトのインデックス。 |
| destsheetName    | string  | query  | 作成先ワークシートの名前。                |
| request          | object  | body   | ピ벗表を定義する JSON ペイロード。        |
| folder           | string  | query  | ワークブックが配置されているフォルダーのパス。 |
| storageName      | string  | query  | ストレージの名前。                        |

リクエストボディは、以下の JSON スキーマに従う必要があります：

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "type": "object",
  "properties": {
    "Name": { "type": "string", "description": "新しいピ벗表の名前。" },
    "DestCellName": { "type": "string", "description": "ピ벗表の左上セル（例：\"C1\"）。" },
    "PivotFieldRows": {
      "type": "array",
      "items": { "type": "integer" },
      "description": "行に配置するフィールドの 0 から始まるインデックス。"
    },
    "PivotFieldColumns": {
      "type": "array",
      "items": { "type": "integer" },
      "description": "列に配置するフィールドの 0 から始まるインデックス。"
    },
    "PivotFieldData": {
      "type": "array",
      "items": { "type": "integer" },
      "description": "データ フィールドとして使用するフィールドの 0 から始まるインデックス。"
    }
  },
  "required": ["Name", "DestCellName", "PivotFieldRows", "PivotFieldColumns", "PivotFieldData"]
}
```

<a href="https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObjectSummarizeWithPivotTable" rel="noopener noreferrer">OpenAPI スペック</a> はパブリックにアクセス可能なプログラミング インターフェースを定義し、Web ブラウザーから直接 REST アクセスを実行できるようにします。

**cURL** コマンドラインツールを使用して Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API に呼び出しを行う方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/TestCase.xlsx/worksheets/Sheet2/listobjects/0/SummarizeWithPivotTable?folder=CellsTests&destsheetName=Sheet4" \
-X POST \
-d '{"Name":"TestPivot","DestCellName":"C1","PivotFieldRows":[0,1],"PivotFieldColumns":[2],"PivotFieldData":[3,4]}' \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

*注：本番環境では本番エンドポイント（`api.aspose.cloud`）を使用してください。QA エンドポイント（`api-qa.aspose.cloud`）はテスト目的のみに使用してください。本番環境の呼び出しには HTTPS が必須です。*

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

**HTTP ステータスコード**

| コード | 意味                         | 説明                                            |
| ------ | ---------------------------- | ----------------------------------------------- |
| 200    | OK                           | フィルターの適用に成功。レスポンスには操作の詳細が含まれます。 |
| 400    | Bad Request                  | パラメーターが不足または無効（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized                 | JWT トークンが無効または不足しています。         |
| 413    | Payload Too Large            | アップロードされたファイルがサイズ制限を超えています。 |
| 500    | Internal Server Error        | 予期しないサーバーエラーが発生しました。         |

## Cloud SDK ファミリー

SDK を使用すると、開発を最速で進めることができます。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリー](https://github.com/aspose-cells-cloud) を確認してください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスに呼び出しを行う方法を示しています：
---