---
title: "Excel 워크시트의 페이지 수 가져오기"
second_title: "문서"
linktitle: "페이지 수"
type: docs
url: /ko/worksheets/page-count/
keywords: "Aspose.Cells, Excel API, 워크시트 페이지 수, REST, 클라우드 SDK, Excel 페이지 나누기"
description: "Aspose.Cells Cloud REST API(v3.0)를 사용하여 Excel 워크시트의 인쇄 가능한 페이지 수를 조회합니다. HTTPS 요청 형식, 인증 절차, 샘플 cURL 명령어, 전체 JSON 응답, 상태 코드 및 SDK 코드 예제가 포함됩니다."
weight: 10
ArticleTitle: "Excel 워크시트의 페이지 수 가져오기 – Aspose.Cells Cloud API"
---

이 REST API는 워크시트의 **페이지 수**를 반환합니다.

**인증:** Aspose.Cells Cloud의 모든 엔드포인트는 OAuth2 흐름을 통해 얻은 Bearer 토큰이 필요합니다. 아래 cURL 예제에 표시된 대로 토큰을 `Authorization` 헤더에 포함하세요.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pagecount
```

### 요청 매개변수

| 매개변수      | 유형     | 위치   | 설명                         |
| ------------- | -------- | ------ | ---------------------------- |
| name          | string   | path   | 문서 이름                    |
| sheetName     | string   | path   | 워크시트 이름                |
| folder        | string   | query  | 문서가 위치한 폴더 이름      |
| storageName   | string   | query  | 스토리지 이름                |

[OpenAPI 명세서](https://apireference.aspose.cloud/cells/#/Worksheets/GetPageCount)는 공개적으로 사용 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 요청을 수행할 수 있도록 합니다.

**cURL** 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예제는 cURL을 사용하여 API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/worksheets/Sheet1/pagecount" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access_token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "PageCount": 3
}
```

{{< /tab >}}

{{< /tabs >}}

### 응답 세부정보

| HTTP 상태 코드 | 의미                                                  |
| -------------- | ----------------------------------------------------- |
| **200**        | 성공 – 위에 표시된 JSON 페이로드를 반환합니다.       |
| **401**        | 인증 실패 – 토큰 누락 또는 유효하지 않은 토큰입니다.  |
| **404**        | 찾을 수 없음 – 파일 또는 워크시트가 존재하지 않습니다. |
| **500**        | 내부 서버 오류 – 예기치 않은 서버 조건입니다.         |

### 버전 이력

_API 버전 **v3.0** (2025년 출시). 최신 버전을 사용 중인 경우, 업데이트된 엔드포인트 문서를 참조하세요._

## 클라우드 SDK 패밀리

SDK를 사용하면 가장 빠르게 개발할 수 있습니다. SDK는 저수준 세부 사항을 추상화하여 비즈니스 로직에 집중할 수 있도록 도와줍니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetPageCount.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetPageCount.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetPageCount.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetPageCount.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetPageCount.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetPageCount.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetPageCount.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetPageCount.go" >}}

{{< /tab >}}

{{< /tabs >}}

### 참고 사항

- 페이지 수는 페이지 나누기, 여백, 배율 등을 고려한 인쇄 레이아웃을 반영합니다. 숨겨진 행 또는 열은 결과에 영향을 줄 수 있습니다.
- 요청을 수행하기 전에 대상 워크시트가 존재하며, 파일이 지정된 `folder` 및 `storageName`에 저장되어 있는지 확인하세요.