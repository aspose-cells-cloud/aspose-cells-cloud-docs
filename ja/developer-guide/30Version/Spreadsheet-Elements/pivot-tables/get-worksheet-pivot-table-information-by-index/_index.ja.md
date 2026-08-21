---
title: "Excelワークシート内のピボットテーブルを取得する"
second_title: "Document"
linktitle: Get
type: docs
url: /ja/pivot-tables/get/
aliases: [  /ja/get-worksheet-pivot-table-information-by-index/ ]
keywords: "Aspose.Cells, ピボットテーブル, Excel, REST API, ワークシートピボットテーブルの取得"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークシートからピボットテーブルを取得します。リクエスト構文、パラメーター、認証、レスポンススキーマ、エラーハンドリング、および SDK サンプルを含みます。"
weight: 10
ArticleTitle: "Excelワークシート内のピボットテーブルを取得する"
---

この REST API は、インデックスによってワークシートの **ピボットテーブル** 情報を取得します。

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を必要とします。

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivottableIndex}
```

### リクエストパラメーター

| パラメーター名      | 型      | 位置   | 説明                                                |
| ------------------- | ------- | ------ | ----------------------------------------------------- |
| **name**            | 文字列  | パス   | Excel ファイルの名前。                               |
| **sheetName**       | 文字列  | パス   | ピボットテーブルを含むワークシートの名前。           |
| **pivottableIndex** | 整数    | パス   | ワークシート内のピボットテーブルの 0 から始まるインデックス。 |
| **folder**          | 文字列  | クエリ | ドキュメントが保存されているフォルダー。             |
| **storageName**     | 文字列  | クエリ | Aspose Cloud ストレージの名前。                      |

**cURL** コマンドラインツールを使用して、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用して API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "PivotFilters": [
    {
      "AutoFilter": {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "FilterColumns": [
          {
            "FieldIndex": 0,
            "FilterType": "string",
            "MultipleFilters": {
              "MatchBlank": true,
              "MultipleFilterList": [{}]
            },
            "ColorFilter": {
              "FilterByFillColor": "string",
              "Pattern": "string",
              "Color": {
                "Color": {
                  "A": 0,
                  "R": 0,
                  "G": 0,
                  "B": 0
                },
                "ColorIndex": 0,
                "IsShapeColor": true,
                "ThemeColor": {
                  "ColorType": "string",
                  "Tint": 0
                },
                "Type": "string"
              },
              "ForegroundColorColor": {
                "Color": {
                  "A": 0,
                  "R": 0,
                  "G": 0,
                  "B": 0
                },
                "ColorIndex": 0,
                "IsShapeColor": true,
                "ThemeColor": {
                  "ColorType": "string",
                  "Tint": 0
                },
                "Type": "string"
              },
              "BackgroundColor": {
                "Color": {
                  "A": 0,
                  "R": 0,
                  "G": 0,
                  "B": 0
                },
                "ColorIndex": 0,
                "IsShapeColor": true,
                "ThemeColor": {
                  "ColorType": "string",
                  "Tint": 0
                },
                "Type": "string"
              }
            },
            "CustomFilters": [
              {
                "FilterOperatorType": "string"
              }
            ],
            "DynamicFilter": {
              "DynamicFilterType": "string"
            },
            "IconFilter": {
              "IconId": 0,
              "IconSetType": "string"
            },
            "Top10Filter": {
              "Criteria": "string",
              "IsPercent": true,
              "IsTop": true,
              "Items": 0
            },
            "VisibleDropdown": "string"
          }
        ],
        "Range": "string",
        "Sorter": {
          "CaseSensitive": true,
          "HasHeaders": true,
          "KeyList": [
            {
              "Key": 0,
              "SortOrder": "string",
              "CustomList": "string"
            }
          ],
          "SortLeftToRight": true
        }
      },
      "EvaluationOrder": 0,
      "FieldIndex": 0,
      "FilterType": "string",
      "MeasureFldIndex": 0,
      "MemberPropertyFieldIndex": 0,
      "Name": "string",
      "Value1": "string",
      "Value2": "string"
    }
  ]
}
```

**レスポンススキーマ**

| フィールド        | 型      | 説明                                            |
|------------------|---------|-------------------------------------------------|
| Status           | 文字列  | 操作のステータステキスト（例: “OK”）。           |
| PivotFilters     | 配列    | ピボットフィルター定義のコレクション。          |
| └─ AutoFilter    | オブジェクト | ピボットに適用される自動フィルタリングの詳細。 |
|    └─ link       | オブジェクト | フィルターのハイパーリンク情報。               |
|    └─ FilterColumns | 配列 | 個々の列フィルター設定。                     |
|    └─ Range      | 文字列  | フィルターが適用されるセル範囲。                |
|    └─ Sorter     | オブジェクト | フィルター処理されたデータの並べ替え設定。     |
| （追加のネストされたフィールドは、上記のサンプル JSON と同様の構造を持ちます） |

{{< /tab >}}

{{< /tabs >}}

### エラーハンドリング

API は標準的な HTTP ステータスコードに従います。主なレスポンスは以下の通りです。

| ステータスコード | 意味                                                              | 例（エラー） JSON                                  |
| ---------------- | ----------------------------------------------------------------- | -------------------------------------------------- |
| 200              | 成功 – ピボットテーブルが返される                                | —                                                  |
| 401              | 認証エラー – 無効または不足しているトークン                      | `{"code":401,"message":"Invalid access token."}`  |
| 404              | 見つからない – ファイル、ワークシート、またはピボットテーブルインデックスが存在しない | `{"code":404,"message":"Pivot table not found."}` |
| 500              | サーバーエラー – 予期しない条件                                   | `{"code":500,"message":"Internal server error."}` |

**注意事項:** API は最大 150 MB の Excel ファイルをサポートし、Excel 2007～2021 形式で動作します。ワークシート名は大文字・小文字を区別することに注意してください。

## Cloud SDK ファミリー

SDK を使用すると、開発を最適化できます。SDK は低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリー](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Objective C" tabName8="Android" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-GetWorksheetPivotTableByIndex-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-GetWorksheetPivotInfoByIndex-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetWorksheetPivotTablesInformationByIndex.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-GetWorksheetPivotTableByIndex-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Examples-Android-pivottables-GetPivotTableIndexWorksheet-get-pivottable-index-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-GetWorksheetPivotTableByIndex-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3ff21d138764aa6b6fd51fbaab8cdb95" >}}

{{< /tab >}}

{{< /tabs >}}