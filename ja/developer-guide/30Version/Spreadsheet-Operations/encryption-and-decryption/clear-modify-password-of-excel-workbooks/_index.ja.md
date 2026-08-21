---
title: "Excel ワークブックから書き込み保護（パスワード）を解除する"
second_title: "Document"
linktitle: "Excel ファイルのパスワードを解除する"
type: docs
url: /clear-excel-files-password/
aliases:
  [
    /clear-modify-password-of-excel-workbooks/,
    /workbook/clear-modify-password/，/workbook/password/clear/,
  ]
keywords: "Aspose.Cells, Excel, パスワード解除, 書き込み保護, REST API, SDK サンプル"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークブックから書き込み保護（パスワード）を削除する方法を学びます。cURL サンプル、認証手順、SDK コードサンプルを含みます。"
weight: 110
ArticleTitle: "Excel ワークブックから書き込み保護（パスワード）を解除する"
---

この REST API は、Excel ワークブックから**書き込み保護（パスワード）**を解除し、プログラムで Excel のパスワード保護を解除できるようにします。

**前提条件:** 有効な JWT トークンを取得し、ワークブックがサポートされているストレージの場所に保存されていることを確認し、API バージョン v3.0 を使用してください。

保護を追加する方法については、[Excel の保護](/cells/protect/)ガイドを参照してください。

## DeleteDocumentUnprotectFromChanges API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/writeProtection
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を必要とします。

### **リクエストパラメータ**

| パラメータ名     | 型     | 位置   | 説明                                        |
| ---------------- | ------ | ------ | --------------------------------------------- |
| `name`           | string | path   | Excel ワークブックの名前。                    |
| `folder`         | string | query  | ワークブックを含むフォルダ（オプション）。     |
| `storageName`    | string | query  | ストレージサービスの名前（オプション）。       |


### レスポンス

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP ステータスコード**

| コード | 意味                         | 説明                                              |
| ------ | ---------------------------- | ------------------------------------------------- |
| 200    | OK                           | フィルターが正常に適用された。レスポンスには操作の詳細が含まれる。 |
| 400    | Bad Request                  | パラメータが不足または無効（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized                 | JWT トークンが無効または不足している。             |
| 413    | Payload Too Large            | アップロードされたファイルがサイズ制限を超えている。 |
| 500    | Internal Server Error        | 予期しないサーバーエラーが発生しました。           |

## SDK を使用した DeleteDocumentUnprotectFromChanges API の使用方法

### DeleteDocumentUnprotectFromChanges API の仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Workbook/DeleteDocumentUnprotectFromChanges) は、パブリックにアクセス可能なプログラミングインタフェースを定義し、Web ブラウザから直接 REST アクセスを実行できるようにします。

cURL コマンドラインツールを使用して Aspose.Cells サービスに簡単にアクセスできます。以下の例は、cURL を使用して REST API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xlsx/writeProtection" \
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


### Aspose.Cells Cloud SDK の使用

SDK を使用すると、開発を迅速に進めることができます。SDK が低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDocumentUnprotectFromChanges.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDocumentUnprotectFromChanges.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDocumentUnprotectFromChanges.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDocumentUnprotectFromChanges.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_DeleteDocumentUnprotectFromChanges.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDocumentUnprotectFromChanges.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDocumentUnprotectFromChanges.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDocumentUnprotectFromChanges.go" >}}

{{< /tab >}}

{{< /tabs >}}