---
title: "Excelワークシートの最終セルを取得する – Aspose.Cells Cloud API（v4.0）"
type: docs
url: /ja/get-last-cell-of-excel-worksheet/
weight: 30
keywords: "Aspose.Cells, Excel API, 最終セルの取得, スプレッドシート, クラウド"
description: "Aspose.Cells Cloud REST API v4.0 を使用して Excel ワークシートの最終セルのアドレスを取得します。リクエスト詳細、cURL の例、JSON 応答、および SDK サンプルを含みます。"
ArticleTitle: "Excelワークシートの最終セルを取得する – Aspose.Cells Cloud API v4.0"
---

この REST API は、`cellOrMethodName` パラメータを `endcell` に設定した場合、Excel ワークシートの**最終セル（endcell）**のアドレスを返します。

**概要**  
**最終セルの取得**操作は、指定されたワークシート内で最後に使用されたセルのアドレスを返します。ワークブック全体をスキャンすることなく、シートの実質的なデータ範囲を特定するのに便利です。

- **cURL の例**

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="応答" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/endcell" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Cell": {
    "Name": "F341",
    "Row": 340,
    "Column": 5,
    "Value": "<More Info>",
    "Type": "IsString",
    "Formula": "=HYPERLINK(SUBSTITUTE(HelpURLTemplate,\"xxxxxxxxxx\",[Help Topic]),\"<More Info>\")",
    "IsFormula": false,
    "IsMerged": false,
    "IsArrayHeader": false,
    "IsInArray": false,
    "IsErrorValue": false,
    "IsInTable": false,
    "IsStyleSet": false,
    "HtmlString": "<Font Style=\"TEXT-DECORATION: underline;FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\">&lt;More Info&gt;</Font>",
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### パラメータ
| パラメータ名         | 型     | 必須 | 説明 |
|----------------------|--------|------|------|
| `fileName`           | 文字列 | はい | クラウド上に保存されている Excel ファイルの名前。 |
| `worksheetName`      | 文字列 | はい | 最終セルを取得するワークシートの名前。 |
| `cellOrMethodName`   | 文字列 | はい | **`endcell`** を指定してこの操作を実行する必要があります。 |
| `folder` *(任意)*    | 文字列 | いいえ | ワークブックが存在するクラウドフォルダのパス。 |
| `storageName` *(任意)*| 文字列 | いいえ | ストレージの名前。省略した場合、デフォルトストレージが使用されます。 |

**HTTP ステータスコード**

| コード | 意味                         | 説明                                             |
|--------|------------------------------|--------------------------------------------------|
| 200    | OK                           | フィルターが正常に適用され、応答に操作の詳細が含まれます。 |
| 400    | Bad Request                  | パラメータが不足または無効です（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized                 | JWT トークンが無効または不足しています。 |
| 413    | Payload Too Large            | アップロードされたファイルがサイズ制限を超えています。 |
| 500    | Internal Server Error        | 予期せぬサーバーエラーが発生しました。 |

- **Aspose.Cells Cloud SDK の使用**

SDK を使用すると、開発を最適化できます。SDK が低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全なリストについては、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetLastCellWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetEndCellWorksheet-get-last-cell-excel-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetLastCell.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_last_cell.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetLastCellOfExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetLastCellWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetEndCellWorksheet-get-last-cell-excel-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

_近日公開予定。_

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetLastCellWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3cf3e145c223fd6f6f3d9f6377092db5" >}}

{{< /tab >}}

{{< /tabs >}}

セルのナビゲーションに関するその他の操作については、**[最初のセルを取得する](/ja/get-first-cell-of-excel-worksheet/)** および **[最大行を取得する](/ja/get-max-row-of-worksheet/)** のトピックをご参照ください。