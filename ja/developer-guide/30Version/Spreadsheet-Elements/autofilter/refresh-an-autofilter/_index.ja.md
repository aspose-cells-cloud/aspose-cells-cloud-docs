---
title: "Excelワークシート内のオートフィルターを更新する"
second_title: "Document"
linktitle: "オートフィルターの更新"
type: docs
url: /autofilter/refresh/
aliases: [/refresh-an-autofilter/]
weight: 100
keywords: "Aspose.Cells, AutoFilter, refresh, Excel, API, REST"
description: "Aspose.Cells Cloud REST API を使用して、Excelワークシート上の既存のオートフィルターを更新します。C#、Java、Python など、 various SDK および cURL の使用例を含みます。"
ArticleTitle: "Excelワークシート内のオートフィルターを更新する"
---

### **更新**（Refresh）とは？

このエンドポイントを呼び出すと、ワークシートのデータが変更された後（例：行の追加や削除後）に、現在のフィルター条件を再適用します。この操作はフィルター定義自体を変更せず、単に表示を更新し、ステータス応答を返すだけです。

### REST API

この REST API は、Excelワークシート上のオートフィルターを更新します（API バージョン **v3.0**）。

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/refresh
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### **応答**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP ステータスコード**

| コード | 意味                     | 説明                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | フィルターが正常に適用された。応答には操作の詳細が含まれます。 |
| 400  | Bad Request（不正なリクエスト） | パラメーターが不足している、または無効（例：サポートされていないファイル形式）です。 |
| 401  | Unauthorized（認証されていません） | JWT トークンが無効または不足しています。 |
| 413  | Payload Too Large（ペイロードが大きすぎます） | アップロードされたファイルがサイズ制限を超えています。 |
| 500  | Internal Server Error（内部サーバーエラー） | 予期しないサーバーエラーが発生しました。 |

*エラー応答の例*  

```json
// 400 Bad Request
{
    "Code": 400,
    "Message": "Invalid parameter: sheetName not found."
}

// 401 Unauthorized
{
    "Code": 401,
    "Message": "Authentication failed. JWT token is missing or invalid."
}

// 413 Payload Too Large
{
    "Code": 413,
    "Message": "The uploaded file exceeds the maximum allowed size."
}

// 500 Internal Server Error
{
    "Code": 500,
    "Message": "An unexpected error occurred on the server."
}
```

## SDK を使用した PostWorksheetAutoFilterRefresh API の使用方法

### PostWorksheetAutoFilterRefresh API の仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/AutoFilter/PostWorksheetAutoFilterRefresh) は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザーから直接 REST 操作を実行できるようにします。

cURL コマンドラインツールを使用すると、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API に呼び出しを行う方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/refresh" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your-jwt-token>"
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

### Aspose.Cells Cloud SDK を使用する

SDK を使用すると、開発を高速化できます。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスに呼び出しを行う方法を示しています。
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetAutoFilterRefresh.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetAutoFilterRefresh.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetAutoFilterRefresh.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetAutoFilterRefresh.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetAutoFilterRefresh.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetAutoFilterRefresh.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetAutoFilterRefresh.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetAutoFilterRefresh.go" >}}

{{< /tab >}}

{{< /tabs >}}
---