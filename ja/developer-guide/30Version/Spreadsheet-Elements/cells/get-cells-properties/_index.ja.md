---
title: "セルのプロパティを取得する"
type: docs
url: /get-cells-properties/
weight: 130
keywords: "Aspose Cells Cloud、REST API、Excel、ワークシート、セルのプロパティ、セルのプロパティを取得"
description: "Aspose.Cells Cloud REST API を使用して、Excelワークシート内の特定のセルまたは定義済みセルメソッドのプロパティを取得する方法を学びます。"
---

この REST API は、Excel ファイル内の特定のセルを取得する方法を示します。

## REST API

```bash
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellOrMethodName}
```

## セキュリティと認証

Aspose.Cells Cloud API は安全であり、[JWT トークンベースの認証](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)が必要です。

### リクエストパラメータ

| パラメータ名         | 型     | 位置   | 説明                                                                                                                                                                                                 |
| -------------------- | ------ | ------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**             | 文字列 | パス   | Excel ドキュメントの名前。                                                                                                                                                                          |
| **sheetName**        | 文字列 | パス   | セルを含むワークシートの名前。                                                                                                                                                                      |
| **cellOrMethodName** | 文字列 | パス   | セル名または定義済みメソッド名（例: `firstcell`, `endcell`, `maxrow`, `maxdatarow`, `maxcolumn`, `maxdatacolumn`, `minrow`, `mindatarow`, `mincolumn`, `mindatacolumn`）。                             |
| **folder**           | 文字列 | クエリ | ドキュメントが格納されているフォルダ。                                                                                                                                                              |
| **storageName**      | 文字列 | クエリ | ストレージサービスの名前。                                                                                                                                                                          |

## **レスポンス**

CellResponse を返します。

- **レスポンスフィールド概要**

| フィールド         | 型      | 説明                                      |
| ----------------- | ------- | ----------------------------------------- |
| `Name`            | 文字列  | セルのアドレス（例: `F341`）。             |
| `Row`             | 整数    | 0 から始まる行インデックス。               |
| `Column`          | 整数    | 0 から始まる列インデックス。               |
| `Value`           | 文字列  | セルに表示される値。                       |
| `Type`            | 文字列  | セルのデータ型（例: `IsString`）。         |
| `Formula`         | 文字列  | セルに数式が含まれている場合の数式テキスト。 |
| `IsFormula`       | 真偽値  | セルに数式が含まれているかどうかを示します。 |
| `IsMerged`        | 真偽値  | セルが結合範囲の一部かどうかを示します。   |
| `IsArrayHeader`   | 真偽値  | セルが配列ヘッダーかどうかを示します。     |
| `IsInArray`       | 真偽値  | セルが配列に属しているかどうかを示します。 |
| `IsErrorValue`    | 真偽値  | セルにエラー値が含まれているかどうかを示します。 |
| `IsInTable`       | 真偽値  | セルがテーブル内にあるかどうかを示します。 |
| `IsStyleSet`      | 真偽値  | セルにスタイルが適用されているかどうかを示します。 |
| `HtmlString`      | 文字列  | セルの値の HTML エンコード表現。           |
| `Style.link`      | オブジェクト | スタイルリソースへのハイパーリンク。       |


```json
{
  "Status":"OK",
  "Code":200,
  "Cell":{
    "Name":"A1",
    "Row": 0,
    "Column":0,
    "Value": "Hello Aspose.Cells",
    "Type":"String",
    "Formula" : "",
    ...
  }
}
```

**HTTP ステータスコード**

| コード | 意味                         | 説明                                        |
| ------ | ---------------------------- | ------------------------------------------- |
| 200    | OK                           | フィルターが正常に適用され、レスポンスに操作の詳細が含まれます。 |
| 400    | Bad Request                  | パラメータが不足または無効（例: サポートされていないファイル形式）。 |
| 401    | Unauthorized                 | JWT トークンが無効または不足しています。     |
| 413    | Payload Too Large            | アップロードされたファイルがサイズ制限を超えています。 |
| 500    | Internal Server Error        | 予期しないサーバーエラーが発生しました。     |

## SDK を使用した GetWorksheetCell API の使い方

### GetWorksheetCell API 仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell) はパブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST アクセスを実行できるようにします。

cURL コマンドラインツールを使用して Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API にリクエストを行う方法を示しています。
{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3?client_id=YOUR_CLIENT_ID&client_secret=YOUR_CLIENT_SECRET" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Cell": {
    "Name": "A3",
    "Row": 2,
    "Column": 0,
    "Value": "Statistical",
    "Type": "IsString",
    "IsFormula": false,
    "IsMerged": false,
    "IsArrayHeader": false,
    "IsInArray": false,
    "IsErrorValue": false,
    "IsInTable": false,
    "IsStyleSet": false,
    "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\">Statistical</Font>",
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    },
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、開発を最も効率的に加速できます。SDK は低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCell.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCell.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCell.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCell.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCell.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCell.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCell.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCell.go" >}}

{{< /tab >}}

{{< /tabs >}}

### 特定のセルを取得する方法

- [ワークシートからセルデータを取得する](/cells/get-cell-data-from-a-worksheet/)
- [Excel ワークシートの最初のセルを取得する](/cells/get-first-cell-from-excel-worksheet/)
- [Excel ワークシートの最後のセルを取得する](/cells/get-last-cell-of-excel-worksheet/)
- [Excel ワークシートの MaxRow を取得する](/cells/get-maxrow-from-excel-worksheet/)
- [Excel ワークシートの MaxDataRow を取得する](/cells/get-maxdatarow-from-excel-worksheet/)
- [Excel ワークシートの MaxColumn を取得する](/cells/get-maxcolumn-from-excel-worksheet/)
- [Excel ワークシートの MaxDataColumn を取得する](/cells/get-maxdatacolumn-from-excel-worksheet/)
- [Excel ワークシートの MinRow を取得する](/cells/get-minrow-from-excel-worksheet/)
- [Excel ワークシートの MinDataRow を取得する](/cells/get-mindatarow-from-excel-worksheet/)
- [Excel ワークシートの MinColumn を取得する](/cells/get-mincolumn-from-excel-worksheet/)
- [Excel ワークシートの MinDataColumn を取得する](/cells/get-mindatacolumn-from-excel-worksheet/)