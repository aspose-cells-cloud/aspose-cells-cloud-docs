---
title: "Excelワークシート内のすべての画像を取得する"
second_title: "Document"
linktype: "Get all"
type: docs
url: /ja/pictures/get-all/
aliases: [  /ja/get-picture-from-a-worksheet/ ]
keywords: "Aspose.Cells Cloud, Excelワークシート, 画像API, すべての画像を取得, REST API, SDK"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークシートからすべての画像オブジェクトを取得します。"
ArticleTitle: "Excelワークシート内のすべての画像を取得する - Aspose.Cells Cloud API"
weight: 10
---

この REST API は、Excel ワークシートからすべての画像情報を取得します。

**前提条件**  
このエンドポイントを呼び出す前に、以下の条件が満たされていることを確認してください。

- 有効な Aspose Cloud JWT アクセストークン。
- 対象の Excel ファイルが選択されたストレージにアップロードされていること。
- カスタムストレージを使用する場合の正しいストレージ名。
- 画像を含むワークシート名。

## GetWorksheetPictures API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures
```

**注意:** API を呼び出す際には HTTPS（TLS 1.2 以降）を使用し、`Authorization` ヘッダーに有効な JWT トークンを含めてください。

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を必要とします。

### **リクエストパラメータ**

| パラメータ名 | 型     | 位置   | 説明                                    |
| ------------ | ------ | ------ | --------------------------------------- |
| name         | string | path   | Excel ファイルの名前。                  |
| sheetName    | string | path   | 画像を含むワークシートの名前。          |
| folder       | string | query  | ファイルが保存されているフォルダのパス。|
| storageName  | string | query  | ストレージサービスの名前。              |

### エラーレスポンス

| HTTP コード | 説明                                                               |
| ----------- | ------------------------------------------------------------------ |
| 401         | 認証エラー – トークンが不足しているか、無効です。                 |
| 404         | 見つかりません – 指定されたファイル、ワークシート、またはページ区切りインデックスが存在しません。 |
| 400         | 不正なリクエスト – リクエスト構文が不正、またはパラメータが無効です。 |
| 500         | サーバー内部エラー – 予期しない状態が発生しました。              |

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/Pictures/GetWorksheetPictures) はパブリックに利用可能なプログラミングインターフェースを定義し、ウェブブラウザから直接 REST 通信を実行できるようにします。

cURL コマンドラインツールを使用して Aspose.Cells Web サービスに簡単にアクセスできます。以下の例では、cURL を使用して Cloud API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Pictures": {
    "PictureList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/1",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/2",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      }
    ],
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet2/pictures",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**成功レスポンス** – 成功した呼び出しは HTTP 200 を返し、各画像のリソースリンクを含む `Pictures` オブジェクトを持つ JSON ペイロードが含まれます。

## Cloud SDK ファミリー

SDK を使用することで、開発速度を最適化できます。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストは [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスにリクエストを行う方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetPictureWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetPictureWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetPictureWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetPictureWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetPictureWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetPictureWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetPictureWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetPictureWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}

SDK は、それぞれのパッケージマネージャ（例: .NET 用 NuGet、Java 用 Maven Central、PHP 用 Composer、Node.js 用 npm、Python 用 PyPI、Perl 用 CPAN、Go 用 Go modules）から直接ダウンロードできます。

*関連項目:* 画像の追加、画像の削除、画像プロパティの更新。