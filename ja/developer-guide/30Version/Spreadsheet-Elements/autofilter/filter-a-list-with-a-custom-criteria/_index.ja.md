---
title: "Excelワークシートにカスタム基準を追加する"
second_title: "Document"
linktitle: "カスタムフィルターを追加"
type: docs
url: /autofilter/add-custom-filter/
aliases: [/filter-a-list-with-a-custom-criteria/,/autofilter/add-a-custom-filter/]
keywords: "Excel, カスタムフィルター, Aspose.Cells Cloud, REST API, 自動フィルター, ワークシート, カスタム基準"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークシートにカスタムフィルターを追加する方法を学びます。リクエストの詳細、cURL の例、および複数のプログラミング言語向けの SDK コードスニペットを含みます。"
weight: 65
ArticleTitle: "Excelワークシートにカスタム基準を追加する – Aspose.Cells Cloud API"
---

この REST API は、**カスタム基準**を使用してリストをフィルタリングします。

## PutWorksheetCustomFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/custom
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメーター

| パラメーター名   | 型      | 位置           | 説明                                                                 |
|----------------|---------|----------------|---------------------------------------------------------------------|
| name           | string  | path           | Excel ファイルの名前。                                              |
| sheetName      | string  | path           | フィルタリング対象のデータを含むワークシートの名前。                |
| range          | string  | query          | フィルターを適用するセル範囲（例：`A1:B1`）。                       |
| fieldIndex     | integer | query          | フィルターを適用する列の 0 から始まるインデックス。                 |
| operatorType1  | string  | query          | 最初の比較演算子（例：`LessOrEqual`, `Equal`）。                   |
| criteria1      | string  | query          | 最初のフィルター値または式。                                        |
| isAnd          | boolean | query          | `true` の場合、2 つの基準を **AND** で組み合わせます。それ以外の場合は **OR** です。 |
| operatorType2  | string  | query          | 2 番目の比較演算子（オプション）。                                  |
| criteria2      | string  | query          | 2 番目のフィルター値または式（オプション）。                        |
| matchBlanks    | boolean | query          | `true` の場合、空白セルがフィルタリング結果に含まれます。           |
| refresh        | boolean | query          | `true` の場合、フィルター適用後にワークシートを強制的に更新します。 |
| folder         | string  | query          | ファイルが配置されているストレージ内のフォルダーのパス。            |
| storageName    | string  | query          | ストレージサービスの名前。                                          |

### **レスポンス**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP ステータスコード**

| コード | 意味                         | 説明                                                   |
|------|----------------------------|--------------------------------------------------------|
| 200  | OK                         | フィルターが正常に適用された。レスポンスには操作の詳細が含まれます。 |
| 400  | Bad Request                | パラメーターが不足または無効（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized               | JWT トークンが無効または不足しています。               |
| 413  | Payload Too Large          | アップロードされたファイルがサイズ制限を超えています。 |
| 500  | Internal Server Error      | 予期しないサーバーエラーが発生しました。               |

## SDK を使用した PutWorksheetCustomFilter API の使用方法

### PutWorksheetCustomFilter API の仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetCustomFilter) はパブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザーから直接 REST アクセスを実行できるようにします。

**cURL** コマンドラインツールを使用すると、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/custom?range=A1:B1&fieldIndex=0&operatorType1=LessOrEqual&criteria1=1" \
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

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、開発を最速で行えます。SDK が低レベルの詳細を処理するため、プロジェクトのロジックに集中できます。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) を確認してください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetCustomFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetCustomFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetCustomFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetCustomFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetCustomFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetCustomFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetCustomFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetCustomFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}

標準フィルターまたは日付フィルターを追加するなど、その他の AutoFilter 操作については、AutoFilter セクション内の関連ドキュメントページをご覧ください。