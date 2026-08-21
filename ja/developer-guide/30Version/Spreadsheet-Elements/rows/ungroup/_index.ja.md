---
title: "Excelワークシートの行をグループ解除する"
second_title: "Document"
linktitle: "Ungroup"
type: docs
url: /ja/rows/ungroup/
aliases: [  /ja/ungroup-rows-in-excel-worksheet/ ]
keywords: "行のグループ解除, Excel, Aspose.Cells Cloud, REST API, SDK, スプレッドシート"
description: "Aspose.Cells Cloud REST API および various programming languages の SDK を使用して Excel ワークシートの行をグループ解除する方法を学びます。"
weight: 70
---

この REST API は、Excel ワークシートの行をグループ解除します。

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/ungroup
```

### **リクエストパラメーター**

| パラメーター名 | 型      | 位置   | 説明                                                                 |
| -------------- | ------- | ------ | ------------------------------------------------------------------- |
| name           | string  | path   | ワークブックの名前。                                               |
| sheetName      | string  | path   | ワークシートの名前。                                               |
| firstIndex     | integer | query  | グループ解除する最初の行の 0 から始まるインデックス。               |
| lastIndex      | integer | query  | グループ解除する最後の行の 0 から始まるインデックス。               |
| isAll          | boolean | query  | **true** の場合、指定された範囲内のすべての行がグループ解除されます。 |
| folder         | string  | query  | ワークブックを含むフォルダー。                                     |
| storageName    | string  | query  | ワークブックが配置されているストレージの名前。                     |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/PostUngroupWorksheetRows) は、公開可能なプログラミングインターフェースを定義し、Web ブラウザーから直接 REST アクセスを実行できるようにします。

cURL コマンドラインツールを使用すると、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用して Cloud API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/ungroup?firstIndex=1&lastIndex=5&isAll=true" \
 -X POST \
 -H "Content-Type: application/json" \
 -H "Accept: application/json" \
 -H "Authorization: Bearer <jwt token>"
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

## Cloud SDK Family

SDK を使用することは、開発を迅速化する最良の方法です。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストについては、[GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUngroupWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUngroupWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUngroupWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUngroupWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUngroupWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUngroupWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUngroupWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUngroupWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}