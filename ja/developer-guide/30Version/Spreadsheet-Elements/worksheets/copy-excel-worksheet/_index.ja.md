---
title: "他のワークシートからコンテンツと書式をコピーする"
second_title: "Document"
linktype: "コピー"
type: docs
url: /ja/worksheets/copy/
aliases: [  /ja/copy-excel-worksheet/ ]
keywords: "Aspose Cells copy worksheet API, Excel copy sheet REST, Aspose Cloud SDK copy, spreadsheet copy worksheet"
description: "Aspose.Cells Cloud REST API を使用して、ワークシートとその書式を新しいシートにコピーする方法を学びます。C#、Java、Python など向けのエンドポイント、パラメーター、cURL、および SDK の例を含みます。"
weight: 20
---

この REST API は、同じワークブック内でワークシートとその書式を新しいシートにコピーします。

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/copy
```

リクエストパラメーターは以下の通りです：

| パラメーター名     | 型     | 位置   | 説明                                                                 |
| ------------------ | ------ | ------ | -------------------------------------------------------------------- |
| `name`             | 文字列 | path   | ワークブックファイルの名前。                                         |
| `sheetName`        | 文字列 | path   | コピー先ワークシート（新しいシート）の名前。                         |
| `sourceSheet`      | 文字列 | query  | コピー元のワークシートの名前。                                       |
| `options`          | オブジェクト | body | コピーオプションを含む JSON オブジェクト（例：列幅、数式など）。    |
| `sourceWorkbook`   | 文字列 | query  | コピー元のワークブックの名前（現在のワークブックと異なる場合）。     |
| `sourceFolder`     | 文字列 | query  | コピー元のワークブックが保存されているフォルダーのパス。             |
| `folder`           | 文字列 | query  | コピー先のワークブックが保存されるフォルダーのパス。                 |
| `storageName`      | 文字列 | query  | 使用するストレージサービスの名前。                                   |

### リクエストおよびレスポンスの例

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/PostCopyWorksheet) は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザーから直接 REST によるインタラクションを実行できるようにします。

cURL コマンドラインツールを使用すると、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、cURL を使用して Cloud API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/NewSheet/copy?sourceSheet=Sheet3X" \
  -X POST \
  -d '{ "ColumnCharacterWidth": true, "CopyInvalidFormulasAsValues": true, "CopyNames": true, "ExtendToAdjacentRange": true, "ReferToDestinationSheet": true, "ReferToSheetWithSameName": true}' \
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

### エラー処理

API は、標準的な HTTP ステータスコードと JSON 形式のエラーボディを返します。主なレスポンス例は以下の通りです：

| HTTP コード | 説明                                                         | サンプル JSON エラーボディ                                    |
| ----------- | ------------------------------------------------------------ | ------------------------------------------------------------- |
| 400         | 不正なリクエスト — パラメーターが不足しているか無効です。     | `{ "Code": 400, "Message": "Invalid request parameters." }`   |
| 401         | 認証失敗 — トークンが不足しているか無効です。                 | `{ "Code": 401, "Message": "Authentication failed." }`        |
| 404         | 見つかりません — ワークブック、ワークシート、またはフォルダーが存在しません。 | `{ "Code": 404, "Message": "Resource not found." }`           |
| 500         | サーバー内部エラー — 予期しない状況が発生しました。          | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

## Cloud SDK ファミリー

SDK を使用すると、開発を最適化できます。SDK は低レベルの詳細処理を担い、開発者はプロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリー](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスにリクエストを送信する方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCopyWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCopyWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCopyWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCopyWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCopyWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCopyWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCopyWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCopyWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}