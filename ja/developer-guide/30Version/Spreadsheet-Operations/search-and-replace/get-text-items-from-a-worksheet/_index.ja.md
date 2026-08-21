---
title: "Excelワークシートからテキスト項目を取得する"
second_title: "Document"
linktitle: "ワークシート内のテキスト項目を取得する"
type: docs
url: /worksheets/get-text-items/
aliases: [/get-text-items-from-a-worksheet/]
weight: 20
keywords: "Aspose.Cells, Cloud API, Excel, ワークシート, テキスト項目, REST"
description: "Aspose.Cells Cloud REST API を使用して、Excelファイル内の特定のワークシートからすべてのテキスト項目を取得します。cURL、SDKコード、認証手順、レスポンススキーマのサンプルを含みます。"
ArticleTitle: "Excelワークシートからテキスト項目を取得する"
---

## REST API

このREST APIは、Excelファイル内のワークシートのテキスト項目を読み取ります。

```
https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{worksheet}/textItems
```

### セキュリティと認証
Aspose.Cells Cloud API はセキュアであり、[JWT トークンベースの認証](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)が必要です。

### リクエストパラメータ


| パラメータ名 | 型     | 位置   | 必須 | 説明                               |
| ------------ | ------ | ------ | ---- | ----------------------------------- |
| name         | string | path   | はい  | ワークブックファイル名。           |
| sheetName    | string | path   | はい  | ワークシートの名前。               |
| folder       | string | query  | いいえ | ワークブックを含むフォルダへのパス。 |
| storageName  | string | query  | いいえ | Aspose Cloud ストレージの名前。     |

### **レスポンス**

```json
{
  "Status":"OK",
  "Code":200,
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "Text": "string"
      }
    ]
  }
}
```

**HTTP ステータスコード**

| コード | 意味                   | 説明                                             |
|------|------------------------|--------------------------------------------------|
| 200  | OK                     | フィルターの適用が成功しました。レスポンスには操作の詳細が含まれます。 |
| 400  | Bad Request            | パラメータが不足している、または無効です（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized           | JWT トークンが無効または不足しています。 |
| 413  | Payload Too Large      | アップロードされたファイルがサイズ制限を超えています。 |
| 500  | Internal Server Error  | 予期しないサーバーエラーが発生しました。 |

## SDK を使用した GetWorksheetTextItems API の利用方法

### GetWorksheetTextItems API 仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetTextItems){:target="_blank" rel="noopener noreferrer"} は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST のやり取りを実行できるようにします。

cURL コマンドラインツールを使用して、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例では、cURL を使用して Cloud API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/sheet1/textItems" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "Text": "string"
      }
    ]
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK の使用

SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにすることで、統合を簡素化します。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud){:target="_blank" rel="noopener noreferrer"} をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスにリクエストを送信する方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetTextItems.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetTextItems.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetTextItems.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetTextItems.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetTextItems.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetTextItems.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetTextItems.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetTextItems.go" >}}

{{< /tab >}}

{{< /tabs >}}

---