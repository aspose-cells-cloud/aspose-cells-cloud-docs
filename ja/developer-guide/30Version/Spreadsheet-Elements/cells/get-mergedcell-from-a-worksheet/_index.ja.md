---
title: "Excelワークシートから結合セルを取得する – Aspose.Cells Cloud API"
type: docs
url: /get-mergedcell-from-a-worksheet/
weight: 60
keywords: "Aspose.Cells Cloud, 結合セル, Excelワークシート, REST API, Aspose.Cells SDK, Excel 結合セル"
description: "Aspose.Cells Cloud API（v3.0）を使用して、Excelワークシートから結合セル範囲を取得する方法を学びます。認証手順、完全なcURLリクエスト、レスポンススキーマ、エラーハンドリング、およびC#、Java、PythonなどのSDKサンプルを含みます。"
---

このREST APIは、Excelワークシート内の**結合セル**に関する情報を返します。

> **注** – APIオブジェクト名は **MergedCell**（単数形）です。本文中では、結合セルの*概念*（複数形）について言及します。

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/mergedCells
```

## セキュリティと認証

Aspose.Cells Cloud APIは安全で、[JWTトークンによる認証](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)が必要です。

### リクエストパラメータ

| パラメータ名   | 型     | 位置   | 説明                            |
|----------------|--------|--------|---------------------------------|
| **name**       | string | path   | Excelファイル名。               |
| **sheetName**  | string | path   | ワークシート名。                |
| **folder**     | string | query  | ドキュメントを含むフォルダ。    |
| **storageName**| string | query  | 使用するストレージ名。          |

## **レスポンス**

MergedCellsResponse を返します。

```json
{
  "Status":"OK",
  "Code":200,
  "MergedCells":{
    "Count": 0,
    "MergedCellList":[
      {
        "Link":{
          "Href":"",
          "Rel":"",
          "Type":"",
          "Title":""
        }
      }
    ]
  }
}
```

**HTTPステータスコード**

| コード | 意味               | 説明                                      |
|--------|--------------------|-------------------------------------------|
| 200    | OK                 | フィルターが正常に適用され、レスポンスに操作詳細が含まれます。 |
| 400    | Bad Request        | 必須パラメータが不足しているか、無効です（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized       | JWTトークンが無効または不足しています。    |
| 413    | Payload Too Large  | アップロードされたファイルがサイズ制限を超えています。 |
| 500    | Internal Server Error | サーバー内部で予期せぬエラーが発生しました。 |

## SDKを使用して GetWorksheetMergedCells API を利用する方法

### GetWorksheetMergedCells API 仕様

[OpenAPI仕様](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetMergedCells)は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Webブラウザから直接REST操作を実行できるようにします。

cURLコマンドラインツールを使用すると、Aspose.Cellsウェブサービスに簡単にアクセスできます。以下の例は、cURLでCloud APIを呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/mergedCells" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MergedCells": {
    "Count": 1,
    "MergedCells": [
      {
      "link": {
            "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/cells/mergedcells/0",
            "Rel": "self"
          }
      }
    ]    
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}


### Aspose.Cells Cloud SDK を使用する

SDKを使用すると、APIに対する開発が最速で行えます。SDKが低レベルの詳細処理を担当するため、ビジネスロジックの開発に集中できます。Aspose.Cells Cloud SDKの完全な一覧は[GitHubリポジトリ](https://github.com/aspose-cells-cloud)をご覧ください。

以下のコード例では、さまざまなSDKを使用してAspose.Cellsウェブサービスを呼び出す方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetMergedCells.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetMergedCells.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetMergedCells.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetMergedCells.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetMergedCells.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetMergedCells.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetMergedCells.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetMergedCells.go" >}}

{{< /tab >}}

{{< /tabs >}}
---