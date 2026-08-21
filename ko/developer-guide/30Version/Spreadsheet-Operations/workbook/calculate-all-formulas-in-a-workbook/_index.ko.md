---
title: "Excel 워크북의 모든 수식 계산"
second_title: "문서"
linktitle: "계산"
type: docs
url: /calculate-all-formulas-on-an-excel-file/
aliases:
  [/calculate-all-formulas-in-a-workbook/, /workbook/calculate-all-formulas/]
keywords: "Aspose.Cells, 수식 계산, Excel API, 클라우드 SDK"
description: "Aspose.Cells Cloud REST API를 통해 Excel 워크북의 모든 수식을 계산합니다. cURL 예제, 요청 매개변수, 응답 스키마, 사전 조건, 다수 언어의 SDK 스니펫을 포함합니다."
weight: 140
ArticleTitle: "Excel 워크북의 모든 수식 계산"
---

이 REST API는 Excel 워크북의 **모든 수식**을 계산합니다.

**사전 조건:** 이 엔드포인트를 호출하기 전에 다음을 확인하십시오:
- 유효한 JWT 인증 토큰. ([인증 가이드](/authentication/) 참조)  
- Aspose.Cells Cloud 클라이언트 ID 및 비밀번호.  
- 대상 워크북이 지정된 저장소 위치에 업로드되어 있음. ([저장소 설정](/storage/) 참조)

## PostWorkbookCalculateFormula API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/calculateformula
```

요청 매개변수는 다음과 같습니다:

| 매개변수 이름    | 유형                 | 위치   | 설명                                                                 |
| --------------- | -------------------- | ------ | ------------------------------------------------------------------- |
| **name**        | string               | path   | 워크북 파일 이름.                                                     |
| **options**     | CalculationOptions   | body   | 계산 설정을 지정하는 JSON 객체(예: `CalcStackSize`, `IgnoreError`). |
| **ignoreError** | boolean              | query  | `true`인 경우 계산 중 발생하는 오류를 무시합니다.                      |
| **folder**      | string               | query  | 워크북이 포함된 폴더 경로.                                            |
| **storageName** | string               | query  | 워크북이 저장된 저장소 서비스 이름.                                   |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookCalculateFormula)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/calculateformula?ignoreError=true" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt 토큰>" \
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

#### 응답 세부 정보

| 필드              | 유형   | 설명                                                         |
| ---------------- | ------ | ------------------------------------------------------------ |
| **Code**         | int    | HTTP 유사 상태 코드(200은 성공을 나타냄).                       |
| **Status**       | string | 결과의 짧은 텍스트 설명(예: `OK`).                            |
| **WorkbookUrl**  | string | 업데이트된 워크북을 다운로드할 수 있는 직접 URL.               |
| **ErrorMessage** | string | 요청 실패 시 상세 오류 정보; 성공 시 `null`.                   |

#### 다음 단계 / 일반적인 오류

- **계산 오류 처리** – 수식을 평가할 수 없는 경우 오류 응답을 받으려면 `ignoreError=false`로 설정합니다.
- **속도 제한 인식** – `X-RateLimit-Remaining` 헤더를 확인합니다. 값이 `0`에 도달하면 재시도 전에 대기합니다.
- **HTTP 상태 코드 안내**:
  - `400` – 잘못된 요청 매개변수.
  - `401` – 인증 실패(유효하지 않거나 만료된 JWT).
  - `404` – 워크북을 찾을 수 없음.
  - `500` – 서버 측 오류; 지속될 경우 Aspose 지원팀에 문의.

| 코드 | 의미               | 발생 시점                                               |
|------|-------------------|--------------------------------------------------------|
| 400  | 잘못된 요청        | 잘못된 요청 매개변수 또는 잘못된 형식의 JSON.           |
| 401  | 인증되지 않음      | JWT 토큰 누락, 유효하지 않거나 만료됨.                   |
| 404  | 찾을 수 없음       | 지정된 워크북이 저장소에 존재하지 않음.                 |
| 500  | 내부 서버 오류     | 예기치 않은 서버 측 실패; Aspose 지원팀에 문의.           |

## 클라우드 SDK 패밀리

SDK를 사용하면 개발 속도를 최대한 빠르게 할 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

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