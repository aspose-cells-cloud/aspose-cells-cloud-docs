---
title: "ワークシートの削除"
second_title: "Document"
linktype: "One worksheet"
type: docs
url: /ja/worksheets/delete-worksheet/
aliases: [  /ja/remove-worksheets-from-excel-workbooks/ ]
keywords: "Aspose.Cells Cloud, ワークシートの削除, Excel, スプレッドシート, REST API"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークブックからワークシートを削除します。C#、Java、PHP、Ruby、Node.js、Python、Perl、Go、cURL の SDK をサポートしています。"
weight: 20
ArticleTitle: "ワークシートの削除 – Aspose.Cells Cloud API"
---

この REST API はワークシートを削除します。  
前提条件：この API を呼び出すには、**Authorization** ヘッダーに有効な JWT 認証トークンを提供し、ワークブックが存在するストレージ場所へのアクセス権が必要です。

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

*注：API は現在の安定版であるバージョン **v3.0** を使用します。今後のバージョン変更はリリースノートで公告されます。*

### **リクエストパラメーター**

| パラメーター名 | 型     | 位置   | 説明           |
| -------------- | ------ | ------ | --------------- |
| name           | string | path   | ドキュメント名。 |
| sheetName      | string | path   | ワークシート名。 |
| folder         | string | query  | ドキュメントのフォルダー。 |
| storageName    | string | query  | ストレージ名。   |

考えられる HTTP 応答：

| ステータスコード | 説明 |
| --------------- | --- |
| 200 OK | ワークシートが正常に削除されました。 |
| 400 Bad Request | 無効なリクエストパラメーターです。 |
| 401 Unauthorized | 認証に失敗したか、トークンが不足しています。 |
| 404 Not Found | 指定されたワークブックまたはワークシートが存在しません。 |
| 500 Internal Server Error | 予期しないサーバーエラーです。 |

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheet) はパブリックに利用可能なプログラミングインターフェースを定義し、Web ブラウザーから直接 REST 通信を実行できるようにします。

cURL コマンドラインツールを使用すると、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例では、cURL を使用してクラウド API にアクセスする方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet3" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

*すべてのリクエストは HTTPS 経由で行う必要があります。API は非 TLS 接続をサポートしていません。*

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

## Cloud SDK Family

SDK を使用すると、開発を最適化できます。SDK は低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリー](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例では、さまざまな SDK を使用して Aspose.Cells ウェブサービスにアクセスする方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}