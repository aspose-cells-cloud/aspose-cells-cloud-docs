---
title: "Aspose.Cells Cloud Web API - スプレッドシートのテーブルデータをCSVファイルに変換する - 無料オンラインツール"
second_title: "ドキュメント"
ArticleTitle: "スプレッドシートのテーブルデータをCSVファイルに変換する方法：ステップ・バイ・ステップ・ガイド"
linktype: "Convert Table to CSV"
type: docs
url: /convert-table-to-csv/
keywords: "Aspose.Cells Cloud, テーブルからCSVへ, スプレッドシート変換, ExcelからCSVへ, API, REST, データエクスポート"
description: "Aspose.Cells Cloud APIを使用して、Excelスプレッドシートのテーブルを迅速にCSVファイルに変換します。"
weight: 100
---

ローカルのExcelファイルからCloud APIを使用してテーブルデータをCSVファイルにエクスポートします。

## **テーブルをCSVに変換するAPI**

### Web API

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/csv
```

### **セキュリティと認証**

Aspose.Cells Cloud APIは安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWTトークンベースの認証</a>が必要です。

```bash
-H "Authorization: Bearer {access_token}"
```

### **リクエストパラメータ**

| パラメータ名 | 型     | パス/クエリ文字列/HTTP本文 | 説明                                                                                                                             |
| ------------ | ------ | --------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet  | ファイル | FormData                    | スプレッドシートファイルをアップロードします。                                                                                                            |
| worksheet    | 文字列   | クエリ                      | スプレッドシート内のワークシート名。                                                                                               |
| tableName    | 文字列   | クエリ                      | 変換するテーブルの名前。                                                                                                      |
| outPath      | 文字列   | クエリ                      | （オプション）ブックが保存されるフォルダのパス。既定値はnull。                                                                  |
| outStorageName | 文字列 | クエリ                      | 出力ファイル用のストレージ名。                                                                                                |
| fontsLocation | 文字列 | クエリ                      | カスタムフォントを使用するためのパス。                                                                                                            |
| region       | 文字列   | クエリ                      | スプレッドシートの地域/言語設定（例: `en-US`, `fr-FR`）。数値の書式設定、日付の解析、ロケール固有の動作に影響を与えます。 |
| password     | 文字列   | クエリ                      | スプレッドシートファイルを開くためのパスワード。                                                                                              |

### **レスポンス**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**HTTPステータスコード**

| コード | 意味               | 説明                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | フィルターが正常に適用され、レスポンスに操作の詳細が含まれます。 |
| 400  | リクエストエラー     | パラメータが不足または無効（例: 未対応のファイル形式）。      |
| 401  | 認証エラー          | JWTトークンが無効または不足しています。                                     |
| 413  | ペイロードが大きすぎます     | アップロードされたファイルがサイズ制限を超えています。                                 |
| 500  | サーバー内部エラー | 予期しないサーバーエラーが発生しました。                                          |

## **Convert Table to CSV APIの使用例**

- **データベース移行**: ExcelテーブルをCSVに変換し、SQLデータベース（MySQL、PostgreSQL、SQL Server）へ一括インポート。
- **データウェアハウスへのロード**: ExcelベースのレポートテーブルをCSVに変換し、Snowflake、Redshift、BigQueryへロード。
- **バッチAPIペイロード**: ExcelテーブルデータをCSVに変換し、RESTサービスへ一括アップロード。
- **サービス間通信**: マイクロサービス間で軽量なデータ交換形式としてCSVを使用。
- **機械学習のデータ前処理**: Excelの特徴量テーブルをCSVに変換し、Python/Rの機械学習ライブラリへインポート。
- **統計分析**: 研究データのテーブルをCSVに変換し、SPSS、SAS、Stataへインポート。
- **コンテンツ移行**: 構造化されたコンテンツをExcelからCSV経由でCMSシステムへ移行。

## **なぜConvert Table to CSV APIを使用すべきなのか？**

- **開発者に優しい**: Aspose.Cells Cloudは複数の言語でSDKライブラリを提供しており、迅速な開発が可能で、豊富なドキュメントも備えています。カスタムソリューションを構築する場合と比べ、開発工数が大幅に削減されます。
- **コスト効率**: ワークブックを事前にアップロードせずにテーブルデータを変換できるため、ストレージ容量を節約し、コストを削減します。
- **書式を除いた純粋なデータ抽出**。
- **CSVはほぼすべてのシステムでサポートされています**：
  - データベース（すべての主要なRDBMS）
  - プログラミング言語（すべての言語でネイティブパーサーを搭載）
  - ビジネスインテリジェンスツール（Tableau、Power BI、Looker）
  - スプレッドシートソフトウェア（Excel、Google Sheets、LibreOffice）
  - コマンドラインツール（awk、sed、grep）

## **SDKを使用してConvert Table to CSV APIを利用する方法**

### Convert Table to CSV API仕様

[Convert Table to CSV API仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToCSV)はパブリックに利用可能なプログラミングインターフェースを提供し、Webブラウザから直接REST操作が可能です。
cURLコマンドラインツールを使用してAspose.Cells Webサービスに簡単にアクセスできます。以下の例では、cURLを使用してCloud APIを呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/csv?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.csv
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 encoded)",
  "contentType": "MIME type",
  "fileDownloadName": "optional file name"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDKの使用

SDKを使用すると、低レベルの詳細を抽象化してくれるため、最小限のコードでスプレッドシートのテーブルデータをCSVファイルに変換できます。Aspose.Cells Cloud SDKの完全なリストについては、[GitHubリポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例では、さまざまなSDKを使用してAspose.Cells Webサービスを呼び出す方法を示しています。
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToCSV.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToCSV.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToCSV.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToCSV.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToCSV.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToCSV.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToCSV.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToCSV.go" >}}
{{</tab>}}
{{< /tabs >}}