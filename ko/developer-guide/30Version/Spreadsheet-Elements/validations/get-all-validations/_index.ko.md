---
title: "엑셀 워크시트에서 모든 유효성 검사 규칙 가져오기"
second_title: "문서"
linktitle: "모두 가져오기"
type: docs
url: /ko/validations/get-all/
keywords: "Aspose.Cells Cloud, 엑셀, 워크시트 유효성 검사, REST API, 모든 유효성 검사 가져오기, SDK"
description: "Aspose.Cells Cloud REST API를 사용하여 엑셀 워크시트에서 모든 유효성 검사 규칙을 가져옵니다. 다양한 SDK(C#, Java, PHP, Ruby, Node.js, Python, Perl, Go)를 지원하여 빠른 통합이 가능합니다."
weight: 10
---

워크시트 유효성 검사를 사용하면 셀에 입력될 수 있는 데이터 유형 또는 범위를 제한하는 규칙을 정의할 수 있습니다. 일반적으로 데이터 무결성을 보장하기 위해, 예를 들어 입력을 특정 값 목록, 특정 범위 내의 날짜, 또는 숫자 제한으로 제한하는 데 사용됩니다.

이 REST API는 엑셀 워크시트의 모든 유효성 검사 규칙을 가져옵니다.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations
```

### **요청 매개변수**

| 매개변수 이름 | 유형   | 위치 | 설명                                     |
| ------------- | ------ | ---- | ---------------------------------------- |
| name          | string | path | 엑셀 문서의 이름입니다.                 |
| sheetName     | string | path | 워크시트의 이름입니다.                  |
| folder        | string | query | 문서가 저장된 폴더 경로입니다.          |
| storageName   | string | query | 스토리지 서비스의 이름입니다.           |

**응답 상태 코드**

| 코드 | 설명                                     |
|------|------------------------------------------|
| 200  | 요청 성공 – 유효성 검사 목록             |
| 401  | 인증 실패 – 잘못되거나 누락된 토큰      |
| 404  | 없음 – 문서 또는 워크시트가 없습니다.   |
| 500  | 내부 서버 오류                           |

[OpenAPI 사양서](https://apireference.aspose.cloud/cells/#/WorksheetValidations/GetWorksheetValidations)는 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells Cloud 웹 서비스에 쉽게 액세스할 수 있습니다. **사전 조건:** `Authorization` 헤더에 유효한 JWT 토큰을 포함해야 합니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "validations": [
    {
      "name": "Validation1",
      "type": "WholeNumber",
      "operator": "Between",
      "formula1": "1",
      "formula2": "100",
      "showErrorMessage": true,
      "errorMessage": "값은 1에서 100 사이여야 합니다."
    },
    {
      "name": "Validation2",
      "type": "List",
      "formula1": "\"Option1,Option2,Option3\"",
      "showErrorMessage": true,
      "errorMessage": "목록에서 값을 선택하세요."
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## 클라우드 SDK 패밀리

SDK를 사용하면 개발 속도를 최대한 높일 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetValidations.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetValidations.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetValidations.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetValidations.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetValidations.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetValidations.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetValidations.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetValidations.go" >}}

{{< /tab >}}

{{< /tabs >}}