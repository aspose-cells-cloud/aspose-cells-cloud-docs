---
title: "Excelワークシートに色フィルターを追加する"
second_title: "Document"
linktype: "Add color filter"
type: docs
url: /autofilter/add-color-filter/
aliases: [/filter-a-list-using-a-color-filter/,/autofilter/add-a-color-filter/]
keywords: "Excel, 色フィルター, Aspose.Cells Cloud, REST API, 自動フィルター, JWT認証"
description: "Aspose.Cells Cloud API を使用して Excel ワークシートに色フィルターを適用する方法を学びます。エンドポイント、パラメーター、cURL の例、エラー処理、SDK サンプルを含みます。"
weight: 65
ArticleTitle: "Aspose.Cells Cloud API を使用して Excel ワークシートに色フィルターを追加する"
---

Aspose.Cells Cloud API を使用して Excel ワークシートに色フィルターを追加する方法を学びます。このガイドでは、必要なエンドポイント、パラメーター、認証の前提条件、cURL リクエストのサンプル、SDK の例、レスポンス処理について説明します。

この REST API は、Excel ワークシートに**色フィルター**を追加します。

## PutWorksheetColorFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/colorFilter
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベース認証</a>が必要です。

### リクエストパラメーター：

| パラメーター名 | 型      | 位置   | 説明                                                                 |
|----------------|---------|--------|-----------------------------------------------------------------------------|
| name           | 文字列  | path   | Excel ファイルの名前。                                                 |
| sheetName      | 文字列  | path   | フィルターを適用するデータを含むワークシートの名前。           |
| range          | 文字列  | query  | フィルターを適用するセル範囲（例: `A1:B10`）。            |
| fieldIndex     | 整数    | query  | 色フィルターを適用する列の 0 から始まるインデックス。       |
| colorFilter    | オブジェクト | body   | フィルター対象の前景色と背景色を定義する JSON オブジェクト。   |
| matchBlanks    | 真偽値  | query  | 空白セルを含む行をフィルター結果に含めるかどうか。   |
| refresh        | 真偽値  | query  | `true` の場合、フィルター適用後にワークシートを再計算します。           |
| folder         | 文字列  | query  | Excel ファイルが格納されているストレージ内のフォルダー。                      |
| storageName    | 文字列  | query  | ストレージサービスの名前（例: Aspose Cloud Storage）。              |

**`colorFilter` JSON スキーマ**

| プロパティ          | 型     | 説明                                                                    | 必須   |
|-------------------|--------|--------------------------------------------------------------------------------|----------|
| Pattern           | 文字列 | フィルターのパターン（例: `"Solid"`）。                                             | はい      |
| ForegroundColor   | オブジェクト | 前景色を定義します。`Color`、`ColorIndex`、`IsShapeColor`、`ThemeColor`、`Type` などのサブプロパティを含みます。 | いいえ |
| BackgroundColor   | オブジェクト | 背景色を定義します。`ForegroundColor` と同じサブプロパティを含みます。      | いいえ |

### **レスポンス**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP ステータスコード**

| コード | 意味                         | 説明                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | フィルターが正常に適用された。レスポンスには操作の詳細が含まれます。 |
| 400  | リクエストエラー            | パラメーターが不足している、または無効（例: 未対応のファイル形式）。 |
| 401  | 認証エラー                  | JWT トークンが無効または不足しています。 |
| 413  | ペイロードが大きすぎます    | アップロードされたファイルがサイズ制限を超えています。 |
| 500  | サーバー内部エラー          | 予期しないサーバーエラーが発生しました。 |

## SDK を使用した PutWorksheetColorFilter API の利用方法

### PutWorksheetColorFilter API の仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetColorFilter) は、パブリックに利用可能なプログラミングインターフェースを定義し、Web ブラウザーから直接 REST 通信を実行できます。

cURL コマンドラインツールを使用すると、Aspose.Cells の Web サービスに簡単にアクセスできます。以下の例は、cURL を使用して Cloud API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/colorFilter?range=A1%3AB1&fieldIndex=0" \
-X PUT \
-d "{ \"Pattern\": \"Solid\", \"ForegroundColor\": { \"Color\": { \"A\": 255, \"R\": 0, \"G\": 255, \"B\": 255 }, \"ColorIndex\": 0, \"IsShapeColor\": true, \"ThemeColor\": { \"ColorType\": \"Text2\", \"Tint\": 1 }, \"Type\": \"Automatic\" }, \"BackgroundColor\": { \"Color\": { \"A\": 255, \"R\": 0, \"G\": 255, \"B\": 255 }, \"ColorIndex\": 0, \"IsShapeColor\": true, \"ThemeColor\": { \"ColorType\": \"Text2\", \"Tint\": 0 }, \"Type\": \"Automatic\" }}" \
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

SDK を使用すると、開発を迅速に進めることができます。SDK は低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリー](https://github.com/aspose-cells-cloud) をご覧ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetColorFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetColorFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetColorFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetColorFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetColorFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetColorFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetColorFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetColorFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}

**関連項目:** [カスタムフィルターを追加する](https://docs.aspose.cloud/cells/autofilter/add-custom-filter/)、[日付フィルターを追加する](https://docs.aspose.cloud/cells/autofilter/add-date-filter/)、[自動フィルターを削除する](https://docs.aspose.cloud/cells/autofilter/remove-auto-filter/)。