---
title: "Excelワークシートの名前変更"
second_title: "Document"
linktitle: "名前変更"
type: docs
url: /ja/worksheets/rename/
aliases: [  /ja/rename-excel-worksheet/ ]
keywords: "Aspose.Cells Cloud, Excelワークシートの名前変更, REST API, スプレッドシートSDK, ワークシート名変更, クラウドストレージ"
description: "Aspose.Cells Cloud REST APIを使用してExcelワークブック内のワークシートの名前を変更します。SDKはAndroid、C#、Go、Java、Node.js、Perl、PHP、Python、Ruby、Swiftで利用可能です。"
weight: 20
---

このREST APIは、Excelワークシートの名前を変更します。

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/rename
```

### **リクエストパラメータ**

| パラメータ名     | タイプ   | 位置   | 説明                                     |
| ---------------- | -------- | ------ | ---------------------------------------- |
| name             | string   | path   | Excelファイルの名前。                    |
| sheetName        | string   | path   | 名前を変更するワークシートの現在の名前。 |
| newname          | string   | query  | ワークシートの新しい名前。               |
| folder           | string   | query  | ストレージ内のフォルダーパス（オプション）。 |
| storageName      | string   | query  | ストレージの名前（オプション）。         |

[OpenAPI仕様書](https://apireference.aspose.cloud/cells/#/Worksheets/PostRenameWorksheet)には、パブリックにアクセス可能なプログラミングインターフェースが定義されており、Webブラウザから直接REST通信を実行できます。

cURLコマンドラインツールを使用することで、Aspose.Cells Webサービスに簡単にアクセスできます。以下の例では、cURLを使用してCloud APIへの呼び出しを行う方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/rename?newname=newSheet" \
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

SDKを使用することが開発を最適化する最良の方法です。SDKが低レベルの詳細を処理するため、開発者はプロジェクトのタスクに集中できます。Aspose.Cells Cloud SDKの完全なリストは[GitHubリポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまなSDKを使用してAspose.Cells Webサービスへの呼び出しを行う方法を示しています。

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPostRenameWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-RenameWorksheet-rename-excel-worksheeet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PostRenameWorksheet-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-rename_worksheet-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "RenameExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-RenameWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-RenameWorksheet-rename-excel-worksheeet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-RenameWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "accf2723cfaa2a328d3dea355156e4d9" >}}

{{< /tab >}}

{{< /tabs >}}