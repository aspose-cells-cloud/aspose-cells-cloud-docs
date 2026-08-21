---
title: "Excelワークシートの範囲データを並び替える"
second_title: "Document"
linktitle: "Sort"
type: docs
url: /ja/worksheets/sort-data/
aliases: [  /ja/sort-worksheet-data/ ]
keywords: "Aspose.Cells Cloud, Excel sort API, worksheet range sorting, REST API, dataSorter"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークシート内の特定の範囲を並び替えます。エンドポイント、必要なパラメータ、認証手順、エラー処理、SDK の使用例を含みます。"
weight: 20
---

REST API は、Excel ワークシート内の指定された範囲のデータを並び替えます。

## REST API

```shell
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/sort
```

### リクエストパラメータ

| パラメータ名 | 型     | 位置   | 必須 | 説明                                                              |
|------------|--------|--------|------|-------------------------------------------------------------------|
| name       | string | path   | はい  | ワークブック名。                                                   |
| sheetName  | string | path   | はい  | ワークシート名。                                                   |
| cellArea   | string | query  | はい  | 並び替え対象のセル範囲（例: `A5:A10`）。                              |
| dataSorter | object | body   | はい  | 並び替え設定を定義する JSON オブジェクト（下記スキーマ参照）。             |
| folder     | string | query  | いいえ | ワークブックが格納されているフォルダ。                               |
| storageName| string | query  | いいえ | ワークブックが存在するストレージの名前。                              |

**`dataSorter` オブジェクトのスキーマ** – リクエストボディには以下のプロパティを持つ JSON オブジェクトを含める必要があります：

- `CaseSensitive` （boolean、必須）– 大文字・小文字を区別して並び替えるかどうかを指定します。
- `HasHeaders` （boolean、必須）– 範囲にヘッダー行が含まれているかどうかを示します。
- `KeyList` （array、必須）– 並び替えキーのコレクション。各キー・オブジェクトには以下の要素があります：
  - `Key` （integer）– 0から始まる列のインデックス。
  - `SortOrder` （string）– `"ascending"` または `"descending"`。
- `SortLeftToRight` （boolean、必須）– `true` の場合、左から右へ並び替えます。それ以外の場合、上から下へ並び替えます。
- （任意）`CaseOrder`、`SortLeftToRight` など、OpenAPI 仕様に従って追加のプロパティを指定できます。

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetRangeSort) はパブリックに利用可能なプログラミング・インタフェースを定義し、Web ブラウザから直接 REST アクセスを実行できるようにします。

Aspose.Cells ウェブサービスに簡単にアクセスするには、cURL コマンドラインツールを使用できます。以下の例では、cURL を使って Cloud API にリクエストを送信する方法を示します。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```shell
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/sort?cellArea=A5:A10" \
  -X POST \
  -d '{"CaseSensitive":false,"HasHeaders":false,"KeyList":[{"Key":0,"SortOrder":"descending"}],"SortLeftToRight":false}' \
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

**エラー処理** – API は標準的な HTTP エラーコードを返すことがあります。一般的なレスポンス例は以下の通りです：

| HTTP ステータス | コード | メッセージ                                          |
|----------------|------|---------------------------------------------------|
| 400            | 400  | Bad request – パラメータが不足している、または無効です。           |
| 401            | 401  | Unauthorized – JWT トークンが無効またはありません。               |
| 404            | 404  | Not found – ワークブックまたはワークシートが存在しません。          |
| 500            | 500  | Internal server error.                            |

エラー発生時のレスポンスボディは `{ "Code": <status>, "Message": "<description>", "Status": "Error" }` の形式になります。

## Cloud SDK Family

SDK を使用すると、開発を最も迅速に行えます。SDK が低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご覧ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPostWorksheetRangeSort.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-SortWorksheetData-sort-worksheet-data.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PostWorksheetRangeSort-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-sort_worksheet_range-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SortWorkSheetData.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-SortWorksheetData-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-SortWorksheetData-sort-worksheet-data.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-SortWorksheetData-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "48dd9dae5e2188a64e2284bb12b9201b" >}}

{{< /tab >}}

{{< /tabs >}}