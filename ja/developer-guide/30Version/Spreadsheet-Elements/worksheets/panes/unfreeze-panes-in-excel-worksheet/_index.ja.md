---
title: "Excelワークシートのペインの固定を解除する"
second_title: "Document"
linktitle: "Unfreeze"
type: docs
url: /ja/worksheets/panes/unfreeze/
aliases:
  - /unfreeze-panes-in-excel-worksheet/
  - /worksheets/unfreeze-panes/
keywords: "ペインの固定解除, Excel, Aspose.Cells Cloud, REST API, SDK, C#, Java, PHP, Python, Node.js, Go, Swift, Android, Ruby, Perl"
description: "Aspose.Cells Cloud REST API (v3.0) を使用して Excel ワークシートから固定ペインを解除（削除）する方法を学習します。cURL の例と、C#、Java、Python などの SDK コードスニペットを含みます。"
weight: 200
---

この REST API の呼び出しは、Excel ワークシートから**固定ペインを解除**（削除）します。

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/freezepanes
```

### **リクエストパラメーター**

| パラメーター名 | 型     | 位置   | 説明                                      |
| -------------- | ------ | ------ | ----------------------------------------- |
| `name`         | string | path   | Excel ファイル名。                        |
| `sheetName`    | string | path   | ワークシート名。                          |
| `folder`       | string | query  | ファイルが配置されているストレージ内のフォルダー パス。 |
| `storageName`  | string | query  | Aspose Cloud ストレージの名前。           |

_固定ペインの解除処理には、追加のクエリ パラメーター（行、列、frozenRows、frozenColumns など）は必要ありません。_

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetFreezePanes) は、パブリックにアクセス可能なプログラミング インターフェースを定義し、ウェブブラウザーから直接 REST アクセスを実行できます。

cURL コマンドラインツールを使用すると、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使ってクラウド API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/freezepanes" \
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

## Cloud SDK ファミリー

SDK を使用すると、開発速度が最も高まります。SDK が低レベルの詳細処理を担当するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全なリストについては、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsDeleteWorksheetFreezePanes.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-UnfreezePanes-unfreeze-panes.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-DeleteWorksheetFreezePanes-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-unfreeze_panes-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UnfreezePanesInExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-UnfreezePanes-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-UnfreezePanes-unfreeze-panes.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-UnfreezePanes-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "23052de16f4f1cd75542ce4ae9b3ada8" >}}

{{< /tab >}}

{{< /tabs >}}