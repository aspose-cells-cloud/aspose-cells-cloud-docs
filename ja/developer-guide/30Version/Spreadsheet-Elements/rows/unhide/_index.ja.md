---
title: "Excelワークシートで行を表示状態に戻す"
second_title: "Document"
linktitle: "Unhide"
type: docs
url: /ja/rows/unhide/
aliases: [  /ja/unhide-rows-in-excel-worksheet/ ]
keywords: "Aspose.Cells Cloud, Excel, 行を表示状態に戻す, REST API, スプレッドシート, .NET, Java, Python, Node.js, Ruby, Go, PHP, Perl, Swift, Aspose.Cells Cloud REST API"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークシートの行を表示状態に戻します。この API は、.NET、Java、Python、Node.js、Ruby、Go、PHP、Perl、Swift などの複数の SDK を通じて利用できます。"
weight: 50
ArticleTitle: "Aspose.Cells Cloud API を使用して Excel ワークシートの行を表示状態に戻す"
---

この REST API は、Excel ワークシートの行を表示状態に戻します。

**前提条件:** Aspose Cloud 認証サービスから有効な JWT アクセストークンを取得し、対象のワークブックをサポートされているストレージにアップロード済みであることを確認してください。

## PostUnhideWorksheetRows API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/unhide
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### **リクエストパラメータ**

| パラメータ名   | 型      | 位置   | 説明                                      |
| -------------- | ------- | ------ | ------------------------------------------- |
| name           | string  | path   | ワークブック名。                            |
| sheetName      | string  | path   | ワークシート名。                            |
| startrow       | integer | query  | 表示状態に戻す最初の行の 0 から始まるインデックス。 |
| totalRows      | integer | query  | 表示状態に戻す行数。                        |
| height         | number  | query  | 行の高さ（デフォルト：15.0）。              |
| folder         | string  | query  | ドキュメントフォルダ。                      |
| storageName    | string  | query  | ストレージ名。                              |

<a href="https://apireference.aspose.cloud/cells/#/Cells/PostUnhideWorksheetRows" rel="noopener noreferrer">OpenAPI スペック</a> は、パブリックにアクセス可能なプログラミングインタフェースを定義し、Web ブラウザから直接 REST アクセスを実行できるようにします。

**認証**  
すべてのリクエストは、Aspose Cloud 認証サービスから取得した JWT アクセストークンを使用して認証される必要があります。トークンは `Authorization: Bearer <jwt token>` ヘッダーに含めてください。

cURL コマンドラインツールを使用すると、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例では、cURL を使用してクラウド API にリクエストを行う方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/unhide?startrow=1&totalRows=1&height=15" \
 -X POST \
 -H "Content-Type: application/json" \
 -H "Accept: application/json" \
 -H "Authorization: Bearer <jwt token>"
# 注: このエンドポイントでは POST 本文は空です
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

**HTTP ステータスコード**

| コード | 意味                         | 説明                                            |
|------|-----------------------------|-------------------------------------------------|
| 200  | OK                          | フィルターの適用に成功；レスポンスには操作の詳細が含まれます。 |
| 400  | Bad Request                 | パラメータが不足している、または無効です（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized                | JWT トークンが無効または不足しています。          |
| 413  | Payload Too Large           | アップロードされたファイルがサイズ制限を超えています。 |
| 500  | Internal Server Error       | サーバー側で予期しないエラーが発生しました。      |

詳細なトラブルシューティングについては、[エラーハンドリングガイド](/error-handling/) を参照してください。

## Cloud SDK ファミリー

SDK を使用すると、開発を最適化できます。SDK が低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全なリストは [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスにリクエストを行う方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnhideWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnhideWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnhideWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnhideWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnhideWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnhideWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnhideWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnhideWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnhideWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnhideWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnhideWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnhideWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnhideWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnhideWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnhideWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnhideWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}
---