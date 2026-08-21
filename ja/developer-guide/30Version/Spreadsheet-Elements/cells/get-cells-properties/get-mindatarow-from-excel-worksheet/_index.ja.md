---
title: "ExcelワークシートからMinDataRowを取得する"
type: docs
url: /get-mindatarow-from-excel-worksheet/
weight: 90
keywords: "Aspose Cells, MinDataRow, Excel API, Cloud SDK"
description: "Aspose.Cells Cloud API v3.0 を使用してワークシートの最小データ行インデックスを取得します。リクエスト形式、パラメータ、サンプル cURL、レスポンス例、ステータスコード、および SDK スニペットを含みます。"
ArticleTitle: "ExcelワークシートからMinDataRowを取得する – Aspose.Cells Cloud API"
---

**Aspose.Cells Cloud API v3.0** の **Get MinDataRow** エンドポイントは、指定されたワークシート内にデータが含まれる最初の行のインデックスを返します。この操作には、有効なアクセス トークン（ベアラー認証）と、クエリパラメータ `cellOrMethodName` を `mindatarow` に設定する必要があります。

**APIバージョン: 3.0**

### cURLの例

このリクエストは HTTP GET メソッドを使用します。プレースホルダー `{fileName}` および `{sheetName}` を実際のワークブック名およびワークシート名に置き換えてください。

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/cells/mindatarow?cellOrMethodName=mindatarow" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

**リクエストパラメータ**

| パラメータ           | 位置     | 型     | 必須   | 説明                                           |
|---------------------|----------|--------|--------|------------------------------------------------|
| `fileName`          | Path     | string | はい    | Excelワークブックの名前（拡張子を含む）。       |
| `sheetName`         | Path     | string | はい    | ワークブック内のワークシートの名前。            |
| `cellOrMethodName`  | Query    | string | はい    | この操作を実行するには `mindatarow` を指定する必要があります。 |

**レスポンス例**

```json
{
  "MinDataRow": 5
}
```

**HTTPステータスコード**

| コード | 意味                     | 説明                                      |
|--------|--------------------------|-------------------------------------------|
| 200    | OK                       | フィルターが正常に適用され、レスポンスに操作の詳細が含まれます。 |
| 400    | Bad Request              | パラメータが不足している、または無効です（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized             | JWT トークンが無効または不足しています。 |
| 413    | Payload Too Large        | アップロードされたファイルがサイズ制限を超えています。 |
| 500    | Internal Server Error    | 予期しないサーバーエラーが発生しました。 |

### SDKの例

SDK を使用すると、開発を最速で進めることができます。SDK が低レベルの詳細を処理するため、プロジェクトのロジックに集中できます。Aspose.Cells Cloud SDK の完全なリストについては、<a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener">GitHubリポジトリ</a>をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinDataRowWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinDataRowWorksheet-get-min-data-row.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinDataRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_data_row.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinDataRowFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinDataRowWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinDataRowWorksheet-get-min-data-row.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinDataRowWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "85f2a886ba296b8abf640c0638b4eec1" >}}

{{< /tab >}}

{{< /tabs >}}

**関連項目**

- [Get MaxDataRow](https://docs.aspose.cloud/cells/get-maxdatarow-from-excel-worksheet/)
- [Get MinColumn](https://docs.aspose.cloud/cells/get-mincolumn-from-excel-worksheet/)
- [Get MaxColumn](https://docs.aspose.cloud/cells/get-maxcolumn-from-excel-worksheet/)
---