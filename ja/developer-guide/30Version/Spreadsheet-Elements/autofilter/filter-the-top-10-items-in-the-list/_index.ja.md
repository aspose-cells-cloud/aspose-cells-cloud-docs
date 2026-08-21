---
title: "Excelワークシートに上位10件フィルターを追加する（Aspose.Cells Cloud）"
ArticleTitle: "Excelワークシートに上位10件フィルターを追加する – Aspose.Cells Cloud"
second_title: "ドキュメント"
linktitle: "上位10件フィルターの追加"
type: docs
url: /autofilter/add-top-10-filter/
aliases:
  [/filter-the-top-10-items-in-the-list/, /autofilter/add-a-top-10-filter/]
keywords: "Aspose.Cells, AutoFilter, 上位10件フィルター, Excel API"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークシートに上位10件の AutoFilter を適用する方法を学びます。エンドポイント、パラメーター、HTTPS cURL の使用例、認証の詳細、エラー処理、および C#、Java、Python などの SDK スニペットが含まれます。"
weight: 65
---

この REST API は、リスト内の**上位10件**のアイテムをフィルタリングします。

> **前提条件**  
> • Aspose.Cells Cloud の認証を使用して有効な JWT トークンを取得します。  
> • Excel ワークブックを Aspose Cloud ストレージにアップロードする（または、存在するストレージ/フォルダーを指定します）。  
> • フィルターを適用したいワークシート名とセル範囲を把握します。

## PutWorksheetFilterTop10 API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filterTop10
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を必要とします。

### リクエストパラメーター

| パラメーター名  | 型      | 位置     | 必須 | デフォルト | 説明                                                                 |
| --------------- | ------- | -------- | ---- | --------- | --------------------------------------------------------------------------- |
| **name**        | 文字列  | パス     | はい  | —         | Excel ファイルの名前。                                                 |
| **sheetName**   | 文字列  | パス     | はい  | —         | データを含むワークシートの名前。                           |
| **range**       | 文字列  | クエリ   | はい  | —         | フィルターを適用するセル範囲（例: `A1:B10`）。             |
| **fieldIndex**  | 整数    | クエリ   | はい  | —         | フィルターを適用する列の 0 から始まるインデックス。              |
| **isTop**       | 真偽値  | クエリ   | はい  | `true`  | 上位のアイテムをフィルタリングする場合は `true`、下位のアイテムの場合は `false`。                   |
| **isPercent**   | 真偽値  | クエリ   | いいえ | `false` | `itemCount` をパーセンテージとして扱う場合は `true`、絶対値として扱う場合は `false`。 |
| **itemCount**   | 整数    | クエリ   | いいえ | `10`    | フィルターに含めるアイテムの数。                                   |
| **matchBlanks** | 真偽値  | クエリ   | いいえ | `false` | フィルター結果に空白セルを含める場合は `true`。                        |
| **refresh**     | 真偽値  | クエリ   | いいえ | `false` | 適用後にフィルターを更新する場合は `true`。                             |
| **folder**      | 文字列  | クエリ   | いいえ | —         | Excel ファイルが存在するストレージ内のフォルダー。                      |
| **storageName** | 文字列  | クエリ   | いいえ | —         | Aspose Cloud ストレージの名前。                                       |

### **レスポンス**

```json
{
    "Status":"OK",
    "Code":200
}
```

**一般的なエラーレスポンス**

```json
{
    "Code":400,
    "Message":"Bad Request – missing or invalid parameters."
}
```

```json
{
    "Code":401,
    "Message":"Unauthorized – invalid or missing JWT token."
}
```

```json
{
    "Code":413,
    "Message":"Payload Too Large – uploaded file exceeds the allowed size."
}
```

```json
{
    "Code":500,
    "Message":"Internal Server Error – unexpected server condition."
}
```

**HTTP ステータスコード**

| コード | 意味                         | 説明                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | フィルターが正常に適用された。レスポンスには操作の詳細が含まれます。 |
| 400  | Bad Request                 | パラメーターが不足している、または無効（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized                | JWT トークンが無効、または不足しています。 |
| 413  | Payload Too Large           | アップロードされたファイルがサイズ制限を超えています。 |
| 500  | Internal Server Error       | 予期しないサーバーエラーが発生しました。 |

## SDK を使用して PutWorksheetFilterTop10 API を利用する方法

### PutWorksheetFilterTop10 API 仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetFilterTop10) は、パブリックにアクセス可能なプログラミングインタフェースを定義し、Web ブラウザーから直接 REST アクセスを実行できるようにします。

cURL コマンドラインツールを使用して Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用して API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filterTop10?range=A1:B10&fieldIndex=0&isTop=true&itemCount=10" \
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

SDK を使用すると、開発を最速で行えます。SDK が低レベルの詳細を処理するため、プロジェクトの本質的な作業に集中できます。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリー](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetFilterTop10.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetFilterTop10.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetFilterTop10.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetFilterTop10.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetFilterTop10.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetFilterTop10.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetFilterTop10.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetFilterTop10.go" >}}

{{< /tab >}}

{{< /tabs >}}
---