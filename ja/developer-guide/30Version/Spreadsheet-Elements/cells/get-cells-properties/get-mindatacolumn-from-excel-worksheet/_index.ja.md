---
title: "MinDataColumn の取得 – Aspose.Cells Cloud API リファレンス (v3.0)"
type: docs
url: /ja/get-mindatacolumn-from-excel-worksheet/
weight: 110
keywords: "Aspose.Cells Cloud, MinDataColumn, Excelワークシート, REST API, APIリファレンス, v3.0, データ列, クラウドAPI"
description: "Aspose.Cells Cloud REST API (v3.0) を使用して、Excelワークシート内のデータを含む最も左側の列を取得します。認証の詳細、リクエスト構文、JSONレスポンスの例、エラーコード、SDKスニペットを含みます。"
ArticleTitle: "MinDataColumn の取得 – Aspose.Cells Cloud API リファレンス (v3.0)"
---

**`mindatacolumn`** エンドポイントは、指定されたワークシート内に何らかのセルデータを含む最も左側の列の 0 から始まるインデックスを返します。  
つまり、実際にデータを保持している最初の列がどこかを教えてくれます。

> **定義** – `mindatacolumn`: ワークシート内でデータを含む最初の列のインデックス（0 から始まる）。

**前提条件**  
- 有効な OAuth2 アクセストークンが必要です。  
- Excel ファイルは Aspose Cloud ストレージにアップロードされている必要があります。

**リクエストパラメータ**

| パラメータ          | 型     | 必須 | 説明                                         |
|---------------------|--------|------|---------------------------------------------|
| `fileName`          | 文字列 | はい | クラウドストレージに保存されている Excel ファイルの名前。 |
| `sheetName`         | 文字列 | はい | 列インデックスを取得するワークシートの名前。 |
| `Authorization` (ヘッダー) | 文字列 | はい | OAuth2 認証用の Bearer トークン。 |

- **cURL の例**

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/mindatacolumn" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/mindatacolumn" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MinDataColumn": 2
}
```

{{< /tab >}}

{{< /tabs >}}

**HTTP ステータスコード**

| コード | 意味                         | 説明                                             |
|--------|------------------------------|--------------------------------------------------|
| 200    | OK                           | フィルターの適用に成功しました。レスポンスには操作の詳細が含まれます。 |
| 400    | Bad Request                  | パラメータが不足または無効です（例: サポートされていないファイル形式）。 |
| 401    | Unauthorized                 | JWT トークンが無効または不足しています。 |
| 413    | Payload Too Large            | アップロードされたファイルがサイズ制限を超えています。 |
| 500    | Internal Server Error        | 予期しないサーバーエラーが発生しました。 |
---

- Aspose.Cells Cloud SDK の使用

SDK を使用すると、開発を迅速に進めるのに最適です。SDK が低レベルの詳細を処理するため、プロジェクトのロジックに集中できます。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinDataColumnWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinDataColumnWorksheet-get-min-data-column.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinDataColumn.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_data_column.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinDataColumnFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinDataColumnWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinDataColumnWorksheet-get-min-data-column.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinDataColumnWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "48105eac1e6a64ad3ae4f269c32f3a88" >}}

{{< /tab >}}

{{< /tabs >}}