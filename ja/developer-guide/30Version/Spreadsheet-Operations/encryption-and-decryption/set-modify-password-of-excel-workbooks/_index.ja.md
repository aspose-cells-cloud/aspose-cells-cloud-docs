---
title: "Excel ワークブックのパスワード保護を変更する"
second_title: "Document"
linktitle: "Excel ファイルのパスワードを変更する"
type: docs
url: /ja/workbook/password/modify/
aliases:
  - /set-modify-password-of-excel-workbooks/
  - /workbook/modify-password/
keywords: "Excel パスワード, Aspose.Cells Cloud, 書き込み保護, REST API, ワークブックのパスワードを変更"
description: "Aspose.Cells Cloud REST API (v3.0) を使用して Excel ワークブックの書き込み保護パスワードを変更します。cURL および SDK の例を含みます。"
weight: 100
ArticleTitle: "Excel ワークブックのパスワード保護を変更する – Aspose.Cells Cloud"
---

この REST API は、既存の Excel ワークブックの**書き込み保護パスワードを変更**します。

書き込み保護パスワードをプログラムで更新することで、ファイルをダウンロードすることなくパスワードをローテーションまたは置換できます。これは、Aspose.Cells Cloud ストレージに保存されたセキュリティで保護されたワークブックを管理する場合に特に便利です。


## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/writeProtection
```

### セキュリティと認証

Aspose.Cells Cloud API は安全であり、[JWT トークンベースの認証](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)が必要です。


### リクエストパラメータ

| パラメータ名  | 型     | 位置    | 説明                                      |
| --------------- | ------ | ----------- | ------------------------------------------------ |
| **name**        | 文字列 | path        | Excel ワークブックの名前（必須）。           |
| **password**    | 文字列 | body (JSON) | 設定する新しい書き込み保護パスワード（必須）。 |
| **folder**      | 文字列 | query       | ワークブックが格納されているフォルダ（オプション）。    |
| **storageName** | 文字列 | query       | ストレージサービスの名前（オプション）。            |

### レスポンス

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP ステータスコード**

| コード | 意味                     | 説明                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | フィルターが正常に適用された。レスポンスには操作の詳細が含まれます。 |
| 400  | Bad Request                 | パラメータが不足または無効（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized                | JWT トークンが無効または不足しています。 |
| 413  | Payload Too Large           | アップロードされたファイルがサイズ制限を超えています。 |
| 500  | Internal Server Error       | 予期しないサーバーエラーが発生しました。 |
## SDK を使用した PutDocumentProtectFromChanges API の使用方法

### PutDocumentProtectFromChanges API 仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Workbook/PutDocumentProtectFromChanges) は、Web ブラウザから直接 REST 通信を実行できるパブリックにアクセス可能なプログラミングインターフェースを定義しています。

**cURL** コマンドラインツールを使用して Aspose.Cells Web サービスに簡単にアクセスできます。以下の cURL コマンドは、Cloud API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/writeProtection?folder=Samples&storageName=Default" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{ "Password": "aspose" }'
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

SDK を使用すると、開発が最も迅速に行えます。SDK が低レベルの詳細を処理するため、ビジネスロジックの開発に集中できます。Aspose.Cells Cloud SDK の完全なリストについては、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) を確認してください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutDocumentProtectFromChanges.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutDocumentProtectFromChanges.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutDocumentProtectFromChanges.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutDocumentProtectFromChanges.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutDocumentProtectFromChanges.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutDocumentProtectFromChanges.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutDocumentProtectFromChanges.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutDocumentProtectFromChanges.go" >}}

{{< /tab >}}

{{< /tabs >}}
---