---
title: "Excelワークシート上のすべての図形を削除する"
ArticleTitle: "Excelワークシート上のすべての図形を削除する – Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktitle: "クリア"
type: docs
url: /ja/shapes/clear/
aliases: [  /ja/delete-all-shapes-inside-the-worksheet/ ]
keywords: "Aspose.Cells Cloud, すべての図形を削除, Excelワークシート, REST API, SDK, cURL, .NET, Java, PHP, Ruby, Node.js, Python, Perl, Go, Android, Swift"
description: "Aspose.Cells Cloud REST APIを使用してExcelワークシート上のすべての図形を削除します。この操作はcURLおよび幅広いSDK（C#、Java、PHP、Ruby、Node.js、Python、Perl、Go、Android、Swift）を介して利用可能です。"
weight: 40
---

このREST APIは、Excelワークシート上のすべての図形を削除します。

**前提条件:** 有効なJWTアクセストークンが必要です。Aspose Cloud OAuth2フローで取得し、以下の例に示すように`Authorization`ヘッダーに含めてください。

## DeleteWorksheetShapes API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes
```

### **セキュリティと認証**

Aspose.Cells Cloud APIは安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWTトークンベースの認証</a>を必要とします。

### **リクエストパラメーター**

| パラメーター名 | 型     | 位置   | 説明                             |
| -------------- | ------ | ------ | --------------------------------- |
| name           | string | path   | Excelドキュメントの名前です。     |
| sheetName      | string | path   | ワークシートの名前です。          |
| folder         | string | query  | ドキュメントが配置されているフォルダーです。 |
| storageName    | string | query  | ドキュメントが存在するストレージ名です。     |

<a href="https://apireference.aspose.cloud/cells/#/Shapes/DeleteWorksheetShapes" rel="noopener noreferrer">OpenAPI仕様</a>はパブリックにアクセス可能なプログラミングインターフェースを定義し、Webブラウザーから直接REST通信を実行できるようにします。

cURLコマンドラインツールを使用すると、Aspose.Cells Webサービスに簡単にアクセスできます。以下の例は、cURLでCloud APIに呼び出しを行う方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes" \
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

{{< /tab >}}

{{< /tabs >}}

## Cloud SDKファミリー

SDKを使用することが開発を高速化する最良の方法です。SDKは低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDKの完全なリストについては、[GitHubリポジトリー](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまなSDKを使用してAspose.Cells Webサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetShapes.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetShapes.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetShapes.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetShapes.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetShapes.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetShapes.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetShapes.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetShapes.go" >}}

{{< /tab >}}

{{< /tabs >}}