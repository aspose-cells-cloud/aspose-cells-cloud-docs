---
title: "워크시트 유효성 검사 모두 삭제하기 – Aspose.Cells Cloud API"
second_title: "문서"
linktype: "삭제"
type: docs
url: /validations/clear/
keywords: "Aspose.Cells Cloud, 워크시트 유효성 검사 삭제, Excel, REST API, 스프레드시트 유효성 검사, API"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 파일의 워크시트에서 모든 데이터 유효성 검사 규칙을 제거합니다. 인증 단계, 요청 세부 정보, cURL 예제, 응답 스키마, 오류 처리, SDK 스니펫이 포함됩니다."
weight: 10
---

**사전 요구 사항**

- 유효한 Aspose Cloud 계정.
- Aspose Cloud 인증 API(`/connect/token`)를 통해 획득한 JWT 액세스 토큰.
- 워크북은 Aspose Cloud 스토리지에 저장되어 있어야 하며, 또는 적절한 `folder`/`storageName` 쿼리 매개변수를 제공해야 합니다.

이 REST API는 Excel 워크시트의 모든 워크시트 유효성 검사를 삭제합니다.

## REST API

```bash
DELETE http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations
```

### **요청 매개변수**

| 매개변수 이름 | 유형   | 위치 | 설명                                               |
| -------------- | ------ | -------- | ----------------------------------------------------- |
| name           | string | path     | Excel 문서의 이름입니다.                       |
| sheetName      | string | path     | 유효성 검사가 포함된 워크시트의 이름입니다. |
| folder         | string | query    | 문서가 저장된 폴더입니다.              |
| storageName    | string | query    | 스토리지 서비스의 이름입니다.                      |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/WorksheetValidations/DeleteWorksheetValidation)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 JWT 토큰을 획득한 후 cURL로 API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### 오류 처리

| HTTP 상태 코드 | 의미                 | 설명                                              |
| ----------- | --------------------- | -------------------------------------------------------- |
| 400         | 잘못된 요청           | 요청이 잘못된 형식이거나 필수 매개변수가 누락되었습니다. |
| 401         | 인증되지 않음          | JWT 토큰이 누락되었거나 유효하지 않거나 만료되었습니다.           |
| 404         | 찾을 수 없음             | 지정된 워크북 또는 워크시트가 존재하지 않습니다.      |
| 500         | 내부 서버 오류         | 서버 측에서 예기치 않은 오류가 발생했습니다.         |

오류 페이로드는 동일한 JSON 구조를 따르며, `Code` 및 `Message` 필드를 포함합니다. 예를 들면 다음과 같습니다:

```json
{
  "Code": 401,
  "Message": "Invalid or expired token."
}
```

## 클라우드 SDK 패밀리

SDK를 사용하면 가장 빠르게 개발할 수 있습니다. SDK는 저수준 세부 사항을 추상화하여 비즈니스 로직에 집중할 수 있도록 합니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetValidations.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetValidations.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetValidations.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetValidations.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetValidations.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetValidations.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetValidations.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetValidations.go" >}}

{{< /tab >}}

{{< /tabs >}}