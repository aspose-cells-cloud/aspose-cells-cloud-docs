---
title: "Aspose.Cells Cloud API – ワークシートから画像を取得"
second_title: "ドキュメント"
linktitle: "取得"
type: docs
url: /ja/pictures/get/
aliases: [  /ja/convert-picture-to-image/ ]
keywords: "Aspose.Cells, 画像の取得, API, Excel, クラウド, REST"
description: "Aspose.Cells Cloud REST API を使用して、Excelワークシートから特定の画像を取得します。エンドポイント、パラメーター、認証手順、レスポンスコード、およびコード例を含みます。"
weight: 10
ArticleTitle: "Aspose.Cells Cloud API – ワークシートから画像を取得"
---

この REST API は、Excelワークシートから0から始まるインデックスで指定された画像を取得します。

## REST API

このエンドポイントを呼び出すには、**Authorization** ヘッダーに有効なJWTアクセストークンを含める必要があります。トークンは Aspose.Cells Cloud の認証フローを通じて取得され、ファイルアクセスに必要なスコープが付与されている必要があります。トークンの取得方法の詳細については、グローバルな **認証** ガイドを参照してください。

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/{pictureIndex}
```

### リクエストパラメーター

| パラメーター名 | 型      | 位置   | 説明                                                                                               |
| -------------- | ------- | ------ | -------------------------------------------------------------------------------------------------- |
| name           | string  | path   | Excelドキュメントの名前。                                                                          |
| sheetName      | string  | path   | ワークシートの名前。                                                                               |
| pictureIndex   | integer | path   | 画像の0から始まるインデックス。                                                                     |
| format         | string  | query  | 期望するエクスポート形式（例: png, jpg, bmp, gif, tiff）。省略された場合、画像は元の形式で返されます。 |
| folder         | string  | query  | ドキュメントを含むフォルダー。                                                                      |
| storageName    | string  | query  | ストレージロケーションの名前。                                                                       |

### エラーレスポンス

| HTTPコード | 説明                                                               |
| --------- | ------------------------------------------------------------------ |
| 401       | 認証エラー – トークンが不足しているか、無効です。                   |
| 404       | 見つかりません – 指定されたファイル、ワークシート、または改ページインデックスが存在しません。 |
| 400       | 不正リクエスト – リクエストの構文が不正、またはパラメーターが無効です。     |
| 500       | サーバーエラー – 予期しない状態が発生しました。                      |

[OpenAPI仕様](https://apireference.aspose.cloud/cells/#/Pictures/GetWorksheetPicture) はパブリックにアクセス可能なプログラミングインタフェースを定義し、Webブラウザから直接REST操作を実行できるようにします。

cURLコマンドラインツールを使用すると、Aspose.Cellsウェブサービスに簡単にアクセスできます。以下の例では、cURLを用いてCloud APIを呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures/1?format=png" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```bash
# レスポンスボディにバイナリ画像データ（PNG）が返されます。
# 例: base64エンコードされたスニペット
iVBORw0KGgoAAAANSUhEUgAA...
```

{{< /tab >}}

{{< /tabs >}}

## クラウドSDKファミリー

SDKを使用すると、開発が最も迅速に行えます。SDKが低レベルの詳細を処理するため、プロジェクトの本質的な作業に集中できます。Aspose.Cells Cloud SDKの完全な一覧については、[GitHubリポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまなSDKを使用してAspose.Cellsウェブサービスを呼び出す方法を示しています：

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

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "ExampleGetWorksheetPictureWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "ExampleGetWorksheetPictureWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ExampleGetWorksheetPictureWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "ExampleGetWorksheetPictureWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "ExampleGetWorksheetPictureWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}