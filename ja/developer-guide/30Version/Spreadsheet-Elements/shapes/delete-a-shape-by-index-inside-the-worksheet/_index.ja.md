---
title: "Excelワークシート上の図形をインデックスで削除する"
second_title: "Document"
linktitle: "削除"
type: docs
url: /shapes/delete/
aliases: [/delete-a-shape-by-index-inside-the-worksheet/]
keywords: "Aspose.Cells Cloud, 図形の削除, 図形インデックス, Excelワークシート, REST API, SDK"
description: "Aspose.Cells Cloud REST APIを使用して、Excelワークシート上の図形をそのインデックスで削除します。このAPIは、複数のSDK（C#、Java、PHP、Ruby、Node.js、Python、Perl、Go）で利用可能で、さまざまなストレージオプションをサポートしています。"
weight: 50
---

このREST APIは、Excelワークシート上の図形を削除します。

## REST API

```bash
DELETE http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes/{shapeindex}
```

### **リクエストパラメータ**

| パラメータ名   | 型      | 位置   | 説明                                      |
| -------------- | ------- | ------ | ----------------------------------------- |
| name           | string  | path   | ワークブックファイルの名前。              |
| sheetName      | string  | path   | ワークシートの名前。                      |
| shapeindex     | integer | path   | ワークシート内の図形のインデックス。      |
| folder         | string  | query  | ワークブックが保存されているフォルダ。    |
| storageName    | string  | query  | ストレージの名前。                        |

[OpenAPI仕様書](https://apireference.aspose.cloud/cells/#/Shapes/DeleteWorksheetShape) は、パブリックに利用可能なプログラミングインターフェースを定義し、ウェブブラウザから直接RESTのやり取りを実行できるようにしています。

**cURL** コマンドラインツールを使用すると、Aspose.Cellsウェブサービスに簡単にアクセスできます。以下の例は、cURLでクラウドAPIにリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes/1" \
-X DELETE \
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

## クラウドSDKファミリー

SDKを使用することが、開発を最速で進める方法です。SDKが低レベルの詳細を処理するため、あなたはプロジェクトのタスクに集中できます。Aspose.Cells Cloud SDKの完全なリストについては、[GitHubリポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまなSDKを使用してAspose.Cellsウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}