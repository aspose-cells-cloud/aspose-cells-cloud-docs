---
title: "範囲内のセルの結合を解除する"  
second_title: "Document"  
linktitle: "Unmerge"  
type: docs  
url: /ranges/unmerge/  
aliases: [/unmerge-merged-cells-of-the-range/]  
keywords: "Aspose.Cells Cloud、セルの結合解除、Excel API、ワークシート範囲、REST API"  
description: "Aspose.Cells Cloud API を使用して、特定のワークシート範囲内の結合済みセルを解除する方法を学びます。エンドポイント、パラメーター、サンプルの cURL、および C#、Java、Python などの SDK コードスニペットを含みます。"  
weight: 20  
---  

この REST API は、Excel ワークシート上の指定された範囲内の結合済みセルを解除します。

## REST API  

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/unmerge
```  

リクエストパラメーターは以下の通りです：

| パラメーター名 | 型     | 位置   | 必須 | 説明                                     |
|----------------|--------|--------|------|---------------------------------------------|
| name           | 文字列 | パス   | はい  | ワークブック名。                            |
| sheetName      | 文字列 | パス   | はい  | ワークシート名。                            |
| range          | オブジェクト | 本体 | はい  | 解除するセルを定義する範囲オブジェクト。       |
| folder         | 文字列 | クエリ | いいえ | ワークブックを含むフォルダー。               |
| storageName    | 文字列 | クエリ | いいえ | ストレージ名。                              |

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeUnmerge) は、パブリックに利用可能なプログラミングインタフェースを定義し、Web ブラウザーから直接 REST のやり取りを実行できるようにします。

cURL コマンドラインツールを使用すると、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例では、cURL を使用してクラウド API にアクセスする方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/unmerge" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
    "ColumnCount": 7,
    "ColumnWidth": 19,
    "FirstColumn": 0,
    "FirstRow": 9,
    "Name": "string",
    "RefersTo": "string",
    "RowCount": 1,
    "RowHeight": 15,
    "Worksheet": "Sheet1"
}'
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

## Cloud SDK ファミリー  

SDK を使用することが開発を加速する最良の方法です。SDK は低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全なリストについては、[GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeUnMerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeUnMerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeUnMerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeUnMerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeUnMerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeUnMerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeUnMerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeUnMerge.go" >}}

{{< /tab >}}

{{< /tabs >}}