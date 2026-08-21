---
title: "Excel 워크시트에서 열 복사"
second_title: "문서"
linktype: "복사"
type: docs
url: /ko/columns/copy/
aliases:
  /ko/copy-columns-in-excel-worksheet/
  /ko/copy-columns-in-an-excel-worksheet/
keywords: "Aspose.Cells, 열 복사, Excel API, REST, 클라우드 SDK, cURL, C#, Java, Python, Ruby, Node.js, Go, Perl"
description: "Aspose.Cells Cloud REST API(v3.0)를 사용하여 Excel 워크시트에서 하나 이상의 열을 복사하는 방법을 알아보세요. 요청 구문, 필수 매개변수, 인증 세부 정보, 오류 처리, C#, Java, Python, Ruby, Node.js, Go, Perl 등 다양한 언어의 SDK 예제를 포함합니다."
articleTitle: "Aspose.Cells Cloud API를 사용한 Excel 워크시트 열 복사"
weight: 30
---

이 REST API는 Excel 워크시트에서 **열**을 복사합니다. **열 복사**(Copy Columns) 작업을 사용하면 단일 열 또는 열 범위를 복사하여 동일한 워크시트 내 지정된 위치에 삽입할 수 있습니다. 이 엔드포인트를 사용하여 대규모 스프레드시트 작업 시 열을 효율적으로 복사할 수 있으며, 추가 열 관리 작업을 위해 [열 추가](/ko/columns/add/) 및 [열 숨기기](/ko/columns/hide/)와 관련 작업도 참고하세요.

## 보안 및 인증
Aspose.Cells Cloud API는 [JWT 토큰 기반 인증](https://docs.aspose.cloud/ko/total/getting-started/rest-api-overview/authenticating-api-requests/)이 필요합니다.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/copy
```

### 요청 매개변수

| 매개변수 이름               | 유형    | 위치   | 설명                                                                            |
| -------------------------- | ------- | ------ | ------------------------------------------------------------------------------- |
| **name**                   | string  | path   | 워크북 이름.                                                                    |
| **sheetName**              | string  | path   | 워크시트 이름.                                                                  |
| **sourceColumnIndex**      | integer | query  | 복사할 열의 0 기준 인덱스.                                                      |
| **destinationColumnIndex** | integer | query  | 복사된 열이 삽입될 위치의 0 기준 인덱스.                                        |
| **columnNumber**           | integer | query  | 복사할 연속 열의 수.                                                            |
| **worksheet**              | string  | query  | _(선택 사항)_ 워크시트 이름이 경로와 다를 때 사용하는 워크시트 식별자.          |
| **folder**                 | string  | query  | Aspose Cloud 저장소 내 워크북이 포함된 폴더 경로.                               |

이 작업의 전체 계약은 [OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Cells/PostCopyWorksheetColumns)에 정의되어 있습니다.

### cURL 예제

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/copy?sourceColumnIndex=1&destinationColumnIndex=12&columnNumber=10" \
     -H "Authorization: Bearer $ASPOSE_TOKEN" \
     -H "accept: application/json"
```

### 응답

```json
{
  "Code": 200,
  "Status": "OK"
}
```

## 오류 처리

API는 표준 HTTP 상태 코드와 오류를 설명하는 JSON 페이로드를 반환합니다.

| 상태 코드 | 의미                                              | 예시 JSON 본문                                                       |
| --------- | ------------------------------------------------- | -------------------------------------------------------------------- |
| **400**   | 잘못된 요청 – 유효하지 않은 매개변수               | `{ "Code": 400, "Message": "Invalid column index." }`               |
| **401**   | 인증되지 않음 – 토큰 누락 또는 잘못됨              | `{ "Code": 401, "Message": "Access token is invalid or expired." }` |
| **404**   | 없음 – 워크북 또는 워크시트가 존재하지 않음        | `{ "Code": 404, "Message": "Workbook not found." }`                 |
| **500**   | 내부 서버 오류 – 예기치 않은 조건                  | `{ "Code": 500, "Message": "An unexpected error occurred." }`       |

> **문제 해결 방법:** 액세스 토큰이 유효한지, 워크북 및 워크시트 이름이 정확한지, `sourceColumnIndex`, `destinationColumnIndex`, `columnNumber`가 워크시트 열 범위 내에 있는지 확인하세요.

## 클라우드 SDK 패밀리

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCopyWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCopyWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCopyWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCopyWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCopyWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCopyWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCopyWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCopyWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "열 복사 API를 호출할 때 인증하려면 어떻게 해야 하나요?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "클라이언트 ID와 비밀번호를 사용해 Aspose Cloud에서 OAuth2 액세스 토큰을 획득한 후, 요청 헤더에 `Authorization: Bearer <access_token>` 형태로 포함하세요."
      }
    },
    {
      "@type": "Question",
      "name": "`sourceColumnIndex`와 `destinationColumnIndex`의 차이는 무엇인가요?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "`sourceColumnIndex`는 복사하려는 열의 0 기준 인덱스입니다. `destinationColumnIndex`는 복사된 열이 삽입될 위치의 0 기준 인덱스입니다."
      }
    },
    {
      "@type": "Question",
      "name": "복사 작업이 실패하면 어떤 응답을 받게 되나요?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "API는 200이 아닌 상태 코드(예: 400은 잘못된 요청, 401은 인증되지 않음)를 반환합니다. 응답 본문에는 오류를 설명하는 `Code` 및 `Message` 필드를 포함하는 JSON 객체가 포함됩니다."
      }
    }
  ]
}
</script>
---