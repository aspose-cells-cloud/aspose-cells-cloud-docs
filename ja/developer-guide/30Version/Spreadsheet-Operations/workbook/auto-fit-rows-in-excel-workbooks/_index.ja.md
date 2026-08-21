---
title: "Excel ワークブックの行を自動調整する"
second_title: "Document"
linktitle: "Rows"
type: docs
url: /ja/autofit-rows-on-an-excel-file/
aliases: [  /ja/auto-fit-rows-in-excel-workbooks/ , /ja/workbook/autofit/rows/ ]
keywords: "行の自動調整, Excel ワークブック, Aspose.Cells Cloud, REST API, 自動調整オプション"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークブック内の行の高さを自動的に調整する方法を学びます。エンドポイント、パラメータ、cURL の例、および C#、Java、Python など複数の言語向けの SDK スニペットを含みます。"
weight: 90
ArticleTitle: "Excel ワークブックの行を自動調整する – Aspose.Cells Cloud API"
---

**前提条件**  
API を呼び出す前に、Aspose 認証サービスから有効な Bearer JWT トークンを取得し、対象のワークブックがサポートされているストレージ場所（デフォルトストレージまたは設定済みのカスタムストレージ）に保存されていることを確認してください。

この REST API を使用すると、Excel ワークブック内の行を**自動調整**し、データの挿入または変更後に行の高さを自動的に調整できます。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/autofitrows
```

リクエストパラメータは以下の通りです：

| パラメータ名      | 型                | 位置   | 説明                                                                 |
| ----------------- | ----------------- | ------ | ------------------------------------------------------------------- |
| name              | string            | path   | ワークブックファイルの名前。                                        |
| autoFitterOptions | AutoFitterOptions | body   | 自動調整の動作を制御するオプション。                                |
| startRow          | integer           | query  | 自動調整対象の最初の行のインデックス。                              |
| endRow            | integer           | query  | 自動調整対象の最後の行のインデックス。                              |
| firstColumn       | integer           | query  | 自動調整時に考慮する最初の列のインデックス。                        |
| lastColumn        | integer           | query  | 自動調整時に考慮する最後の列のインデックス。                        |
| onlyAuto          | boolean           | query  | **true** の場合、AutoFit フラグが設定された行のみを処理します（デフォルトは **false**）。 |
| folder            | string            | query  | ワークブックが保存されているフォルダのパス。                        |
| storageName       | string            | query  | ストレージサービスの名前。                                          |

**AutoFitterOptions** は、自動調整操作の動作（例：`AutoFitMergedCells`、`IgnoreHidden`）を指定するオブジェクトです。

**HTTP ステータスコード**

| コード | 意味                 | 説明                                           |
|------|----------------------|------------------------------------------------|
| 200  | OK                   | フィルターが正常に適用された；レスポンスには操作の詳細が含まれます。 |
| 400  | Bad Request          | パラメータが不足しているか無効（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized         | JWT トークンが無効または不足している。         |
| 413  | Payload Too Large    | アップロードされたファイルがサイズ制限を超えています。 |
| 500  | Internal Server Error| サーバー側で予期せぬエラーが発生しました。     |

[OpenAPI 仕様書](https://apireference.aspose.cloud/cells/#/Workbook/PostAutofitWorkbookRows) はパブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST によるやり取りを実行できます。

cURL コマンドラインツールを使用して Aspose.Cells の Web サービスを呼び出すことができます。`<jwt token>` は、Aspose 認証サービスから取得した有効な Bearer JWT トークンに置き換えてください。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/autofitrows" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"AutoFitMergedCells":true, "IgnoreHidden":true}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*エラー応答の例（例：ワークブックが存在しない場合）：*

```json
{
  "Code": 404,
  "Status": "Not Found",
  "Message": "指定されたワークブック 'myWorkbook.xlsx' は存在しません。"
}
```

{{< /tab >}}

{{< /tabs >}}

**注意事項**  
- `AutoFitMergedCells` を **true** に設定すると、結合セルは単一のエンティティとして自動調整操作時に考慮されます。  
- `IgnoreHidden` を **true** に設定すると、非表示の行と列はスキップされ、その現在の寸法が保持されます。

## Cloud SDK Family

SDK を使用すると、開発速度が最も速くなります。SDK は低レベルの詳細を抽象化するため、プロジェクトに集中できます。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) を参照してください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorkbookRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorkbookRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorkbookRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorkbookRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorkbookRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorkbookRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorkbookRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorkbookRows.go" >}}

{{< /tab >}}

{{< /tabs >}}