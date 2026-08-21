---
title: レンジの並べ替え
second_title: "Document"
linktitle: "並べ替え"
type: docs
keywords: "レンジの並べ替え, Aspose.Cells Cloud, REST API, スプレッドシート, Excel, API"
url: /ja/ranges/sort/
description: Aspose.Cells Cloud を使用して、ワークブック内のセル範囲を並べ替えるための API を提供します。
weight: 20
---

この REST API は、指定されたセル範囲を並べ替えます。

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/sort
```

リクエストパラメーターは以下の通りです：

| パラメーター名 | 型     | 位置   | 説明                                       |
|----------------|--------|--------|---------------------------------------------|
| name           | String | Path   | ワークブック名。                            |
| sheetName      | String | Path   | シート名。                                  |
| rangeOperate   | Class  | Body   | レンジ並べ替えリクエストオブジェクト。     |
| folder         | String | Query  | 元のワークブックが格納されているフォルダー。|
| storageName    | String | Query  | ストレージ名。                              |

[OpenAPI スペック](https://reference.aspose.cloud/cells/#/RangesController/PostWorksheetCellsRangeSort) はパブリックに利用可能なプログラミングインターフェースを定義し、Web ブラウザーから直接 REST アクセスを実行できるようにします。

cURL コマンドラインツールを使用して Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使って Cloud API にリクエストを送る方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}
{{< tab tabNum="1" >}}

```powershell
curl -v "http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/sort" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="2" >}}

```powershell
# （レスポンスの例はここに表示されます）
```

{{< /tab >}}
{{< /tabs >}}

## Cloud SDK ファミリー

SDK を使用するのが開発を最適化する最良の方法です。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧については、GitHub リポジトリーをご確認ください。

以下のコード例は、さまざまな SDK を使って Aspose.Cells ウェブサービスにリクエストを送る方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeSort.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeSort.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeSort.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeSort.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeSort.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeSort.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeSort.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeSort.go" >}}

{{< /tab >}}

{{< /tabs >}}