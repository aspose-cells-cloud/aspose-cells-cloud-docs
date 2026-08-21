---
title: "Excelワークシート上のすべての図形を取得する"
second_title: "Document"
linktitle: "Get-all"
type: docs
url: /shapes/get-all/
aliases: [/get-all-shapes-inside-the-worksheet/]
keywords: "Aspose.Cells, Cloud API, Excel 図形, 図形の取得, REST, SDK"
description: "Aspose.Cells Cloud REST API を使用してワークシート内のすべての図形（チャート、画像、テキストボックスなど）を取得します。cURL の例、SDK のスニペット、認証手順、エラー処理を含みます。"
ArticleTitle: "Excelワークシート上のすべての図形を取得する"
weight: 10
---

この REST API は、Excelワークシート上のすべての図形を取得することを可能にします。

## セキュリティと認証
Aspose.Cells Cloud API は安全であり、[JWT トークンベースの認証](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)を必要とします。

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes
```

### リクエストパラメータ

| パラメータ名     | タイプ   | 位置   | 説明                                                                                       |
| ---------------- | -------- | ------ | ------------------------------------------------------------------------------------------ |
| **name**         | 文字列   | パス   | Excel ファイルの名前。                                                                     |
| **sheetName**    | 文字列   | パス   | ワークシートの名前。                                                                       |
| **folder**       | 文字列   | クエリ | 文書が格納されているフォルダ。                                                             |
| **storageName**  | 文字列   | クエリ | 使用するストレージサービスの名前。                                                         |
| **include**      | 文字列   | クエリ | `details` を設定すると図形の全プロパティを返します。それ以外の場合は `link` オブジェクトのみ返されます。 |

> **オプション**: ファイルがルートストレージに存在する場合、`folder`、`storageName`、`include` は省略可能です。

cURL コマンドラインツールを使用して Aspose.Cells ウェブサービスにアクセスできます。以下の例では、オプションのクエリパラメータを含むリクエストを示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes?folder=Samples&storageName=MyStorage" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Shapes": {
    "ShapeList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      },
      {
        "link": {
          "Href": "/1",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      },
      {
        "link": {
          "Href": "/2",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      },
      {
        "link": {
          "Href": "/3",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes",
      "Rel": "self",
      "Type": null,
      "Title": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### レスポンスフィールド

`Shapes` オブジェクトには `Shape` オブジェクトのリストが含まれます。各図形には以下のプロパティが含まれます（`include=details` フラグを使用した場合；それ以外の場合は `link` オブジェクトのみ返されます）。

| プロパティ   | タイプ   | 説明                                                     |
| ------------ | -------- | -------------------------------------------------------- |
| **Name**     | 文字列   | 図形に割り当てられた名前（例："Chart 1"）。              |
| **Type**     | 文字列   | 図形のタイプ（例：`Chart`、`Picture`、`TextBox`）。       |
| **Top**      | 数値     | ワークシート上端から図形までの距離（ポイント単位）。     |
| **Left**     | 数値     | ワークシート左端から図形までの距離（ポイント単位）。     |
| **Width**    | 数値     | 図形の幅（ポイント単位）。                               |
| **Height**   | 数値     | 図形の高さ（ポイント単位）。                             |
| **Link**     | オブジェクト | ハイパーリンク情報（`Href`、`Rel`、`Type`、`Title`）。  |

## エラー処理

| HTTP ステータス | 説明                                                 | サンプルのエラーボディ                                     |
| --------------- | ---------------------------------------------------- | ---------------------------------------------------------- |
| **400**         | 不正なリクエスト – 不正な形式のパラメータ。         | `{ "Code": 400, "Message": "Invalid parameter value." }`   |
| **401**         | 認証エラー – トークンの欠如または無効。             | `{ "Code": 401, "Message": "Access token is missing or invalid." }` |
| **404**         | 見つからない – ワークブックまたはワークシートが存在しない。 | `{ "Code": 404, "Message": "File or worksheet not found." }` |
| **500**         | サーバ内部エラー – 予期しない状態。                 | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

成功したリクエストは **HTTP 200** を返し、上記のレスポンス例のように `Shapes` オブジェクトを含みます。

この API は、JWT トークンごとに **1 分あたり 150 リクエスト** という制限を適用します。この制限を超えると、**HTTP 429** が返され、`Retry-After` ヘッダーにより再試行のタイミングが示されます。

## Cloud SDK Family

SDK を使用すると、開発を最適化できます。SDK は低レベルの詳細な処理を担当し、開発者はプロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetShapes.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetShapes.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetShapes.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetShapes.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetShapes.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetShapes.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetShapes.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetShapes.go" >}}

{{< /tab >}}

{{< /tabs >}}