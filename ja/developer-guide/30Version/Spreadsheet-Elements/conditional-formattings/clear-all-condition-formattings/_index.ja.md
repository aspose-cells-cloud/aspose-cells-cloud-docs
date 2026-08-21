---
title: "条件付き書式のクリア"
type: docs
url: /ja/conditional-formattings/clear/
aliases: [  /ja/clear-all-condition-formattings/ ]
keywords: "Aspose.Cells Cloud, REST API, 条件付き書式のクリア, Excel, ワークシート, JWT, v3.2"
description: "Aspose.Cells Cloud API（v3.2）を使用してワークシートからすべての条件付き書式ルールを削除します。リクエスト構文、必要なパラメータ、認証手順について学習し、複数のSDKでのサンプルコードを確認してください。"
weight: 80
---

この REST API は、ワークシートからすべての条件付き書式ルールをクリアします。

## REST API

```bash
DELETE https://api.aspose.cloud/v3.2/cells/{name}/worksheets/{sheetName}/conditionalFormattings
```

### リクエストパラメータ

| パラメータ名      | 型     | 位置   | 説明                                                         |
| ----------------- | ------ | ------ | ------------------------------------------------------------ |
| **name**          | string | path   | ワークブックファイルの名前（例: `Book1.xlsx`）。             |
| **sheetName**     | string | path   | 条件付き書式を削除するワークシートの名前。                   |
| **folder**        | string | query  | （省略可）ワークブックが配置されているストレージ内のフォルダパス。 |
| **storageName**   | string | query  | （省略可）ストレージサービスの名前。                         |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormattings) は、公開可能なプログラミングインターフェースを定義しており、**OpenAPI Specification** を利用することで、Web ブラウザから直接 REST アクセスを行うことができます。

cURL コマンドラインツールを使用すると、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、cURL を使って Cloud API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.2/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### エラーレスポンス

| HTTP コード | 理由                                                   | 例（レスポンスボディ）                                               |
| ----------- | ------------------------------------------------------ | -------------------------------------------------------------------- |
| **400**     | リクエストエラー — パラメータが欠落または無効です。    | `{ "Code":"400", "Message":"Invalid parameter value." }`            |
| **401**     | 認証エラー — JWT トークンが欠落または無効です。         | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**     | 見つかりません — ワークブックまたはワークシートが存在しません。 | `{ "Code":"404", "Message":"File not found." }`                     |
| **500**     | サーバー内部エラー — 予期せぬサーバー障害が発生しました。 | `{ "Code":"500", "Message":"An unexpected error occurred." }`       |

## SDK のサンプルコード

SDK を使用することで、開発スピードを最大限に高めることができます。SDK は低レベルの詳細を処理してくれるため、開発者はプロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご参照ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスにリクエストを送信する方法を示しています。

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-ClearConditionFormattings-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-clear-all-formatting.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-delete_worksheet_conditional_formattings-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-ClearConditionFormattings-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-ClearConditionFormattings-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "63fda1be9e5149f83edca47ce58dac87" >}}

{{< /tab >}}

{{< /tabs >}}