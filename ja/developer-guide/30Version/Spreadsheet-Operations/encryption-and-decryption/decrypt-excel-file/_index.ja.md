---
title: "Excel ワークブックの復号化"
second_title: "ドキュメント"
linktitle: "Excel ファイルの復号化"
type: docs
url: /excel-file-decrypt/
aliases: [/decrypt-excel-workbooks/, /workbook/decrypt/]
keywords: "Aspose.Cells, Excel 復号化, REST API, クラウド SDK"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークブックを復号化する方法を学びます。必要なパラメータ、cURL の例、SDK のコードサンプル、エラー処理の詳細を含みます。"
ArticleTitle: "Aspose.Cells Cloud API を使用して Excel ワークブックを復号化する方法"
weight: 50
---

**前提条件**

- 有効な JWT アクセストークン。
- ワークブックは Aspose Cloud ストレージにアップロード済みで、`folder` クエリパラメータにそのパスが指定されていること。

## DeleteDecryptWorkbook API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/encryption
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を必要とします。

### クエリパラメータ

| パラメータ名 | 型     | 説明                                     |
| ------------ | ------ | ----------------------------------------- |
| folder       | string | 元のワークブックが存在するフォルダのパス。   |
| storageName  | string | ワークブックが存在するストレージの名前。     |

### リクエストボディパラメータ

| パラメータ名 | 型                      | 説明                               |
| ------------ | ----------------------- | ----------------------------------- |
| encryption   | WorkbookEncryptionRequest | 復号化に必要な暗号化設定。 |

### WorkbookEncryptionRequest

| パラメータ名 | 型     | 説明                                                                 |
| ------------ | ------ | --------------------------------------------------------------------- |
| EncryptionType | string | 暗号化アルゴリズム（`XOR`, `Compatible`, `EnhancedCryptographicProviderV1`, `StrongCryptographicProvider`） |
| KeyLength    | integer | 暗号化キーの長さ（ビット単位）。                                      |
| Password     | string | 復号化に使用するパスワード。                                           |

### レスポンス

```json
{
  "Status":"OK",
  "Code":200
}
```

**サンプルエラーレスポンス**

```json
{
  "Code": "400",
  "Message": "無効なリクエストパラメータです。"
}
```

```json
{
  "Code": "401",
  "Message": "認証に失敗しました。無効な JWT トークン、またはトークンが不足しています。"
}
```

```json
{
  "Code": "413",
  "Message": "ペイロードが大きすぎます。アップロードされたファイルが許容サイズを超えています。"
}
```

```json
{
  "Code": "500",
  "Message": "サーバー内部エラーが発生しました。後でもう一度お試しください。"
}
```

**HTTP ステータスコード**

| コード | 意味                     | 説明                                      |
|------|-------------------------|-------------------------------------------|
| 200  | OK                      | フィルターが正常に適用され、レスポンスには操作の詳細が含まれます。 |
| 400  | Bad Request             | パラメータが不足しているか無効です（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized            | 無効な JWT トークン、またはトークンが不足しています。 |
| 413  | Payload Too Large       | アップロードされたファイルがサイズ制限を超えています。 |
| 500  | Internal Server Error   | 予期しないサーバーエラーが発生しました。 |

## SDK を使用した DeleteDecryptWorkbook API の利用方法

### DeleteDecryptWorkbook API の仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Workbook/DeleteDecryptWorkbook) はパブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST によるインタラクションを実行できるようにします。

**cURL** を使用すれば Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は cURL を使用してクラウド API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/encryption" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -d '{ "EncryptionType": "XOR", "KeyLength": 1280, "Password": "aspose"}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、開発速度を最大限に向上させることができます。SDK が低レベルの詳細を処理するため、あなたはプロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全なリストについては [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDecryptWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDecryptWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDecryptWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDecryptWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteDecryptWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDecryptWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDecryptWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDecryptWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
---