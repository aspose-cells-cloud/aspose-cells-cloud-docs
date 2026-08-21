---
title: "Excelワークシートに背景を設定する"
ArticleTitle: "Excelワークシートに背景を設定する – Aspose.Cells Cloud APIガイド"
second_title: "ドキュメント"
linktitle: "追加"
type: docs
url: /ja/worksheets/background/add/
aliases: [  /ja/set-background-or-watermark-for-excel-worksheet/ ]
keywords: "Aspose.Cells, Excel, ワークシート, 背景, REST API, SDK, 画像の追加"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークシートに背景画像（PNG、JPEG、BMP）を追加する方法を学びます。エンドポイント、必要なパラメータ、認証手順、cURL の使用例、および SDK のコードサンプルを含みます。"
weight: 180
---

この REST API は、ワークシートに背景画像を追加します。

## セキュリティと認証
Aspose.Cells Cloud API は安全であり、[JWT トークンベースの認証](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)を必要とします。

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/background
```

### **リクエストパラメータ**

| パラメータ名    | 型     | 位置   | 説明                                          |
| -------------- | ------ | ------ | --------------------------------------------- |
| name           | string | path   | Excel ワークブックの名前。                    |
| sheetName      | string | path   | 画像を適用するワークシートの名前。            |
| imageFile      | file   | body   | 背景として設定するバイナリ画像ファイル（PNG、JPEG、BMP など）。 |
| folder         | string | query  | ワークブックが配置されているストレージ内のフォルダ。 |
| storageName    | string | query  | Aspose Cloud ストレージの名前。               |

**サポートされる形式と制限事項**

- 受け入れられる画像拡張子：**PNG、JPEG、BMP、GIF**。
- 最大ファイルサイズ：**5 MB**。
- 画像はワークシート全体の背景にタイル状に敷き詰められます。

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Worksheets/PutWorksheetBackground) はパブリックにアクセス可能なプログラミングインターフェースを定義し、ウェブブラウザから直接 REST によるやり取りを実行できるようにします。

cURL コマンドラインツールを使用すると、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用して Cloud API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/background" \
  -X PUT \
  -F "imageFile=@Creative.jpg" \
  -H "Content-Type: multipart/form-data" \
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

_考えられるエラーレスポンス_

| HTTP コード | 説明                                               |
| ----------- | -------------------------------------------------- |
| 400         | 不正なリクエスト – パラメータが不足または無効です。   |
| 401         | 認証エラー – JWT トークンが無効または期限切れです。   |
| 404         | 見つかりません – ワークブックまたはワークシートが存在しません。 |
| 500         | サーバ内部エラー – サーバ上で予期しない状態が発生しました。 |

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK ファミリー

SDK を使用することが開発を最適化する最良の方法です。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}
---