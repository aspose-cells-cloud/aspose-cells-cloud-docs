---
title: 조건부 서식에 셀 영역 추가
description: Aspose.Cells Cloud REST API(v3.0)를 사용하여 Excel 워크시트의 조건부 서식 규칙에 셀 영역을 추가합니다. 엔드포인트, 매개변수, cURL 예제, SDK 예제, 응답 스키마 및 오류 처리를 포함합니다.
keywords: Aspose.Cells, 조건부 서식, CellArea, REST API, Excel, 클라우드 SDK
weight: 30
aliases:
  - /add-a-cell-area-for-format-condition/
---

# 조건부 서식에 셀 영역 추가

**요약** – 워크시트의 기존 조건부 서식 규칙에 셀 영역을 추가합니다.

---

## 사전 요구 사항

1. **Aspose.Cells Cloud 계정** – **App SID** 및 **App Key**를 획득하세요.  
2. **JWT 토큰** – App SID/Key를 사용하여 JWT 토큰을 생성하세요(자세한 내용은 [인증 가이드](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) 참조).  
3. 대상 Excel 파일이 지정된 스토리지/폴더에 이미 존재해야 합니다.

---

## 인증

모든 요청은 **JWT 토큰 기반 인증**이 필요합니다. 토큰을 `Authorization` 헤더에 전달하세요:

```http
Authorization: Bearer <jwt token>
```

---

## HTTP 요청

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/area
```

### 경로 매개변수

| 이름        | 유형   | 설명                                   |
|-------------|--------|----------------------------------------|
| `name`      | string | Excel 파일 이름(예: `Book1.xlsx`)     |
| `sheetName` | string | 규칙이 포함된 워크시트 이름(예: `Sheet1`) |
| `index`     | integer| 조건부 서식 규칙의 0부터 시작하는 인덱스 |

### 쿼리 매개변수

| 이름            | 유형   | 필수 여부 | 설명                                      |
|-----------------|--------|-----------|-------------------------------------------|
| `cellArea`      | string | **예**    | 추가할 셀 범위(A1 표기법, 예: `A1:C3`)     |
| `folder`        | string | 아니요    | 파일이 저장된 폴더 경로                   |
| `storageName`   | string | 아니요    | 스토리지 서비스 이름                      |

---

## 요청 예시(cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/conditionalFormattings/0/area?cellArea=A1:C3" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

### 예상 성공 응답

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

**응답 스키마 – `CellArea`**

| 속성             | 유형 | 설명                           |
|------------------|------|--------------------------------|
| `StartRow`       | int  | 첫 번째 행의 0부터 시작하는 인덱스 |
| `StartColumn`    | int  | 첫 번째 열의 0부터 시작하는 인덱스 |
| `EndRow`         | int  | 마지막 행의 0부터 시작하는 인덱스  |
| `EndColumn`      | int  | 마지막 열의 0부터 시작하는 인덱스  |

---

**HTTP 상태 코드**

| 코드 | 의미                   | 설명                                      |
|------|------------------------|-------------------------------------------|
| 200  | OK                     | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함 |
| 400  | 잘못된 요청            | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형) |
| 401  | 인증되지 않음          | 잘못되거나 누락된 JWT 토큰                 |
| 413  | 페이로드가 너무 큼     | 업로드된 파일이 크기 제한을 초과함         |
| 500  | 내부 서버 오류         | 예기치 않은 서버 오류                      |

---

## SDK 예제

가장 흔하게 사용되는 SDK에 대한 짧은 코드 스니펫입니다. `YOUR_APP_SID` 및 `YOUR_APP_KEY`를 귀하의 자격 증명으로 바꾸고, 필요한 경우 생성된 JWT 토큰을 설정하세요.

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

## 참고 사항 및 팁

- **CellArea 형식** – 유효한 A1 범위(`A1`, `A1:C3`, `Sheet2!B2:D5`)여야 합니다. 잘못된 형식은 **400 Bad Request**를 반환합니다.
- **중복 영역** – 동일한 규칙의 기존 영역과 겹치는 범위를 추가하면 **409 Conflict**가 발생합니다.
- **0부터 시작하는 인덱싱** – 응답의 행/열 인덱스는 `0`부터 시작합니다. 필요에 따라 Excel의 1부터 시작하는 표기법으로 변환하세요.
- **스토리지** – `folder` 및 `storageName`을 생략하면 API가 기본 스토리지/루트 폴더를 사용합니다.

---

## 관련 작업

- **셀 영역 삭제** – `DELETE /cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/area`
- **조건부 서식에 조건 추가** – `POST /cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/condition`
- **조건부 서식 조회** – `GET /cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}`

이러한 작업을 조합하여 전체 조건부 서식 워크플로우를 구성할 수 있습니다.

---
---