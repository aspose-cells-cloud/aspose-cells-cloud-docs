---
title: "Excelワークシート内のListObjectデータを並べ替える"
second_title: "Document"
linktitle: "Sort"
type: docs
url: /list-objects/sort-data/
aliases: [/get-a-list-object-or-table-inside-the-worksheet/, /tables/sort-data/]
keywords: "Aspose.Cells Cloud, Excel, ListObject, データの並べ替え, REST API, ワークシート"
description: "Aspose.Cells Cloud REST API（v3.0）を使用してExcelワークシート内のListObject（テーブル）データを並べ替える方法を学びます。エンドポイント、パラメーター、サンプルcURLリクエスト、SDKの使用例を含みます。"
weight: 40
ArticleTitle: "Excelワークシート内のListObjectデータを並べ替える – Aspose.Cells Cloud API"
---

**前提条件**  
このAPIを呼び出すには、有効なAspose Cloud JWTアクセストークンが必要であり、ワークブックはAspose Cloudストレージにアップロードされている必要があります。すべてのリクエストにヘッダー `Authorization: Bearer <jwt token>` を含めてください。

このREST APIは、Excelワークシート内のテーブルデータを並べ替えます。  
この操作を使用するには、ワークブック名、ワークシート名、および対象となるListObjectのインデックスを指定し、さらにソート条件を定義する`dataSorter` JSON本文を提供します。

## PostWorksheetListObjectSortTable API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/sort
```

### **セキュリティと認証**

Aspose.Cells Cloud APIは安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWTトークンベースの認証</a>を要求します。

### **リクエストパラメーター**

| パラメーター名      | 型       | パス/クエリ文字列/HTTP本文 | 説明                                                                                                     |
| ------------------- | -------- | -------------------------- | --------------------------------------------------------------------------------------------------------------- |
| name                | 文字列    | パス                        | Aspose Cloudストレージに保存されたExcelファイルの名前。                                                      |
| sheetName           | 文字列    | パス                        | ListObjectを含むワークシートの名前。                                                         |
| listObjectIndex     | 整数      | パス                        | ワークシート内でのListObject（テーブル）の0から始まるインデックス。                                                |
| dataSorter          | オブジェクト | 本文                        | ソートオプションを指定するJSONオブジェクト（例: `CaseSensitive`, `HasHeaders`, `KeyList`, `SortLeftToRight`）。 |
| folder              | 文字列    | クエリ                      | Excelファイルが配置されているストレージ内のフォルダーパス。                                                         |
| storageName         | 文字列    | クエリ                      | Aspose Cloudストレージの名前。                                                                               |

**注意事項**  
リクエスト本文は、`dataSorter` スキーマに一致する有効なJSONオブジェクトである必要があります。並べ替え操作を実行する前に、ワークブック、ワークシート、およびListObjectが存在することを確認してください。

[OpenAPI仕様](https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObjectSortTable)は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Webブラウザから直接RESTインタラクションを実行できるようにします。

cURLコマンドラインツールを使用してAspose.Cells Webサービスに簡単にアクセスできます。以下の例は、cURLを使用してCloud APIを呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet7/listobjects/1/sort" \
  -X POST \
  -d '{
        "CaseSensitive": true,
        "HasHeaders": true,
        "KeyList": [
          {
            "Key": 1,
            "SortOrder": "Ascending",
            "CustomList": "string"
          }
        ],
        "SortLeftToRight": true
      }' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**HTTPステータスコード**

| ステータスコード | 説明                                    |
|----------------|-----------------------------------------|
| 200            | OK – 並べ替えが正常に完了しました。    |
| 400            | Bad Request – 無効なパラメーターです。       |
| 401            | Unauthorized – 認証に失敗しました。    |
| 404            | Not Found – ワークブック、ワークシート、またはListObjectが見つかりません。 |
| 500            | Internal Server Error – サーバー側の問題です。|

**レスポンスパラメーター**

| パラメーター | 型       | 説明                                 |
|-------------|----------|---------------------------------------------|
| Code        | 整数      | APIによって返されたHTTPステータスコード。       |
| Status      | 文字列    | 結果のテキストによる説明（例: "OK"）。 |

{{< /tab >}}

{{< /tabs >}}

## Cloud SDKファミリー

SDKを使用することが開発を高速化する最良の方法です。SDKは低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDKの完全なリストについては、[GitHubリポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまなSDKを使用してAspose.Cells Webサービスを呼び出す方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectSortTable.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectSortTable.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectSortTable.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectSortTable.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectSortTable.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectSortTable.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectSortTable.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectSortTable.go" >}}

{{< /tab >}}

{{< /tabs >}}

[ListObjects概要へ戻る](/list-objects/)
---