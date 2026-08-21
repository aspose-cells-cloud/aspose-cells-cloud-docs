---
title: 조건부 서식에 조건 추가
description: Aspose.Cells Cloud REST API(v3.0)를 사용하여 워크시트의 조건부 서식에 조건을 추가하는 방법을 알아보세요. 엔드포인트, 매개변수, 인증, cURL 예제, SDK 코드 조각, 오류 처리를 포함합니다.
keywords: "Aspose.Cells Cloud, 조건부 서식, 조건 추가, REST API, Excel, 워크시트"
type: docs
url: /conditional-formattings/add-a-condition/
aliases:
  - /add-a-condition-for-format-condition/
weight: 40
---

# 조건부 서식에 조건 추가

Aspose.Cells Cloud REST API(v3.0)를 사용하여 워크시트의 기존 조건부 서식 규칙에 조건을 추가합니다.

---

## 사전 요구 사항

| 요구 사항 | 세부 정보 |
|-----------|-----------|
| **인증** | OAuth 2.0 흐름을 통해 얻은 유효한 JWT 액세스 토큰(Bearer) |
| **API 버전** | v3.0 – 엔드포인트 URL에 `/v3.0/`이 포함됩니다. |
| **스토리지** | 워크북은 Aspose.Cells Cloud에서 접근 가능한 위치에 있어야 합니다(기본값은 `Default`). |
| **권한** | 대상 워크북에 대한 읽기/쓰기 권한 |
| **지원되는 형식** | Aspose.Cells에서 지원하는 모든 워크북 형식(예: `.xlsx`, `.xls`, `.xlsm`) |

---

## 엔드포인트

**HTTP 메서드:** `PUT`  
**URL:**  

```
https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/condition
```

| 매개변수 | 위치 | 유형 | 필수 여부 | 설명 |
|----------|------|------|-----------|------|
| `name` | 경로(path) | string | **필수** | 워크북 파일 이름(확장자 포함) |
| `sheetName` | 경로(path) | string | **필수** | 조건부 서식이 포함된 워크시트 이름 |
| `index` | 경로(path) | integer | **필수** | 수정할 조건부 서식 컬렉션의 0부터 시작하는 인덱스 |
| `type` | 쿼리(query) | string | **필수** | 조건 유형. 허용되는 값: `CellValue`, `Expression`, `ColorScale`, `DataBar`, `IconSet`, `Top10`, `UniqueValues`, `DuplicateValues`, `ContainsText`, `NotContainsText`, `BeginsWith`, `EndsWith`, `ContainsBlanks`, `NotContainsBlanks`, `ContainsErrors`, `NotContainsErrors`, `TimePeriod`, `AboveAverage` |
| `operatorType` | 쿼리(query) | string | **필수** | 조건에 대한 연산자. 허용되는 값: `Between`, `Equal`, `GreaterThan`, `GreaterOrEqual`, `LessThan`, `None`, `NotBetween`, `NotEqual` |
| `formula1` | 쿼리(query) | string | **필수** | 조건과 관련된 첫 번째 수식/값 |
| `formula2` | 쿼리(query) | string | 아니요 | 두 번째 수식/값(두 개의 값을 필요로 하는 연산자, 예: `Between`에만 필요) |
| `folder` | 쿼리(query) | string | 아니요 | 워크북이 위치한 스토리지 폴더 |
| `storageName` | 쿼리(query) | string | 아니요 | 스토리지 서비스 이름 |

> **참고:** 모든 경로 매개변수(`name`, `sheetName`, `index`) 및 쿼리 매개변수 `type`, `operatorType`, `formula1`은 필수입니다. `formula2`, `folder`, `storageName`은 선택 사항입니다.

---

## 요청 예제(cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/conditionalFormattings/0/condition?type=CellValue&operatorType=Equal&formula1=v1&formula2=v2" \
 -X PUT \
 -H "Content-Type: application/json" \
 -H "Accept: application/json" \
 -H "Authorization: Bearer <jwt_token>"
```

*`<jwt_token>`을 유효한 액세스 토큰으로 바꾸고, 필요에 따라 `name`, `sheetName`, `index`, 쿼리 값들을 조정하세요.*

---

## 성공 응답

```json
{
  "Code": "200",
  "Status": "OK"
}
```

응답은 조건이 성공적으로 추가되었음을 나타냅니다. 이 작업은 HTTP 상태 코드와 간단한 상태 메시지를 포함하는 일반적인 `CellsCloudResponse` 객체를 반환합니다.

---

## 오류 응답

| HTTP 코드 | 원인 | 예시 본문 |
|-----------|------|-----------|
| **400** | 잘못된 요청 — 누락되거나 유효하지 않은 매개변수 | `{ "Code":"400", "Message":"Invalid parameter value." }` |
| **401** | 인증되지 않음 — 누락되거나 유효하지 않은 JWT 토큰 | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404** | 찾을 수 없음 — 워크북, 워크시트 또는 조건부 서식 인덱스가 존재하지 않음 | `{ "Code":"404", "Message":"File not found." }` |
| **500** | 내부 서버 오류 — 예기치 않은 서버 실패 | `{ "Code":"500", "Message":"An unexpected error occurred." }` |

---

## 참고 사항 및 일반적인 오류

* **매개변수 인코딩** — `formula1`/`formula2`에 포함된 특수 문자는 URL 인코딩해야 합니다(예: 공백 → `%20`).  
* **연산자 호환성** — 일부 연산자(예: `Between`)는 `formula1`과 `formula2` 모두를 필요로 합니다. 단일 값을 필요로 하는 연산자의 경우 `formula2`를 생략하세요.  
* **조건부 서식 인덱스** — 인덱스는 0부터 시작합니다. 정확한 인덱스를 모를 경우 **조건부 서식 가져오기** 엔드포인트를 사용해 확인하세요.  
* **스토리지 폴더** — 워크북이 기본 폴더가 아닌 다른 폴더에 있는 경우, `folder` 쿼리 매개변수를 지정해야 합니다. 지정하지 않으면 API는 루트 폴더로 가정합니다.  
* **요청 제한** — Aspose.Cells Cloud는 계정당 요청 제한을 적용합니다. 429 응답을 받은 경우, 일정 시간 후에 다시 시도하세요.  

---

## SDK 예제

아래는 가장 인기 있는 SDK에 대한 실행 가능한 코드 조각입니다. 자리 표시자 값(`YOUR_FILE`, `YOUR_SHEET` 등)을 실제 데이터로 바꾸세요.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

class Program
{
    static void Main()
    {
        var apiInstance = new ConditionalFormattingsApi();
        string name = "Book1.xlsx";
        string sheetName = "Sheet1";
        int index = 0;
        string type = "CellValue";
        string operatorType = "Equal";
        string formula1 = "v1";
        string formula2 = "v2";
        string folder = null;          // optional
        string storageName = null;     // optional

        try
        {
            var response = apiInstance.PutWorksheetFormatConditionCondition(
                name, sheetName, index, type, operatorType, formula1, formula2, folder, storageName);
            Console.WriteLine($"Status: {response.Status}");
        }
        catch (Exception e)
        {
            Console.WriteLine("Exception when calling ConditionalFormattingsApi.PutWorksheetFormatConditionCondition: " + e.Message);
        }
    }
}
```

### Java

```java
import com.aspose.cloud.cells.api.ConditionalFormattingsApi;
import com.aspose.cloud.cells.model.CellsCloudResponse;

public class AddConditionExample {
    public static void main(String[] args) {
        ConditionalFormattingsApi api = new ConditionalFormattingsApi();

        String name = "Book1.xlsx";
        String sheetName = "Sheet1";
        int index = 0;
        String type = "CellValue";
        String operatorType = "Equal";
        String formula1 = "v1";
        String formula2 = "v2";

        try {
            CellsCloudResponse resp = api.putWorksheetFormatConditionCondition(
                    name, sheetName, index, type, operatorType, formula1, formula2, null, null);
            System.out.println("Response: " + resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### Node.js

```javascript
const { ConditionalFormattingsApi, ApiClient } = require('asposecellscloud');
const api = new ConditionalFormattingsApi();

const name = "Book1.xlsx";
const sheetName = "Sheet1";
const index = 0;
const type = "CellValue";
const operatorType = "Equal";
const formula1 = "v1";
const formula2 = "v2";

api.putWorksheetFormatConditionCondition(
    name,
    sheetName,
    index,
    type,
    operatorType,
    formula1,
    formula2,
    null,
    null
).then((response) => {
    console.log('Status:', response.body.Status);
}).catch((err) => {
    console.error(err);
});
```

### Ruby

```ruby
require 'aspose_cells_cloud'

api_instance = AsposeCellsCloud::ConditionalFormattingsApi.new
name = 'Book1.xlsx'
sheet_name = 'Sheet1'
index = 0
type = 'CellValue'
operator_type = 'Equal'
formula1 = 'v1'
formula2 = 'v2'

begin
  result = api_instance.put_worksheet_format_condition_condition(
    name, sheet_name, index, type, operator_type, formula1, formula2, nil, nil
  )
  puts "Status: #{result.status}"
rescue AsposeCellsCloud::ApiError => e
  puts "Exception when calling ConditionalFormattingsApi->put_worksheet_format_condition_condition: #{e}"
end
```

### Perl

```perl
use AsposeCellsCloud::ConditionalFormattingsApi;

my $api_instance = AsposeCellsCloud::ConditionalFormattingsApi->new();

my $name         = 'Book1.xlsx';
my $sheet_name   = 'Sheet1';
my $index        = 0;
my $type         = 'CellValue';
my $operatorType = 'Equal';
my $formula1     = 'v1';
my $formula2     = 'v2';

eval {
    my $result = $api_instance->put_worksheet_format_condition_condition(
        name => $name,
        sheet_name => $sheet_name,
        index => $index,
        type => $type,
        operator_type => $operatorType,
        formula1 => $formula1,
        formula2 => $formula2,
        folder => undef,
        storage_name => undef
    );
    print "Status: " . $result->{status} . "\n";
};
if ($@) {
    warn "Exception when calling ConditionalFormattingsApi->put_worksheet_format_condition_condition: $@\n";
}
```

### Go

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    cfg := sdk.NewConfiguration()
    cfg.AccessToken = "YOUR_JWT_TOKEN"
    api := sdk.NewConditionalFormattingsApi(cfg)

    name := "Book1.xlsx"
    sheetName := "Sheet1"
    index := int32(0)
    condType := "CellValue"
    operatorType := "Equal"
    formula1 := "v1"
    formula2 := "v2"

    resp, _, err := api.PutWorksheetFormatConditionCondition(
        name, sheetName, index, condType, operatorType, formula1, formula2, nil, nil,
    )
    if err != nil {
        fmt.Printf("Error: %v\n", err)
        return
    }
    fmt.Printf("Status: %s\n", resp.Status)
}
```

> **누락된 SDK** — 필요한 언어 SDK가 목록에 없는 경우, 일반적인 **API 참조**를 참고하여 HTTP 요청을 수동으로 구성하세요.

---

## 참고 자료

- **[조건부 서식 가져오기](https://docs.aspose.cloud/cells/conditional-formattings/get-conditional-formattings/)** – 워크시트의 조건부 서식 규칙 목록을 조회합니다.  
- **[조건부 서식 삭제](https://docs.aspose.cloud/cells/conditional-formattings/delete-a-conditional-formatting/)** – 기존 조건부 서식 규칙을 제거합니다.  
- **[OpenAPI 명세서](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/PutWorksheetFormatConditionCondition)** – 이 작업의 전체 기계 판독 가능 정의입니다.  

---