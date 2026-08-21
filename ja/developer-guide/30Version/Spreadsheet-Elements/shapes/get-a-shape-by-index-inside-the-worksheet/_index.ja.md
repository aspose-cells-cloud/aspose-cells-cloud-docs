---
title: "Excelワークシート上のインデックスで図形を取得する"
second_title: "Document"
linktitle: "Get"
type: docs
url: /shapes/get/
aliases: [/get-a-shape-by-index-inside-the-worksheet/]
keywords: "Aspose.Cells Cloud, Excel shape API, get shape by index, worksheet shape, REST API, shape retrieval, Aspose.Cells SDK"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークシートからインデックスで図形（shape）を取得します。リクエスト構文、パラメータ、レスポンス詳細、および SDK の使用例を含みます。"
weight: 20
ArticleTitle: "Excelワークシート上のインデックスで図形を取得する – Aspose.Cells Cloud ドキュメント"
---

この REST API は、Excel ワークシートから図形（画像データまたはメタデータを含む）を取得します。

## GetWorksheetShape API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes/{shapeindex}
```

**前提条件**  
- 有効な Aspose Cloud アクセストークン（Bearer JWT）が必要です。  
- ワークブックは、Aspose Cloud ストレージまたは指定されたフォルダ内に保存されている必要があります。  

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を必要とします。

### **リクエストパラメータ**

| パラメータ名 | 型      | 位置   | 説明                                     |
| ------------ | ------- | ------ | --------------------------------------- |
| name         | string  | path   | Excel ドキュメントの名前。              |
| sheetName    | string  | path   | 図形を含むワークシートの名前。          |
| shapeindex   | integer | path   | ワークシート内での図形の 0 から始まるインデックス。 |
| folder       | string  | query  | ドキュメントが保存されているフォルダのパス。       |
| storageName  | string  | query  | ストレージサービスの名前。                         |

**注意:** `shapeindex` は 0 から始まります。最初の図形のインデックスは 0 です。デフォルトストレージを使用しない場合は、ワークブックが指定された `folder` および `storageName` に保存されていることを確認してください。

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Shapes/GetWorksheetShape) はパブリックにアクセス可能なプログラミングインタフェースを定義し、Web ブラウザから直接 REST 連携を実行できるようにします。

cURL コマンドラインツールを使用して、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、cURL を使用して Cloud API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
# 正しいエンドポイントとパス
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet4/shapes/1" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "Shape": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "Name": "string",
    "MsoDrawingType": "string",
    "AutoShapeType": "string",
    "Placement": "string",
    "UpperLeftRow": 0,
    "Top": 0,
    "UpperLeftColumn": 0,
    "Left": 0,
    "LowerRightRow": 0,
    "Bottom": 0,
    "LowerRightColumn": 0,
    "Right": 0,
    "Width": 0,
    "Height": 0,
    "X": 0,
    "Y": 0,
    "RotationAngle": 0,
    "HtmlText": "string",
    "Text": "string",
    "AlternativeText": "string",
    "TextHorizontalAlignment": "string",
    "TextHorizontalOverflow": "string",
    "TextOrientationType": "string",
    "TextVerticalAlignment": "string",
    "TextVerticalOverflow": "string",
    "IsGroup": true,
    "IsHidden": true,
    "IsLockAspectRatio": true,
    "IsLocked": true,
    "IsPrintable": true,
    "IsTextWrapped": true,
    "IsWordArt": true,
    "LinkedCell": "string",
    "ZOrderPosition": 0
  }
}
```

{{< /tab >}}

{{< /tabs >}}

**発生する可能性のある HTTP ステータスコード**

| コード | 説明 |
|------|-------------|
| **200 OK** | 図形の取得に成功しました。 |
| **400 Bad Request** | リクエストが不正な形式であるか、必須パラメータが不足しています。 |
| **401 Unauthorized** | 認証に失敗したか、トークンが不足しているか、無効です。 |
| **404 Not Found** | 指定されたワークブック、ワークシート、または図形インデックスが存在しません。 |
| **500 Internal Server Error** | 予期せぬサーバーエラーが発生しました。 |

**よくある落とし穴:** 異なるベースドメイン（`api.aspose.com`）や、古い `/autoshapes/` セグメントを使用すると、404 エラーが発生します。常に `/shapes/` セグメントと `api.aspose.cloud` ドメインを使用してください。

## Cloud SDK ファミリー

SDK を使用すると、開発を迅速化できます。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}

関連する操作については、**[図形の追加](/shapes/add/)** および **[図形の更新](/shapes/update/)** のドキュメントをご参照ください。