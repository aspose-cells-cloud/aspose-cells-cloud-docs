---
title: "Excelワークシートの列を表示状態に戻す"
ArticleTitle: "Excelワークシートの列を表示状態に戻す - Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktitle: "表示状態に戻す"
type: docs
url: /ja/columns/unhide/
aliases:
  [/unhide-columns-in-an-excel-worksheet/, /unhide-columns-in-excel-worksheet/]
keywords: "Aspose.Cells, Cloud API, 列の表示状態に戻す, Excel, REST, SDK"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークシートの列を表示状態に戻す方法を学びます。リクエストの詳細、cURL の例、および複数のプログラミング言語向けの SDK コードサンプルを含みます。"
weight: 50
---

この REST API は、ワークシートの列を表示状態に戻します。

**前提条件** – Aspose.Cells Cloud のすべてのエンドポイントは HTTPS および有効な OAuth 2.0 アクセストークンを必要とします。アクセストークンを取得し、リクエストの `Authorization` ヘッダーに含めることを確認してください。

## PostUnhideWorksheetColumns API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/unhide
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を必要とします。

### リクエストパラメーター

| パラメーター名     | 型       | 位置   | 説明                               |
| ---------------- | -------- | ------ | ----------------------------------- |
| name             | 文字列   | path   | ワークブック名。                    |
| sheetName        | 文字列   | path   | ワークシート名。                    |
| startColumn      | 整数     | query  | 処理する最初の列のインデックス。     |
| totalColumns     | 整数     | query  | 処理する列の数。                    |
| width            | 数値     | query  | 期望する列幅（デフォルト = 50.0）。  |
| folder           | 文字列   | query  | ドキュメントを含むフォルダー。      |
| storageName      | 文字列   | query  | ストレージサービスの名前。          |

<a href="https://apireference.aspose.cloud/cells/#/Cells/PostUnhideWorksheetColumns" target="_blank" rel="noopener noreferrer">OpenAPI スペック</a> は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザーから直接 REST 通信を実行できるようにします。

**cURL** コマンドラインツールを使用して、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、cURL を使用して Cloud API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/unhide?startColumn=1&totalColumns=1&width=15" -H "accept: application/json"
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

**一般的な HTTP ステータスコード**

| コード | 説明                                           |
|--------|-----------------------------------------------|
| 200    | OK – 列が正常に表示状態に戻されました。        |
| 400    | Bad Request – 無効なパラメーター。            |
| 401    | Unauthorized – トークンが不足しているか無効です。|
| 404    | Not Found – ワークブックまたはワークシートが見つかりません。|
| 500    | Internal Server Error – 予期せぬエラーが発生しました。|

## Cloud SDK Family

SDK を使用することが開発を高速化する最良の方法です。SDK が低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全なリストについては、<a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub リポジトリー</a>をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnhideWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnhideWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnhideWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnhideWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnhideWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnhideWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnhideWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnhideWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}