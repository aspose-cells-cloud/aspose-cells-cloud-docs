---
title: "名前付き範囲に基づいてセルのデータを取得する"
second_title: "Document"
linktitle: "値"
type: docs
url: /ja/ranges/get/values/
aliases: [  /ja/get-cells-data-based-on-named-range/ ]
keywords: "Aspose.Cells, クラウド, REST API, Excel, 名前付き範囲, セル値, ワークシート"
description: "Aspose.Cells Cloud REST API を使用して、Excel ワークシート内の名前付き範囲からセル値を取得します。このサービスは、複数の SDK（C#、Java、PHP、Ruby、Node.js、Python、Perl、Go）を介して利用可能で、幅広い開発プラットフォームで動作します。"
weight: 20
ArticleTitle: "名前付き範囲に基づいてセルのデータを取得する – Aspose.Cells Cloud API"
---

**前提条件**

- 適切なスコープを持つ有効な JWT アクセストークン。
- ワークブックが Aspose Cloud ストレージ（または指定されたフォルダ）にアップロードされていること。
- デフォルト以外のストレージを使用する場合は、対象のストレージ名を指定すること。

この REST API は、名前付き範囲または行・列のインデックスで識別される範囲内のセルのリストを返します。

この操作により、開発者は Excel ワークシート内の特定の名前付き範囲に属するセルの値をプログラムで取得できます。`namedRange` 識別子または明示的な行・列のインデックスを指定することで、API はアドレス、行、列、値、データ型、書式情報などの詳細なセルリストを返します。このレスポンスは、データ駆動型アプリケーションの実行、レポートの生成、サーバーサイドでの追加計算などに利用できます。Aspose.Cells Cloud サービスは、SDK を通じて複数のプログラミング言語をサポートしており、開発プラットフォームにかかわらずシームレスな統合を実現します。HTTPS を使用することでデータの安全な送信が保証され、API は REST 原則に準拠しており、成功時およびエラー時に標準的な HTTP ステータスコードを返します。

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/value
```

### **リクエストパラメータ**

| パラメータ名 | 型      | 位置   | 説明                                                                                      |
|--------------|---------|--------|-------------------------------------------------------------------------------------------|
| name         | 文字列  | パス   | ワークブックのファイル名。                                                                |
| sheetName    | 文字列  | パス   | ワークブック内のワークシート名。                                                          |
| namedRange   | 文字列  | クエリ | 取得する名前付き範囲（例: `A1:B2` または `range_name1`）。                                 |
| firstRow     | 整数    | クエリ | 範囲の最初の行の 0 から始まるインデックス（`namedRange` を指定しない場合に使用）。          |
| firstColumn  | 整数    | クエリ | 範囲の最初の列の 0 から始まるインデックス（`namedRange` を指定しない場合に使用）。         |
| rowCount     | 整数    | クエリ | 範囲に含める行数。                                                                        |
| columnCount  | 整数    | クエリ | 範囲に含める列数。                                                                        |
| folder       | 文字列  | クエリ | ワークブックを含むフォルダ。                                                              |
| storageName  | 文字列  | クエリ | ワークブックが配置されているクラウドストレージの名前。                                   |

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/Ranges/GetWorksheetCellsRangeValue)は、パブリックに利用可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 通信を実行できるようにします。

cURL コマンドラインツールを使用すると、Aspose.Cells ウェブサービスを簡単に呼び出すことができます。以下の例では、名前付き範囲からセル値をリクエストする方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/value?namerange=data" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "CellsList": [
    {
      "Name": "B10",
      "Row": 9,
      "Column": 1,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "C10",
      "Row": 9,
      "Column": 2,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "D10",
      "Row": 9,
      "Column": 3,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "E10",
      "Row": 9,
      "Column": 4,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "F10",
      "Row": 9,
      "Column": 5,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "G10",
      "Row": 9,
      "Column": 6,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "H10",
      "Row": 9,
      "Column": 7,
      "Value": "a8",
      "Type": "IsString",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\">a8</Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    }
  ],
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**セキュリティ上の注意:** API を呼び出す際は、常に HTTPS を使用してください。このサービスはプレーン HTTP をサポートしておらず、HTTPS を使用することでリクエストが暗号化され、セキュリティのベストプラクティスに準拠します。

**HTTP ステータスコード**

| コード | 意味                         | 説明                                                      |
|--------|------------------------------|-----------------------------------------------------------|
| 200    | OK                           | フィルターが正常に適用された。レスポンスには操作の詳細が含まれる。 |
| 400    | Bad Request                  | パラメータが不足しているか、無効（例: サポートされていないファイル形式）。 |
| 401    | Unauthorized                 | JWT トークンが無効または不足している。                     |
| 413    | Payload Too Large            | アップロードされたファイルがサイズ制限を超えた。          |
| 500    | Internal Server Error        | サーバーで予期しないエラーが発生した。                    |

**エラーレスポンスの例（400 Bad Request）**

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "パラメータ 'namedRange' が不足しているか、無効です。"
}
```

> **ヒント:** API では、`firstRow` および `firstColumn` に 0 から始まるインデックスを使用します。たとえば、ワークシートの最初の行は `0` です。

## Cloud SDK Family

SDK を使用すると、開発を最も効率的に進めることができます。SDK は低レベルの詳細を抽象化し、ビジネスロジックの開発に集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) を参照してください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCellsRangeValue.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCellsRangeValue.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCellsRangeValue.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCellsRangeValue.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCellsRangeValue.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCellsRangeValue.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCellsRangeValue.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCellsRangeValue.go" >}}

{{< /tab >}}

{{< /tabs >}}