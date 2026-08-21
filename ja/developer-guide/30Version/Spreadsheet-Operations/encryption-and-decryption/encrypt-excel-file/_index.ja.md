---
title: "Aspose.Cells Cloud API を使用して Excel ワークブックを暗号化 – クイック cURL および SDK サンプル"
second_title: "ドキュメント"
linktype: "docs"
url: "/excel-file-encrypt/"
aliases: [/encrypt-excel-workbooks/, /workbook/encrypt/]
keywords: "Aspose Cells ワークブック暗号化, Excel 暗号化 API, REST API, cURL, .NET, Java, Python, PHP, Ruby, Node.js, Go, Perl"
description: "Aspose.Cells Cloud REST API (v3.0) を使用して Excel ワークブックを暗号化する方法を学びます。cURL コマンド、SDK コードサンプル（C#、Java、Python など）、必要なパラメーター、エラーハンドリングを含みます。"
weight: 20
ArticleTitle: "Aspose.Cells Cloud API を使用して Excel ワークブックを暗号化 – cURL および SDK サンプル"
---

この REST API は Excel **ワークブック** を暗号化します。

**前提条件:** このエンドポイントを呼び出す前に、有効な JWT トークンと、ストレージにアップロードされたワークブックが必要です。

## PostEncryptDocument API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/encryption
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### **クエリパラメーター**

| パラメーター名 | 型     | 必須 | 説明                     |
| -------------- | ------ | ---- | ------------------------- |
| folder         | string | ✗    | 元のワークブックのあるフォルダーパス。 |
| storageName    | string | ✗    | 使用するストレージの名前。 |

### **リクエストボディパラメーター**

| パラメーター名 | 型                        | 必須 | 説明                 |
| -------------- | ------------------------- | ---- | --------------------- |
| encryption     | WorkbookEncryptionRequest | ✓    | ワークブックの暗号化設定。 |

#### **WorkbookEncryptionRequest**

| パラメーター名 | 型      | 必須 | 説明                                                                 |
| -------------- | ------- | ---- | -------------------------------------------------------------------- |
| EncryptionType | string  | ✓    | 暗号化アルゴリズム。サポートされる値とその意味については、以下の表を参照してください。 |
| KeyLength      | integer | ✗    | 暗号化キーの長さ（ビット単位）。`XOR` および `Compatible` の場合は無視されます。 |
| Password       | string  | ✓    | 暗号化に使用するパスワード。                                         |

#### **EncryptionType の値**

| 値                                | 説明                                      |
| --------------------------------- | ----------------------------------------- |
| `XOR`                             | 単純な XOR アルゴリズム（レガシー、セキュリティが低い）。 |
| `Compatible`                      | Excel 97‑2003 互換暗号化（40 ビット）。     |
| `EnhancedCryptographicProviderV1` | SHA‑1 ハッシュを使用した AES‑128。          |
| `StrongCryptographicProvider`     | SHA‑512 ハッシュを使用した AES‑256（最も強力）。 |

### レスポンス

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP ステータスコード**

| コード | 意味                       | 説明                                             |
|------|---------------------------|--------------------------------------------------|
| 200  | OK                        | フィルターが正常に適用された。レスポンスには操作の詳細が含まれます。 |
| 400  | Bad Request               | パラメーターが不足しているか、無効です（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized              | JWT トークンが無効または不足しています。             |
| 413  | Payload Too Large         | アップロードされたファイルがサイズ制限を超えています。 |
| 500  | Internal Server Error     | 予期しないサーバーエラーが発生しました。             |

## SDK を使用した PostEncryptDocument API の利用方法

### PostEncryptDocument API の仕様

<a href="https://apireference.aspose.cloud/cells/#/Workbook/PostEncryptDocument" rel="noopener noreferrer">OpenAPI 仕様</a> はパブリックにアクセス可能なプログラミングインターフェースを定義し、ウェブブラウザーから直接 REST 操作を実行できます。

**cURL** コマンドラインツールを使用して Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例では、cURL を使用してクラウド API にアクセスする方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
# XOR アルゴリズム（128 ビットキー）とパスワード「mateen」を使用して、ワークブック「test.xlsx」を暗号化します。
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/encryption" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -d '{ "EncryptionType": "XOR", "KeyLength": 128, "Password": "mateen"}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

**発生する可能性のあるエラーレスポンス**

| HTTP ステータス | コード                | メッセージ                                     |
| --------------- | ------------------- | --------------------------------------------- |
| 400             | BadRequest          | パラメーターが不足しているか、無効です。         |
| 401             | Unauthorized        | 認証トークンがありません、または無効です。       |
| 403             | Forbidden           | ストレージへのアクセス権限が不足しています。      |
| 500             | InternalServerError | 予期しないサーバーエラーが発生しました。          |

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、開発を最速で進められます。SDK が低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全な一覧については、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリー</a> をご確認ください。

以下のコード例では、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostEncryptWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostEncryptWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostEncryptWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostEncryptWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostEncryptWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostEncryptWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostEncryptWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostEncryptWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
---