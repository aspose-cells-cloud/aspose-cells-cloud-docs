---
title: "ExcelワークシートからMinRowを取得する – Aspose.Cells Cloud APIリファレンス"
type: docs
url: /get-minrow-from-excel-worksheet/
weight: 80
keywords: "Aspose.Cells, GetMinRow, Excelワークシート, REST API, 最小行インデックス, クラウドSDK"
description: "Aspose.Cells Cloud REST API (v3.0) を使用してワークシートの最小行インデックスを取得する方法を学びます。認証を含む完全なcURLリクエスト、レスポンススキーマ、および複数の言語向けSDKのサンプルを含みます。"
ArticleTitle: "ExcelワークシートからMinRowを取得する – Aspose.Cells Cloud APIリファレンス"
---

このREST APIは、`cellOrMethodName`パラメータを`minrow`に設定した場合、Excelワークシート内の最小行インデックスを返します。このエンドポイントを使用して、指定されたワークシート内で最初の空でない行（0ベース）を特定できます。

- **cURLの例:**

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/minrow" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "MinRow": 0
}
```

{{< /tab >}}

{{< /tabs >}}

**リクエスト**

```
GET https://api.aspose.com/v3.0/cells/{fileName}/worksheets/{sheetName}/cells/minrow
```

| プロパティ名            | 型     | 必須 | 説明                                                |
|------------------------|--------|------|-----------------------------------------------------|
| `fileName`             | 文字列 | はい  | ワークブックのファイル名（例: `myWorkbook.xlsx`）。 |
| `sheetName`            | 文字列 | はい  | 対象ワークシート名（例: `Sheet1`）。                |
| `cellOrMethodName`     | 文字列 | はい  | 固定値 `minrow`。                                   |
| `folder`               | 文字列 | いいえ | クラウドストレージのフォルダーパス。                |
| `storageName`          | 文字列 | いいえ | 非デフォルトストレージを使用する場合のストレージ名。|

**レスポンス**

このサービスは、`MinRow`プロパティを含むJSONオブジェクトを返します。このプロパティは、最初の空でない行のインデックス（0ベース）を示します。

| HTTPステータスコード | 意味                                     |
|--------------------|------------------------------------------|
| 200                | 成功 – `MinRow`を含むJSONペイロード。    |
| 401                | 認証エラー – 無効または不足しているトークン。 |
| 404                | ワークブックまたはワークシートが見つかりません。 |
| 500                | サーバー内部エラー。                     |

`MinRow`の値は、シート内のデータの開始位置を素早く特定する必要がある場合に便利です。

- **Aspose.Cells Cloud SDKの使用**

SDKを使用すると、開発を最も迅速に行えます。SDKが低レベルの詳細を処理するため、プロジェクトのロジックに集中できます。Aspose.Cells Cloud SDKの完全な一覧については、<a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHubリポジトリ</a>をご確認ください。

以下のコード例は、さまざまなSDKを使用してAspose.Cells Webサービスを呼び出す方法を示しています：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinRowWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinRowWorksheet-get-min-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_row.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinRowFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinRowWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinRowWorksheet-get-min-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinRowWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "d9497c39cde5cecb6709ff5feb2ab2b8" >}}

{{< /tab >}}

{{< /tabs >}}