---
title: "Excel ワークブックにデジタル署名を追加する"
ArticleTitle: "Excel ワークブックにデジタル署名を追加する – Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktype: "デジタル署名"
type: docs
url: /excel-digital-signature/
aliases:
  - /protect/digital-signature/
  - /workbook/digital-signature/
keywords: "Aspose.Cells Cloud, デジタル署名, Excel ワークブック, REST API, .pfx, JWT, 署名 API"
description: "Aspose.Cells Cloud REST API (v4.0) を使用して Excel ワークブックにデジタル署名を追加する方法を学びます。エンドポイント、パラメータ、認証、レスポンススキーマ、エラーハンドリング、および複数の言語向け SDK のサンプルを含みます。"
weight: 35
---


**前提条件:**  
このエンドポイントを呼び出す前に、次のものを確認してください。

- Aspose Cloud の認証を通じて取得した有効な JWT アクセストークン  
- 対象のワークブックが Aspose Cloud ストレージにアップロードされていること  
- `.pfx` または `.p12` 形式のデジタル署名ファイルとそのパスワード  

この REST API は、Excel ワークブックに**デジタル署名**を追加します。

## PostDigitalSignature API

```http
POST https://api.aspose.cloud/v4.0/cells/{name}/digitalsignature
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を必要とします。

### リクエストパラメータ

| パラメータ名             | 型     | 位置                 | 説明                                                    |
| ------------------------ | ------ | -------------------- | ------------------------------------------------------ |
| **name**                 | 文字列 | `<code>path</code>`  | ワークブックの名前。                                    |
| **digitalsignaturefile** | 文字列 | `<code>query</code>` | デジタル署名ファイル（`.pfx` または `.p12`）へのパス。   |
| **password**             | 文字列 | `<code>query</code>` | ワークブックが保護されている場合のパスワード。           |
| **folder**               | 文字列 | `<code>query</code>` | ワークブックが保存されているフォルダ。                  |
| **storageName**          | 文字列 | `<code>query</code>` | 使用するストレージサービスの名前。                      |

*注：ファイル名に特殊文字が含まれる場合は、クエリ文字列に追加する前に URL エンコードしてください。*

### エラーハンドリング

| HTTP ステータス | 意味                                                    |
| --------------- | ------------------------------------------------------- |
| 200             | 署名が正常に適用されました。                            |
| 400             | 不正なリクエスト – パラメータが不足または無効です。     |
| 401             | 認証エラー – 無効または期限切れの OAuth トークンです。   |
| 403             | アクセス拒否 – 権限が不足しているか、アクセスが拒否されました。 |
| 500             | サーバーエラー – 予期せぬ失敗が発生しました。            |

### HTTP ステータスのエラーレスポンス

| HTTP ステータス | コード                | 説明                                                       |
| --------------- | --------------------- | ---------------------------------------------------------- |
| 400             | BadRequest            | パラメータが不足または無効です。                            |
| 401             | Unauthorized          | アクセストークンが無効または不足しています。                |
| 404             | NotFound              | 指定されたワークブックが、指定されたフォルダ/ストレージに見つかりません。 |
| 500             | InternalServerError   | 予期せぬサーバーエラーです。                                |


## SDK を使用して PostDigitalSignature API を使用する方法

### PostDigitalSignature API 仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Protection/PostDigitalSignature) はパブリックにアクセス可能なプログラミングインターフェースを定義し、ウェブブラウザから直接 REST 通信を実行できるようにします。

cURL コマンドラインツールを使用して Aspose.Cells ウェブサービスを呼び出すことができます。以下の例は、API へのリクエストを示しています：

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/digitalsignature?digitalsignaturefile=signature.pfx&password=YourPassword" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**レスポンススキーマ**  
API は、以下のフィールドを含む JSON オブジェクトを返します：

| フィールド        | 型     | 説明                                                    |
| --------------- | ------ | ------------------------------------------------------- |
| `Code`          | int    | 結果を示す HTTP スタイルのステータスコード。             |
| `Status`        | 文字列 | 結果を表す短いテキスト（例：`OK`）。                    |
| `SignatureId`   | 文字列 | 適用されたデジタル署名の識別子（オプション）。           |
| `Message`       | 文字列 | 補足情報またはエラーの詳細（オプション）。               |

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、統合が容易になり、ボイラープレートコードを削減できます。Aspose.Cells Cloud SDK の完全なリストについては、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostDigitalSignature.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostDigitalSignature.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostDigitalSignature.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostDigitalSignature.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82a2de2e4189bc27ae92abf73c36b4df0" "Example_PostDigitalSignature.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostDigitalSignature.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostDigitalSignature.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostDigitalSignature.go" >}}

{{< /tab >}}

{{< /tabs >}}