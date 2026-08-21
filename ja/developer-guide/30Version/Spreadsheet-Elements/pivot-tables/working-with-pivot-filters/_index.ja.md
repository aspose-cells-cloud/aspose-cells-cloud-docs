---
title: "ピボットフィルターの使用"
second_title: "Document"
linktitle: フィルター
type: docs
url: /pivot-tables/add-filters/
aliases: [/working-with-pivot-filters/]
keywords: "Aspose.Cells, ピボットテーブル, フィルター, REST API, クラウド"
description: "Aspose.Cells Cloud REST API を使用してピボットテーブルフィルターの追加、取得、削除を行う方法を学びます。リクエスト構文、必要なパラメータ、cURL の使用例、C# および Go の SDK スニペットが含まれます。"
weight: 50
ArticleTitle: "ピボットフィルターの使用 – Aspose.Cells Cloud ドキュメント"
---

この REST API は、指定されたインデックスにあるピボットテーブルに**ピボットフィルター**を追加します。

**前提条件**  
このエンドポイントを呼び出す前に、以下の準備が必要です。

- 有効な OAuth/JWT アクセストークンを生成し、`Authorization` ヘッダーに含めてください。  
- 対象のワークブックが、アクセス可能なクラウドフォルダーに格納されていることを確認してください（`folder` を指定し、必要に応じて `storageName` も指定します）。  
- Aspose.Cells Cloud API バージョン 3.0 以降を使用してください。

## PutWorksheetPivotTableFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotFilters
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必須です。

### リクエストパラメータ

| パラメータ名        | 型      | 位置   | 説明                                                                                             |
| ------------------- | ------- | ------ | ------------------------------------------------------------------------------------------------- |
| **name**            | 文字列  | パス   | Excel ファイルの名前。                                                                            |
| **sheetName**       | 文字列  | パス   | ピボットテーブルを含むワークシート名。                                                            |
| **pivotTableIndex** | 整数    | パス   | フィルターを適用するピボットテーブルの 0 から始まるインデックス。                                 |
| **filter**          | オブジェクト | 本文   | フィルター設定を定義する JSON オブジェクト。詳細は以下の**フィルタースキーマ**テーブルを参照してください。 |
| **needReCalculate** | 真偽値  | クエリ | **true** の場合、フィルター追加後にワークブックを強制的に再計算します。既定値は **false** です。 |
| **folder**          | 文字列  | クエリ | ファイルが存在するクラウドストレージ上のフォルダー。                                              |
| **storageName**     | 文字列  | クエリ | クラウドストレージの名前。                                                                        |

**フィルタースキーマ**

| プロパティ                   | 型      | 説明                                                                                          |
| ---------------------------- | ------- | --------------------------------------------------------------------------------------------- |
| **AutoFilter**               | オブジェクト | AutoFilter の設定。使用しない場合は省略可能です。                                            |
| **EvaluationOrder**          | 整数    | フィルターの評価順序。                                                                        |
| **FieldIndex**               | 整数    | フィルターを適用するフィールドの 0 から始まるインデックス。                                   |
| **FilterType**               | 文字列  | フィルターの種類（例：`Value`、`Count`、`Label`）。                                            |
| **MeasureFldIndex**          | 整数    | 適用される場合、測定フィールドのインデックス。                                                |
| **MemberPropertyFieldIndex** | 整数    | 適用される場合、メンバー プロパティ フィールドのインデックス。                                |
| **Name**                     | 文字列  | フィルターの任意の名前。                                                                      |
| **Value1**                   | 文字列  | フィルターで使用される最初の値（例：範囲の下限）。                                            |
| **Value2**                   | 文字列  | フィルターで使用される 2 つ目の値（例：範囲の上限）。                                          |
| **CustomFilters**            | 配列    | カスタムフィルターオブジェクトのコレクション（各オブジェクトには `FilterOperatorType`、`Value1`、`Value2` が含まれます）。 |
| **DynamicFilter**            | オブジェクト | ダイナミックフィルターの設定（例：Top10、Bottom10）。                                         |
| **IconFilter**               | オブジェクト | アイコンベースのフィルターの設定。                                                             |
| **Top10Filter**              | オブジェクト | Top10/Bottom10 フィルターの設定。                                                             |
| **ColorFilter**              | オブジェクト | 色ベースのフィルターの設定。                                                                   |
| **Visibledropdown**          | 真偽値  | フィルターのドロップダウンが表示されるかどうかを示します。                                    |

> **注：** 上記のすべてのパラメータは、API リファレンスで明示的に「オプション」とされていない限り、必須です。

### 応答コード

| コード | 意味                                             |
| ------ | ------------------------------------------------ |
| 200    | フィルターが正常に追加されました。              |
| 400    | 不正なリクエスト—無効なパラメータ。             |
| 401    | 認証エラー—トークンが不足しているか無効です。    |
| 404    | 見つかりません—ワークブックまたはピボットテーブルが存在しません。 |
| 500    | サーバー内部エラー。                             |

**ベストプラクティス**  
- フィルターオブジェクトは可能な限り最小限に保ちます。大きなフィルター定義はリクエストの遅延を引き起こす可能性があります。  
- 呼び出しは冪等性があります—同じフィルターを 2 回追加しても重複は発生しません。  
- アカウントごとの API レート制限（1 分あたり 100 回のリクエスト）を守ってください。

*追加注意事項：*  
- フィルター定義の最大サイズは 1 MB です。それより大きなペイロードは 400 エラーで拒否されます。  
- `needReCalculate=true` を使用する場合、ワークブックが大きいと応答時間が長くなる可能性があります。

完全な OpenAPI 定義は以下から確認できます：  
[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/PivotTables/PutWorksheetPivotTableFilter)

### cURL リクエストの例

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/pivottables/0/PivotFilters?needReCalculate=true" \
  -X PUT \
  -d '{
        "AutoFilter": {
          "link": { "Href": "https://example.com", "Rel": "self", "Title": "AutoFilter Link", "Type": "application/json" },
          "FilterColumns": [
            {
              "FieldIndex": 0,
              "FilterType": "Value",
              "MultipleFilters": {
                "MatchBlank": true,
                "MultipleFilterList": [ { "Value": "example" } ]
              },
              "ColorFilter": {
                "FilterByFillColor": "FF0000",
                "Pattern": "Solid",
                "Color": {
                  "Color": { "A": 255, "R": 255, "G": 0, "B": 0 },
                  "ColorIndex": 3,
                  "IsShapeColor": false,
                  "ThemeColor": { "ColorType": "Accent1", "Tint": 0 },
                  "Type": "Rgb"
                },
                "ForegroundColorColor": null,
                "BackgroundColor": null
              },
              "CustomFilters": [ { "FilterOperatorType": "Equals", "Value1": "Example" } ],
              "DynamicFilter": { "DynamicFilterType": "Top10" },
              "IconFilter": { "IconId": 1, "IconSetType": "3Arrows" },
              "Top10Filter": { "Criteria": "Top", "IsPercent": true, "IsTop": true, "Items": 10 },
              "Visibledropdown": "true"
            }
          ],
          "Range": "A1:D100",
          "Sorter": {
            "CaseSensitive": false,
            "HasHeaders": true,
            "KeyList": [ { "Key": 0, "SortOrder": "Ascending", "CustomList": null } ],
            "SortLeftToRight": false
          }
        },
        "EvaluationOrder": 0,
        "FieldIndex": 0,
        "FilterType": "Value",
        "MeasureFldIndex": 0,
        "MemberPropertyFieldIndex": 0,
        "Name": "MyFilter",
        "Value1": "10",
        "Value2": "20"
      }' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

## Cloud SDK ファミリー

SDK を使用すると、Aspose.Cells Cloud への開発が最速で行えます。SDK は低レベルの詳細を処理し、ビジネスロジックの開発に集中できるようになります。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) を参照してください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using System;
using System.Threading.Tasks;
using Aspose.Cells.Cloud.Sdk.Api;
using Aspose.Cells.Cloud.Sdk.Model;

public class PivotFilterExample
{
    public static async Task AddPivotFilterAsync()
    {
        // API クライアントを初期化（資格情報を自身のものに置き換えてください）
        var config = new Configuration
        {
            ClientId = "YOUR_CLIENT_ID",
            ClientSecret = "YOUR_CLIENT_SECRET"
        };
        var apiInstance = new CellsApi(config);

        // フィルターオブジェクトを構築
        var filter = new PivotFilter
        {
            AutoFilter = null,
            EvaluationOrder = 0,
            FieldIndex = 1,
            FilterType = "Count"
        };

        // リクエストを準備
        var request = new PutWorksheetPivotTableFilterRequest(
            name: "Book1.xlsx",
            sheetName: "PivotSheet",
            pivotTableIndex: 0,
            filter: filter,
            needReCalculate: true,
            folder: "Temp",
            storageName: null);

        // リクエストを実行
        var response = await apiInstance.PutWorksheetPivotTableFilterAsync(request);
        Console.WriteLine($"Status: {response.Status}");
    }
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "2a2aa16c2d9fd7e46b1b19f5fea5842b" >}}

{{< /tab >}}

{{< /tabs >}}

ピボットテーブルに関連するその他の操作については、**追加**、**削除**、**クリア**フィルターのドキュメントをご覧ください。