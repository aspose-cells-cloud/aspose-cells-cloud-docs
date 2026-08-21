---
title: "Excelワークシートでセルを結合する方法 – Aspose.Cells Cloud API (v3.0)"
type: docs
url: /ja/merge-cells-in-excel-worksheet/
weight: 110
keywords: "セルの結合, Aspose.Cells, Cloud API, Excel"
description: "Aspose.Cells Cloud REST API を使用して Excelワークシートでセルを結合するガイド。cURL および SDK の使用例を含みます。"
ArticleTitle: "Excelワークシートでセルを結合する方法 – Aspose.Cells Cloud API (v3.0)"
---

Aspose.Cells Cloud REST API は、指定された行と列にまたがる矩形のセルブロックを1つのセルに結合します。

**事前条件**  
- 認証用の有効な JWT トークン  
- ワークブックが指定されたストレージフォルダ内に既に存在していること  
- Aspose.Cloud アカウントでストレージ設定（フォルダ名およびストレージ名）が行われていること  

## PostWorksheetMerge API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/merge
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を必要とします。

### リクエストパラメータ

| 名前            | 型      | 位置   | 説明                                      |
|-----------------|---------|--------|-------------------------------------------|
| name            | string  | path   | ワークブック名                             |
| sheetName       | string  | path   | ワークシート名                             |
| startRow        | integer | query  | 最初の行の 0 から始まるインデックス（0 = 最初の行） |
| startColumn     | integer | query  | 最初の列の 0 から始まるインデックス（0 = 最初の列） |
| totalRows       | integer | query  | 結合する行数                                |
| totalColumns    | integer | query  | 結合する列数                                |
| folder          | string  | query  | ワークブックを含むフォルダ                  |
| storageName     | string  | query  | ストレージ名                               |

*この操作にはリクエストボディは不要です。*

## **レスポンス**

CellsCloudResponse を返します。

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP ステータスコード**

| コード | 意味              | 説明                                      |
|--------|-------------------|-------------------------------------------|
| 200    | OK                | フィルターが正常に適用された。レスポンスには操作の詳細が含まれます。 |
| 400    | Bad Request       | 必須パラメータが欠落している、または無効です（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized      | JWT トークンが無効または欠落しています。 |
| 413    | Payload Too Large | アップロードされたファイルがサイズ制限を超えています。 |
| 500    | Internal Server Error | サーバーで予期せぬエラーが発生しました。 |

## SDK を使用した PostWorksheetMerge API の利用方法

### PostWorksheetMerge API の仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetMerge) はパブリックにアクセス可能なプログラミングインタフェースを定義し、Web ブラウザから直接 REST アクセスを実行できるようにします。

**cURL コマンドラインツール**を使用すると、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例では、cURL を使って Cloud API にリクエストを送信する方法を示します。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/merge?startRow=10&startColumn=10&totalRows=10&totalColumns=10" \
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

SDK を使用すると、開発を高速化できます。SDK が低レベルの詳細処理を担当するため、あなたはプロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全なリストについては、[GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご覧ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスにリクエストを送信する方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetMerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetMerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetMerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetMerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetMerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetMerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetMerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetMerge.go" >}}

{{< /tab >}}

{{< /tabs >}}
---