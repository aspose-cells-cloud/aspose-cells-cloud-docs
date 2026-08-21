---
title: "ワークシートからすべてのチャートを削除する"
type: docs
url: /charts/clear/
aliases: [/delete-all-charts-from-a-worksheet/]
weight: 30
keywords: "Aspose.Cells, Cloud, 削除, 全チャート, ワークシート, REST API, DELETE, SDK"
description: "Aspose.Cells Cloud REST API（v3.0）を使用してワークシート内のすべてのチャートを削除する方法を学びます。エンドポイント、パラメータ、cURLサンプル、SDKコードスニペット、認証手順、エラーハンドリングを含みます。"
ArticleTitle: "Aspose.Cells Cloud API を使用してワークシートからすべてのチャートを削除する"
---

この REST API は、指定されたワークシートからすべてのチャートを削除します。

**背景** – ワークシートからすべてのチャートを削除するのは、シートの視覚的レイアウトをリセットしたり、陳腐化したビジュアライゼーションを置き換えたり、以前のチャートデータを保持せずにワークブックを再利用できるように準備したりする場合に便利です。

API を呼び出す前に、以下の前提条件が満たされていることを確認してください。

- 認証用に有効な JWT トークンが取得できていること。  
- ワークブックファイルが指定されたストレージの場所およびフォルダ内に存在すること。  
- API バージョン **v3.0** を使用していること。

## DeleteWorksheetClearCharts API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を必要とします。

### リクエストパラメータ

| パラメータ名 | 型     | 位置   | 説明                             |
| ------------ | ------ | ------ | -------------------------------- |
| name         | string | path   | ワークブックファイル名。         |
| sheetName    | string | path   | ワークシート名。                 |
| folder       | string | query  | ワークブックが保存されているフォルダ。 |
| storageName  | string | query  | ストレージ名。                   |

**リクエストヘッダー**

| ヘッダー        | 説明                         |
|---------------|------------------------------|
| Authorization | Bearer `<jwt トークン>`      |
| Accept        | `application/json`           |
| Content-Type  | `application/json`（ボディなし）|

**リクエストボディ**

DELETE 操作では、リクエストボディは**不要**です。

**レスポンス**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP ステータスコード**

| コード | 意味                         | 説明                                             |
|------|------------------------------|--------------------------------------------------|
| 200  | OK                           | フィルターが正常に適用された。レスポンスには操作の詳細が含まれる。 |
| 400  | Bad Request                  | パラメータが不足または無効（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized                 | JWT トークンが無効または不足している。 |
| 413  | Payload Too Large            | アップロードされたファイルがサイズ制限を超えた。 |
| 500  | Internal Server Error        | サーバー上で予期せぬエラーが発生した。 |

*エラーレスポンスの例*

```json
// 400 Bad Request
{
    "Code": 400,
    "Message": "無効なパラメータ: 'sheetName' は必須です。"
}

// 401 Unauthorized
{
    "Code": 401,
    "Message": "認証に失敗しました。無効な JWT トークンです。"
}

// 413 Payload Too Large
{
    "Code": 413,
    "Message": "リクエストペイロードが許容される最大サイズを超えています。"
}

// 500 Internal Server Error
{
    "Code": 500,
    "Message": "サーバー上で予期せぬエラーが発生しました。"
}
```

## SDK を使用した DeleteWorksheetClearCharts API の利用方法

### DeleteWorksheetClearCharts API 仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetClearCharts)は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 通信を実行できるようにします。

cURL コマンドラインツールを使用して、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例では、cURL を使用してクラウド API にリクエストを行う方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/charts" \
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

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、ワークシートから**すべてのチャートを削除**する際の開発を高速化できます。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスにリクエストを行う方法を示しています。

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-DeleteAllCharts-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-DeleteAllCharts-delete-all-charts.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetClearCharts-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-clear_the_charts-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteAllChartsFromAWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-DeleteAllCharts-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-DeleteAllCharts-delete-all-charts.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-DeleteAllCharts-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "1775c5a8985efa819486b7ede2c34bfc" >}}

{{< /tab >}}

{{< /tabs >}}