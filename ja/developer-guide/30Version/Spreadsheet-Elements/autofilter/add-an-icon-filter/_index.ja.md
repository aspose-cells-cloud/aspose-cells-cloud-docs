---
title: "Excelワークシートにアイコンフィルターを追加する"
second_title: "Document"
linktype: "Add icon filter"
type: docs
url: /autofilter/add-icon-filter/
aliases: [/add-an-icon-filter/,/autofilter/add-an-icon-filter/]
keywords: "Aspose.Cells Cloud, Excel, アイコンフィルター, 自動フィルター, REST API"
description: "Aspose.Cells Cloud REST API を使用して Excelワークシートにアイコンフィルターを追加する方法を、リクエストの詳細、cURLの例、SDKコードサンプル、エラーハンドリングを交えて学びます。"
weight: 65
ArticleTitle: "Excelワークシートにアイコンフィルターを追加する – Aspose.Cells Cloud ドキュメント"
---

## REST API

この REST API は、**Aspose.Cells Cloud REST API** を使用して Excelワークシートに**アイコンフィルター**を追加します。

**背景:** アイコンフィルターは、セルの値に基づいて視覚的なアイコンセットを適用し、データのトレンドを素早く視覚的に分析できるようにします。一般的な使用例としては、業績指標の強調表示、ステータスインジケーターの表示、またはトライアングル（信号機）アイコンを直接ワークシート内に配置して値を分類などが挙げられます。

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/iconFilter
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全で、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ:

| パラメータ名     | 型      | 位置     | 説明 |
|------------------|---------|----------|------|
| name             | 文字列  | Path     | ワークブック名。 |
| sheetName        | 文字列  | Path     | ワークシート名。 |
| range            | 文字列  | Query    | フィルターを適用するセル範囲（例: `A1:B1`）。 |
| fieldIndex       | 整数    | Query    | フィルターの対象となる列の 0 から始まるインデックス。 |
| iconSetType      | 文字列  | Query    | 使用するアイコンセット。許可される値: `Arrows3`, `ArrowsGray3`, `Flags3`, `Signs3`, `Symbols3`, `Symbols32`, `TrafficLights31`, `TrafficLights32`, `Arrows4`, `ArrowsGray4`, `Rating4`, `RedToBlack4`, `TrafficLights4`, `Arrows5`, `ArrowsGray5`, `Quarters5`, `Rating5`, `Stars3`, `Boxes5`, `Triangles3`, `None`, `CustomSet`, `Smilies3`, `ColorSmilies3`。 |
| iconId           | 整数    | Query    | 選択したアイコンセット内での特定のアイコンの識別子。 |
| matchBlanks      | 真偽値  | Query    | 空白セルを含めるかどうか（`true` または `false`）。 |
| refresh          | 真偽値  | Query    | 適用後にフィルターを更新するかどうか（`true` または `false`）。 |
| folder           | 文字列  | Query    | 元のワークブックが格納されているフォルダー。 |
| storageName      | 文字列  | Query    | ワークブックが存在するストレージの名前。 |

### **レスポンス**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP ステータスコード**

| コード | 意味                     | 説明 |
|--------|--------------------------|------|
| 200    | OK                       | フィルターが正常に適用された。レスポンスには操作の詳細が含まれる。 |
| 400    | Bad Request              | パラメータが欠落または不正（例: 未対応のファイル形式）。 |
| 401    | Unauthorized             | JWT トークンが不正または欠落。 |
| 413    | Payload Too Large        | アップロードされたファイルがサイズ制限を超えた。 |
| 500    | Internal Server Error    | サーバー内部で予期せぬエラーが発生した。 |

## SDK を使用して PutWorksheetIconFilter API を利用する方法

### PutWorksheetIconFilter API スペック

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetIconFilter) は公開可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 通信を実行できます。

cURL コマンドラインツールを使用すると、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/iconFilter?range=A1:B1&fieldindex=0&iconsettype=ArrowsGray3&iconid=1" \
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

可能なレスポンスステータスコード:

| コード | 説明 |
|--------|------|
| 200    | フィルターが正常に適用された。 |
| 400    | 不正なリクエスト — パラメータが欠落または不正。 |
| 401    | 認証エラー — 無効または不足している認証トークン。 |
| 404    | ワークブック、ワークシート、または指定された範囲が見つからない。 |
| 500    | サーバー内部エラー。 |
{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK を使用する

SDK を使用すると、開発 speed を大きく向上させることができます。SDK が低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全なリストは [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetIconFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetIconFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetIconFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetIconFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetIconFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetIconFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetIconFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetIconFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}

その他の AutoFilter 機能については、**[色フィルターを追加](/autofilter/add-color-filter/)**、**[日付フィルターを追加](/autofilter/add-date-filter/)**、および**[自動フィルターをクリア](/autofilter/clear-autofilter/)** のドキュメントをご参照ください。