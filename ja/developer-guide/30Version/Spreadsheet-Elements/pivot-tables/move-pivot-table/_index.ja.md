---
title: "Excel ファイル内のピボットテーブルを移動する"
second_title: "Document"
linktitle: 移動
type: docs
url: /ja/pivot-tables/move/
aliases: [  /ja/move-pivot-table/ ]
keywords: "Aspose.Cells Cloud, ピボットテーブルの移動, Excel, REST API, SDK, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby, Swift"
description: "Aspose.Cells Cloud REST API を使用して、Excel ブック内でピボットテーブルを移動する方法を学びます。Android、C#、Go、Java、Node.js、Perl、PHP、Python、Ruby、Swift 向けの SDK が利用可能です。"
weight: 120
---

この REST API は、Excel ブック内でピボットテーブルを移動します。

**前提条件:** この操作を実行する前に、有効な JWT アクセストークンを取得し、ワークブックが Aspose Cloud ストレージに保存されている必要があります。必要に応じて `folder` および `storageName` パラメーターを指定してください。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotField/Move
```

### **リクエストパラメーター**

| パラメーター名      | 型      | 位置   | 説明                                      |
|-------------------|---------|--------|-------------------------------------------|
| name              | string  | path   | Excel ファイルの名前。                     |
| sheetName         | string  | path   | ピボットテーブルを含むワークシートの名前。 |
| pivotTableIndex   | integer | path   | 移動対象のピボットテーブルの 0 から始まるインデックス。 |
| fieldIndex        | integer | query  | 移動するピボットフィールドのインデックス。 |
| from              | string  | query  | フィールドの元のエリア（例: `Row` または `Column`）。 |
| to                | string  | query  | フィールドの移動先エリア（例: `Row` または `Column`）。 |
| folder            | string  | query  | ファイルが配置されているストレージ内のフォルダー。 |
| storageName       | string  | query  | ストレージサービスの名前。                 |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableFieldMoveTo) は、公開されているプログラミングインターフェースを定義しており、ウェブブラウザーから直接 REST のやり取りを実行できます。

cURL コマンドラインツールを使用すると、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用して Cloud API にアクセスする方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/pivottables/0/PivotField/Move?fieldIndex=0&from=C1&to=C10" \
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

## Cloud SDK ファミリー

SDK を使用すると、開発を最適化できます。SDK が低レベルの詳細処理を担当するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全なリストは [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスにアクセスする方法を示しています。

{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// 本番環境では HTTPS エンドポイントを使用してください。
public void Run_PivotTable_Move()
{
    url = @"https://api.aspose.com/v3.0/storage/file/Temp/V17.02.00_01.xlsx";
    using (HttpWebResponse response = _helper.CallDelete(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = @"https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = @"https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = @"https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/Sheet2?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = @"https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/importdata?folder=Temp";
    data = "{ \"BatchData\":[{\"rowIndex\":0,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Sport\",\"style\":null}, ... ],\"DestinationWorksheet\":\"Sheet2\",\"IsInsert\":false}";
    using (HttpWebResponse response = _helper.CallPost(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = "https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables?folder=Temp";
    data = "{\"Name\":\"TestPivot\",\"SourceData\":\"=Sheet2!A1:E8\",\"DestCellName\":\"C1\",\"UseSameSource\":true,\"PivotFieldRows\":[0,1],\"PivotFieldColumns\":[2],\"PivotFieldData\":[3,4]}";
    using (HttpWebResponse response = _helper.CallPut(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = "https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/Move?row=10&column=10&folder=Temp";
    using (HttpWebResponse response = _helper.CallPost(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = "https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/PivotField/Move?fieldIndex=1&from=Row&to=Column&folder=Temp";
    using (HttpWebResponse response = _helper.CallPost(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "60360c7d035abd1b2c9e36c68c9f00fb" >}}

{{< /tab >}}

{{< /tabs >}}