---
title: "日付フィルターの削除 – Aspose.Cells Cloud"
second_title: "ドキュメント"
linktitle: "日付フィルターの削除"
type: docs
url: /autofilter/delete-date-filter/
aliases:
  - /remove-a-date-filter/
  - /autofilter/delete-a-date-filter/
weight: 100
keywords: "Aspose.Cells, 日付フィルターの削除, Excel AutoFilter, REST API, SDK"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークシートから日付フィルターを削除する方法を学びます。エンドポイント、パラメーター、HTTPS cURL の例、レスポンスペイロード、および SDK のコードサンプルを含みます。"
ArticleTitle: "日付フィルターの削除 – Aspose.Cells Cloud API ドキュメント"
---

この REST API は、Excel ワークシート上の日付フィルターを削除します。

**前提条件:** 無効な JWT トークンを持たず、ワークブックが Aspose Cloud ストレージに保存されており、ワークシートを変更する適切な権限を持っていることを確認してください。

## DeleteWorksheetDateFilter API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dateFilter
```

### **セキュリティと認証**

Aspose.Cells Cloud API はセキュアであり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を必要とします。

### リクエストパラメーター

| パラメーター名         | 型      | 位置   | 説明                                                                                      |
|------------------------|---------|--------|---------------------------------------------------------------------------------------------|
| name                   | 文字列  | path   | Excel ファイルの名前。                                                                       |
| sheetName              | 文字列  | path   | ワークシート名。                                                                             |
| fieldIndex             | 整数    | query  | フィルターを適用する列の 0 から始まるインデックス。                                           |
| dateTimeGroupingType   | 文字列  | query  | 日付フィルターのグループ化タイプ（例：Year、Month、Day）。                                   |
| year                   | 整数    | query  | フィルターの年コンポーネント（デフォルト：0）。                                              |
| month                  | 整数    | query  | フィルターの月コンポーネント（デフォルト：0）。                                             |
| day                    | 整数    | query  | フィルターの日コンポーネント（デフォルト：0）。                                              |
| hour                   | 整数    | query  | フィルターの時間コンポーネント（デフォルト：0）。                                            |
| minute                 | 整数    | query  | フィルターの分コンポーネント（デフォルト：0）。                                             |
| second                 | 整数    | query  | フィルターの秒コンポーネント（デフォルト：0）。                                             |
| folder                 | 文字列  | query  | ファイルが存在するストレージ内のフォルダーのパス。                                          |
| storageName            | 文字列  | query  | Aspose Cloud ストレージの名前。                                                              |

### **レスポンス**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP ステータスコード**

| コード | 意味                         | 説明                                                 |
|--------|------------------------------|--------------------------------------------------------|
| 200    | OK                           | フィルターが正常に適用された。レスポンスには操作の詳細が含まれる。 |
| 400    | Bad Request                  | パラメーターが不足しているか無効（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized                 | JWT トークンが無効または不足している。                           |
| 413    | Payload Too Large            | アップロードされたファイルがサイズ制限を超えた。                    |
| 500    | Internal Server Error        | 予期しないサーバーエラーが発生した。                              |

この API は、削除操作の結果を示す標準的な HTTP ステータスコードを返します。

| コード | 意味 | 説明 |
|--------|------|------|
| 200    | OK   | 日付フィルターが正常に削除された。レスポンスには操作の状態が含まれる。 |
| 400    | Bad Request | パラメーターが不足しているか無効（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized | JWT トークンが無効または不足している。 |
| 413    | Payload Too Large | アップロードされたファイルがサイズ制限を超えた。 |
| 500    | Internal Server Error | 予期しないサーバーエラーが発生した。 |

## SDK を使用した DeleteWorksheetDateFilter API の利用方法

### DeleteWorksheetDateFilter API 仕様

<a href="https://apireference.aspose.cloud/cells/#/AutoFilter/DeleteWorksheetDateFilter" rel="noopener noreferrer">OpenAPI 仕様</a> はパブリックに利用可能なプログラミングインタフェースを定義し、Web ブラウザーから直接 REST アクセスを実行できるようにします。

cURL コマンドラインツールを使用して Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、cURL を使用して Cloud API にアクセスする方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dateFilter?fieldIndex=0&dateTimeGroupingType=Year&year=1920" \
  -X DELETE \
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

### Aspose.Cells Cloud SDK の利用

SDK を使用すると、開発を迅速化できます。SDK が低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全なリストについては、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリー</a>をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスにアクセスする方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetDateFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetDateFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetDateFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetDateFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetDateFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetDateFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetDateFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetDateFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}