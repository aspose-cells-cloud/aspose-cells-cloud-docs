---
title: "Excelワークシート内のセルの書式設定をクリアする"
type: docs
url: /clear-cells-formatting-in-excel-worksheet/
weight: 100
keywords: "Aspose.Cells Cloud, Excel, セルの書式設定のクリア, REST API, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "Aspose.Cells Cloud REST API を使用して、Excelワークシート内のセルの書式設定をクリアします。リクエストの詳細、cURLの例、複数の言語向けのSDKコードスニペットを含みます。"
ArticleTitle: "Excelワークシート内のセルの書式設定をクリアする - Aspose.Cells Cloud API"
---

**注意:** すべての Aspose.Cells Cloud API の呼び出しは **HTTPS** 経由で行う必要があります。HTTPエンドポイントは非推奨となっており、ブラウザによってブロックされる可能性があります。

- **メソッド:** POST  
- **エンドポイント:** `https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/clearformats`

このREST APIは、Excelファイル内のセルの書式設定をクリアし、Aspose.Cells Cloudスイートの一部としてExcelワークシート内のセル書式設定をクリアするための機能を提供します。

## PostClearFormats API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/clearformats
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### **レスポンス**

```json
{
    "Status":"OK",
    "Code":200
}
```

**レスポンススキーマ**

| フィールド | タイプ    | 説明                                   |
|-----------|-----------|-----------------------------------------------|
| Code      | 整数      | API が返す HTTP ステータスコード（例: 200）。 |
| Status    | 文字列    | 操作の結果（成功時は `OK`）。   |

**HTTPステータスコード**

| コード | 意味                         | 説明                                      |
|--------|------------------------------|---------------------------------------------|
| 200    | OK                           | フィルターが正常に適用された。レスポンスには操作の詳細が含まれます。 |
| 400    | リクエストエラー             | パラメータが不足または無効（例: 未対応のファイル形式）。 |
| 401    | 認証エラー                   | JWT トークンが無効または不足しています。 |
| 413    | ペイロードが大きすぎます     | アップロードされたファイルがサイズ制限を超えています。 |
| 500    | サーバ内部エラー             | 予期せぬサーバーエラーが発生しました。 |

## SDK を使用した PostClearFormats API の利用方法

### PostClearFormats API 仕様

<a href="https://apireference.aspose.cloud/cells/#/Cells/PostClearFormats" rel="noopener noreferrer">OpenAPI 仕様</a> は、パブリックに利用可能なプログラミングインターフェースを定義し、ウェブブラウザから直接 REST の操作を実行できるようにします。

cURL コマンドラインツールを使用すると、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API に呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/clearformats?range=a1%3Aa10&startRow=1&startColumn=1&endRow=10&endColumn=10" \
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

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、開発が最も迅速に行えます。SDK が低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご覧ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostClearFormats.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostClearFormats.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostClearFormats.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostClearFormats.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostClearFormats.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostClearFormats.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostClearFormats.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostClearFormats.go" >}}

{{< /tab >}}

{{< /tabs >}}

**関連項目**

- [セルのコンテンツとスタイルをクリアする](https://docs.aspose.cloud/cells/clear-contents-and-styles)  
- [セルのスタイルを設定する](https://docs.aspose.cloud/cells/set-cell-style)
---