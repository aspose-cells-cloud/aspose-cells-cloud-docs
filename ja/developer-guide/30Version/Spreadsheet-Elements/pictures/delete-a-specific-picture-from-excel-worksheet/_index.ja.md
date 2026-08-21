---
title: "Excelワークシートから画像を削除する – Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktitle: "削除"
type: docs
url: /ja/pictures/delete/
aliases: [  /ja/delete-a-specific-picture-from-excel-worksheet/ ]
keywords: "Aspose.Cells, Cloud API, 画像削除, Excelワークシート, REST"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークシートから画像を削除します。DELETE エンドポイント、必要なパラメータ、認証、エラーコード、およびサンプルコードについて学習します。"
weight: 50
ArticleTitle: "Excelワークシートから画像を削除する – Aspose.Cells Cloud API"
---

この REST API は、Excel ワークシートから画像を削除します。

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を必要とします。

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/{pictureIndex}
```

### リクエストパラメータ

| パラメータ名     | 型     | 位置   | 必須 | 説明                                     |
| ---------------- | ------ | ------ | ---- | ------------------------------------------ |
| name             | string | path   | はい  | ワークブックファイルの名前です。          |
| sheetName        | string | path   | はい  | 画像を含むワークシートの名前です。        |
| pictureIndex     | integer| path   | はい  | 削除する画像の 0 から始まるインデックスです。|
| folder           | string | query  | いいえ| ワークブックが保存されているフォルダです。|
| storageName      | string | query  | いいえ| ストレージサービスの名前（オプション）です。|

cURL コマンドラインツールを使用すると、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例では、cURL を使用して呼び出しを行う方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures/0" \
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

**サンプルレスポンスヘッダー**

| ヘッダー名      | 値                            |
|----------------|-------------------------------|
| Content-Type   | application/json             |
| Content-Length | (変動)                        |
| Date           | (サーバー日時)                |

{{< /tab >}}

{{< /tabs >}}

### エラーハンドリング

| HTTP コード | 意味                                                         | サンプルエラーペイロード                                           |
| ----------- | ------------------------------------------------------------ | ------------------------------------------------------------------- |
| 200         | 画像が正常に削除されました。                                 | `{ "Code": 200, "Status": "OK" }`                                   |
| 400         | 不正リクエスト – 無効なパラメータです。                     | `{ "Code": 400, "Message": "Invalid pictureIndex." }`               |
| 401         | 認証エラー – トークンが不足または無効です。                 | `{ "Code": 401, "Message": "Access token is missing or invalid." }` |
| 404         | 見つかりません – ワークブック、ワークシート、または画像が存在しません。 | `{ "Code": 404, "Message": "Resource not found." }`                 |
| 500         | サーバー内部エラーです。                                     | `{ "Code": 500, "Message": "Unexpected server error." }`            |

## Cloud SDK ファミリー

SDK を使用すると、開発が最も迅速に行えます。SDK が低レベルの詳細を処理するため、プロジェクトの開発に集中できます。Aspose.Cells Cloud SDK の完全なリストについては、[GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetPicture.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetPicture.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetPicture.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetPicture.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetPicture.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetPicture.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetPicture.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetPicture.go" >}}

{{< /tab >}}

{{< /tabs >}}