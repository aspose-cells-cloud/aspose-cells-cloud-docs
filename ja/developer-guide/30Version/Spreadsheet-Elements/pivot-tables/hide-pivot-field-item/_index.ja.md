---
title: "ピボットテーブル内のピボットフィールド項目を非表示にする"
second_title: "Document"
linktitle: Hide
type: docs
url: /ja/pivot-tables/hide-pivot-field-item/
aliases: [  /ja/hide-pivot-field-item/ ]
keywords: "Aspose.Cells, ピボットフィールド項目の非表示, PivotTable API, REST API, クラウドSDK"
description: "Aspose.Cells Cloud REST API を使用してピボットテーブル内のピボットフィールド項目を非表示にする方法を学びます。リクエストの詳細、cURL の使用例、および複数言語向けの SDK コードスニペットを含みます。"
weight: 110
ArticleTitle: "ピボットテーブルでピボットフィールド項目を非表示にする – Aspose.Cells Cloud API ガイド"
---

API を呼び出す前に、以下の条件を満たしていることを確認してください。

* 有効な **JWT アクセストークン**（Aspose Cloud の認証フローで取得可能）。  
* 対象となるワークブックが Aspose Cloud ストレージにアップロードされていること。  
* シートおよびピボットテーブルが既に作成されていること。

これらの前提条件を満たすことで、認証エラーや「リソースが見つかりません」という応答を回避できます。以下に、API を呼び出す前に必要なセットアップ手順を示します。

この REST API は、ピボットテーブル内のピボットフィールド項目を非表示にします。

## PostPivotTableFieldHideItem API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotField/Hide
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を必要とします。

### **リクエストパラメータ**

| パラメータ名      | 型     | 位置   | 説明                                                                                   |
| ----------------- | ------ | ------ | -------------------------------------------------------------------------------------- |
| name              | 文字列 | パス   | Excel ファイルの名前。                                                                 |
| sheetName         | 文字列 | パス   | ピボットテーブルを含むワークシート名。                                                 |
| pivotTableIndex   | 整数   | パス   | ワークシート内のピボットテーブルのインデックス。                                       |
| pivotFieldType    | 文字列 | クエリ | ピボットフィールドのタイプ（Row、Column、Page、Data など）。                            |
| fieldIndex        | 整数   | クエリ | 変更対象のピボットフィールドの 0 から始まるインデックス。                               |
| itemIndex         | 整数   | クエリ | 非表示にするフィールド内の特定の項目のインデックス。                                    |
| isHide            | 真偽値 | クエリ | 項目を非表示にする場合は **true**、表示する場合は **false** を設定します。               |
| needReCalculate   | 真偽値 | クエリ | 変更後にピボットテーブルを再計算するかどうかを示します。デフォルトは **false** です。    |
| folder            | 文字列 | クエリ | ワークブックが保存されているフォルダのパス。                                            |
| storageName       | 文字列 | クエリ | ストレージサービスの名前。                                                              |

**必要なクエリパラメータの簡単な目次**

- **pivotFieldType** – フィールドのタイプ（例：`Row`）。  
- **fieldIndex** – 変更するフィールドの 0 から始まるインデックス。  
- **itemIndex** – 非表示／表示する項目の 0 から始まるインデックス。  
- **isHide** – 非表示にする場合は `true`、表示する場合は `false`。  
- **needReCalculate** – オプション、デフォルトは `false`。

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableFieldHideItem) はパブリックに利用可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 経由で操作を実行可能にします。

cURL コマンドラインツールを使用すると、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例では、cURL を使用して API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="応答" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/pivottables/0/PivotField/Hide?pivotFieldType=Row&fieldIndex=0&itemIndex=1&isHide=true&needReCalculate=true" \
  -X POST \
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

**応答の詳細**

| ステータスコード | 説明                                                               |
| --------------- | ------------------------------------------------------------------ |
| 200             | 項目が正常に非表示になりました。                                  |
| 400             | リクエストエラー – パラメータが不足または無効です。               |
| 401             | 認証エラー – JWT トークンが無効または不足しています。               |
| 500             | サーバーエラー – 処理を完了できませんでした。                      |

**注意:** 指定した `fieldIndex` または `itemIndex` が範囲外の場合、API は **400 Bad Request** 応答を返します。

## クラウド SDK ファミリー

SDK を使用すると、API に対する開発が最も迅速になります。SDK は低レベルの詳細を処理するため、ビジネスロジックの開発に集中できます。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) を参照してください。

以下のコード例では、 various SDK を使用してピボットフィールド項目を非表示にする方法を示しています。

{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

```csharp
public void Run_PivotTable_NeedReCalculate()
{
    // ワークブックとワークシートの準備
    url = @"https://api.aspose.cloud/v3.0/storage/file/Temp/V17.02.00_01.xlsx";
    using (HttpWebResponse response = _helper.CallDelete(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // ワークブックのアップロード
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // ピボットテーブルを含むワークシートを作成
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // サンプルデータ用の 2 番目のワークシートを作成
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/Sheet2?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Sheet2 にサンプルデータをインポート
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/importdata?folder=Temp";
    data = "{ \"BatchData\":[{...}] }"; // 説明のため省略
    using (HttpWebResponse response = _helper.CallPost(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // PivotSheet にピボットテーブルを追加
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables?folder=Temp";
    data = "{\"Name\":\"TestPivot\",\"SourceData\":\"=Sheet2!A1:E8\",\"DestCellName\":\"C1\",\"UseSameSource\":true,\"PivotFieldRows\":[0,1],\"PivotFieldColumns\":[2],\"PivotFieldData\":[3,4]}";
    using (HttpWebResponse response = _helper.CallPut(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // 特定の行フィールド項目を非表示
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/PivotField/Hide?pivotFieldType=Row&fieldIndex=0&itemIndex=1&isHide=true&needReCalculate=true&folder=Temp";
    using (HttpWebResponse response = _helper.CallPost(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "a0bec26a8274b9f7cb514015843a214e" >}}

{{< /tab >}}

{{< /tabs >}}

**注意:** SDK の例では、認証（JWT トークン）が既に設定されており、ワークブックが指定されたストレージフォルダ内にあることを前提としています。ご使用の環境に合わせて `folder` および `storageName` パラメータを適宜調整してください。