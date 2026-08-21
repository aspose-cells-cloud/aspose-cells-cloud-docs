---
title: "ExcelワークシートにOLEオブジェクトを追加する"
second_title: "Document"
linktitle: "OLEオブジェクトの追加"
type: docs
url: /oleobjects/add/
aliases: [/add-oleobject-to-excel-worksheet/]
keywords: "OLEオブジェクトの追加, Excel, Aspose.Cells Cloud, REST API, SDK"
description: "Aspose.Cells Cloud REST APIを使用してExcelワークシートにOLEオブジェクトを追加します。このAPIは、C#、Java、PHP、Ruby、Node.js、Python、Perl、GoのSDKを介して、または直接呼び出すことができます。"
ArticleTitle: "Aspose.Cells Cloud APIを使用してExcelワークシートにOLEオブジェクトを追加する"
weight: 20
---

Aspose.Cells Cloud APIは、Excelワークブックのプログラムによる操作を可能にし、Word文書、PDF、その他のバイナリファイルなどのOLEオブジェクトをワークシートに直接埋め込む機能を提供します。

このREST APIは、Excelワークシートに**OLEオブジェクト**を追加します。

**前提条件** – 有効なJWT認証トークンが必要です。また、`oleFile`または`imageFile`で参照されるソースファイルは、エンドポイントを呼び出す前に、指定されたストレージの場所にアップロードしておく必要があります。

## PutWorksheetOleObject API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects
```

### **セキュリティと認証**

Aspose.Cells Cloud APIは安全で、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWTトークンベースの認証</a>を必要とします。

### リクエストパラメータ

| パラメータ名        | 型     | 位置   | 説明                                       |
|-------------------|--------|--------|---------------------------------------------|
| name              | string | path   | ワークブックファイル名。                    |
| sheetName         | string | path   | ワークシート名。                            |
| oleObject         | object | body   | OLEオブジェクトの定義。                     |
| upperLeftRow      | integer | query | 上左隅の行インデックス（デフォルトは0）。    |
| upperLeftColumn   | integer | query | 上左隅の列インデックス（デフォルトは0）。    |
| height            | integer | query | OLEオブジェクトの高さ（デフォルトは0）。     |
| width             | integer | query | OLEオブジェクトの幅（デフォルトは0）。       |
| oleFile           | string | query  | OLEソースファイル名。                       |
| imageFile         | string | query  | プレビュー画像ファイル名。                  |
| folder            | string | query  | ワークブックを含むフォルダ。                |
| storageName       | string | query  | 使用するストレージ名。                      |

**注意事項** – `upperLeftRow`と`upperLeftColumn`は0から始まるインデックスを使用します。`oleFile`（および任意で`imageFile`）は、対象のストレージ内に事前に存在している必要があります。そうでない場合、リクエストはエラーを返します。

[OpenAPI仕様](https://apireference.aspose.cloud/cells/#/OleObjects/PutWorksheetOleObject)はパブリックにアクセス可能なプログラミングインターフェースを定義し、ウェブブラウザから直接REST APIとのやり取りを可能にします。

**cURL**コマンドラインツールを使用してAspose.Cellsウェブサービスを呼び出すことができます。以下の例は、cURLでOLEオブジェクトを追加する方法を示しています。**本番環境での呼び出しにはHTTPSが必須です。**

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/oleobjects" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"ImageSourceFullName":"aspose-logo.png", "IsAutoSize":true, "SourceFullName":"Sample_Book2.xls", "UpperLeftRow":15, "Top":10, "UpperLeftColumn":5, "Left":10, "Width":400, "Height":400}'
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

![Excelワークシートに埋め込まれたOLEオブジェクトを示すスクリーンショット](/cells/images/ole-object-example.png)

**返される可能性のあるHTTPステータスコード**

| コード | 説明                                               |
|--------|----------------------------------------------------|
| 200    | OLEオブジェクトが正常に追加されました。            |
| 400    | 不正なリクエスト – パラメータが不足または無効です。|
| 401    | 認証エラー – JWTトークンが無効または不足しています。|
| 404    | 見つかりません – ワークブック、ワークシート、またはソースファイルが存在しません。 |
| 500    | サーバー内部エラー – 予期せぬエラーが発生しました。 |

正常なレスポンスの典型的なJSONペイロードは以下の通りです：

```json
{
  "Code": 200,
  "Status": "OK",
  "Data": {
    "OleObjectId": "12345",
    "UpperLeftRow": 15,
    "UpperLeftColumn": 5,
    "Width": 400,
    "Height": 400,
    "SourceFullName": "Sample_Book2.xls",
    "ImageSourceFullName": "aspose-logo.png"
  }
}
```

## Cloud SDKファミリー

SDKを使用することで、開発を迅速化できます。SDKは低レベルの詳細を抽象化し、ビジネスロジックの開発に集中できるようにします。Aspose.Cells Cloud SDKの完全な一覧は[GitHubリポジトリ](https://github.com/aspose-cells-cloud)をご覧ください。

以下のコード例は、さまざまなSDKを使用してAspose.Cellsウェブサービスを呼び出す方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}