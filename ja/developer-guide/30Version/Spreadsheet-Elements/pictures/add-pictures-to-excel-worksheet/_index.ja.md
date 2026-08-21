---
title: "Excel ファイルに画像を追加する"
second_title: "ドキュメント"
linktype: "追加"
type: docs
url: /ja/pictures/add/
aliases: [  /ja/add-pictures-to-excel-worksheet/ ]
keywords: "Aspose.Cells, Excel, 画像の追加, REST API"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークシートに画像を追加します。Android、C#、Go、Java、Node.js、Perl、PHP、Python、Ruby、Swift の SDK により、プラットフォーム間の統合が簡素化されます。"
weight: 20
ArticleTitle: "Excel ワークシートに画像を追加する – Aspose.Cells Cloud API"
---

この REST API は、Excel ワークシートに新しい画像を追加します。  
**前提条件:** 有効な Aspose Cloud 認証トークン、サポートされるストレージに保存された既存のワークブック、およびワークシートを変更するための適切な権限が必要です。

## PutWorksheetAddPicture API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名        | 型     | 位置   | 説明                                                                                     |
| ------------------ | ------ | ------ | --------------------------------------------------------------------------------------- |
| name               | 文字列 | パス   | ワークブック名。                                                                         |
| sheetName          | 文字列 | パス   | ワークシート名。                                                                         |
| picture            | オブジェクト | 本文 | 画像オブジェクト（バイナリデータ）。                                                     |
| upperLeftRow       | 整数   | クエリ | 画像を配置する左上セルの行インデックス（0 から始まる）。                                 |
| upperLeftColumn    | 整数   | クエリ | 画像を配置する左上セルの列インデックス（0 から始まる）。                                |
| lowerRightRow      | 整数   | クエリ | 画像領域の右下セルの行インデックス（0 から始まる）。                                     |
| lowerRightColumn   | 整数   | クエリ | 画像領域の右下セルの列インデックス（0 から始まる）。                                    |
| picturePath        | 文字列 | クエリ | 画像ファイルのパス。省略した場合、リクエスト本文で画像データを提供する必要があります。 |
| folder             | 文字列 | クエリ | ワークブックを含むフォルダ。                                                             |
| storageName        | 文字列 | クエリ | ストレージサービスの名前。                                                               |

**リクエスト本文に関する注意:** `picturePath` を省略した場合、リクエスト本文で `multipart/form-data` を使用してバイナリ画像データを送信してください。

**HTTP ステータスコード**

| コード | 意味                     | 説明                                           |
|--------|--------------------------|------------------------------------------------|
| 200    | OK                       | フィルターが正常に適用されました。レスポンスには操作の詳細が含まれます。 |
| 400    | Bad Request              | パラメータが不足または無効です（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized             | JWT トークンが無効または不足しています。       |
| 413    | Payload Too Large        | アップロードされたファイルがサイズ制限を超えています。 |
| 500    | Internal Server Error    | 予期しないサーバーエラーが発生しました。       |

**例：200 レスポンススキーマ**

```json
{
  "Code": 200,
  "Status": "OK",
  "PictureUrl": "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/1"
}
```

**注意:** 画像の最大サイズは 10 MB です。それより大きいファイルは `400 Bad Request` レスポンスで拒否されます。

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/Pictures/PutWorksheetAddPicture) は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST アクセスを可能にします。

cURL コマンドラインツールを使用して、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.com/v1.1/cells/Sample_Test_Book.xls/worksheets/Sheet6/pictures?picturePath=aspose-cloud.png" \
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
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK ファミリー

SDK を使用すると、開発を最適化できます。SDK は低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) を確認してください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスにリクエストを送信する方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetAddPicture.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetAddPicture.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetAddPicture.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetAddPicture.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82deb4189bc27ae92abf73c36b4df0" "Example_PutWorksheetAddPicture.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetAddPicture.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetAddPicture.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetAddPicture.go" >}}

{{< /tab >}}

{{< /tabs >}}

**注意:** サポートされる画像形式は PNG、JPEG、BMP、GIF です。画像の最大サイズは 10 MB です。それより大きいファイルは `400 Bad Request` レスポンスで拒否されます。