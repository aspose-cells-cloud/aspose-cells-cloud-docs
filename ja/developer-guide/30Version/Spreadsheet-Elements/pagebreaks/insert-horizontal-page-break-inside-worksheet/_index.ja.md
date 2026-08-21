---
title: "水平ページ区切りを追加する"
second_title: "Document"
linktitle: "水平ページ区切りを追加する"
type: docs
url: /page-breaks/add-horizontal-page-break/
aliases: [/insert-horizontal-page-break-inside-worksheet/]
keywords: "水平ページ区切り, Aspose.Cells Cloud, Excel API, REST, SDK, ワークシート, cURL"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークシートに水平ページ区切りを追加する方法を学びます。リクエストの詳細、cURL の例、複数のプログラミング言語用の SDK コードスニペットを含みます。"
weight: 30
ArticleTitle: "水平ページ区切りを追加する – Aspose.Cells Cloud API"
---

**Add Horizontal Page Break** API は、Excel ワークシート内に水平ページ区切りを挿入します。

**前提条件と認証**  
Aspose.Cells Cloud API へのすべての呼び出しには、有効な JWT トークンが必要です。認証ガイドに記載された OAuth 2.0 フローを通じてトークンを取得し、リクエストヘッダーに `Authorization: Bearer <jwt token>` として含めてください。対象のワークブックは、API がアクセス可能なストレージ場所（デフォルトストレージまたは指定したカスタムの `storageName`）に配置されている必要があります。

## PutHorizontalPageBreak API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメーター

| パラメーター名 | 型      | 位置   | 説明                                                                 |
| -------------- | ------- | ------ | --------------------------------------------------------------------- |
| name           | 文字列  | パス   | Excel ファイルの名前。                                               |
| sheetName      | 文字列  | パス   | 区切りを追加するワークシートの名前。                                 |
| cellname       | 文字列  | クエリ | ページ区切りの開始位置を示すセル参照（例：**A1**）。                 |
| row            | 整数    | クエリ | ページ区切りの 0 から始まる行インデックス。                          |
| column         | 整数    | クエリ | ページ区切りの 0 から始まる列インデックス。                          |
| startColumn    | 整数    | クエリ | 区切りを挿入する範囲の開始列。                                       |
| endColumn      | 整数    | クエリ | 区切りを挿入する範囲の終了列。                                       |
| folder         | 文字列  | クエリ | Excel ファイルが格納されているフォルダーのパス。                    |
| storageName    | 文字列  | クエリ | Aspose Cloud ストレージの名前。                                      |

<a href="https://apireference.aspose.cloud/cells/#/PageBreaks/PutHorizontalPageBreak" target="_blank" rel="noopener noreferrer">OpenAPI スペック</a>は、Web ブラウザーから直接 REST 操作を実行できるパブリックにアクセス可能なインターフェースを定義しています。

**cURL** コマンドラインツールを使用して、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例では、cURL を使用して API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
# 暗号化された通信を確保するため HTTPS を使用
curl -v "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/horizontalpagebreaks?row=18" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

JWT トークンが欠落している、または無効な場合のエラーレスポンスの例：

```json
{
  "Code": 401,
  "Status": "Unauthorized",
  "Message": "Invalid or missing JWT token."
}
```

**HTTP ステータスコード**

| コード | 意味                         | 説明                                          |
|------|-----------------------------|----------------------------------------------|
| 200  | OK                          | フィルターが正常に適用された。レスポンスには操作の詳細が含まれる。 |
| 400  | Bad Request                 | パラメーターが欠落または無効（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized                | 無効または欠落している JWT トークン。 |
| 413  | Payload Too Large           | アップロードされたファイルがサイズ制限を超過している。 |
| 500  | Internal Server Error       | 予期しないサーバーエラー。 |

関連する操作の詳細については、API ページ **[Get Horizontal Page Breaks](../get-horizontal-page-breaks/)** および **[Delete Horizontal Page Break](../delete-horizontal-page-break/)** を参照してください。

## Cloud SDK Family

SDK を使用すると、最も迅速に開発できます。SDK は低レベルの詳細を抽象化するため、プロジェクトに集中できます。Aspose.Cells Cloud SDK の完全なリストについては、<a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub リポジトリー</a>をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutHorizontalPageBreak.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutHorizontalPageBreak.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutHorizontalPageBreak.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutHorizontalPageBreak.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutHorizontalPageBreak.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutHorizontalPageBreak.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutHorizontalPageBreak.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutHorizontalPageBreak.go" >}}
{{< /tab >}}

{{< /tabs >}}