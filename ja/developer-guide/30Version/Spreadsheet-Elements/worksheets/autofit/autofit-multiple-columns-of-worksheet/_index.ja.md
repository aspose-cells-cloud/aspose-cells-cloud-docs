---
title: "Excelワークシートの複数列を自動調整する"
second_title: "Document"
linktitle: "Columns"
type: docs
url: /worksheets/autofit/columns/
aliases: [/autofit-multiple-columns-of-worksheet/]
keywords: "Aspose.Cells, カラムの自動調整, Excel API, クラウド表計算, REST"
description: "Aspose.Cells Cloud REST API（v3.0）を使用してExcelワークシートの複数列を自動調整する方法を学びます。エンドポイント、パラメータ、cURLの使用例、エラーハンドリング、C#、Java、PythonなどのSDKコードスニペットを含みます。"
weight: 20
---

このREST APIは、Excelワークシート上の**複数列**を自動調整します。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitcolumns
```

### **リクエストパラメータ**

| パラメータ名          | 型       | 位置   | 説明                                                                                                                                     |
| --------------------- | -------- | ------ | ---------------------------------------------------------------------------------------------------------------------------------------- |
| name                  | string   | path   | ファイル名。                                                                                                                             |
| sheetName             | string   | path   | ワークシート名。                                                                                                                         |
| firstColumn           | integer  | query  | 開始列インデックス。                                                                                                                     |
| lastColumn            | integer  | query  | 終了列インデックス。                                                                                                                     |
| autoFitterOptions\*   | object   | body   | 自動調整オプション（[Auto Fitter Options](/cells/auto-fitter-options/)を参照）。`AutoFitMergedCells`、`IgnoreHidden`、`OnlyAuto`を含みます。 |
| firstRow              | integer  | query  | 自動調整対象の開始行インデックス（**オプション**）。                                                                                     |
| lastRow               | integer  | query  | 自動調整対象の終了行インデックス（**オプション**）。                                                                                     |
| folder                | string   | query  | ストレージ内のフォルダパス（**オプション**）。                                                                                           |
| storageName           | string   | query  | ストレージ名（**オプション**）。                                                                                                         |

\*パラメータ名は関連ドキュメントへのリンクとして表示されます。

[OpenAPI仕様](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetColumns)は、公開可能なプログラミングインターフェースを定義し、Webブラウザから直接RESTによる連携を可能にします。

cURLコマンドラインツールを使用すると、Aspose.Cells Webサービスに簡単にアクセスできます。以下の例では、cURLを使用してクラウドAPIへリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitcolumns?lastColumn=5&firstColumn=0" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"AutoFitMergedCells": true, "IgnoreHidden": true, "OnlyAuto": true}'
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

## クラウドSDKファミリー

SDKを使用するのが開発を高速化する最良の方法です。SDKが低レベルの詳細処理を担当するため、開発者はプロジェクトのタスクに集中できます。Aspose.Cells Cloud SDKの完全な一覧は[GitHubリポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例では、さまざまなSDKを使用してAspose.Cells Webサービスへリクエストを送信する方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}