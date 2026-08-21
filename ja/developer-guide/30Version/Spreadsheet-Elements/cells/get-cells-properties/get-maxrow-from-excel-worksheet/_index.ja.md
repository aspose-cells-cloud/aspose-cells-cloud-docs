---
title: "Excelワークシートから最大行番号を取得する"
type: docs
url: /ja/get-maxrow-from-excel-worksheet/
weight: 40
ArticleTitle: "Excelワークシートの最大行番号を取得する – Aspose.Cells Cloud API"
keywords: "Aspose.Cells, Excel, MaxRow, REST API, Cloud SDK, スプレッドシート, ワークシート, GetMaxRow"
description: "Aspose.Cells Cloud REST API を使用して、Excelファイル内のワークシートの最大行番号を取得する方法を学びます。リクエスト構文、レスポンススキーマ、SDKの使用例、および使用上の注意を含みます。"
---

この REST API は、`cellOrMethodName` パラメータを `maxrow` に設定した場合、Excelワークシートの**最大行番号**を返します。

- **cURL の例**

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/maxrow" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MaxRow": 1048576
}
```

{{< /tab >}}

{{< /tabs >}}

- **Aspose.Cells Cloud SDK の使用**

SDK を使用することは、開発を最適化する最も効率的な方法です。SDK は低レベルの詳細を処理し、プロジェクトのロジックに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMaxRowWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMaxRowWorksheet-get-max-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMaxRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_max_row.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMaxRowFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMaxRowWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMaxRowWorksheet-get-max-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMaxRowWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "afcfd72b172e9c3e2d283a9ac059c8c7" >}}

{{< /tab >}}

{{< /tabs >}}

**API リファレンス**

| 項目 | 詳細 |
|------|------|
| **メソッド** | `GET` |
| **エンドポイント** | `/cells/{fileName}/worksheets/{sheetName}/cells/maxrow` |
| **パスパラメータ** | `fileName` – Excel ファイル名（必須） <br> `sheetName` – ワークシート名（必須） |
| **クエリパラメータ** | `folder` – ストレージ内のフォルダパス（オプション） <br> `storageName` – ストレージ名（オプション） |
| **成功レスポンス** | `200 OK` <br> ```json { "MaxRow": integer } ``` |
| **エラーレスポンス** | `400 Bad Request` – 無効なパラメータ <br> `401 Unauthorized` – 認証失敗 <br> `404 Not Found` – ファイルまたはワークシートが見つからない |

**前提条件**

- 有効な Aspose Cloud 認証トークン。
- 対象のワークブックは Aspose Cloud ストレージにアップロードされているか、公開 URL でアクセス可能である必要があります。

**注意事項**

- この操作は API バージョン **v3.0** 以降で利用可能です。  
- 返される `MaxRow` 値は、使用されている最も高い行のインデックス（1始まり）に対応します。空白のワークシートの場合、通常は `1` が返されます。  

以下の SDK の例は、さまざまなプログラミング言語でこの操作を呼び出す方法を示しています。