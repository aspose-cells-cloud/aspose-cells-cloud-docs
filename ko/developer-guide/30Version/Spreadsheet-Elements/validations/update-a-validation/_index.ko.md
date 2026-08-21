---
title: "Excel 워크시트에서 유효성 검사 업데이트"
second_title: "문서"
linktitle: "업데이트"
type: docs
url: /validations/update/
keywords: "Aspose.Cells Cloud, Excel 유효성 검사 업데이트, REST API, 워크시트 유효성 검사, Excel API"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 파일의 워크시트 유효성 검사를 업데이트하는 방법으로, cURL 예제 및 여러 프로그래밍 언어의 SDK 코드 스니펫을 제공합니다."
weight: 10
ArticleTitle: "Aspose.Cells Cloud API를 사용한 워크시트 유효성 검사 업데이트"
---

이 REST API는 Excel 워크시트에서 인덱스를 기준으로 워크시트 유효성 검사를 업데이트합니다.

이 엔드포인트를 호출하기 전에, 적절한 범위(예: `Cells.ReadWrite`)가 포함된 JWT 액세스 토큰을 획득한 후, 아래 예제와 같이 `Authorization` 헤더에 토큰을 포함시켜야 합니다.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations/{validationIndex}
```

### **요청 매개변수**

| 매개변수 이름     | 유형     | 위치   | 설명                                                       |
| ---------------- | ------- | ------ | ---------------------------------------------------------- |
| name             | string  | path   | 워크북 파일의 이름입니다.                                 |
| sheetName        | string  | path   | 유효성 검사가 포함된 워크시트의 이름입니다.               |
| validationIndex  | integer | path   | 업데이트할 유효성 검사의 0부터 시작하는 인덱스입니다.      |
| validation       | object  | body   | 업데이트된 유효성 검사 설정을 정의하는 JSON 객체입니다.    |
| folder           | string  | query  | 워크북이 위치한 클라우드 스토리지의 폴더입니다.            |
| storageName      | string  | query  | 스토리지 서비스의 이름(사용자 정의 스토리지를 사용하는 경우)입니다. |

<a href="https://apireference.aspose.cloud/cells/#/WorksheetValidations/PostWorksheetValidation" target="_blank" rel="noopener noreferrer">OpenAPI 사양</a>은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스를 쉽게 호출할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API에 호출을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations/0" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{ "AlertStyle":"Warning" }'
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

**가능한 HTTP 상태 코드**

| 코드 | 의미                                  | 설명 |
|------|---------------------------------------|------|
| 200  | OK                                    | 유효성 검사가 성공적으로 업데이트되었습니다. |
| 400  | Bad Request                           | 요청이 잘못되었거나 필수 매개변수가 누락되었습니다. |
| 401  | Unauthorized                          | JWT 토큰이 잘못되었거나 누락되었습니다. |
| 403  | Forbidden                             | 토큰에 필요한 범위가 충분하지 않습니다. |
| 404  | Not Found                             | 지정된 워크북, 워크시트 또는 유효성 검사 인덱스가 존재하지 않습니다. |
| 500  | Internal Server Error                 | 서버에서 예기치 않은 오류가 발생했습니다. |

오류 처리에 대한 자세한 내용은 <a href="https://apireference.aspose.cloud/cells/#/Errors" target="_blank" rel="noopener noreferrer">Aspose.Cells Cloud 오류 문서</a>를 참조하십시오.

새 유효성 검사 추가 또는 기존 유효성 검사 삭제와 같은 관련 작업도 확인해 보시기 바랍니다:

- [워크시트 유효성 검사 추가](https://docs.aspose.cloud/cells/validations/add/)
- [워크시트 유효성 검사 삭제](https://docs.aspose.cloud/cells/validations/delete/)

## 클라우드 SDK 패밀리

SDK를 사용하면 가장 빠르게 개발할 수 있습니다. SDK는 저수준 세부 사항을 추상화하여 비즈니스 로직에 집중할 수 있도록 합니다. Aspose.Cells Cloud SDK 전체 목록은 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 저장소</a>를 확인하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}