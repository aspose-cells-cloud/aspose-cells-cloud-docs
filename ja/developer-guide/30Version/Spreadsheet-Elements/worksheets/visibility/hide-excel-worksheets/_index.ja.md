---
title: "Excelワークシートを非表示にする"
second_title: "ドキュメント"
linktitle: "非表示"
type: docs
url: /worksheets/hide/
aliases: [/hide-excel-worksheets/]
keywords: "Aspose.Cells Cloud, Excel, ワークシートを非表示にする, REST API, スプレッドシート"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークブック内のワークシートを非表示にする手順ガイド。リクエスト詳細、cURL の使用例、複数の言語向け SDK のコードスニペットを含みます。"
weight: 50
---

この REST API は、ワークシートを非表示にします。

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/visible
```

### **リクエストパラメータ**

| パラメータ名     | 型      | 位置   | 説明                                                  |
| ---------------- | ------- | ------ | ----------------------------------------------------- |
| name             | string  | path   | Excel ワークブックファイルの名前。                   |
| sheetName        | string  | path   | 変更するワークシートの名前。                         |
| isVisible        | boolean | query  | 表示フラグ（`true` は表示、`false` は非表示）。     |
| folder           | string  | query  | ワークブックが保存されているフォルダのパス。         |
| storageName      | string  | query  | ストレージサービスの名前。                           |

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/Worksheets/PutChangeVisibilityWorksheet) では、パブリックにアクセス可能なプログラミングインターフェースを定義し、ウェブブラウザから直接 REST アクセスを実行できるようにしています。

Aspose.Cells ウェブサービスにアクセスするには、cURL コマンドラインツールを使用するのが最も簡単です。以下の例では、cURL を使用して Cloud API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.com/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/visible?isVisible=false" \
-X PUT \
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

## クラウド SDK ファミリー

SDK を使用すると、開発 speed を最大化できます。SDK が低レベルの詳細処理を担い、あなたはプロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全な一覧は、[GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご覧ください。

以下のコード例では、さまざまな SDK を使用して Aspose.Cells ウェブサービスへの呼び出しを行う方法を示しています。

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Worksheet-HideWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-HideWorksheet-hide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PutChangeVisibilityWorksheet-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-change_worksheet_visibility-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "HideExcelWorkSheets.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-HideWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-HideWorksheet-hide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-HideWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "cb5a1656cea2f870f0a5ef6d066525ef" >}}

{{< /tab >}}

{{< /tabs >}}