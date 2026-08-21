---
title: "Excel ワークブック内のテキストを検索する"
second_title: "Document"
linktitle: "ワークブック内を検索"
type: docs
url: /ja/workbook/find-text/
aliases: [  /ja/find-text-in-a-workbook/ ]
weight: 30
keywords: "Aspose.Cells, テキスト検索, Excel API, ワークブック検索"
description: "Aspose.Cells Cloud API を使用して Excel ワークブック (XLSX、ODS) 内で**テキストを検索**する方法を学びます。cURL の例、SDK スニペット、レスポンススキーマを含みます。今すぐ始めましょう。"
ArticleTitle: "Aspose.Cells Cloud API を使用して Excel ワークブック内でテキストを検索する"
---

この REST API は、Excel ワークブック内でテキストを検索します。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/findText
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名 | 型     | 位置   | 説明                                      |
| ------------ | ------ | ------ | ----------------------------------------- |
| name         | string | path   | Excel ワークブックの名前。                |
| text         | string | query  | 検索するテキスト文字列。                  |
| folder       | string | query  | ワークブックが格納されているフォルダ（オプション）。 |
| storageName  | string | query  | ワークブックが存在するストレージの名前（オプション）。 |

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

| コード | 意味             | 説明                                           |
|--------|------------------|------------------------------------------------|
| 200    | OK               | フィルターが正常に適用された。レスポンスには操作の詳細が含まれます。 |
| 400    | Bad Request      | パラメータが不足しているか無効です（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized     | JWT トークンが無効または不足しています。       |
| 413    | Payload Too Large| アップロードされたファイルがサイズ制限を超えています。 |
| 500    | Internal Server Error | 予期しないサーバーエラーが発生しました。   |

## SDK を使用して PostWorkbooksTextSearch API を活用する方法

### PostWorkbooksTextSearch API 仕様

<a href="https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbooksTextSearch" target="_blank" rel="noopener noreferrer">OpenAPI 仕様</a>はパブリックにアクセス可能なプログラミングインタフェースを定義し、ウェブブラウザから直接 REST アクセスを実行できるようにします。

cURL コマンドラインツールを使用して Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例では、cURL を使用して API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/findText?text=a" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <your_access_token>"
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

### Aspose.Cells Cloud SDK を使用する

SDK を使用すると、開発が最も迅速に行えます。SDK が低レベルの詳細を処理するため、プロジェクトの本質的な作業に集中できます。Aspose.Cells Cloud SDK の完全な一覧は、<a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例では、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbooksTextSearch.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbooksTextSearch.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbooksTextSearch.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbooksTextSearch.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbooksTextSearch.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbooksTextSearch.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbooksTextSearch.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbooksTextSearch.go" >}}

{{< /tab >}}

{{< /tabs >}}
---