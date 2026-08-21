---
title: "Excelワークシート内のすべての空白セルを一致させる"
ArticleTitle: "Excelワークシート内のすべての空白セルを一致させる – Aspose.Cells Cloud APIガイド"
second_title: "ドキュメント"
linktype: "docs"
url: /ja/autofilter/match-all-blank/
aliases: [  /ja/match-all-blank-cells-in-the-list/ ]
keywords: "Aspose.Cells, 空白セル, AutoFilter, REST API, Excel"
description: "Aspose.Cells Cloud REST APIを使用して、Excelワークシート内のすべての空白セルをフィルタリングおよび一致させる方法を学びます。エンドポイント、パラメータ、認証手順、cURLの例、およびC#、Java、Pythonなど向けのSDKスニペットを含みます。"
weight: 100
---

このREST APIは、Excelワークシートのフィルターリスト内のすべての**空白セル**を一致させます。

**前提条件:** このエンドポイントを呼び出す前に、有効なJWTアクセストークンを取得し、ワークブックをAspose Cloudストレージにアップロード済みであること、およびストレージフォルダ（該当する場合）の情報を把握していることを確認してください。ファイルがデフォルトのルートフォルダにない場合は、`folder`および`storageName`パラメータを指定してください。

## PostWorksheetMatchBlanks API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/matchBlanks
```

### **セキュリティと認証**

Aspose.Cells Cloud APIは安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWTトークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名 | 型      | 位置   | 説明                                                      |
|-------------|---------|--------|-----------------------------------------------------------|
| name        | string  | path   | ワークブックファイルの名前。                               |
| sheetName   | string  | path   | フィルターを含むワークシートの名前。                       |
| fieldIndex  | integer | query  | フィルターを適用する列の0から始まるインデックス。          |
| folder      | string  | query  | ワークブックが配置されているストレージ内のフォルダパス。   |
| storageName | string  | query  | Aspose Cloudストレージの名前。                             |

### **レスポンス**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTPステータスコード**

| コード | 意味                   | 説明                                      |
|-------|------------------------|-------------------------------------------|
| 200   | OK                     | フィルターが正常に適用され、レスポンスに操作の詳細が含まれます。 |
| 400   | Bad Request            | パラメータが不足している、または無効です（例：サポートされていないファイル形式）。 |
| 401   | Unauthorized           | JWTトークンが無効または不足しています。   |
| 413   | Payload Too Large      | アップロードされたファイルがサイズ制限を超えています。 |
| 500   | Internal Server Error  | 予期しないサーバーエラーが発生しました。   |

## SDKを使用してPostWorksheetMatchBlanks APIを活用する方法

### PostWorksheetMatchBlanks API仕様

[OpenAPI仕様](https://apireference.aspose.cloud/cells/#/AutoFilter/PostWorksheetMatchBlanks)は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Webブラウザから直接RESTのやり取りを実行できるようにします。

cURLコマンドラインツールを使用してAspose.Cellsウェブサービスにアクセスできます。以下の例では、cURLを使用してCloud APIを呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}
```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/matchBlanks?fieldIndex=0" \
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

### Aspose.Cells Cloud SDKの使用

SDKを使用することが開発を高速化する最良の方法です。SDKは低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDKの完全な一覧については、[GitHubリポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまなSDKを使用してAspose.Cellsウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetMatchBlanks.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetMatchBlanks.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetMatchBlanks.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetMatchBlanks.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetMatchBlanks.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetMatchBlanks.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetMatchBlanks.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetMatchBlanks.go" >}}
{{< /tab >}}

{{< /tabs >}}