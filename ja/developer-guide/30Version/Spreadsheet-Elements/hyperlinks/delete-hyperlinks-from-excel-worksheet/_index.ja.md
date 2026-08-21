---
title: "ハイパーリンクのクリア"
type: docs
url: /hyperlinks/clear/
aliases: [/add-hyperlinks-to-excel-worksheet/]
keywords: "Aspose.Cells Cloud, Excel, ハイパーリンクのクリア, ハイパーリンクの削除, REST API, ワークシート, SDK"
description: "Aspose.Cells Cloud REST API またはサポートされている SDK（C#、Java、Python、Node.js、Go、PHP、Ruby、Perl など）を使用して、Excel ワークシートからすべてのハイパーリンクを削除する方法を学習します。"
weight: 40
ArticleTitle: "ハイパーリンクのクリア – Aspose.Cells Cloud API ドキュメント"
---

この REST API は、Excel ワークシート上の**すべてのハイパーリンク**を削除します。

## セキュリティと認証
Aspose.Cells Cloud API は安全であり、[JWT トークンベースの認証](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)が必要です。

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks
```

### リクエストパラメータ

| パラメータ名   | 型     | 位置   | 説明                                   |
| -------------- | ------ | ------ | -------------------------------------- |
| name           | string | path   | Excel ファイルの名前。                 |
| sheetName      | string | path   | ワークシートの名前。                   |
| folder         | string | query  | ドキュメントを含むフォルダ。           |
| storageName    | string | query  | ストレージサービスの名前。             |

### エラーレスポンス

| HTTP コード | 理由                                                 | 例のボディ                                                            |
| ----------- | ---------------------------------------------------- | --------------------------------------------------------------------- |
| **400**     | リクエストエラー – パラメータが不足しているか、無効です。 | `{ "Code":"400", "Message":"Invalid parameter value." }`            |
| **401**     | 認証エラー – JWT トークンが不足しているか、無効です。    | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**     | 見つかりません – ワークブックまたはワークシートが存在しません。 | `{ "Code":"404", "Message":"File not found." }`                     |
| **500**     | サーバーエラー – 予期しないサーバー障害が発生しました。   | `{ "Code":"500", "Message":"An unexpected error occurred." }`       |

[OpenAPI 仕様書](https://apireference.aspose.cloud/cells/#/Hyperlinks/DeleteWorksheetHyperlinks) はパブリックにアクセス可能なプログラミングインターフェースを定義しており、ウェブブラウザから直接 REST アクセスを実行できます。

**cURL** コマンドラインツールを使用して Aspose.Cells Web サービスを呼び出すことができます。以下の例は、ワークシートからすべてのハイパーリンクを削除する方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test1.xlsx/worksheets/Sheet1/hyperlinks" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## クラウド SDK ファミリー
SDK を使用すると、低レベルの詳細を処理してくれるため、開発 speed が向上します。Aspose.Cells Cloud SDK の完全な一覧は、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご覧ください。

以下のコード例は、さまざまな SDK を使用してワークシートのハイパーリンクを削除する方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetHyperlinks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetHyperlinks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetHyperlinks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetHyperlinks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetHyperlinks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetHyperlinks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetHyperlinks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetHyperlinks.go" >}}

{{< /tab >}}

{{< /tabs >}}