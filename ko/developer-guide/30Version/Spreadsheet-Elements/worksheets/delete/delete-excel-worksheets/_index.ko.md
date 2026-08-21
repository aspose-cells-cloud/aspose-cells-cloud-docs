---
title: "여러 개의 Excel 워크시트 삭제"
second_title: "문서"
linktitle: "여러 워크시트"
type: docs
url: /ko/worksheets/delete-multiple/
aliases: [  /ko/delete-excel-worksheets/ ]
keywords: "Aspose.Cells Cloud, 여러 워크시트 삭제, Excel API, REST API, v3.0, 워크시트 삭제"
description: "Aspose.Cells Cloud REST API(v3.0)를 사용하여 Excel 워크북에서 여러 워크시트를 삭제하는 방법을 알아보세요. 안전한 HTTPS 엔드포인트, 필요한 매개변수, 수정된 cURL 예제, 다양한 프로그래밍 언어의 SDK 스니펫이 포함됩니다."
weight: 20
ArticleTitle: "Aspose.Cells Cloud REST API를 사용하여 여러 Excel 워크시트 삭제하기"
---

이 REST API는 워크북에서 여러 워크시트를 삭제합니다.

## 보안 및 인증
Aspose.Cells Cloud API는 [JWT 토큰 기반 인증](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)이 필요하며, 안전하게 설계되었습니다.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets
```

### **요청 매개변수**

| 매개변수 이름 | 타입   | 위치 | 설명                                                                 |
| -------------- | ------ | -------- | --------------------------------------------------------------------------- |
| name           | string | path     | Excel 파일의 이름.                                                 |
| matchCondition | object | body     | 삭제할 워크시트를 지정하는 `MatchConditionRequest` 객체. |
| folder         | string | query    | 파일이 위치한 저장소 내 폴더 경로.                           |
| storageName    | string | query    | 저장소 서비스의 이름.                                                |

**MatchConditionRequest 속성**

| 이름                | 타입     | 설명                                  | 비고    |
| ------------------- | -------- | -------------------------------------------- | -------- |
| RegexPattern        | string   | 워크시트 이름과 일치시킬 정규 표현식. | 선택 사항 |
| FullMatchConditions | string[] | 삭제할 정확한 워크시트 이름 목록.         | 선택 사항 |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheets)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예제는 cURL을 사용하여 Cloud API에 요청하는 방법을 보여줍니다. **`Authorization` 헤더에 유효한 JWT 토큰이 필요합니다.**

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets?folder=Temp" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>" \
  -d '{"FullMatchConditions":["Sheet1","Sheet2","Sheet3"]}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

요청은 다음과 같은 일반적인 오류 응답도 반환할 수 있습니다:

| HTTP 상태 코드 | 의미                                      | 예시 페이로드                                           |
| ----------- | -------------------------------------------- | -------------------------------------------------------- |
| 400         | 잘못된 요청 – 유효하지 않은 JSON 또는 매개변수     | `{"Code":400,"Message":"Invalid request payload."}`      |
| 401         | 인증되지 않음 – 누락되거나 유효하지 않은 JWT 토큰  | `{"Code":401,"Message":"Authentication failed."}`        |
| 403         | 권한 없음 – 부족한 권한                         | `{"Code":403,"Message":"Access denied."}`                |
| 404         | 찾을 수 없음 – 파일 또는 워크시트가 존재하지 않음 | `{"Code":404,"Message":"Resource not found."}`           |
| 500         | 내부 서버 오류                        | `{"Code":500,"Message":"An unexpected error occurred."}` |

{{< /tab >}}

{{< /tabs >}}

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 요청하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheets.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheets.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheets.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheets.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheets.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheets.go" >}}

{{< /tab >}}

{{< /tabs >}}

**참고:**  
- [단일 워크시트 삭제](https://docs.aspose.cloud/cells/ko/worksheets/delete/)  
- [워크시트 복사](https://docs.aspose.cloud/cells/ko/worksheets/copy/)  
- [워크시트 이동](https://docs.aspose.cloud/cells/ko/worksheets/move/)  
---