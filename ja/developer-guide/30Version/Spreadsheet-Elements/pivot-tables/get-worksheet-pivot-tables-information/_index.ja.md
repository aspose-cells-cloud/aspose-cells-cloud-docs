---
title: "Excelワークシート内のすべてのピボットテーブルを取得する"
second_title: "Document"
linktitle: すべてを取得
type: docs
url: /ja/pivot-tables/get-all/
aliases: [  /ja/get-worksheet-pivot-tables-information/ ]
keywords: "すべてのピボットテーブルを取得, Aspose.Cells Cloud API, Excel ピボットテーブル, REST API"
description: "Aspose.Cells Cloud API を使用して Excel ワークシート内のすべてのピボットテーブルを取得します。ピボットテーブル API には、エンドポイント、パラメータ、認証手順、cURL、および SDK サンプルが含まれます。"
weight: 20
ArticleTitle: "Excelワークシート内のすべてのピボットテーブルを取得する – Aspose.Cells Cloud API"
---

**ピボットテーブル** は、Excel 内で大規模なデータセットを再整理・分析できるデータ集計ツールです。この REST API は、指定されたワークシート内の**すべて**のピボットテーブルに関する情報を取得します。

## セキュリティと認証

Aspose.Cells Cloud API は安全であり、[JWT トークンベースの認証](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)を必要とします。

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### **リクエストパラメータ**

| パラメータ名 | 型     | 位置   | 説明                             |
| ------------ | ------ | ------ | --------------------------------- |
| name         | string | path   | Excel ドキュメントの名前。        |
| sheetName    | string | path   | ワークシートの名前。              |
| folder       | string | query  | ドキュメントが保存されているフォルダ。 |
| storageName  | string | query  | ストレージサービスの名前。        |

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/PivotTables/GetWorksheetPivotTables) はパブリックに利用可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 通信を実行できるようにします。

### リクエスト

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

### レスポンス

{{< tab tabNum="2" >}}

```json
{
  "PivotTables": {
    "PivotTableList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self"
        }
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### エラーレスポンス

| HTTP コード | 説明                                                             | サンプル JSON ペイロード                                      |
| ----------- | ---------------------------------------------------------------- | ------------------------------------------------------------- |
| 400         | リクエストエラー – 必須パラメータが不足しています。             | `{ "Code": "400", "Message": "Missing required parameter." }` |
| 401         | 認証エラー – トークンが無効または不足しています。                | `{ "Code": "401", "Message": "Authentication failed." }`      |
| 404         | 見つかりません – ワークブック、ワークシート、またはピボットテーブルが存在しません。 | `{ "Code": "404", "Message": "Resource not found." }`         |
| 500         | サーバ内部エラー – サーバ上で予期しない状態が発生しました。      | `{ "Code": "500", "Message": "Server error." }`               |

## Cloud SDK ファミリー

SDK を使用すると、開発が最も迅速に行えます。SDK が低レベルの詳細を処理するため、プロジェクトの本質的な部分に集中できます。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-GetWorksheetPivotTables-1.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-GetPivotTableWorksheet-GetPivotTableWorksheet-12345.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetWorksheetPivotTablesInformation.py" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-GetWorksheetPivotTables-1.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-GetPivotTableWorksheet-GetPivotTableWorksheet-12345.java" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-GetWorksheetPivotTables-1.pl" >}}
{{< /tab >}}

{{< tab tabNum="10" >}}
{{< gist "aspose-cells-cloud-gists" "6b30a17927feeb2899283e4dbe566c42" >}}
{{< /tab >}}

{{< /tabs >}}