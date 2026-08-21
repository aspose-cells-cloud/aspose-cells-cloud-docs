---
title: "Excel ワークブックのすべての数式を計算する"
second_title: "Document"
linktitle: "Calculate"
type: docs
url: /ja/calculate-all-formulas-on-an-excel-file/
aliases:
  [/calculate-all-formulas-in-a-workbook/, /workbook/calculate-all-formulas/]
keywords: "Aspose.Cells, 数式の計算, Excel API, クラウド SDK"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークブック内のすべての数式を計算します。cURL の例、リクエストパラメーター、レスポンススキーマ、前提条件、および複数言語向けの SDK スニペットを含みます。"
weight: 140
ArticleTitle: "Excel ワークブックのすべての数式を計算する"
---

この REST API は、Excel ワークブック内の**すべての数式**を計算します。

**前提条件:** このエンドポイントを呼び出す前に、以下の条件を満たしていることを確認してください。
- 有効な JWT 認証トークン。（[認証ガイド](/authentication/) を参照）
- Aspose.Cells Cloud のクライアント ID とシークレット
- 対象となるワークブックが指定されたストレージの場所にアップロードされていること。（[ストレージ設定](/storage/) を参照）

## PostWorkbookCalculateFormula API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/calculateformula
```

リクエストパラメーターは以下の通りです：

| パラメーター名  | 型                 | 位置   | 説明                                                                 |
| --------------- | ------------------ | ------ | -------------------------------------------------------------------- |
| **name**        | string             | path   | ワークブックファイルの名前。                                         |
| **options**     | CalculationOptions | body   | 計算設定を指定する JSON オブジェクト（例：`CalcStackSize`、`IgnoreError`）。 |
| **ignoreError** | boolean            | query  | `true` の場合、計算中に発生したエラーは無視されます。               |
| **folder**      | string             | query  | ワークブックを含むフォルダーのパス。                                 |
| **storageName** | string             | query  | ワークブックが保存されているストレージサービスの名前。               |

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookCalculateFormula) は、パブリックに利用可能なプログラミングインタフェースを定義し、Web ブラウザーから直接 REST 通信を実行できるようにします。

cURL コマンドラインツールを使用すると、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/calculateformula?ignoreError=true" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "CalcStackSize": 1,
        "IgnoreError": true,
        "PrecisionStrategy": "string",
        "Recursive": true
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "WorkbookUrl": "https://api.aspose.cloud/v3.0/storage/file/Book1.xlsx",
  "ErrorMessage": null
}
```

{{< /tab >}}

{{< /tabs >}}

#### レスポンスの詳細

| フィールド         | 型     | 説明                                                         |
| ----------------- | ------ | ------------------------------------------------------------ |
| **Code**          | int    | HTTP 風のステータスコード（200 は成功を示します）。           |
| **Status**        | string | 結果の短いテキスト説明（例：`OK`）。                          |
| **WorkbookUrl**   | string | 更新されたワークブックをダウンロードできる直接の URL。        |
| **ErrorMessage**  | string | リクエストが失敗した場合の詳細なエラー情報。成功時は `null`。 |

#### 次のステップ / 共通のエラー

- **計算エラーの処理** – 数式が評価できない場合にエラーレスポンスを受け取るには、`ignoreError=false` を設定します。
- **レート制限への対応** – `X-RateLimit-Remaining` ヘッダーを確認し、`0` になった場合はリトライ前に待機してください。
- **HTTP ステータスのガイドライン**：
  - `400` – 無効なリクエストパラメーター
  - `401` – 認証失敗（無効または期限切れの JWT）
  - `404` – ワークブックが見つからない
  - `500` – サーバー側エラー。継続する場合は Aspose のサポートに連絡してください。

| コード | 意味                 | 返されるタイミング                                           |
| ------ | -------------------- | ------------------------------------------------------------ |
| 400    | Bad Request（不正なリクエスト） | 無効なリクエストパラメーター、または不正な形式の JSON。     |
| 401    | Unauthorized（認証エラー）     | JWT トークンが欠落、無効、または期限切れ。                  |
| 404    | Not Found（未検索）           | 指定されたワークブックがストレージ内に存在しない。          |
| 500    | Internal Server Error（内部サーバーエラー） | 予期しないサーバー側エラー。Aspose のサポートにお問い合わせください。 |

## Cloud SDK Family

SDK を使用すると、開発スピードを最大限に引き上げられます。SDK が低レベルの詳細処理を担当するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var api = new CellsApi("<clientId>", "<clientSecret>");
var request = new PostWorkbookCalculateFormulaRequest(
    name: "Book1.xlsx",
    folder: "",
    storageName: "",
    ignoreError: true,
    options: new CalculationOptions { CalcStackSize = 1, IgnoreError = true });

var response = api.PostWorkbookCalculateFormula(request);
Console.WriteLine($"Status: {response.Status}");
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.*;

CellsApi api = new CellsApi("<clientId>", "<clientSecret>");
PostWorkbookCalculateFormulaRequest request = new PostWorkbookCalculateFormulaRequest()
        .name("Book1.xlsx")
        .ignoreError(true)
        .options(new CalculationOptions().calcStackSize(1).ignoreError(true));

WorkbookResponse result = api.postWorkbookCalculateFormula(request);
System.out.println("Status: " + result.getStatus());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
require_once 'vendor/autoload.php';

use Aspose\Cells\Cloud\Api\CellsApi;
use Aspose\Cells\Cloud\Model\CalculationOptions;
use Aspose\Cells\Cloud\Model\PostWorkbookCalculateFormulaRequest;

$api = new CellsApi("<clientId>", "<clientSecret>");
$options = new CalculationOptions([
    "CalcStackSize" => 1,
    "IgnoreError"   => true
]);

$request = new PostWorkbookCalculateFormulaRequest([
    "name"    => "Book1.xlsx",
    "ignoreError" => true,
    "options" => $options
]);

$response = $api->postWorkbookCalculateFormula($request);
echo "Status: " . $response->getStatus();
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
require 'aspose_cells_cloud'

api = AsposeCellsCloud::CellsApi.new("<clientId>", "<clientSecret>")
options = AsposeCellsCloud::CalculationOptions.new(
  calc_stack_size: 1,
  ignore_error: true
)

request = AsposeCellsCloud::PostWorkbookCalculateFormulaRequest.new(
  name: 'Book1.xlsx',
  ignore_error: true,
  options: options
)

response = api.post_workbook_calculate_formula(request)
puts "Status: #{response.status}"
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```javascript
const {
  CellsApi,
  PostWorkbookCalculateFormulaRequest,
  CalculationOptions,
} = require("asposecellscloud");

const api = new CellsApi("<clientId>", "<clientSecret>");
const options = new CalculationOptions({ CalcStackSize: 1, IgnoreError: true });

const request = new PostWorkbookCalculateFormulaRequest({
  name: "Book1.xlsx",
  ignoreError: true,
  options: options,
});

api.postWorkbookCalculateFormula(request).then((response) => {
  console.log(`Status: ${response.status}`);
});
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```python
from asposecellscloud import CellsApi, PostWorkbookCalculateFormulaRequest, CalculationOptions

api = CellsApi("<clientId>", "<clientSecret>")
options = CalculationOptions(calc_stack_size=1, ignore_error=True)

request = PostWorkbookCalculateFormulaRequest(
    name="Book1.xlsx",
    ignore_error=True,
    options=options
)

response = api.post_workbook_calculate_formula(request)
print(f"Status: {response.status}")
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
use AsposeCellsCloud::CellsApi;
use AsposeCellsCloud::Object::PostWorkbookCalculateFormulaRequest;
use AsposeCellsCloud::Object::CalculationOptions;

my $api = AsposeCellsCloud::CellsApi->new(
    client_id     => '<clientId>',
    client_secret => '<clientSecret>'
);

my $options = AsposeCellsCloud::Object::CalculationOptions->new(
    CalcStackSize => 1,
    IgnoreError   => JSON::true
);

my $request = AsposeCellsCloud::Object::PostWorkbookCalculateFormulaRequest->new(
    name        => 'Book1.xlsx',
    ignoreError => JSON::true,
    options     => $options
);

my $response = $api->post_workbook_calculate_formula(request => $request);
print "Status: " . $response->{Status} . "\n";
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/asposecellscloud-go/v3/api"
    "github.com/asposecellscloud/asposecellscloud-go/v3/model"
)

func main() {
    cfg := api.NewConfiguration()
    cfg.AddDefaultHeader("client-id", "<clientId>")
    cfg.AddDefaultHeader("client-secret", "<clientSecret>")
    client := api.NewAPIClient(cfg)

    opts := model.CalculationOptions{
        CalcStackSize: 1,
        IgnoreError:   true,
    }

    req := model.PostWorkbookCalculateFormulaRequest{
        Name:        "Book1.xlsx",
        IgnoreError: true,
        Options:     &opts,
    }

    resp, _, err := client.CellsApi.PostWorkbookCalculateFormula(req)
    if err != nil {
        panic(err)
    }
    fmt.Printf("Status: %s\n", resp.Status)
}
```

{{< /tab >}}

{{< /tabs >}}