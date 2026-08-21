---
title: "Excelワークシート内のピボットテーブルを削除する"
second_title: "Document"
linktitle: "削除"
type: docs
url: "/ja/pivot-tables/delete/"
aliases: [/delete-worksheet-pivot-table-by-index/]
keywords: "Aspose.Cells, ピボットテーブル, 削除, Excel, REST API"
description: "Aspose.Cells Cloud REST API (v3.0) を使用して Excel ワークシートからピボットテーブルを削除します。リクエスト形式、cURL の例、エラーコード、および C#、Java、Python、Node.js 向けの SDK スニペットを含みます。"
weight: 70
ArticleTitle: "Aspose.Cells Cloud を使って Excel ワークシート内のピボットテーブルを削除する方法"
---

この REST API は、ワークシート内のピボットテーブルをインデックスで削除します。

**前提条件** – Aspose.Cells Cloud 用の有効な JWT アクセストークンと、対象となる Excel ファイルがサポートされたストレージの場所に保存されている必要があります。API を呼び出す前に、ファイル名、ワークシート名、およびストレージの詳細が正しく指定されていることを確認してください。

ピボットテーブルは、**Excel ワークシート**でデータを要約する強力な手段です。Aspose.Cells Cloud を使用すると、単一の HTTP DELETE リクエストで不要なピボットテーブルをプログラムで削除できます。この操作は、ワークシートのクリーンアップ、レポート生成の自動化、または Excel 操作をアプリケーションに統合する必要がある場合に最適です。

## DeleteWorksheetPivotTable API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### **リクエストパラメータ**

| パラメータ名      | 型     | 位置   | 説明                                             |
| ---------------- | ------ | ------ | ------------------------------------------------- |
| name             | 文字列 | path   | Excel ドキュメントの名前。                        |
| sheetName        | 文字列 | path   | ピボットテーブルを含むワークシートの名前。        |
| pivotTableIndex  | 整数   | path   | 削除するピボットテーブルの 0 から始まるインデックス。 |
| folder           | 文字列 | query  | ドキュメントが保存されているフォルダへのパス。    |
| storageName      | 文字列 | query  | ストレージサービスの名前。                        |

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/PivotTables/DeleteWorksheetPivotTable) は、パブリックにアクセス可能なプログラミングインタフェースを定義し、Web ブラウザから直接 REST 通信を実行できるようにします。

**cURL コマンドラインツール** を使用すると、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API にアクセスする方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

**レスポンスの例**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

レスポンスは以下のシンプルな JSON スキーマに従います：

```json
{
  "Code": 整数,   // 操作の HTTP に似たステータスコード
  "Status": 文字列   // 例："OK" などのテキスト説明
}
```

{{< /tab >}}

{{< /tabs >}}

### エラーハンドリング

一般的なレスポンスステータスコードを以下に示します：

| HTTP ステータス | 説明                                          |
| --------------- | --------------------------------------------- |
| 400             | 不正なリクエスト – パラメータが不足または無効。     |
| 401             | 認証エラー – 無効または未指定の JWT トークン。     |
| 404             | 見つかりません – ファイル、ワークシート、またはピボットテーブルが存在しません。 |
| 500             | サーバー内部エラー – サーバー上で予期しない状態が発生しました。 |

## クラウド SDK ファミリー

SDK を使用すると、開発を最適化できます。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストについては、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) を確認してください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスにアクセスする方法を示しています：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-DeleteWorksheetPivotTableIndex-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-DeleteWorksheetPivotTableIndex-delete-worksheet-pivot-table-index.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteWorksheetPivotTablesByIndex.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-DeleteWorksheetPivotTableIndex-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-DeleteWorksheetPivotTableIndex-delete-worksheet-pivot-table-index.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-DeleteWorksheetPivotTableIndex-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "8798eca5f30bf41a4675b83583a72ec3" >}}

{{< /tab >}}

{{< /tabs >}}
---