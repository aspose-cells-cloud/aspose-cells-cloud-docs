---
title: "Excelワークシートの行を自動調整する"
second_title: "Document"
linktype: "Row"
type: docs
url: /ja/worksheets/autofit/row/
aliases: [  /ja/autofit-single-row-of-worksheet/ ]
description: "Aspose.Cells Cloud REST API を使って Excel ワークシートの行を自動調整する方法を学びます。エンドポイント、パラメータ、認証、エラーハンドリング、cURL リクエスト、および SDK の例を含みます。"
keywords: "行の自動調整, Aspose.Cells Cloud, Excel API, REST, ワークシート, SDK, スプレッドシート, クラウド API"
weight: 30
ArticleTitle: "Aspose.Cells Cloud API を使用して Excel ワークシートの行を自動調整する"
---

この REST API は、Excel ワークシートの**行を自動調整**します。

## セキュリティと認証
Aspose.Cells Cloud API は安全であり、[JWT トークンベースの認証](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)が必要です。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitrow
```

### **リクエストパラメータ**

| パラメータ名      | 型      | 位置   | 説明                                                                                                                                                                                                 |
| ----------------- | ------- | ------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name              | 文字列  | path   | Excel ファイルの名前。                                                                                                                                                                              |
| sheetName         | 文字列  | path   | ワークシートの名前。                                                                                                                                                                                |
| rowIndex          | 整数    | query  | 自動調整する行の 0 から始まるインデックス。                                                                                                                                                         |
| firstColumn       | 整数    | query  | 操作に含める最初の列のインデックス。                                                                                                                                                                |
| lastColumn        | 整数    | query  | 操作に含める最後の列のインデックス。                                                                                                                                                                |
| autoFitterOptions | オブジェクト | body   | 自動調整の動作を制御するオブジェクト（例：マージされたセルや折り返し文字列を考慮するかどうかなど）。詳細は [AutoFitterOptions](/cells/auto-fitter-options){:rel="noopener" title="自動調整の動作を制御"} を参照してください。 |
| folder            | 文字列  | query  | ファイルが保存されているフォルダ。                                                                                                                                                                  |
| storageName       | 文字列  | query  | ストレージの名前。                                                                                                                                                                                  |

**`autoFitterOptions` の JSON ボディの例**

```json
{
  "IsMergedCells": true,
  "IsWrapped": false,
  "AutoFitMergedCells": true,
  "AutoFitWrappedCells": false
}
```

### エンティティ定義

| エンティティ            | 説明                                                                 |
| ----------------------- | -------------------------------------------------------------------- |
| `rowIndex`              | 対象となる行の 0 から始まるインデックス。                            |
| `firstColumn`           | 自動調整操作の開始列。                                               |
| `lastColumn`            | 自動調整操作の終了列。                                               |
| `autoFitterOptions`     | 行の自動調整方法に影響を与えるオプションの設定（マージされたセル、折り返し文字列など）。 |

[OpenAPI スペック](/cells/#/Worksheets/PostAutofitWorksheetRow) はパブリックに利用可能なプログラミング・インタフェースを定義し、Web ブラウザから直接 REST のやり取りを実行できるようにします。

cURL コマンドラインツールを使用すると、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使って API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitrow?rowIndex=2&firstColumn=1&lastColumn=10" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

| フィールド | 説明                                     |
| ---------- | ---------------------------------------- |
| Code       | `200` – リクエストが成功しました。       |
| Status     | `"OK"` – 行が正常に自動調整されました。 |

{{< /tab >}}

{{< /tabs >}}

## エラーハンドリング

API は標準的な HTTP ステータスコードを返します。このエンドポイントで発生する一般的なエラーレスポンスは以下の通りです。

| HTTP コード | ペイロードの例                                           | 意味                                                                 |
| ----------- | -------------------------------------------------------- | -------------------------------------------------------------------- |
| 400         | `{ "Code": 400, "Message": "Row index out of range." }`  | 指定された `rowIndex` はワークシート内に存在しません。               |
| 401         | `{ "Code": 401, "Message": "Invalid or expired token." }` | 認証に失敗しました。JWT トークンを確認し、HTTPS 経由でのリクエストであることを確認してください。 |
| 404         | `{ "Code": 404, "Message": "File not found." }`          | 指定された Excel ファイルまたはワークシートが見つかりません。        |
| 500         | `{ "Code": 500, "Message": "Internal server error." }`   | 予期せぬサーバー側の問題が発生しました。                              |

## クラウド SDK ファミリー

SDK を使用すると、開発が最も迅速になります。SDK は低レベルの詳細を抽象化し、ビジネスロジックに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud){:rel="noopener noreferrer"} を参照してください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetRow.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetRow.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetRow.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetRow.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2c4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetRow.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetRow.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetRow.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetRow.go" >}}
{{< /tab >}}

{{< /tabs >}}

**関連項目:** [列の自動調整](/worksheets/autofit/column/)、[複数行の自動調整](/worksheets/autofit/rows/)、[AutoFitterOptions](/cells/auto-fitter-options)。