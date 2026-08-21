---
title: "Excel ブック内のテキストを置換する"
second_title: "ドキュメント"
linktitle: "ブック内を置換"
type: docs
url: /ja/workbook/replace-text/
aliases: [  /ja/replace-text-in-a-workbook/ ]
weight: 60
keywords: "Aspose.Cells Cloud, テキスト置換, Excel ブック, XLSX, ODS, REST API, スプレッドシート, SDK"
description: "Aspose.Cells Cloud REST API を使用して Excel (XLS, XLSX, XLSM, XLSB) および OpenDocument スプレッドシート (ODS) ブック内のテキストを置換します。cURL および幅広い SDK (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go など) を通じて利用可能です。"
---

この REST API は、Excel ブック内のテキストを置換します。

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/replaceText
```
### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名 | 型     | 位置   | 説明                                                 |
| ------------ | ------ | ------ | ----------------------------------------------------- |
| name         | string | path   | ブックファイルの名前。                               |
| sheetName    | string | path   | 置換が実行されるワークシートの名前。                 |
| oldValue     | string | query  | 置換されるテキスト。                                 |
| newValue     | string | query  | 古い値を置き換える新しいテキスト。                   |
| folder       | string | query  | ブックが格納されているフォルダのパス。               |
| storageName  | string | query  | ブックが存在するストレージサービスの名前。           |

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
        "Title": "表形式区切りテキスト形式としてダウンロード",
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

| コード | 意味             | 説明                                               |
|------|------------------|----------------------------------------------------|
| 200  | OK               | フィルターが正常に適用されました；レスポンスには操作の詳細が含まれます。 |
| 400  | Bad Request      | パラメータが不足しているか無効です（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized     | JWT トークンが無効または不足しています。             |
| 413  | Payload Too Large| アップロードされたファイルがサイズ制限を超えています。 |
| 500  | Internal Server Error | 予期しないサーバーエラーが発生しました。            |

## SDK を使用した PostReplace API の利用方法

### PostReplace API 仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetTextReplace) は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 操作を実行できるようにします。

cURL コマンドラインツールを使用して Aspose.Cells Web サービスを簡単に呼び出すことができます。以下の例は、cURL を使用してリクエストを行う方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/replaceText?oldValue=a&newValue=a12" -H "accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Matches": 26,
  "Workbook": {
    "link": {
      "Href": "/test.xlsx",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、この機能を最速で統合できます。SDK は低レベルの詳細を処理するため、ビジネスロジックに集中できます。Aspose.Cells Cloud SDK の完全なリストは [GitHub リポジトリ](https://github.com/aspose-cells-cloud) を参照してください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookTextReplace.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookTextReplace.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookTextReplace.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookTextReplace.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookTextReplace.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookTextReplace.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookTextReplace.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbookTextReplace.go" >}}

{{< /tab >}}

{{< /tabs >}}