---
title: "Excelワークシートに日付フィルターを追加する"
second_title: "Document"
linktitle: "日付フィルターの追加"
type: docs
url: /ja/autofilter/add-date-filter/
aliases:
  - /add-date-filter-in-a-worksheet/
  - /autofilter/add-a-date-filter/
description: "Aspose.Cells Cloud REST API（v3.0）を使用してExcelワークシートに日付フィルターを追加する方法を学びます。cURLの例、SDKスニペット（C#、Java、Pythonなど）、パラメーター、エラーハンドリングを含みます。"
weight: 65
ArticleTitle: "Excelワークシートに日付フィルターを追加する | Aspose.Cells Cloud API"
keywords: "Aspose.Cells, Excel日付フィルター, AutoFilter API, REST API, クラウドSDK, cURL, スプレッドシート自動化"
---

このREST APIは、Excelワークシートに**日付フィルター**を追加します。

**前提条件:** 有効なJWTトークンが必要であり、対象のワークブックは指定されたストレージ場所に既に存在している必要があります。このリクエストにはJSONボディは不要です。

## PutWorksheetDateFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dateFilter
```

### **セキュリティと認証**

Aspose.Cells Cloud APIは安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWTトークンベースの認証</a>を要求します。

### リクエストパラメーター


| パラメーター名           | 型      | 位置   | 説明                                                                                                                                                              |
| ------------------------ | ------- | ------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**                 | string  | Path   | ワークブック名。                                                                                                                                                  |
| **sheetName**            | string  | Path   | ワークシート名。                                                                                                                                                  |
| **range**                | string  | Query  | フィルターを適用するExcel範囲（例: `A1:B1`）。                                                                                                                    |
| **fieldIndex**           | integer | Query  | フィルター対象の列の0から始まるインデックス。                                                                                                                     |
| **dateTimeGroupingType** | string  | Query  | 日付/時刻フィルターのグループ化タイプ。許可される値は `Day`、`Hour`、`Minute`、`Month`、`Second`、`Year` です。値は大文字・小文字を区別し、デフォルトは `Day` です。 |
| **year**                 | integer | Query  | フィルター値の年コンポーネント。                                                                                                                                  |
| **month**                | integer | Query  | フィルター値の月コンポーネント。                                                                                                                                  |
| **day**                  | integer | Query  | フィルター値の日コンポーネント。                                                                                                                                  |
| **hour**                 | integer | Query  | フィルター値の時コンポーネント。                                                                                                                                  |
| **minute**               | integer | Query  | フィルター値の分コンポーネント。                                                                                                                                  |
| **second**               | integer | Query  | フィルター値の秒コンポーネント。                                                                                                                                  |
| **matchBlanks**          | boolean | Query  | 空白セルを含めるかどうか（`true` または `false`）。                                                                                                               |
| **refresh**              | boolean | Query  | 適用後にフィルターを更新するかどうか（`true` または `false`）。                                                                                                   |
| **folder**               | string  | Query  | 元のワークブックのフォルダパス。                                                                                                                                  |
| **storageName**          | string  | Query  | ストレージサービスの名前。                                                                                                                                        |

*PUTリクエストにはリクエストボディは不要で、すべてのパラメーターはクエリ文字列で指定されます。*

### **レスポンス**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTPステータスコード**

| コード | 意味                         | 説明                                                             |
|------|-----------------------------|------------------------------------------------------------------|
| 200  | OK                          | フィルターが正常に適用された。レスポンスには操作の詳細が含まれる。 |
| 400  | Bad Request                 | パラメーターが不足しているか、無効（例: サポートされていないファイル形式）。 |
| 401  | Unauthorized                | JWTトークンが無効または不足している。                              |
| 413  | Payload Too Large           | アップロードされたファイルがサイズ制限を超えた。                   |
| 500  | Internal Server Error       | サーバー内で予期しないエラーが発生した。                           |

## SDKを使用したPutWorksheetDateFilter APIの使用方法

### PutWorksheetDateFilter API仕様

<a href="https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetDateFilter" rel="noopener noreferrer">OpenAPI仕様</a>はパブリックに利用可能なプログラミングインターフェースを定義し、ウェブブラウザから直接RESTインタラクションを実行できるようにします。

**cURL** コマンドラインツールを使用すると、Aspose.Cellsウェブサービスに簡単にアクセスできます。以下の例は、cURLを使用してクラウドAPIを呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dateFilter?range=A1:B1&fieldIndex=0&dateTimeGroupingType=Year&year=1920&refresh=true" \
-X PUT \
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

{{< /tab >}}

{{< /tabs >}}



### Aspose.Cells Cloud SDKの使用

SDKを使用するのが開発を進める最も速い方法です。SDKが低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDKの完全なリストについては、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHubリポジトリ</a>をご確認ください。

以下のコード例は、さまざまなSDKを使用してAspose.Cellsウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetDateFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetDateFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetDateFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetDateFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PutWorksheetDateFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetDateFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetDateFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetDateFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}
---