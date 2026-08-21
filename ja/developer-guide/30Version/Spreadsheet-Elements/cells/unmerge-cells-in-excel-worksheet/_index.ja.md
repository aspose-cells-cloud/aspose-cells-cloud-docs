---
title: "Excelワークシートでセルを結合解除する"
type: docs
url: /ja/unmerge-cells-in-excel-worksheet/
weight: 120
keywords: "Aspose.Cells, Excel, セルの結合解除, REST API, クラウドSDK"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークシートのセルを結合解除する方法を、リクエスト例、レスポンス形式、および複数のプログラミング言語向け SDK コードサンプルを交えて学びます。"
ArticleTitle: "Excelワークシートでセルを結合解除する"
---

この REST API は、Excel ファイル内のセルの結合を解除します。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/unmerge
```

## セキュリティと認証

Aspose.Cells Cloud API は安全であり、[JWT トークンベースの認証](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)が必要です。

**リクエストパラメータ**

| パラメータ名     | 型      | 位置   | 説明                                               |
|----------------|---------|--------|----------------------------------------------------|
| name           | string  | path   | ワークブックファイルの名前。                         |
| sheetName      | string  | path   | ワークシートの名前。                                |
| startRow       | integer | query  | 結合解除対象の最初の行の 0 から始まるインデックス。     |
| startColumn    | integer | query  | 結合解除対象の最初の列の 0 から始まるインデックス。     |
| totalRows      | integer | query  | 結合解除処理に含める行数。                            |
| totalColumns   | integer | query  | 結合解除処理に含める列数。                            |
| folder         | string  | query  | ワークブックが保存されているフォルダのパス。           |
| storageName    | string  | query  | ストレージサービスの名前。                           |

## **レスポンス**

CellCloudResponse を返します。

- **レスポンスフィールド概要**

| フィールド         | 型      | 説明                                           |
| --------------- | ------- | --------------------------------------------- |
| `Status`          | string  | ステータス文字列（例: "OK"）                    |
| `Code`            | integer | HTTP ステータスコード（200, 400, 401, 500,...） |

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP ステータスコード**

| コード | 意味              | 説明                                                |
|------|-------------------|-----------------------------------------------------|
| 200  | OK                | フィルターが正常に適用され、レスポンスに操作の詳細が含まれます。 |
| 400  | Bad Request       | パラメータが不足または無効（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized      | JWT トークンが無効または不足しています。               |
| 413  | Payload Too Large | アップロードされたファイルがサイズ制限を超えています。     |
| 500  | Internal Server Error | サーバー内部で予期しないエラーが発生しました。         |

## SDK を使用した PostWorksheetUnmerge API の使い方

### PostWorksheetUnmerge API の仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetUnmerge)はパブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 操作を実行できるようにしています。

cURL コマンドラインツールを使用して Aspose.Cells Web サービスに簡単にアクセスできます。以下の例では、cURL を使ってクラウド API への呼び出しを行う方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/unmerge?startRow=10&startColumn=10&totalRows=10&totalColumns=10" \
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

### Aspose.Cells Cloud SDK を使用する

SDK を使用すると、開発速度が最も高まります。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例では、さまざまな SDK を使用して Aspose.Cells Web サービスへの呼び出しを行う方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetUnmerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetUnmerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetUnmerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetUnmerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetUnmerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetUnmerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetUnmerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetUnmerge.go" >}}

{{< /tab >}}

{{< /tabs >}}