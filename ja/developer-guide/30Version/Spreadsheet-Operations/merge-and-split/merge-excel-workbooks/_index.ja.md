---
title: "Excel ワークブックを別のワークブックにマージする"
second_title: "Document"
linktitle: "Excel ワークブックを別のワークブックにマージする"
type: docs
url: /merge-an-excel-file-into-the-excel-file/
aliases: [/merge-excel-workbooks/, /workbook/merge/]
keywords: "Excel マージ, Aspose.Cells Cloud, ワークブック API, REST API, スpreadsheet マージ, クラウド SDK, 認証, mergeWith, cURL サンプル"
description: "Aspose.Cells Cloud REST API (v3.0) を使って、1 つの Excel ワークブックを別のワークブックにマージするためのステップ・バイ・ステップ・ガイド。認証方法、必要な mergeWith パラメータ、cURL サンプル、および SDK のコードスニペットを含みます。"
ArticleTitle: "Aspose.Cells Cloud API を使って Excel ワークブックを別のワークブックにマージする"
weight: 50
---

## REST API

この REST API は、Excel の **ワークブック** を別のワークブックにマージします。

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/merge
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必須です。

### **クエリパラメータ**

| パラメータ名   | 型     | 説明                                                    |
| -------------- | ------ | ------------------------------------------------------- |
| folder         | string | 元のワークブックを含むフォルダ。                        |
| storageName    | string | ストレージの名前。                                      |
| **mergeWith**  | string | 対象のワークブックにマージされるワークブックの名前。    |

### **レスポンス**

```json
{
    "Status":"OK",
    "Code":200,
      "Workbook": {
    "FileName": "test.xlsx",
    "Links": [
      {
        "Href": "/test.xlsx",
        "Rel": "self",
        "Title": null,
        "Type": null
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "CSV としてダウンロード",
        "Type": "text/csv"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "HTML としてダウンロード",
        "Type": "text/html"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "ODS としてダウンロード",
        "Type": "application/vnd.oasis.opendocument.spreadsheet"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "PDF としてダウンロード",
        "Type": "application/pdf"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "テーブル区切りテキスト形式としてダウンロード",
        "Type": "text/plain"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "TIFF としてダウンロード",
        "Type": "image/tiff"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Microsoft Excel 2003 としてダウンロード",
        "Type": "application/vnd.ms-excel"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Microsoft Excel 2007 としてダウンロード",
        "Type": "application/vnd.openxmlformats-officedocument.spreadsheetml.sheet"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "XPS としてダウンロード",
        "Type": "application/vnd.ms-xpsdocument"
      }
    ],
    "Worksheets": {
      "link": {
        "Href": "/worksheets",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "DefaultStyle": {
      "link": {
        "Href": "/defaultstyle",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "DocumentProperties": {
      "link": {
        "Href": "/documentproperties",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "Names": {
      "link": {
        "Href": "/names",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "Settings": {
      "link": {
        "Href": "/settings",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "IsWriteProtected": "False",
    "IsProtected": "False",
    "IsEncryption": "false",
    "Password": null
  }
}
```

**HTTP ステータスコード**

| コード | 意味                   | 説明                                      |
|------|------------------------|-------------------------------------------|
| 200  | OK                     | フィルターが正常に適用された。レスポンスには操作の詳細が含まれる。 |
| 400  | Bad Request            | パラメータが欠落または不正（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized           | JWT トークンが不正または欠落している。    |
| 413  | Payload Too Large      | アップロードされたファイルがサイズ制限を超えた。 |
| 500  | Internal Server Error  | サーバーで予期せぬエラーが発生した。      |

## SDK を使用した PostWorkbooksMerge API の使い方

### PostWorkbooksMerge API 仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbooksMerge) は、パブリックにアクセス可能なプログラミングインターフェースを定義し、API がウェブブラウザから直接 REST アクセスを実行できるようにします。

**cURL** コマンドラインツールを使用して、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例では、cURL を使って Cloud API にリクエストを送信する方法と、必要な認証ヘッダーを示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
# test2.xlsx を test.xlsx にマージする
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/merge?mergeWith=test2.xlsx" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access-token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Workbook": {
    "FileName": "test.xlsx",
    "Links": [
      {
        "Href": "/test.xlsx",
        "Rel": "self",
        "Title": null,
        "Type": null
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "CSV としてダウンロード",
        "Type": "text/csv"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "HTML としてダウンロード",
        "Type": "text/html"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "ODS としてダウンロード",
        "Type": "application/vnd.oasis.opendocument.spreadsheet"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "PDF としてダウンロード",
        "Type": "application/pdf"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "テーブル区切りテキスト形式としてダウンロード",
        "Type": "text/plain"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "TIFF としてダウンロード",
        "Type": "image/tiff"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Microsoft Excel 2003 としてダウンロード",
        "Type": "application/vnd.ms-excel"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "Microsoft Excel 2007 としてダウンロード",
        "Type": "application/vnd.openxmlformats-officedocument.spreadsheetml.sheet"
      },
      {
        "Href": "/test.xlsx",
        "Rel": "alternate",
        "Title": "XPS としてダウンロード",
        "Type": "application/vnd.ms-xpsdocument"
      }
    ],
    "Worksheets": {
      "link": {
        "Href": "/worksheets",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "DefaultStyle": {
      "link": {
        "Href": "/defaultstyle",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "DocumentProperties": {
      "link": {
        "Href": "/documentproperties",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "Names": {
      "link": {
        "Href": "/names",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "Settings": {
      "link": {
        "Href": "/settings",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "IsWriteProtected": "False",
    "IsProtected": "False",
    "IsEncryption": "false",
    "Password": null
  },
  "Code": 200,
  "Status": "OK"
}
```

レスポンスはマージされたワークブックに関するメタデータを含む `Workbook` オブジェクトを返します。これには、さまざまな形式（CSV、PDF、HTML など）で結果をダウンロードするためのリンクが含まれます。

レスポンスヘッダー

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、開発を高速化できます。SDK は低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストについては、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使って Aspose.Cells Web サービスにリクエストを送信する方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbooksMerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbooksMerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbooksMerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbooksMerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbooksMerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbooksMerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbooksMerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbooksMerge.go" >}}

{{< /tab >}}

{{< /tabs >}}
---