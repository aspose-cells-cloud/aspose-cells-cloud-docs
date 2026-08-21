---
title: "Excelワークシート内のOLEオブジェクトを削除する"
second_title: "Document"
linktitle: "削除"
type: docs
url: /ja/oleobjects/delete/
aliases: [  /ja/delete-a-specific-oleobject-from-excel-worksheet/ ]
keywords: "Aspose.Cells, クラウド, 削除, OLE, オブジェクト, Excel, ワークシート, REST, API, SDK"
description: "Aspose.Cells Cloud REST API（v4.0）を使用してExcelワークシートからOLEオブジェクトを削除する方法を学びます。HTTPSエンドポイント、認証手順、cURLの使用例、SDKスニペット、エラーハンドリングのガイダンス、および次のステップへのリンクを含みます。"
weight: 50
ArticleTitle: "Aspose.Cells Cloud APIを使用してExcelワークシートからOLEオブジェクトを削除する"
---

このページでは、**Aspose.Cells Cloud** を使用してExcelワークブック内のワークシートから特定のOLEオブジェクトを削除する方法を説明します。OLEオブジェクトとは、Excelが別々のエンティティとして格納する、リンクされた画像、チャート、またはその他の埋め込みオブジェクトを指します。

## セキュリティと認証
Aspose.Cells Cloud APIは安全であり、[JWTトークンベースの認証](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)が必須です。

## REST API

```bash
DELETE https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}
```

### リクエストパラメータ

| パラメータ名         | 型     | 位置   | 説明                                         |
|---------------------|--------|--------|----------------------------------------------|
| name                | string | path   | ワークブック名。                              |
| sheetName           | string | path   | ワークシート名。                              |
| oleObjectIndex      | integer| path   | 削除対象のOLEオブジェクトのインデックス。     |
| folder              | string | query  | ワークブックを含むフォルダ。（オプション）    |
| storageName         | string | query  | ストレージサービスの名前。（オプション）      |

[OpenAPI仕様](https://apireference.aspose.cloud/cells/#/OleObjects/DeleteWorksheetOleObject)は、パブリックにアクセス可能なプログラミングインターフェースを定義し、ウェブブラウザから直接REST通信を実行できるようにします。

**cURLコマンドラインツール** を使用することで、Aspose.Cellsウェブサービスに簡単にアクセスできます。以下の例は、cURLでこのリクエストを実行する方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v4.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0" \
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

### レスポンスの詳細

| HTTPステータス       | 説明                                                               | サンプルJSON                                                         |
|----------------------|--------------------------------------------------------------------|----------------------------------------------------------------------|
| **200 OK**           | OLEオブジェクトが正常に削除されました。                             | `{ "Code": 200, "Status": "OK" }`                                   |
| **401 Unauthorized** | JWTトークンが不足している、または無効です。                         | `{ "Code": 401, "Message": "Access token is missing or invalid." }` |
| **404 Not Found**    | 指定されたワークブック、ワークシート、またはOLEオブジェクトインデックスが存在しません。 | `{ "Code": 404, "Message": "OLE object index out of range." }`      |
| **400 Bad Request**  | 必須パラメータが不足している、または不正な形式です。                | `{ "Code": 400, "Message": "Invalid request parameters." }`         |

これらのレスポンスは、ステータスコードを確認し、付随するメッセージを表示することで、アプリケーション内で適切に処理してください。

## クラウドSDKファミリー
SDKを使用することは、開発を高速化する最良の方法です。SDKは低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDKの完全な一覧については、[GitHubリポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまなSDKを使用してAspose.Cellsウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}