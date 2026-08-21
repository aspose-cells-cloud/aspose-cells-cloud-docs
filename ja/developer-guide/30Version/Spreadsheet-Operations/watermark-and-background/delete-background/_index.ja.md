---
title: "Excel ワークブックの背景を削除する"
second_title: "ドキュメント"
linktitle: "削除"
type: docs
url: /ja/delete-background-in-excel-file/
aliases:
  - /delete-background-in-workbook/
  - /workbook/delete-background/
  - /workbook/background/delete/
keywords: "Aspose Cells で背景を削除, Excel API で背景を削除, Aspose.Cells Cloud, DELETE /cells background"
description: "Aspose.Cells Cloud API を使用して Excel ワークブックから背景画像を削除します。DELETE エンドポイント、必要なパラメータ、cURL の例、および C#、Java、Python などの SDK コードについて学びます。"
weight: 170
ArticleTitle: "Aspose.Cells Cloud API を使用して Excel ワークブックから背景画像を削除する"
---

この REST API は、Excel ワークブックの背景画像を削除します。

## DeleteWorkbookBackground API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/background
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全で、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### **クエリパラメータ**

| パラメータ名 | 型     | 説明                                   | 必須 |
| ------------ | ------ | --------------------------------------- | ---- |
| folder       | string | 元のワークブックが含まれるフォルダ。   | いいえ |
| storageName  | string | 使用するストレージサービスの名前。     | いいえ |

### **レスポンス**

```json
{
    "Status" : "OK",
    "Code" : 200
}
```

**HTTP ステータスコード**

| コード | 意味                   | 説明                                               |
|------|------------------------|----------------------------------------------------|
| 200  | OK                     | フィルターが正常に適用され、レスポンスに操作の詳細が含まれます。 |
| 400  | Bad Request            | パラメータが不足または無効（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized           | JWT トークンが無効または不足しています。 |
| 413  | Payload Too Large      | アップロードされたファイルがサイズ制限を超えています。 |
| 500  | Internal Server Error  | サーバーで予期せぬエラーが発生しました。 |

## SDK を使用した DeleteWorkbookBackground API の利用方法

### DeleteWorkbookBackground API の仕様

<a href="https://apireference.aspose.cloud/cells/#/Workbook/DeleteWorkbookBackground" target="_blank" rel="noopener noreferrer">OpenAPI 仕様</a> は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 操作を実行できるようにします。

**cURL** コマンドラインツールを使用して、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、必要な認証ヘッダーを含む完全な DELETE リクエストを示しています。リクエストボディは不要です。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/{name}/background?folder=DotnetFiles" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -H "x-aspose-client: Containerize.Swagger"
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

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、開発速度を最大化できます。SDK が低レベルの詳細処理を担当するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全な一覧については、<a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub リポジトリ</a> をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています：

{{< tabs tabTotal="8" tabID="4"
   tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby"
   tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

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