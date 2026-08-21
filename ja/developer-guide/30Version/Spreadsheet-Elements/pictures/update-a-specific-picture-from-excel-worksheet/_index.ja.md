---
title: "Excel ファイル内の画像を更新する"
second_title: "Document"
linktitle: "Update"
type: docs
url: /pictures/update/
aliases: [/update-a-specific-picture-from-excel-workshee/]
keywords: "Aspose.Cells Cloud, Excel, 画像の更新, REST API, SDK"
description: "Aspose.Cells Cloud REST API を使用して Excel シート内の画像を更新する方法を学びます。リクエストの詳細、cURL の例、および複数言語向けの SDK スニペットを含みます。"
ArticleTitle: "Aspose.Cells Cloud REST API を使用して Excel ファイル内の画像を更新する"
weight: 70
---

この REST API は、Excel シート内のインデックスで識別される画像を更新します。

**前提条件:** 有効な Aspose Cloud JWT トークン、Aspose Cloud ストレージに保存された対象の Excel ファイル、および API バージョン 3.0 以降を使用する必要があります。

## PostWorksheetPicture API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/{pictureIndex}
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### **リクエストパラメータ**

| パラメータ名   | 型     | 位置   | 説明                                                  |
| -------------- | ------ | ------ | ------------------------------------------------------------ |
| name           | string | path   | Excel ドキュメントの名前。                              |
| sheetName      | string | path   | 画像を含むワークシートの名前。         |
| pictureIndex   | integer | path  | 更新する画像の 0 から始まるインデックス。               |
| picture        | object | body   | 更新する画像プロパティを記述する JSON オブジェクト。 |
| folder         | string | query  | ドキュメントが保存されているフォルダ。                     |
| storageName    | string | query  | ストレージサービスの名前。                             |

**注意:** 画像インデックスは 0 から始まります。サポートされている画像形式は JPEG、PNG、BMP、GIF です。画像の最大サイズは 10 MB です。

### エラー応答

| HTTP コード | 説明                                            |
| --------- | ------------------------------------------------------ |
| 401       | 認証エラー – トークンが欠落しているか、無効です。               |
| 404       | 見つかりません – 指定されたファイル、ワークシート、または画像インデックスが存在しません。 |
| 400       | 不正リクエスト – リクエスト構文が不正、または無効なパラメータです。 |
| 500       | サーバー内部エラー – 予期しない状態が発生しました。 |

<a href="https://apireference.aspose.cloud/cells/#/Pictures/PostWorksheetPicture" rel="noopener noreferrer">OpenAPI スペック</a> はパブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 相互通信を実行できるようにします。

cURL コマンドラインツールを使用して Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使ってクラウド API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures/1" \
-X POST \
-d "{ \"UpperLeftRow\": 10, \"Top\": 0, \"UpperLeftColumn\": 1, \"Left\": 0, \"LowerRightRow\": 0, \"Bottom\": 0, \"LowerRightColumn\": 3, \"ImageFormat\": \"jpg\", \"SourceFullName\": \"download.jpg\"}" \
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

## クラウド SDK ファミリー

SDK を使用すると、開発が最も迅速に行えます。SDK が低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全なリストについては、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetPicture.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetPicture.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetPicture.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetPicture.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetPicture.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetPicture.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetPicture.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetPicture.go" >}}

{{< /tab >}}

{{< /tabs >}}

*関連項目:* 画像の追加、画像の削除、画像の取得、画像のクリア – Aspose.Cells Cloud API におけるその他の画像関連操作。