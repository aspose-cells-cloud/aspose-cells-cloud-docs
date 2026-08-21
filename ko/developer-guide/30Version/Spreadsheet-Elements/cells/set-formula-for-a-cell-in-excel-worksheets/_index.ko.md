---
title: "Excel 워크시트에서 셀 수식 설정"
type: docs
url: /ko/set-formula-for-a-cell-in-excel-worksheets/
weight: 80
keywords: "Excel, Aspose.Cells, REST API, 수식 설정, 워크시트, 셀, 클라우드 SDK, cURL"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트의 특정 셀에 수식을 설정하는 방법을 배웁니다. cURL 예제, 전체 매개변수 목록, 오류 처리, SDK 코드 샘플이 포함되어 있습니다."
---

이 REST API는 Excel 파일에서 **셀 수식**을 설정합니다.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}
```

## 보안 및 인증

Aspose.Cells Cloud API는 안전하며, [JWT 토큰 기반 인증](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)이 필요합니다.

**요청 매개변수**

| 매개변수 이름 | 유형   | 위치 | 필수 여부 | 설명                                    |
|---------------|--------|------|-----------|-----------------------------------------|
| name          | string | path | Y         | Excel 문서 이름.                        |
| sheetName     | string | path | Y         | 워크시트 이름.                          |
| cellName      | string | path | Y         | 대상 셀 주소 (예: **A1**).             |
| value         | string | query| N         | 셀에 할당할 값.                         |
| type          | string | query| N         | 값의 데이터 유형 (예: **string**).     |
| formula       | string | query| N         | 셀에 적용할 수식 (예: **sum(A1,A2)**). |
| folder        | string | query| N         | 문서가 포함된 폴더.                     |
| storageName   | string | query| N         | 스토리지 서비스 이름.                   |

## **응답**

CellResponse를 반환합니다.

- **응답 필드 개요**

| 필드             | 유형    | 설명                                              |
| ---------------- | ------- | ------------------------------------------------- |
| `Name`           | string  | 셀 주소 (예: `F341`).                             |
| `Row`            | integer | 0부터 시작하는 행 인덱스.                         |
| `Column`         | integer | 0부터 시작하는 열 인덱스.                         |
| `Value`          | string  | 셀에 표시된 값.                                   |
| `Type`           | string  | 셀의 데이터 유형 (예: `IsString`).               |
| `Formula`        | string  | 셀에 수식이 포함된 경우 수식 텍스트.              |
| `IsFormula`      | bool    | 셀에 수식이 포함되어 있는지 여부.                 |
| `IsMerged`       | bool    | 셀이 병합 범위의 일부인지 여부.                   |
| `IsArrayHeader`  | bool    | 셀이 배열 헤더인지 여부.                          |
| `IsInArray`      | bool    | 셀이 배열의 일부인지 여부.                        |
| `IsErrorValue`   | bool    | 셀에 오류 값이 포함되어 있는지 여부.              |
| `IsInTable`      | bool    | 셀이 테이블 내부에 있는지 여부.                   |
| `IsStyleSet`     | bool    | 셀에 스타일이 적용되어 있는지 여부.               |
| `HtmlString`     | string  | 셀 값의 HTML 인코딩 표현.                         |
| `Style/link`     | object  | 스타일 리소스에 대한 하이퍼링크.                  |


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

**HTTP 상태 코드**

| 코드 | 의미                     | 설명                                            |
|------|--------------------------|-------------------------------------------------|
| 200  | OK                       | 필터가 성공적으로 적용됨; 응답에 작업 세부정보 포함. |
| 400  | Bad Request              | 누락되거나 유효하지 않은 매개변수 (예: 지원되지 않는 파일 유형). |
| 401  | Unauthorized             | 유효하지 않거나 누락된 JWT 토큰.                |
| 413  | Payload Too Large        | 업로드된 파일이 크기 제한을 초과함.             |
| 500  | Internal Server Error    | 예기치 않은 서버 오류.                          |

## SDK를 사용한 PostWorksheetCellSetValue API 사용 방법

### PostWorksheetCellSetValue API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetCellSetValue)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스를 호출할 수 있습니다.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

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

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// C# 예제 – 셀에 수식 설정
// <access-token>, <file-name> 등을 실제 값으로 바꾸세요.
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
// Java 예제 – 셀에 수식 설정
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
// PHP 예제 – 셀에 수식 설정
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
# Ruby 예제 – 셀에 수식 설정
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
# Python 예제 – 셀에 수식 설정
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
// Node.js 예제 – 셀에 수식 설정
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
// Android(Java) 예제 – 셀에 수식 설정
// 표준 Java 예제와 유사하나, Android 호환 SDK를 사용해야 합니다.
```

{{< /tab >}}

{{< tab tabNum="8" >}}

**Swift 예제는 제공되지 않습니다**. Swift용 SDK는 현재 개발 중입니다.

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
# Perl 예제 – 셀에 수식 설정
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
// Go 예제 – 셀에 수식 설정
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
---