---
title: "엑셀 워크시트에서 인덱스로 유효성 검사 가져오기"
second_title: "문서"
linktitle: "가져오기"
type: docs
url: /ko/validations/get/
aliases: [  /ko/get-validation-from-a-worksheet/ ]
keywords: "Aspose.Cells Cloud, 워크시트 유효성 검사 API, 인덱스로 유효성 검사 가져오기, Excel REST API, Aspose.Cells SDK"
description: "Aspose.Cells Cloud API(v3.0)를 사용하여 엑셀 워크북에서 유효성 검사를 0부터 시작하는 인덱스로 검색합니다. cURL 예제, 응답 스키마, 오류 코드, C#, Java, Python 등 다양한 언어의 SDK 코드 스니펫이 포함됩니다."
weight: 10
---

이 REST API는 엑셀 워크시트에서 인덱스를 기준으로 유효성 검사를 가져옵니다.  
엔드포인트를 호출하기 전에 `/connect/token` 엔드포인트를 통해 JWT 토큰을 획득하고, 이를 `Authorization` 헤더에 `Bearer <jwt token>` 형식으로 포함시켜야 합니다.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations/{validationIndex}
```

### **요청 매개변수**

| 매개변수 이름     | 타입     | 위치   | 설명                                         |
| ---------------- | ------- | ------ | -------------------------------------------- |
| name             | string  | path   | 워크북 파일의 이름입니다.                    |
| sheetName        | string  | path   | 워크시트의 이름입니다.                       |
| validationIndex  | integer | path   | 가져올 유효성 검사의 0부터 시작하는 인덱스입니다. |
| folder           | string  | query  | 워크북이 포함된 폴더입니다.                  |
| storageName      | string  | query  | 저장소 서비스의 이름입니다.                  |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/WorksheetValidations/GetWorksheetValidation)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Validation": {
    "AlertStyle": "Stop",
    "AreaList": [
      {
        "EndColumn": 0,
        "EndRow": 0,
        "StartColumn": 0,
        "StartRow": 0
      },
      {
        "EndColumn": 27,
        "EndRow": 0,
        "StartColumn": 26,
        "StartRow": 0
      }
    ],
    "IgnoreBlank": false,
    "InCellDropDown": false,
    "Operator": "None",
    "ShowError": false,
    "ShowInput": false,
    "Type": "AnyValue",
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/Validations/0",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**응답 스키마**

| 필드           | 타입    | 설명                                                             |
| ------------- | ------- | ---------------------------------------------------------------- |
| AlertStyle    | string  | 사용자에게 표시되는 경고 스타일(Stop, Warning, Information)입니다. |
| AreaList      | array   | 유효성 검사가 적용되는 셀 범위들의 컬렉션입니다.                 |
| IgnoreBlank   | boolean | `true`인 경우, 유효성 검사 시 빈 셀을 무시합니다.                 |
| InCellDropDown| boolean | `true`인 경우, 셀에 드롭다운 목록이 표시됩니다.                   |
| Operator      | string  | 유효성 검사에 사용되는 비교 연산자(`None`, `Between` 등)입니다.   |
| ShowError     | boolean | 유효성 검사 실패 시 오류 메시지를 표시할지 여부입니다.            |
| ShowInput     | boolean | 셀이 선택되었을 때 입력 메시지를 표시할지 여부입니다.             |
| Type          | string  | 유효성 검사 유형(`AnyValue`, `WholeNumber`, `Decimal` 등)입니다. |
| link.Href     | string  | 유효성 검사 리소스에 대한 자기 참조 URL입니다.                    |
| link.Rel      | string  | 관계 유형(항상 `self`)입니다.                                     |

**가능한 오류 코드**

| HTTP 상태 코드 | 의미                                                             |
| ------------- | ---------------------------------------------------------------- |
| 200           | 유효성 검사를 성공적으로 가져왔습니다.                            |
| 400           | 잘못된 요청 – 누락되거나 잘못된 매개변수가 있습니다.             |
| 401           | 인증 실패 – 잘못되거나 누락된 JWT 토큰입니다.                    |
| 404           | 없음 – 워크북, 워크시트 또는 유효성 검사 인덱스가 존재하지 않습니다.|
| 500           | 내부 서버 오류 – 예기치 않은 조건입니다.                         |

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 Aspose.Cells Cloud에 대한 개발을 수행하는 가장 빠른 방법입니다. SDK는 저수준 세부 사항을 추상화하여 비즈니스 로직에 집중할 수 있도록 도와줍니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}