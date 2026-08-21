---
title: "Aspose.Cells Cloud API – 차트 값 축 업데이트(POST /valueaxis)"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트의 차트 값 축을 업데이트합니다. 엔드포인트, 매개변수, 요청 본문 스키마, 예제(cURL 및 SDK), 응답 및 오류 처리가 포함됩니다."
keywords:
  - Aspose.Cells Cloud
  - 차트 값 축 업데이트
  - REST API
  - Excel 차트 축
  - POST valueaxis
  - cURL 예제
  - SDK
  - JSON 페이로드
  - 차트 축 설정
last_updated: 2026-07-30
---

# 차트 값 축 업데이트 (POST /valueaxis)

**요약:**  
Aspose Cloud 스토리지에 저장된 Excel 워크북의 특정 차트 값 축을 수정합니다. 단일 요청으로 범위, 눈금 단위, 로그 스케일링 및 기타 축 속성을 설정할 수 있습니다.

---

## 사전 조건

1. **JWT 액세스 토큰** – [인증 가이드](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)에 설명된 대로 토큰을 획득합니다.  
2. 대상 **워크북**은 이미 Aspose Cloud 스토리지(또는 기본 스토리지)에 업로드되어 있어야 합니다.  
3. 수정하려는 워크시트 이름과 **0부터 시작하는 차트 인덱스**를 알고 있어야 합니다.

---

## 엔드포인트

```
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis
```

*플레이스홀더를 실제 값으로 바꿉니다.*

| 플레이스홀더 | 설명 |
|-------------|-------------|
| `{name}` | Excel 파일 이름(예: `Book1.xlsx`). |
| `{sheetName}` | 차트가 포함된 워크시트(예: `Sheet1`). |
| `{chartIndex}` | 업데이트할 차트의 0부터 시작하는 인덱스(예: `0`). |

---

## 인증

이 API는 **JWT 토큰 기반 인증**을 사용합니다. 토큰을 `Authorization` 헤더에 포함합니다:

```
Authorization: Bearer <jwt token>
```

---

### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

## 요청 매개변수

| 이름          | 위치 | 유형   | 필수 여부 | 설명 |
|---------------|------|--------|----------|-------------|
| **name**      | 경로 | string | 예       | 클라우드에 저장된 Excel 파일 이름. |
| **sheetName** | 경로 | string | 예       | 차트를 보유한 워크시트. |
| **chartIndex**| 경로 | int    | 예       | 업데이트할 차트의 0부터 시작하는 인덱스. |
| **axis**      | 본문 | object | 예       | 축 설정(자세한 내용은 *요청 본문 스키마* 참조). |
| **folder**    | 쿼리 | string | 아니요   | 파일이 위치한 클라우드 폴더 경로. |
| **storageName**| 쿼리 | string | 아니요   | 사용할 스토리지 서비스 이름. |

---

## 요청 본문 스키마 (`axis` 객체)

변경하려는 속성만 포함하면 됩니다.

| 속성           | 유형    | 필수 여부 | 설명 |
|----------------|---------|----------|-------------|
| `minimum`      | number  | 아니요   | 축의 하한값. |
| `maximum`      | number  | 아니요   | 축의 상한값. |
| `majorUnit`    | number  | 아니요   | 주요 눈금 간격. |
| `minorUnit`    | number  | 아니요   | 부次要 눈금 간격. |
| `logBase`      | number  | 아니요   | `isLogarithmic`가 `true`일 때 사용할 로그 밑수. |
| `isLogarithmic`| boolean | 아니요   | 축이 로그 스케일을 사용하는지 여부. |
| `displayUnit`  | string  | 아니요   | 축에 표시되는 단위 레이블(예: `"Thousands"`). |
| `tickMark`     | string  | 아니요   | 눈금 스타일(`"inside"`, `"outside"` 등). |
| `crossAt`      | number  | 아니요   | 축이 수직 축과 교차하는 위치. |

### 요청 본문 예제

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

## 요청 예제

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

### SDK 샘플  

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
// Node.js 예제
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
// Android(Java) 예제
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

## 응답

### 성공 (200)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

응답 유형은 `CellsCloudResponse`입니다.

**HTTP 상태 코드**

| 코드 | 의미                         | 설명                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함. |
| 400  | Bad Request                 | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형). |
| 401  | Unauthorized                | 잘못되거나 누락된 JWT 토큰. |
| 413  | Payload Too Large           | 업로드된 파일이 크기 제한을 초과함. |
| 500  | Internal Server Error       | 예기치 않은 서버 오류. |
---

## 추가 자료

- **OpenAPI 사양** – [JSON-YAML 보기 / 다운로드](https://apireference.aspose.cloud/cells/#/Charts/PostChartValueAxis)  
- **SDK 저장소** – <https://github.com/aspose-cells-cloud>  
- **인증 가이드** – <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>

---

*질문이나 피드백이 있으시면 Aspose.Cells Cloud 지원팀에 문의해 주세요.*