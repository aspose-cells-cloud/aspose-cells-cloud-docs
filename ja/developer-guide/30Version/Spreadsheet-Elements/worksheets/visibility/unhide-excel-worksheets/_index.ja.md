---
title: "Excelワークシートを表示状態に戻す"
second_title: "ドキュメント"
linktitle: "表示状態に戻す"
type: docs
url: /worksheets/unhide/
aliases: [/unhide-excel-worksheets/]
keywords: "Aspose.Cells, ワークシートの表示状態に戻す, Excel API, クラウドスプレッドシート, REST, ワークシートの表示設定, Excelワークブック"
description: "Aspose.Cells Cloud REST API を使って Excel ワークブック内のワークシートを表示状態に戻す方法を学びます。リクエストの詳細、cURL の例、複数のプログラミング言語向けの SDK コードスニペットを含みます。"
weight: 60
---

この REST API は、Excel ワークブック内のワークシートを**表示状態に戻す**ためのエンドポイントを提供します。

**事前条件**  
この操作を呼び出す前に、以下の条件を満たしている必要があります：

* `Authorization` ヘッダーに有効な Aspose Cloud アクセストークン（JWT）を含めること。
* `folder` および `storageName` クエリパラメーターで指定した、サポートされているストレージロケーションにワークブックが保存されていること。
* ワークブックの形式が Aspose.Cells でサポートされているもの（例：`.xls`, `.xlsx`, `.xlsm`）であること。

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/visible
```

### **リクエストパラメーター**

| パラメーター名 | 型      | 位置   | 説明                                   |
| -------------- | ------- | ------ | ---------------------------------------- |
| name           | 文字列  | パス   | ドキュメント名。                         |
| sheetName      | 文字列  | パス   | ワークシート名。                         |
| isVisible      | 真偽値  | クエリ | ワークシートの新しい表示状態の値（`true`）。 |
| folder         | 文字列  | クエリ | ドキュメントのフォルダー。               |
| storageName    | 文字列  | クエリ | ストレージ名。                           |

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/Worksheets/PutChangeVisibilityWorksheet) は、Web ブラウザーから直接 REST 操作を実行できるパブリックに利用可能なプログラミングインターフェースを定義しています。

cURL コマンドラインツールを使って、Aspose.Cells Web サービスを簡単に呼び出すことができます。以下の例では、cURL を使ったリクエストの方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/visible?isVisible=true" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"   # <jwt token> の部分を実際のアクセストークンに置き換えてください
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**返される可能性のある HTTP ステータスコード**

| HTTP コード | 意味                                     | サンプル本文（該当する場合）                               |
|-------------|------------------------------------------|--------------------------------------------------------------|
| 200         | ワークシートの表示状態が正常に更新された | `{ "Code": 200, "Status": "OK" }`                           |
| 400         | 不正なリクエスト – パラメーターが不足しているか無効    | `{ "Code": 400, "Message": "Invalid request parameters." }` |
| 401         | 認証エラー – JWT トークンが不足しているか無効          | `{ "Code": 401, "Message": "Authentication failed." }`      |
| 404         | 見つからない – ワークブックまたはワークシートが存在しない | `{ "Code": 404, "Message": "File or worksheet not found." }` |
| 500         | サーバー内部エラー                         | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

{{< /tab >}}

{{< /tabs >}}

## クラウド SDK ファミリー

SDK を使うと、開発速度が最も速くなります。SDK が低レベルの詳細を処理してくれるため、プロジェクト本体に集中できます。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) を参照してください。

以下のコード例は、さまざまな SDK を使って Aspose.Cells Web サービスを呼び出す方法を示しています。

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Perl" tabName8="Android" tabName9="Objective C" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Worksheet-UnhideWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-UnhideWorksheet-unhide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PutChangeVisibilityWorksheet-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-change_worksheet_visibility-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UnhideExcelWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-UnhideWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-UnhideWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-UnhideWorksheet-unhide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "e30ac521e9cdb174baa702a743be16ae" >}}

{{< /tab >}}

{{< /tabs >}}