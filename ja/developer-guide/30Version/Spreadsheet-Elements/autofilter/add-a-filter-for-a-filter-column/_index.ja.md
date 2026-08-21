---
title: "Excelワークシートにフィルターを追加する"
second_title: "Document"
linktype: "フィルターの追加"
type: docs
url: /ja/autofilter/add-filter/
aliases: [  /ja/add-a-filter-for-a-filter-column/ ]
keywords: "Aspose.Cells, Cloud, Excel, AutoFilter, フィルターの追加, REST API, SDK"
description: "Aspose.Cells Cloud REST APIを使用してExcelワークシートの列にオートフィルターを追加する方法を学びます。cURL、SDKサンプル、パラメータガイドを含みます。"
weight: 60
ArticleTitle: "Aspose.Cells Cloudを使用してExcelワークシートにフィルターを追加する"
---

**前提条件:** このAPIを呼び出す前に、有効なJWTトークンを取得し、対象のワークブックが指定されたストレージにアップロードされていること、およびファイルにアクセスするための適切な権限を持っていることを確認してください。コマンドラインの例には、cURLの最新バージョン（7.68以降）の使用を推奨します。

このREST APIは、Excelワークシートの特定の列にフィルターを追加します。

## PutWorksheetFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filter
```

### **セキュリティと認証**

Aspose.Cells Cloud APIは安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWTトークンベースの認証</a>を必要とします。

### リクエストパラメータ

| パラメータ名 | 型      | 位置   | 説明 |
|-------------|---------|--------|------|
| name        | string  | Path   | ワークブック名。 |
| sheetName   | string  | Path   | ワークシート名。 |
| range       | string  | Query  | フィルターを含むセル範囲（例: `A1:B1`）。 |
| fieldIndex  | integer | Query  | フィルターを適用する列の0から始まるインデックス。 |
| criteria    | string  | Query  | フィルター条件（例: 値または式）。 |
| matchBlanks | boolean | Query  | フィルターに空白セルを含める場合は`true`に設定。それ以外の場合は`false`。 |
| refresh     | boolean | Query  | 適用後にフィルターを更新する場合は`true`に設定。それ以外の場合は`false`。 |
| folder      | string  | Query  | 元のワークブックが保存されているフォルダ。 |
| storageName | string  | Query  | ストレージサービスの名前。 |

### **レスポンス**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTPステータスコード**

| コード | 意味             | 説明 |
|-------|------------------|------|
| 200   | OK               | フィルターが正常に適用された。レスポンスには操作の詳細が含まれる。 |
| 400   | Bad Request      | 必須パラメータが不足している、または無効なパラメータ（例: サポートされていないファイル形式）がある。 |
| 401   | Unauthorized     | 無効なJWTトークン、またはトークンが不足している。 |
| 413   | Payload Too Large| アップロードされたファイルがサイズ制限を超えた。 |
| 500   | Internal Server Error | 予期しないサーバーエラーが発生した。 |

## SDKを使用してPutWorksheetFilter APIを利用する方法

### PutWorksheetFilter API仕様

<a href="https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetFilter" target="_blank" rel="noopener noreferrer">OpenAPI仕様</a>はパブリックに利用可能なプログラミングインターフェースを定義し、Webブラウザから直接REST APIとのやり取りを実行できます。

cURLコマンドラインツールを使用すると、Aspose.Cellsウェブサービスに簡単にアクセスできます。以下の例では、cURLでAPIを呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filter?range=A1:B1&fieldIndex=0&criteria=Year" \
-X PUT \
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

### Aspose.Cells Cloud SDKの使用

SDKを使用すると、開発を最速で行えます。SDKが低レベルの詳細を処理するため、プロジェクトの本質的な部分に集中できます。Aspose.Cells Cloud SDKの完全な一覧については、<a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHubリポジトリ</a>をご確認ください。

以下のコード例では、さまざまなSDKを使用してAspose.Cellsウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}