---
title: 条件付き書式にセル範囲を追加
description: Aspose.Cells Cloud REST API (v3.0) を使用して、Excelワークシート内の条件付き書式ルールにセル範囲を追加します。エンドポイント、パラメータ、cURL、SDKの例、レスポンススキーマ、エラーハンドリングを含みます。
keywords: Aspose.Cells, 条件付き書式, CellArea, REST API, Excel, クラウドSDK
weight: 30
aliases:
  - /add-a-cell-area-for-format-condition/
---

# 条件付き書式にセル範囲を追加

**概要** – ワークシート内の既存の条件付き書式ルールにセル範囲を追加します。

---

## 前提条件

1. **Aspose.Cells Cloudアカウント** – **App SID** と **App Key** を取得してください。  
2. **JWTトークン** – App SID/Keyを使用してJWTトークンを生成してください（[認証ガイド](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)を参照）。  
3. 対象のExcelファイルが、指定されたストレージ/フォルダ内に既に存在していること。

---

## 認証

すべての呼び出しは **JWTトークンベースの認証** が必要です。トークンは `Authorization` ヘッダーに渡してください：

```http
Authorization: Bearer <jwt token>
```

---

## HTTPリクエスト

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/area
```

### パスパラメータ

| 名前        | 型     | 説明                                      |
|-------------|--------|-------------------------------------------|
| `name`      | 文字列 | Excelファイル名（例: `Book1.xlsx`）       |
| `sheetName` | 文字列 | ルールが含まれるワークシート名（例: `Sheet1`） |
| `index`     | 整数   | 条件付き書式ルールの0始まりのインデックス |

### クエリパラメータ

| 名前            | 型     | 必須 | 説明                                      |
|-----------------|--------|------|-------------------------------------------|
| `cellArea`      | 文字列 | **はい** | 追加するセル範囲（A1表記、例: `A1:C3`） |
| `folder`        | 文字列 | いいえ | ファイルが格納されているフォルダパス     |
| `storageName`   | 文字列 | いいえ | ストレージサービス名                      |

---

## リクエスト例（cURL）

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/conditionalFormattings/0/area?cellArea=A1:C3" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

### 期待される成功レスポンス

```json
{
  "Code": "200",
  "Status": "OK",
  "CellArea": {
    "StartRow": 0,
    "StartColumn": 0,
    "EndRow": 2,
    "EndColumn": 2
  }
}
```

**レスポンススキーマ – `CellArea`**

| プロパティ      | 型   | 説明                      |
|-----------------|------|---------------------------|
| `StartRow`      | int  | 最初の行の0始まりインデックス |
| `StartColumn`   | int  | 最初の列の0始まりインデックス |
| `EndRow`        | int  | 最後の行の0始まりインデックス |
| `EndColumn`     | int  | 最後の列の0始まりインデックス |

---

**HTTPステータスコード**

| コード | 意味                | 説明                                     |
|--------|---------------------|------------------------------------------|
| 200    | OK                  | フィルターが正常に適用された。レスポンスには操作の詳細が含まれます。 |
| 400    | Bad Request         | パラメータが不足しているか、無効です（例: 非対応のファイル形式） |
| 401    | Unauthorized        | JWTトークンが無効または不足しています。 |
| 413    | Payload Too Large   | アップロードされたファイルがサイズ制限を超えています。 |
| 500    | Internal Server Error | サーバーで予期しないエラーが発生しました。 |
---

## SDKの例

以下は、最も一般的なSDKの短いコードスニペットです。`YOUR_APP_SID` と `YOUR_APP_KEY` をご自身の認証情報に置き換え、必要に応じて生成したJWTトークンを設定してください。

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.Sdk;
using Aspose.Cells.Cloud.Sdk.Model;

var config = new Configuration
{
    AppSid = "YOUR_APP_SID",
    AppKey = "YOUR_APP_KEY"
};

var api = new ConditionalFormattingsApi(config);
var result = api.PutWorksheetFormatConditionArea(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    cellArea: "A1:C3",
    folder: null,
    storageName: null);

Console.WriteLine(result);
```

### Java

```java
import com.aspose.cells.cloud.ApiClient;
import com.aspose.cells.cloud.Configuration;
import com.aspose.cells.cloud.api.ConditionalFormattingsApi;

Configuration config = new Configuration();
config.setAppSid("YOUR_APP_SID");
config.setAppKey("YOUR_APP_KEY");

ConditionalFormattingsApi api = new ConditionalFormattingsApi(new ApiClient(config));

try {
    com.aspose.cells.cloud.model.ResponseMessage resp = api.putWorksheetFormatConditionArea(
        "Book1.xlsx", "Sheet1", 0, "A1:C3", null, null);
    System.out.println(resp);
} catch (Exception e) {
    e.printStackTrace();
}
```

### PHP

```php
<?php
require 'vendor/autoload.php';

use Aspose\Cells\Cloud\Sdk\Api\ConditionalFormattingsApi;
use Aspose\Cells\Cloud\Sdk\Configuration;

$config = new Configuration();
$config->setAppSid('YOUR_APP_SID');
$config->setAppKey('YOUR_APP_KEY');

$api = new ConditionalFormattingsApi($config);

try {
    $result = $api->putWorksheetFormatConditionArea(
        'Book1.xlsx',
        'Sheet1',
        0,
        'A1:C3',
        null,
        null
    );
    print_r($result);
} catch (Exception $e) {
    echo 'Error: ', $e->getMessage();
}
?>
```

### Ruby

```ruby
require 'aspose_cells_cloud_sdk'

config = AsposeCellsCloud::Configuration.new
config.app_sid = 'YOUR_APP_SID'
config.app_key = 'YOUR_APP_KEY'

api_instance = AsposeCellsCloud::ConditionalFormattingsApi.new
begin
  result = api_instance.put_worksheet_format_condition_area(
    'Book1.xlsx', 'Sheet1', 0, 'A1:C3')
  puts result
rescue StandardError => e
  puts "Error: #{e}"
end
```

### Node.js

```javascript
const { Configuration, ConditionalFormattingsApi } = require('asposecellscloudsdk');

const config = new Configuration();
config.appSid = 'YOUR_APP_SID';
config.appKey = 'YOUR_APP_KEY';

const api = new ConditionalFormattingsApi(config);

api.putWorksheetFormatConditionArea('Book1.xlsx', 'Sheet1', 0, 'A1:C3')
   .then(res => console.log(res))
   .catch(err => console.error('Error:', err));
```

### Python

```python
import asposecellscloudsdk
from asposecellscloudsdk.rest import ApiException
from asposecellscloudsdk import Configuration, ApiClient
from asposecellscloudsdk.api import conditional_formattings_api

config = Configuration()
config.app_sid = 'YOUR_APP_SID'
config.app_key = 'YOUR_APP_KEY'

api_instance = conditional_formattings_api.ConditionalFormattingsApi(ApiClient(config))

try:
    result = api_instance.put_worksheet_format_condition_area(
        name='Book1.xlsx',
        sheet_name='Sheet1',
        index=0,
        cell_area='A1:C3')
    print(result)
except ApiException as e:
    print("Exception:", e)
```

### Android (Java)

```java
import com.aspose.cloud.cells.api.ConditionalFormattingsApi;
import com.aspose.cloud.cells.client.ApiClient;
import com.aspose.cloud.cells.client.Configuration;

Configuration config = new Configuration();
config.setAppSid("YOUR_APP_SID");
config.setAppKey("YOUR_APP_KEY");

ConditionalFormattingsApi api = new ConditionalFormattingsApi(new ApiClient(config));

try {
    com.aspose.cloud.cells.model.ResponseMessage resp = api.putWorksheetFormatConditionArea(
        "Book1.xlsx", "Sheet1", 0, "A1:C3", null, null);
    System.out.println(resp);
} catch (Exception e) {
    e.printStackTrace();
}
```

### Swift

```swift
import AsposeCellsCloud

let config = Configuration(appSid: "YOUR_APP_SID", appKey: "YOUR_APP_KEY")
let api = ConditionalFormattingsApi(configuration: config)

api.putWorksheetFormatConditionArea(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    cellArea: "A1:C3",
    folder: nil,
    storageName: nil) { result, error in
        if let err = error {
            print("Error:", err)
        } else if let res = result {
            print(res)
        }
}
```

### Perl

```perl
use AsposeCellsCloud::Api::ConditionalFormattingsApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new(
    app_sid  => 'YOUR_APP_SID',
    app_key  => 'YOUR_APP_KEY'
);
my $api = AsposeCellsCloud::Api::ConditionalFormattingsApi->new($config);

my $result = $api->putWorksheetFormatConditionArea(
    name      => 'Book1.xlsx',
    sheetName => 'Sheet1',
    index     => 0,
    cellArea  => 'A1:C3'
);
print $result;
```

### Go

```go
package main

import (
    "fmt"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    config := sdk.NewConfiguration()
    config.AppSid = "YOUR_APP_SID"
    config.AppKey = "YOUR_APP_KEY"

    api := sdk.NewConditionalFormattingsApi(config)

    resp, _, err := api.PutWorksheetFormatConditionArea(
        "Book1.xlsx", "Sheet1", 0, "A1:C3", nil, nil)
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    fmt.Println(resp)
}
```

---

## 注意事項とヒント

- **CellAreaの形式** – 有効なA1範囲（`A1`、`A1:C3`、`Sheet2!B2:D5`など）である必要があります。無効な形式の場合は **400 Bad Request** が返されます。
- **重複する範囲** – 既存の同じルールの範囲と重複する範囲を追加すると、**409 Conflict** が発生します。
- **0始まりのインデックス** – レスポンス内の行・列のインデックスは `0` から始まります。必要に応じてExcelの1始まり表記に変換してください。
- **ストレージ** – `folder` と `storageName` を省略した場合、APIはデフォルトのストレージ/ルートフォルダを使用します。

---

## 関連する操作

- **セル範囲の削除** – `DELETE /cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/area`
- **条件付き書式への条件追加** – `POST /cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/condition`
- **条件付き書式の取得** – `GET /cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}`

これらの操作を組み合わせることで、完全な条件付き書式のワークフローを構築できます。

---