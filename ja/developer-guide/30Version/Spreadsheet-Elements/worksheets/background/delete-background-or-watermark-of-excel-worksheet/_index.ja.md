---
title: "Excelワークシートの背景を削除する"
second_title: "Document"
linktitle: "削除"
type: docs
url: /worksheets/background/delete/
aliases: [/delete-background-or-watermark-of-excel-worksheet/]
keywords: "Aspose.Cells Cloud, ワークシート背景の削除, Excel, REST API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークシートの背景画像を削除します。SDK は C#、Java、PHP、Ruby、Node.js、Python、Perl、Go で利用可能です。"
weight: 210
ArticleTitle: "Aspose.Cells Cloud API を使用して Excel ワークシートの背景を削除する"
---

この REST API は、ワークシートの背景画像を削除します。

**前提条件:** ワークブックは Aspose Cloud ストレージに保存されており、認証用の有効な JWT アクセストークンを所有している必要があります。

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/background
```

### **リクエストパラメータ**

| パラメータ名   | 型     | 位置   | 説明                                         |
| -------------- | ------ | ------ | -------------------------------------------- |
| name           | string | path   | Excel ファイルの名前。                       |
| sheetName      | string | path   | 背景を削除するワークシートの名前。           |
| folder         | string | query  | ファイルが保存されているストレージ内のフォルダ。 |
| storageName    | string | query  | ストレージ名（デフォルトストレージでない場合）。 |

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetBackground) はパブリックに利用可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 通信を実行できるようにします。

cURL コマンドラインツールを使用すると、Aspose.Cells Web サービスに簡単にアクセスできます。すべてのリクエストには有効な JWT トークンが必要です。認証ガイドに従って OAuth2 トークンエンドポイントからトークンを取得してください。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/WorkSheetBackground_Sample_Test_Book.xls/worksheets/Sheet1/background" \
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

**HTTP ステータスコード**

| コード | 意味                           | 説明                                     |
|------|-------------------------------|------------------------------------------|
| 200  | OK                            | フィルターが正常に適用され、レスポンスには操作の詳細が含まれます。 |
| 400  | Bad Request                   | パラメータが不足または無効です（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized                  | JWT トークンが無効または不足しています。 |
| 413  | Payload Too Large             | アップロードされたファイルがサイズ制限を超えています。 |
| 500  | Internal Server Error         | サーバーで予期しないエラーが発生しました。 |

{{< /tab >}}

{{< /tabs >}}

## クラウド SDK ファミリー

SDK を使用すると、開発を高速化できます。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストについては、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスへの呼び出しを行う方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}
---