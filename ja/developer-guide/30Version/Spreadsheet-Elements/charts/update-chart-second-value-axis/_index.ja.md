---
title: "チャートの第2値軸を更新する"
ArticleTitle: "チャートの第2値軸を更新する – Aspose.Cells Cloud REST API"
type: docs
url: /ja/charts/second-value-axis/update/
weight: 160
keywords: "Aspose.Cells, Chart API, 第2値軸, Excel, REST, Cloud SDK"
description: "Aspose.Cells Cloud REST API を使用して、Excelワークシート内のチャートの第2値軸を更新します。リクエストの例、レスポンスコード、および前提条件を含みます。"
---

この REST API は、チャートの第2値軸を更新します。

**前提条件:**  
- 有効な JWT アクセストークン（[認証ガイド](https://docs.aspose.cloud/cells/authentication/)を参照）。  
- 対象の Excel ファイルは Aspose Cloud ストレージ内に保存されていること（`folder` およびオプションで `storageName` を指定）。  
- API バージョン v3.0 を使用。ベース URL は `https://api.aspose.cloud/v3.0` であることを確認。

## PostChartSecondValueAxis API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondvalueaxis
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を必要とします。

### リクエストパラメータ

| パラメータ名   | 型     | 位置   | 説明                                     |
| -------------- | ------ | ------ | ----------------------------------------- |
| name           | 文字列 | path   | Excel ファイル名。                         |
| sheetName      | 文字列 | path   | チャートを含むワークシート名。             |
| chartIndex     | 整数   | path   | 変更するチャートの 0 から始まるインデックス。|
| axis           | オブジェクト | body | 第2値軸の設定。                            |
| folder         | 文字列 | query  | ファイルが存在するストレージ内のフォルダーパス。|
| storageName    | 文字列 | query  | ストレージサービス名。                     |

**リクエストボディの例（JSON）:**

```json
{
  "IsAutomaticMajorUnit": true,
  "Maximum": 100,
  "Minimum": 0,
  "MajorUnit": 10,
  "MinorUnit": 2,
  "Title": {
    "Text": "第2軸"
  }
}
```

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/Charts/PostChartSecondValueAxis) は、パブリックに利用可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 操作を実行できるようにします。

cURL コマンドラインツールを使用して、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例では、cURL を使用して Cloud API への呼び出しを行う方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondvalueaxis" \
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

**HTTP ステータスコード**

| コード | 意味                         | 説明                                           |
|------|-----------------------------|------------------------------------------------|
| 200  | OK                          | フィルターが正常に適用され、レスポンスには操作の詳細が含まれます。 |
| 400  | Bad Request                 | パラメータが不足または無効（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized                | JWT トークンが無効または不足しています。         |
| 413  | Payload Too Large           | アップロードされたファイルがサイズ制限を超えています。 |
| 500  | Internal Server Error       | 予期しないサーバーエラーが発生しました。         |

**関連リンク:**  
- [チャートの第2値軸を取得する](https://docs.aspose.cloud/cells/charts/second-value-axis/get/)  
- [チャートの値軸を更新する](https://docs.aspose.cloud/cells/charts/value-axis/update/)

## Cloud SDK Family

SDK を使用することで、開発速度を最大限に高めることができます。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスへの呼び出しを行う方法を示しています。

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// C# の例：第2値軸を更新
var api = new CellsApi("clientId", "clientSecret");
var axis = new Axis { IsAutomaticMajorUnit = true, Maximum = 100 };
api.PostChartSecondValueAxis(name, sheetName, chartIndex, axis);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Java の例：第2値軸を更新
CellsApi api = new CellsApi("clientId", "clientSecret");
Axis axis = new Axis();
axis.setIsAutomaticMajorUnit(true);
axis.setMaximum(100.0);
api.postChartSecondValueAxis(name, sheetName, chartIndex, axis);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
// PHP の例：第2値軸を更新
$api = new CellsApi($clientId, $clientSecret);
$axis = new Axis();
$axis->setIsAutomaticMajorUnit(true);
$axis->setMaximum(100);
$api->postChartSecondValueAxis($name, $sheetName, $chartIndex, $axis);
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# Ruby の例：第2値軸を更新
api = AsposeCellsCloud::ApiClient.new(client_id, client_secret)
axis = Axis.new(is_automatic_major_unit: true, maximum: 100)
api.post_chart_second_value_axis(name, sheet_name, chart_index, axis)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
# Python の例：第2値軸を更新
api = asposecellscloud.ApiClient(client_id, client_secret)
axis = Axis(is_automatic_major_unit=True, maximum=100)
api.post_chart_second_value_axis(name, sheet_name, chart_index, axis)
```

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Post-ChartSecondValueAxis.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

```java
// Android（Java）の例：上記の Java コードと同様
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```swift
// Swift の例：第2値軸を更新
let api = CellsApi(clientId: "clientId", clientSecret: "clientSecret")
var axis = Axis()
axis.isAutomaticMajorUnit = true
axis.maximum = 100
api.postChartSecondValueAxis(name: name, sheetName: sheetName, chartIndex: chartIndex, axis: axis)
```

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
# Perl の例：第2値軸を更新
my $api = AsposeCellsCloud::ApiClient->new(client_id => $client_id, client_secret => $client_secret);
my $axis = AsposeCellsCloud::Object::Axis->new(isAutomaticMajorUnit => 1, maximum => 100);
$api->post_chart_second_value_axis(name => $name, sheet_name => $sheet_name, chart_index => $chart_index, axis => $axis);
```

{{< /tab >}}

{{< tab tabNum="10" >}}

```go
// Go の例：第2値軸を更新
api := cells.NewApiClient("clientId", "clientSecret")
axis := cells.Axis{IsAutomaticMajorUnit: true, Maximum: 100}
api.PostChartSecondValueAxis(name, sheetName, chartIndex, axis)
```

{{< /tab >}}

{{< /tabs >}}