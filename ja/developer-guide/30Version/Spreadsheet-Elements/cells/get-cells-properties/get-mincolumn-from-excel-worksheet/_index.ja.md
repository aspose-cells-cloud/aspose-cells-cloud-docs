---
title: "ExcelワークシートからMinColumnを取得する"
type: docs
url: /get-mincolumn-from-excel-worksheet/
weight: 100
keywords: Excel, Aspose.Cells Cloud, REST API, Get MinColumn, Worksheet, SDK, Cloud API
description: Aspose.Cells Cloud REST API を使用して、Excelファイルのワークシート内にデータを含む最小列インデックスを取得します。
ArticleTitle: "ExcelワークシートからMinColumnを取得する - Aspose.Cells Cloud API"
---

このREST APIは、`cellOrMethodName`パラメータを`mincolumn`に設定した場合、Excelワークシート内にデータを含む最小列インデックスを返します。

- **cURLの例**

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/mincolumn" \
     -H "Authorization: Bearer <YOUR_ACCESS_TOKEN>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MinColumn": 2
}
```

{{< /tab >}}

{{< /tabs >}}

**リクエストの詳細**

| パラメータ | 型 | 必須 | 説明 |
|-----------|------|----------|-------------|
| `cellOrMethodName` | 文字列 | はい | 操作を示す固定値 `mincolumn`。 |
| `folder` | 文字列 | いいえ | ワークブックを含むフォルダへのパス（ルートでない場合）。 |
| `storageName` | 文字列 | いいえ | 使用するAspose Cloudストレージの名前。 |

**レスポンスの詳細**

APIは、単一のプロパティを含むJSONオブジェクトを返します：

```json
{
  "MinColumn": 整数   // データを含む最も左側の列の0から始まるインデックス。
}
```

一般的なHTTPステータスコード：

- **200 OK** – リクエスト成功、`MinColumn`値を返します。  
- **401 Unauthorized** – 認証トークンが不足しているか、無効です。  
- **404 Not Found** – 指定されたワークブック、ワークシート、またはセル範囲が存在しません。  
- **500 Internal Server Error** – 予期しないサーバーエラー。

- **Aspose.Cells Cloud SDKの使用**

SDKを使用することが最も効率的な開発方法です。SDKは低レベルの詳細を抽象化し、プロジェクトのロジックに集中できるようにします。Aspose.Cells Cloud SDKの完全なリストについては、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHubリポジトリ</a>をご確認ください。

以下のコード例は、さまざまなSDKを使用してAspose.Cellsウェブサービスを呼び出す方法を示しています：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinColumnWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinColumnWorksheet-get-min-column-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinColumn.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_column.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinColumnFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinColumnWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinColumnWorksheet-get-min-column-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinColumnWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "108bf3803d41abd988a29cdbd39aee44" >}}

{{< /tab >}}

{{< /tabs >}}
---