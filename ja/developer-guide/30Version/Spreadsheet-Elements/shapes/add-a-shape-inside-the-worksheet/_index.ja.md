---
title: "Excelワークシートに図形を追加する"
second_title: "Document"
linktitle: "Add"
type: docs
url: /ja/shapes/add/
aliases: [  /ja/add-a-shape-inside-the-worksheet/ ]
keywords: "Aspose.Cells, 図形の追加, Excel, REST API, クラウドSDK, shapeDTO, 描画タイプ"
description: "Aspose.Cells Cloud REST API v3.0 を使用して、Excelワークシートに図形（弧、線、矩形など）を追加する方法を学びます。リクエスト構文、必須パラメータ、認証手順、およびサンプルSDKコードを含みます。"
weight: 30
ArticleTitle: "Aspose.Cells Cloud API を使用してExcelワークシートに図形を追加する"
---

このREST APIは、Excelワークシートに図形を追加します。  
エンドポイントは **APIバージョン v3.0** に属しており、Aspose Cloud OAuth2フロー（client-id/client-secret）により取得したJWTアクセストークンを使用し、`Authorization: Bearer <token>` ヘッダーに含める必要があります。

### **セキュリティと認証**

Aspose.Cells Cloud APIは安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWTトークンベースの認証</a>が要求されます。

## PutWorksheetShape API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes
```

### **リクエストパラメータ**

| パラメータ名          | 型     | 位置   | 説明                                                                 |
| --------------------- | ------ | ------ | -------------------------------------------------------------------- |
| name                  | string | path   | ドキュメント名。                                                     |
| sheetName             | string | path   | ワークシート名。                                                     |
| shapeDTO              | object | body   | 追加する図形を記述するJSONオブジェクト（完全なスキーマはOpenAPI仕様参照）。 |
| drawingType           | string | query  | 図形オブジェクトのタイプ（例: `arc`, `line`, `rectangle`）。          |
| upperLeftRow          | integer | query | 図形の左上行インデックス。                                           |
| upperLeftColumn       | integer | query | 図形の左上列インデックス。                                           |
| top                   | integer | query | 図形の上端からの垂直オフセット（ピクセル単位）。                      |
| left                  | integer | query | 図形の左端からの水平オフセット（ピクセル単位）。                      |
| width                 | integer | query | 図形の幅（ピクセル単位）。                                           |
| height                | integer | query | 図形の高さ（ピクセル単位）。                                         |
| folder                | string | query  | ドキュメントが格納されているフォルダー。                             |
| storageName           | string | query  | ストレージ名。                                                       |

[OpenAPI仕様](https://apireference.aspose.cloud/cells/#/Shapes/PutWorksheetShape) はパブリックにアクセス可能なプログラミングインタフェースを定義し、Webブラウザーから直接REST通信を実行できるようにします。

cURLコマンドラインツールを使用して、Aspose.Cellsウェブサービスに簡単にアクセスできます。以下の例は、cURLを使用してクラウドAPIにリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes?DrawingType=arc&upperLeftRow=1&upperLeftColumn=1&top=1&left=1&width=100&height=100" \
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
  "Status": "OK",
  "ShapeId": 5
}
```

_成功時のレスポンスは、HTTPステータスコード、テキスト形式のステータス、および新規作成された図形の識別子（`ShapeId`）を返します。_

{{< /tab >}}

{{< /tabs >}}

**HTTPステータスコード**

| コード | 意味             | 説明                                           |
|------|------------------|-----------------------------------------------|
| 200  | OK               | フィルターが正常に適用され、レスポンスに操作の詳細が含まれます。 |
| 400  | Bad Request      | パラメータが不足しているか、無効です（例: 未対応のファイルタイプ）。 |
| 401  | Unauthorized     | JWTトークンが無効または不足しています。         |
| 413  | Payload Too Large| アップロードされたファイルがサイズ制限を超えています。 |
| 500  | Internal Server Error | サーバー内で予期しないエラーが発生しました。     |

一般的なエラーレスポンスは以下の通りです：

- **400 Bad Request** – パラメータが不足しているか、無効です。  
- **401 Unauthorized** – JWTトークンが無効または不足しています。  
- **404 Not Found** – 指定されたワークシートまたはドキュメントが存在しません。

各エラーは、`Code` および `Message` フィールドを含むJSONオブジェクトとして返されます。

## Cloud SDKファミリー

SDKを使用することが開発を高速化する最良の方法です。SDKは低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDKの完全な一覧については、[GitHubリポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまなSDKを使用してAspose.Cellsウェブサービスを呼び出す方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}