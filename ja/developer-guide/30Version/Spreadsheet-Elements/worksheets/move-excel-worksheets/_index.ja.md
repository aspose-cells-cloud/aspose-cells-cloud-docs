---
title: "Excelワークシートの移動 – Aspose.Cells Cloud API (v3.0)"
second_title: "ドキュメント"
linktitle: "移動"
type: docs
url: /ja/worksheets/move/
aliases: [  /ja/move-excel-worksheets/ ]
keywords: "Aspose.Cells Cloud, ワークシートの移動, Excel, REST API, SDK, C#, Java, Python, Node.js, PHP, Ruby, Go, Android, Swift, Perl, v3.0"
description: "Aspose.Cells Cloud API (v3.0) を使用して Excel ワークシートを新しい位置に移動する方法を学びます。エンドポイント、必要なパラメータ、cURL の例、および C#、Java、Python などの SDK コードを含みます。"
weight: 20
ArticleTitle: "Aspose.Cells Cloud API v3.0 を使用して Excel ワークシートを移動する方法"
---

この REST API は、Excel ブック内のワークシートを別の位置に移動します。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/position
```

### リクエストパラメータ

| パラメータ名 | 型     | 位置   | 説明                                                                                         |
|------------|--------|--------|----------------------------------------------------------------------------------------------|
| name       | string | path   | Excel ファイルの名前。                                                                       |
| sheetName  | string | path   | 移動するワークシートの名前。                                                                 |
| moving     | object | body   | 移動先ワークシート (`DestinationWorksheet`) と相対位置 (`Position`) を指定する JSON オブジェクト。 |
| folder     | string | query  | ブックが保存されているフォルダのパス。                                                       |
| storageName| string | query  | ストレージサービスの名前。                                                                   |

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/Worksheets/PostMoveWorksheet) はパブリックにアクセス可能なプログラミングインターフェースを定義し、ウェブブラウザから直接 REST 操作を実行できるようにします。

cURL コマンドラインツールを使用して Aspose.Cells ウェブサービスを呼び出すことができます。以下の例では、単一のリクエストでワークシートを移動する方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/position" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"DestinationWorksheet":"Sheet5","Position":"after"}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**HTTP ステータスコード**

| コード | 意味                         | 説明                                          |
|-------|------------------------------|-----------------------------------------------|
| 200   | OK                           | フィルターが正常に適用され、応答には操作の詳細が含まれます。 |
| 400   | Bad Request                  | パラメータが不足または無効です（例：サポートされていないファイル形式）。 |
| 401   | Unauthorized                 | JWT トークンが無効または不足しています。            |
| 413   | Payload Too Large            | アップロードされたファイルがサイズ制限を超えています。    |
| 500   | Internal Server Error        | サーバーで予期しないエラーが発生しました。            |

**サンプルエラーペイロード**

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "必須パラメータ 'moving' が不足しています。"
}
```

{{< /tab >}}

{{< /tabs >}}

## クラウド SDK ファミリー

SDK を使用すると、開発を最適化できます。SDK は低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全なリストは [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPostMoveWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-UnhideWorksheet-unhide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PostMoveWorksheet-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-move_worksheet-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "MoveExcelWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-MoveWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-MoveWorksheet-move-excel-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-MoveWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "1f9b294ef1cfb23e3775c193f15ff660" >}}

{{< /tab >}}

{{< /tabs >}}
---