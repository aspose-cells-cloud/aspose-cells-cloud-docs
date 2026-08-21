---
title: "Excelワークシートに複数の行を追加する"
ArticleTitle: "Aspose.Cells Cloud API を使用して Excel ワークシートに複数の行を追加する"
second_title: "ドキュメント"
linktitle: "行"
type: docs
url: /ja/rows/add/rows/
keywords: "Aspose.Cells Cloud, 行の挿入, Excel ワークシート, REST API, SDK, 複数行の追加"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークシートに複数の行を挿入する方法を学びます。このガイドでは、エンドポイント、リクエストパラメータ、サンプルの cURL コマンド、および SDK の使用例をカバーしています。"
weight: 20
---

この REST API は、Excel ワークシートに複数の新しい行を追加します。

## PutInsertWorksheetRows API

```http
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### **リクエストパラメータ**

| パラメータ名      | 型      | 位置   | 説明                                                                  |
| ----------------- | ------- | ------ | --------------------------------------------------------------------- |
| name              | 文字列  | path   | ワークブック名。                                                      |
| sheetName         | 文字列  | path   | ワークシート名。                                                      |
| startrow          | 整数    | query  | 挿入する最初の行のインデックス（**0 始まり**）。                      |
| totalRows         | 整数    | query  | 挿入する行数。                                                        |
| updateReference   | 真偽値  | query  | 挿入後にセル参照を更新するかどうか（`true` または `false`）。        |
| folder            | 文字列  | query  | ドキュメントを含むフォルダ。                                          |
| storageName       | 文字列  | query  | ストレージ名。                                                        |

**前提条件**  
この操作を実行する前に、ワークブックが指定されたストレージ（またはフォルダ）に既に存在している必要があります。

**認証**  
API には有効な JWT トークンが必要です。cURL の例に示すように、`Authorization` ヘッダに含めてください。

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/Cells/PutInsertWorksheetRows) は、パブリックに利用可能なプログラミングインタフェースを定義し、ウェブブラウザから直接 REST のやり取りを実行できるようにしています。

cURL コマンドラインツールを使用することで、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例では、cURL を使用してクラウド API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=11&updateReference=true" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **注意:** この `PUT` 操作にはリクエストボディは不要です。クライアントライブラリがペイロードを強制する場合、空の JSON オブジェクト (`{}`) を送信できます。

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*考えられるレスポンスコード*  

- **200 OK** – 行が正常に挿入されました。  
- **400 Bad Request** – 無効なパラメータ（例：負の行インデックス）  
- **401 Unauthorized** – JWT トークンが欠落している、または無効です。  
- **404 Not Found** – 指定されたワークブックまたはワークシートが存在しません。  
- **500 Internal Server Error** – 予期しないサーバーエラーが発生しました。

{{< /tab >}}

{{< /tabs >}}

行に関するその他の操作については、関連ページ「**行の削除**」「**行の取得**」「**行のコピー**」を参照してください。

## Cloud SDK Family

SDK を使用すると、開発が最も迅速に行えます。SDK が低レベルの詳細な処理を担当するため、プロジェクトに集中できます。Aspose.Cells Cloud SDK の完全なリストは [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutInsertWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutInsertWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutInsertWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutInsertWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PutInsertWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutInsertWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutInsertWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutInsertWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}