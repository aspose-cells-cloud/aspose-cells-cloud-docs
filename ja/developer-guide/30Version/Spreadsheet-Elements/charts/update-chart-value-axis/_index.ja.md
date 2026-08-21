---
title: "Aspose.Cells Cloud API – チャートの値軸を更新する (POST /valueaxis)"
description: "Aspose.Cells Cloud REST API を使用して、Excelワークシート内のチャートの値軸を更新します。エンドポイント、パラメータ、リクエストボディのスキーマ、例（cURLとSDK）、レスポンス、エラーハンドリングを含みます。"
keywords:
  - Aspose.Cells Cloud
  - チャートの値軸を更新する
  - REST API
  - Excelチャート軸
  - POST valueaxis
  - cURLの例
  - SDK
  - JSONペイロード
  - チャート軸設定
last_updated: 2026-07-30
---

# チャートの値軸を更新する (POST /valueaxis)

**概要:**  
Aspose Cloud ストレージに保存されたExcelワークブック内の特定のチャートの値軸を変更します。単一のリクエストで、範囲、目盛り間隔、対数目盛りなど、軸のプロパティを設定できます。

---

## 前提条件

1. **JWT アクセストークン** – [認証ガイド](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)に従ってトークンを取得してください。  
2. 対象の**ワークブック**は、すでにAspose Cloud ストレージ（またはデフォルトストレージ）にアップロードされている必要があります。  
3. 変更したい**ワークシート名**と**0から始まるチャートのインデックス**を把握していること。

---

## エンドポイント

```
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis
```

*プレースホルダーを実際の値に置き換えてください。*

| プレースホルダー | 説明 |
|------------------|------|
| `{name}` | Excelファイルの名前（例: `Book1.xlsx`）。 |
| `{sheetName}` | チャートを含むワークシート名（例: `Sheet1`）。 |
| `{chartIndex}` | 更新するチャートの0から始まるインデックス（例: `0`）。 |

---

## 認証

このAPIは**JWT トークンベース認証**を使用します。`Authorization` ヘッダーにトークンを含めてください：

```
Authorization: Bearer <jwt token>
```

---

### **セキュリティと認証**

Aspose.Cells Cloud API は安全で、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベース認証</a>が必要です。

## リクエストパラメータ

| 名前 | 位置 | 型 | 必須 | 説明 |
|------|------|----|------|------|
| **name** | パス | string | はい | クラウドに保存されているExcelファイル名。 |
| **sheetName** | パス | string | はい | チャートを含むワークシート名。 |
| **chartIndex** | パス | int | はい | 更新するチャートの0から始まるインデックス。 |
| **axis** | 本文 | object | はい | 軸の設定（*リクエストボディのスキーマ* を参照）。 |
| **folder** | クエリ | string | いいえ | ファイルが存在するクラウドフォルダーパス。 |
| **storageName** | クエリ | string | いいえ | 使用するストレージサービスの名前。 |

---

## リクエストボディのスキーマ (`axis` オブジェクト)

変更したいプロパティのみを含めればよいです。

| プロパティ | 型 | 必須 | 説明 |
|------------|----|------|------|
| `minimum` | number | いいえ | 軸の下限値。 |
| `maximum` | number | いいえ | 軸の上限値。 |
| `majorUnit` | number | いいえ | 主目盛り間の間隔。 |
| `minorUnit` | number | いいえ | 副目盛り間の間隔。 |
| `logBase` | number | いいえ | `isLogarithmic` が `true` の場合の対数の底。 |
| `isLogarithmic` | boolean | いいえ | 軸が対数目盛りを使用するかどうか。 |
| `displayUnit` | string | いいえ | 軸に表示される単位ラベル（例: `"Thousands"`）。 |
| `tickMark` | string | いいえ | 目盛りのスタイル（`"inside"`、`"outside"` など）。 |
| `crossAt` | number | いいえ | 軸が垂直軸と交差する位置。 |

### リクエストボディの例

```json
{
  "minimum": 0,
  "maximum": 200,
  "majorUnit": 20,
  "minorUnit": 5,
  "logBase": 10,
  "isLogarithmic": false,
  "displayUnit": "Units",
  "tickMark": "inside",
  "crossAt": 0
}
```

---

## 例：リクエスト

### cURL

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/<code class=\"placeholder\">{name}</code>/worksheets/<code class=\"placeholder\">{sheetName}</code>/charts/<code class=\"placeholder\">{chartIndex}</code>/valueaxis?folder=<code class=\"placeholder\">{folder}</code>&storageName=<code class=\"placeholder\">{storageName}</code>" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "minimum": 0,
        "maximum": 200,
        "majorUnit": 20,
        "minorUnit": 5,
        "logBase": 10,
        "isLogarithmic": false,
        "displayUnit": "Units",
        "tickMark": "inside",
        "crossAt": 0
      }'
```

### SDKのサンプル  

{{< tabs tabTotal="10" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var api = new ChartsApi("client_id", "client_secret");
var axis = new Axis()
{
    Minimum = 0,
    Maximum = 200,
    MajorUnit = 20,
    MinorUnit = 5,
    LogBase = 10,
    IsLogarithmic = false,
    DisplayUnit = "Units",
    TickMark = "inside",
    CrossAt = 0
};

var response = api.PostChartValueAxis("Book1.xlsx", "Sheet1", 0, axis);
Console.WriteLine($"Status: {response.Status}");
```
{{< /tab >}}

{{< tab tabNum="2" >}}
```java
import com.aspose.cells.cloud.api.ChartsApi;
import com.aspose.cells.cloud.model.Axis;

ChartsApi api = new ChartsApi("client_id", "client_secret");
Axis axis = new Axis()
        .minimum(0.0)
        .maximum(200.0)
        .majorUnit(20.0)
        .minorUnit(5.0)
        .logBase(10.0)
        .isLogarithmic(false)
        .displayUnit("Units")
        .tickMark("inside")
        .crossAt(0.0);

api.postChartValueAxis("Book1.xlsx", "Sheet1", 0, axis);
System.out.println("Value axis updated.");
```
{{< /tab >}}

{{< tab tabNum="3" >}}
```php
<?php
require 'vendor/autoload.php';

use Aspose\Cells\Cloud\Api\ChartsApi;
use Aspose\Cells\Cloud\Model\Axis;

$api = new ChartsApi('client_id', 'client_secret');
$axis = new Axis([
    'minimum' => 0,
    'maximum' => 200,
    'majorUnit' => 20,
    'minorUnit' => 5,
    'logBase' => 10,
    'isLogarithmic' => false,
    'displayUnit' => 'Units',
    'tickMark' => 'inside',
    'crossAt' => 0
]);

$api->postChartValueAxis('Book1.xlsx', 'Sheet1', 0, $axis);
echo "Value axis updated.\n";
?>
```
{{< /tab >}}

{{< tab tabNum="4" >}}
```ruby
require 'aspose_cells_cloud'

api = AsposeCellsCloud::ChartsApi.new('client_id', 'client_secret')
axis = AsposeCellsCloud::Axis.new(
  minimum: 0,
  maximum: 200,
  majorUnit: 20,
  minorUnit: 5,
  logBase: 10,
  isLogarithmic: false,
  displayUnit: 'Units',
  tickMark: 'inside',
  crossAt: 0
)

api.post_chart_value_axis('Book1.xlsx', 'Sheet1', 0, axis)
puts 'Value axis updated.'
```
{{< /tab >}}

{{< tab tabNum="5" >}}
```python
from asposecellscloud import ChartsApi, Axis

api = ChartsApi('client_id', 'client_secret')
axis = Axis(
    minimum=0,
    maximum=200,
    majorUnit=20,
    minorUnit=5,
    logBase=10,
    isLogarithmic=False,
    displayUnit='Units',
    tickMark='inside',
    crossAt=0
)

api.post_chart_value_axis('Book1.xlsx', 'Sheet1', 0, axis)
print('Value axis updated.')
```
{{< /tab >}}

{{< tab tabNum="6" >}}
```javascript
// Node.jsの例
const { ChartsApi, Axis } = require('asposecellscloud');

const api = new ChartsApi('client_id', 'client_secret');
const axis = new Axis({
    minimum: 0,
    maximum: 200,
    majorUnit: 20,
    minorUnit: 5,
    logBase: 10,
    isLogarithmic: false,
    displayUnit: 'Units',
    tickMark: 'inside',
    crossAt: 0
});

api.postChartValueAxis('Book1.xlsx', 'Sheet1', 0, axis)
   .then(response => console.log('Value axis updated.'))
   .catch(err => console.error(err));
```
{{< /tab >}}

{{< tab tabNum="7" >}}
```java
// Android（Java）の例
ChartsApi api = new ChartsApi("client_id", "client_secret");
Axis axis = new Axis()
        .minimum(0.0)
        .maximum(200.0)
        .majorUnit(20.0)
        .minorUnit(5.0)
        .logBase(10.0)
        .isLogarithmic(false)
        .displayUnit("Units")
        .tickMark("inside")
        .crossAt(0.0);

api.postChartValueAxis("Book1.xlsx", "Sheet1", 0, axis);
```
{{< /tab >}}

{{< tab tabNum="8" >}}
```swift
import AsposeCellsCloud

let api = ChartsApi(clientId: "client_id", clientSecret: "client_secret")
var axis = Axis()
axis.minimum = 0
axis.maximum = 200
axis.majorUnit = 20
axis.minorUnit = 5
axis.logBase = 10
axis.isLogarithmic = false
axis.displayUnit = "Units"
axis.tickMark = "inside"
axis.crossAt = 0

api.postChartValueAxis(name: "Book1.xlsx", sheetName: "Sheet1", chartIndex: 0, axis: axis) { result, error in
    if let error = error {
        print("Error: \\(error)")
    } else {
        print("Value axis updated.")
    }
}
```
{{< /tab >}}

{{< tab tabNum="9" >}}
```perl
use Aspose::Cells::Cloud::Api::ChartsApi;
use Aspose::Cells::Cloud::Model::Axis;

my $api  = ChartsApi->new('client_id', 'client_secret');
my $axis = Axis->new(
    minimum        => 0,
    maximum        => 200,
    majorUnit      => 20,
    minorUnit      => 5,
    logBase        => 10,
    isLogarithmic  => JSON::false,
    displayUnit    => 'Units',
    tickMark       => 'inside',
    crossAt        => 0
);

$api->postChartValueAxis('Book1.xlsx', 'Sheet1', 0, $axis);
print "Value axis updated.\n";
```
{{< /tab >}}

{{< tab tabNum="10" >}}
```go
package main

import (
    "context"
    "fmt"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v2/api"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v2/model"
)

func main() {
    cfg := api.NewConfiguration()
    cfg.AddDefaultHeader("client_id", "client_id")
    cfg.AddDefaultHeader("client_secret", "client_secret")
    client := api.NewAPIClient(cfg)

    axis := model.Axis{
        Minimum:       0,
        Maximum:       200,
        MajorUnit:     20,
        MinorUnit:     5,
        LogBase:       10,
        IsLogarithmic: false,
        DisplayUnit:   "Units",
        TickMark:      "inside",
        CrossAt:       0,
    }

    _, err := client.ChartsApi.PostChartValueAxis(context.Background(), "Book1.xlsx", "Sheet1", 0, axis)
    if err != nil {
        fmt.Println("Error:", err)
    } else {
        fmt.Println("Value axis updated.")
    }
}
```
{{< /tab >}}

{{< /tabs >}}

---

## レスポンス

### 成功 (200)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

レスポンスタイプは `CellsCloudResponse` です。

**HTTPステータスコード**

| コード | 意味 | 説明 |
|--------|------|------|
| 200 | OK | フィルターが正常に適用されました。レスポンスには操作の詳細が含まれます。 |
| 400 | Bad Request | パラメータが不足している、または無効です（例: サポートされていないファイル形式）。 |
| 401 | Unauthorized | JWT トークンが無効または不足しています。 |
| 413 | Payload Too Large | アップロードされたファイルがサイズ制限を超えています。 |
| 500 | Internal Server Error | 予期しないサーバーエラーが発生しました。 |
---

## 関連リソース

- **OpenAPI仕様** – [JSON/YAML形式で表示／ダウンロード](https://apireference.aspose.cloud/cells/#/Charts/PostChartValueAxis)  
- **SDKリポジトリ** – <https://github.com/aspose-cells-cloud>  
- **認証ガイド** – <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>

---

*ご質問やフィードバックがある場合は、Aspose.Cells Cloudサポートチームまでお問い合わせください。*