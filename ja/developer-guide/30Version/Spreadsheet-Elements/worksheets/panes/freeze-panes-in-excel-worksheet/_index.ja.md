---
title: "Excelワークシートでのペインの固定"
second_title: "Document"
linktitle: "固定"
type: docs
url: /worksheets/panes/freeze/
aliases: [/freeze-panes-in-excel-worksheet/, /worksheets/freeze-panes/]
keywords: "Aspose.Cells Cloud, ペインの固定, Excel, REST API, ワークシート"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークシートで行と列を固定する方法を学びます。エンドポイント構文、必要なパラメータ、cURL の使用例、認証ガイド、エラー応答の詳細、および複数言語向けの SDK コードサンプルを含みます。"
weight: 190
---

この REST API は、Excel ワークシートに**ペインの固定**を設定します。

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/freezepanes
```

リクエストパラメータは以下の通りです：

| パラメータ名     | 型      | 位置   | 説明                                                   |
| ---------------- | ------- | ------ | ------------------------------------------------------ |
| name             | string  | path   | ワークブックファイルの名前。                           |
| sheetName        | string  | path   | ペインを固定するワークシートの名前。                   |
| row              | integer | query  | 最初の**固定されていない**行の 0 から始まるインデックス。 |
| column           | integer | query  | 最初の**固定されていない**列の 0 から始まるインデックス。 |
| frozenRows       | integer | query  | 上部から固定する行数。                                 |
| frozenColumns    | integer | query  | 左端から固定する列数。                                 |
| folder           | string  | query  | ストレージ内にワークブックが存在するフォルダのパス。   |
| storageName      | string  | query  | ストレージサービスの名前。                             |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/PutWorksheetFreezePanes) はパブリックにアクセス可能なプログラミングインタフェースを定義し、ウェブブラウザから直接 REST 通信を実行できるようにします。

cURL コマンドラインツールを使用して、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例では、cURL を使って Cloud API へリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/freezepanes?row=1&column=1&frozenRows=1&frozenColumns=1" \
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

### エラー応答

| HTTP ステータス           | コード | メッセージ                         | 例                                                       |
| ------------------------- | ---- | ---------------------------------- | -------------------------------------------------------- |
| 400 Bad Request           | 400  | 無効なパラメータ                   | `{ "Code": 400, "Message": "Invalid frozenRows value" }` |
| 401 Unauthorized          | 401  | JWT トークンが不足しているか無効   | `{ "Code": 401, "Message": "Invalid access token" }`     |
| 404 Not Found             | 404  | ワークブックまたはワークシートが見つからない | `{ "Code": 404, "Message": "File not found" }`           |
| 500 Internal Server Error | 500  | 想定外のサーバーエラー             | `{ "Code": 500, "Message": "Internal server error" }`    |

## Cloud SDK Family

SDK を使用することが開発を高速化する最善の方法です。SDK が低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスへリクエストを送信する方法を示しています：

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Objective C" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPutWorksheetFreezePanes.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-FreezePanes-freeze-panes.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PutWorksheetFreezePanes-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-set_freeze_panes-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-FreezePanes-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-FreezePanes-freeze-panes.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-FreezePanes-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "099a22da7db4d5602c0da3b90bc1dc30" >}}

{{< /tab >}}

{{< /tabs >}}