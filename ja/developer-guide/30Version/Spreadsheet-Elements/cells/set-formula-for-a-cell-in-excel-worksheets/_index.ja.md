---
title: "Excelワークシートのセルに数式を設定する"
type: docs
url: /set-formula-for-a-cell-in-excel-worksheets/
weight: 80
keywords: "Excel, Aspose.Cells, REST API, 数式の設定, ワークシート, セル, クラウドSDK, cURL"
description: "Aspose.Cells Cloud REST API を使用して、Excelワークシート内の特定のセルに数式を設定する方法を学びます。cURLの例、完全なパラメータ一覧、エラー処理、SDKコードサンプルを含みます。"
---

このREST APIは、Excelファイル内の**セルの数式**を設定します。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}
```

## セキュリティと認証

Aspose.Cells Cloud APIは安全であり、[JWTトークンベースの認証](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)が必要です。

**リクエストパラメータ**

| パラメータ名 | 型     | 位置   | 必須 | 説明                           |
|--------------|--------|--------|------|--------------------------------|
| name         | string | path   | はい | Excelドキュメントの名前。       |
| sheetName    | string | path   | はい | ワークシートの名前。            |
| cellName     | string | path   | はい | 対象セルのアドレス（例：**A1**）。 |
| value        | string | query  | いいえ | セルに割り当てる値。            |
| type         | string | query  | いいえ | 値のデータ型（例：**string**）。 |
| formula      | string | query  | いいえ | セルに適用する数式（例：**sum(A1,A2)**）。 |
| folder       | string | query  | いいえ | ドキュメントを含むフォルダ。     |
| storageName  | string | query  | いいえ | ストレージサービスの名前。       |

## **レスポンス**

CellResponseを返します。

- **レスポンスフィールド概要**

| フィールド         | 型      | 説明                                           |
| ----------------- | ------- | ---------------------------------------------- |
| `Name`            | string  | セルのアドレス（例：`F341`）。                   |
| `Row`             | integer | 0始まりの行インデックス。                       |
| `Column`          | integer | 0始まりの列インデックス。                       |
| `Value`           | string  | セルに表示される値。                            |
| `Type`            | string  | セルのデータ型（例：`IsString`）。             |
| `Formula`         | string  | セルに数式が含まれている場合の数式テキスト。     |
| `IsFormula`       | bool    | セルに数式が含まれているかどうかを示します。     |
| `IsMerged`        | bool    | セルが結合範囲の一部であるかどうかを示します。   |
| `IsArrayHeader`   | bool    | セルが配列のヘッダーであるかどうかを示します。   |
| `IsInArray`       | bool    | セルが配列の一部であるかどうかを示します。       |
| `IsErrorValue`    | bool    | セルにエラー値が含まれているかどうかを示します。 |
| `IsInTable`       | bool    | セルがテーブル内にあるかどうかを示します。       |
| `IsStyleSet`      | bool    | セルにスタイルが適用されているかどうかを示します。|
| `HtmlString`      | string  | セルの値のHTMLエンコード表現。                 |
| `Style/link`      | object  | スタイルリソースへのハイパーリンク。            |


```json
{
  "Status":"OK",
  "Code":200,
  "Cell":{
    "Name":"A1",
    "Row": 0,
    "Column":0,
    "Value": "",
    "Type":"String",
    "Formula" : "=Sum(A2:A15)",
    ...
  }
}
```

**HTTPステータスコード**

| コード | 意味                       | 説明                                           |
|--------|----------------------------|-----------------------------------------------|
| 200    | OK                         | フィルターが正常に適用され、レスポンスに操作の詳細が含まれます。 |
| 400    | Bad Request                | パラメータが不足しているか、無効です（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized               | JWTトークンが無効または不足しています。        |
| 413    | Payload Too Large          | アップロードされたファイルがサイズ制限を超えています。 |
| 500    | Internal Server Error      | 予期しないサーバーエラーが発生しました。       |

## SDKを使用したPostWorksheetCellSetValue APIの使用方法

### PostWorksheetCellSetValue API仕様

[OpenAPI仕様](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetCellSetValue)は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Webブラウザから直接REST通信を実行できるようにします。

cURLコマンドラインツールを使用してAspose.Cellsウェブサービスを呼び出します。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A1?value=1234&type=string&formula=sum(A2:A15)" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access‑token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Cell":{
    "Name":"A1",
    "Row": 0,
    "Column":0,
    "Value": "",
    "Type":"String",
    "Formula" : "=Sum(A2:A15)",
    ...
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDKの使用

SDKを使用することが開発の高速化に最適な方法です。SDKは低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDKの完全なリストについては、[GitHubリポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまなSDKを使用してAspose.Cellsウェブサービスを呼び出す方法を示しています：

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// C#の例 – セルに数式を設定
// <access-token>、<file-name>などを実際の値に置き換えてください。
var api = new CellsApi("<client-id>", "<client-secret>", "https://api.aspose.cloud");
var response = api.PostWorksheetCellSetValue(
    name: "myWorkbook.xlsx",
    sheetName: "Sheet1",
    cellName: "A3",
    value: "1234",
    type: "string",
    formula: "SUM(A1,A2)",
    folder: null,
    storageName: null);
Console.WriteLine(response.Status);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Javaの例 – セルに数式を設定
CellsApi api = new CellsApi("<client-id>", "<client-secret>", "https://api.aspose.cloud");
PostWorksheetCellSetValueRequest request = new PostWorksheetCellSetValueRequest()
        .name("myWorkbook.xlsx")
        .sheetName("Sheet1")
        .cellName("A3")
        .value("1234")
        .type("string")
        .formula("SUM(A1,A2)");
CellsResponse response = api.postWorksheetCellSetValue(request);
System.out.println(response.getStatus());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
// PHPの例 – セルに数式を設定
require_once('vendor/autoload.php');

$config = new Aspose\Cells\Configuration();
$config->setAppKey('<client-id>');
$config->setAppSid('<client-secret>');
$config->setHost('https://api.aspose.cloud');

$apiInstance = new Aspose\Cells\Api\CellsApi($config);
$result = $apiInstance->postWorksheetCellSetValue(
    "myWorkbook.xlsx",
    "Sheet1",
    "A3",
    "1234",
    "string",
    "SUM(A1,A2)"
);
echo $result->getStatus();
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# Rubyの例 – セルに数式を設定
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.api_key['client_id'] = '<client-id>'
config.api_key['client_secret'] = '<client-secret>'
config.host = 'https://api.aspose.cloud'

api = AsposeCellsCloud::CellsApi.new
result = api.post_worksheet_cell_set_value(
  name: 'myWorkbook.xlsx',
  sheet_name: 'Sheet1',
  cell_name: 'A3',
  value: '1234',
  type: 'string',
  formula: 'SUM(A1,A2)'
)
puts result.status
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
# Pythonの例 – セルに数式を設定
import asposecellscloud

client = asposecellscloud.CellsApiClient(
    client_id='<client-id>',
    client_secret='<client-secret>',
    base_url='https://api.aspose.cloud'
)

api = asposecellscloud.CellsApi(client)
response = api.post_worksheet_cell_set_value(
    name='myWorkbook.xlsx',
    sheet_name='Sheet1',
    cell_name='A3',
    value='1234',
    type='string',
    formula='SUM(A1,A2)'
)
print(response.status)
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```javascript
// Node.jsの例 – セルに数式を設定
const { CellsApi, ApiClient } = require('asposecellscloud');
const client = new ApiClient();
client.config = {
    clientId: '<client-id>',
    clientSecret: '<client-secret>',
    baseUrl: 'https://api.aspose.cloud'
};

const cellsApi = new CellsApi(client);
cellsApi.postWorksheetCellSetValue({
    name: 'myWorkbook.xlsx',
    sheetName: 'Sheet1',
    cellName: 'A3',
    value: '1234',
    type: 'string',
    formula: 'SUM(A1,A2)'
}).then(res => console.log(res.status));
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```java
// Android（Java）の例 – セルに数式を設定
// 標準的なJavaの例と同様ですが、Android対応SDKを使用することを確認してください。
```

{{< /tab >}}

{{< tab tabNum="8" >}}

**Swiftの例は利用できません**。Swift用SDKは現在開発中です。

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
# Perlの例 – セルに数式を設定
use AsposeCellsCloud::CellsApi;
my $api_instance = AsposeCellsCloud::CellsApi->new(
    client_id => '<client-id>',
    client_secret => '<client-secret>',
    base_url => 'https://api.aspose.cloud'
);
my $result = $api_instance->post_worksheet_cell_set_value(
    name => 'myWorkbook.xlsx',
    sheet_name => 'Sheet1',
    cell_name => 'A3',
    value => '1234',
    type => 'string',
    formula => 'SUM(A1,A2)'
);
print $result->{Status};
```

{{< /tab >}}

{{< tab tabNum="10" >}}

```go
// Goの例 – セルに数式を設定
package main

import (
    "fmt"
    "github.com/asposecellscloud/asposecellscloud-go/v3"
)

func main() {
    config := asposecellscloud.NewConfiguration()
    config.ClientId = "<client-id>"
    config.ClientSecret = "<client-secret>"
    config.BasePath = "https://api.aspose.cloud"

    api := asposecellscloud.NewAPIClient(config).CellsApi
    resp, _, err := api.PostWorksheetCellSetValue(
        "myWorkbook.xlsx",
        "Sheet1",
        "A3",
        map[string]string{
            "value":   "1234",
            "type":    "string",
            "formula": "SUM(A1,A2)",
        },
        nil,
        nil,
    )
    if err != nil {
        fmt.Println(err)
        return
    }
    fmt.Println(resp.Status)
}
```

{{< /tab >}}

{{< /tabs >}}