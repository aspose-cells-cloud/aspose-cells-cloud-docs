---
title: "Excelワークシート上の行をグループ化する"
second_title: "Document"
linktitle: "Group"
type: docs
url: /ja/rows/group/
aliases: [  /ja/group-rows-in-excel-worksheet/ ]
keywords: "行のグループ化, Excel, Aspose.Cells Cloud, REST API, SDK, ワークシート, Excel API"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークシート上の行をグループ化します。複数の SDK（C#, Java, PHP, Ruby, Node.js, Python, Perl, Go）をサポートし、簡単な統合を実現します。"
weight: 60
ArticleTitle: "Aspose.Cells Cloud API を使用した Excel ワークシート上の行のグループ化"
---

この REST API は、Excel ワークシート上の行をグループ化します。

**前提条件:**  
- 有効な OAuth 2.0 アクセストークン（Bearer JWT）を `Authorization` ヘッダーに指定する必要があります。  
- リクエストを実行する前に、ワークブックが指定された `folder` 内の選択された `storageName`（またはデフォルトのストレージ）に既に存在している必要があります。

## PostGroupWorksheetRows API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/group
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を必須とします。

### **リクエストパラメーター**

| パラメーター名 | 型      | 位置   | 説明                                                                 |
|---------------|---------|--------|---------------------------------------------------------------------|
| name          | string  | path   | ワークブックファイルの名前。                                          |
| sheetName     | string  | path   | ワークシートの名前。                                                  |
| firstIndex    | integer | query  | グループ化する最初の行の 0 から始まるインデックス。                     |
| lastIndex     | integer | query  | グループ化する最後の行の 0 から始まるインデックス。                     |
| hide          | boolean | query  | グループ化された行を隠すかどうかを示します（`true` または `false`）。  |
| folder        | string  | query  | ワークブックを含むフォルダーのパス。                                  |
| storageName   | string  | query  | ワークブックが存在するストレージの名前。                              |

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/Cells/PostGroupWorksheetRows) はパブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザーから直接 REST アクセスを可能にします。

cURL コマンドラインツールを使用して Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例では、cURL を使用してクラウド API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/group?firstIndex=1&lastIndex=2&hide=true" \
-X POST \
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

**HTTP ステータスコード**

| コード | 意味                         | 説明                                              |
|--------|------------------------------|---------------------------------------------------|
| 200    | OK                           | フィルターが正常に適用されました。レスポンスには操作の詳細が含まれます。 |
| 400    | Bad Request                  | パラメーターが不足している、または無効です（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized                 | JWT トークンが無効または不足しています。              |
| 413    | Payload Too Large            | アップロードされたファイルがサイズ制限を超えています。 |
| 500    | Internal Server Error        | 予期しないサーバーエラーが発生しました。             |

一般的なエラーレスポンス:

- **400 Bad Request** – `firstIndex` および `lastIndex` が有効な整数であり、`firstIndex` ≤ `lastIndex` であることを確認してください。  
- **401 Unauthorized** – `Authorization` ヘッダーに有効な JWT トークンが含まれていることを確認してください。  
- **404 Not Found** – 指定された `folder` / `storageName` にワークブック（`name`）およびワークシート（`sheetName`）が存在することを確認してください。

{{< /tab >}}

{{< /tabs >}}

**関連項目:** [Excelワークシート上の行のグループ化解除](../rows/ungroup/ "Excelワークシート上の行のグループ化解除"), [Excelワークシート上の行の非表示](../rows/hide/ "Excelワークシート上の行の非表示"), [Excelワークシート上の行の表示](../rows/unhide/ "Excelワークシート上の行の表示")。

## Cloud SDK ファミリー

SDK を使用すると、開発スピードを最大限に引き上げることができます。SDK は低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全なリストは [GitHub リポジトリー](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostGroupWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostGroupWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostGroupWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostGroupWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostGroupWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostGroupWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostGroupWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostGroupWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}