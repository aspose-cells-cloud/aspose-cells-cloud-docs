---
title: "書式条件の追加"
type: docs
url: /ja/conditional-formattings/add-format-condition/
aliases: [  /ja/add-a-format-condition/ ]
keywords: "Aspose.Cells Cloud, 条件付き書式 API, 書式条件の追加, Excel REST API, Cells API"
description: "Aspose.Cells Cloud REST API（v3.0）を使用して Excel ワークシートに書式条件を追加する方法を学習します。リクエスト構文、パラメータ、安全な cURL の例、SDK スニペットを含みます。"
ArticleTitle: "書式条件の追加 – Aspose.Cells Cloud API ドキュメント"
weight: 50
---

この REST API は、ワークシートに書式条件を追加します。

## セキュリティと認証
Aspose.Cells Cloud API は安全であり、[JWT トークンベースの認証](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)を必要とします。

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}
```

### リクエストパラメータ

| パラメータ名 | 型      | 位置   | 説明                                                                 |
| ------------ | ------- | ------ | -------------------------------------------------------------------- |
| name         | string  | path   | Excel ワークブックの名前。                                           |
| sheetName    | string  | path   | 書式を適用する範囲を含むワークシートの名前。                         |
| index        | integer | path   | 追加または置換する書式条件の 0 から始まるインデックス。              |
| cellArea     | string  | query  | 条件が適用されるセル範囲（例: `A1:C3`）。                            |
| type         | string  | query  | 条件のタイプ（例: `Expression`, `CellValue`）。                      |
| operatorType | string  | query  | 条件の演算子（例: `Between`, `Equal`）。                             |
| formula1     | string  | query  | 条件で使用される最初の数式または値。                                 |
| formula2     | string  | query  | 2 番目の数式または値（`Between` などの一部の演算子に必要）。         |
| folder       | string  | query  | ストレージ内にあるワークブックのフォルダ。                           |
| storageName  | string  | query  | ストレージサービスの名前（例: `Default`）。                          |

### エラーレスポンス

| HTTP コード | 理由                                         | 例ボディ                                                            |
| ----------- | -------------------------------------------- | ------------------------------------------------------------------- |
| **400**     | 不正リクエスト – パラメータが不足または無効。 | `{ "Code":"400", "Message":"Invalid parameter value." }`            |
| **401**     | 認証エラー – JWT トークンが不足または無効。   | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**     | 見つからない – ワークブックまたはワークシートが存在しない。 | `{ "Code":"404", "Message":"File not found." }`                     |
| **500**     | サーバー内部エラー – 予期しないサーバー障害。 | `{ "Code":"500", "Message":"An unexpected error occurred." }`       |

### 成功レスポンス

| HTTP コード | 理由                                     | 例ボody                             |
| ----------- | ---------------------------------------- | ------------------------------------ |
| **200**     | OK – 条件が正常に追加または更新されました。 | `{ "Code": "200", "Status": "OK" }` |

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/PutWorksheetFormatCondition)は、パブリックにアクセス可能なプログラミングインターフェースを定義し、ウェブブラウザから直接 REST 連携を実行できるようにします。

**cURL** を使用して Aspose.Cells API を呼び出すことができます。以下の例は空の JSON ボディを含む完全なリクエストを示しています。

### cURL の例

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings/0?cellArea=A1:C3&type=Expression&operatorType=Between&formula1=v1&formula2=v2" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{}'
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

## Cloud SDK ファミリー
SDK を使用すると、開発を最も効率的にスピードアップできます。SDK は低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) を確認してください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-AddFormatCondition-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-add-cells-area-for-format-condition.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-put_worksheet_format_condition-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-AddFormatCondition-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-AddFormatCondition-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "caa13d019b3c7c3b5c14110ccd217e99" >}}

{{< /tab >}}

{{< /tabs >}}
---