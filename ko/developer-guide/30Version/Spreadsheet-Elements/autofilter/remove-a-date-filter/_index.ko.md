---
title: "날짜 필터 삭제 – Aspose.Cells Cloud"
secondtitle: "문서"
linktitle: "날짜 필터 삭제"
type: docs
url: /ko/autofilter/delete-date-filter/
aliases:
  - /remove-a-date-filter/
  - /autofilter/delete-a-date-filter/
weight: 100
keywords: "Aspose.Cells, 날짜 필터 삭제, Excel 자동 필터, REST API, SDK"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트에서 날짜 필터를 삭제하는 방법을 알아보세요. 엔드포인트, 매개변수, HTTPS cURL 예제, 응답 페이로드 및 SDK 코드 샘플 포함."
ArticleTitle: "날짜 필터 삭제 – Aspose.Cells Cloud API 문서"
---

이 REST API는 Excel 워크시트의 날짜 필터를 삭제합니다.

**필수 조건:** 유효한 JWT 토큰을 보유하고 있으며, 워크북이 Aspose Cloud 저장소에 저장되어 있고, 워크시트를 수정할 수 있는 적절한 권한이 있어야 합니다.

## DeleteWorksheetDateFilter API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dateFilter
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 우수하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름        | 유형    | 위치  | 설명                                                                                     |
|----------------------|---------|-------|-------------------------------------------------------------------------------------------------|
| name                 | string  | path  | Excel 파일 이름.                                                                         |
| sheetName            | string  | path  | 워크시트 이름.                                                                                 |
| fieldIndex           | integer | query | 필터를 적용할 열의 0부터 시작하는 인덱스.                                 |
| dateTimeGroupingType | string  | query | 날짜 필터의 그룹화 유형(예: Year, Month, Day).                                    |
| year                 | integer | query | 필터의 연도 구성 요소(기본값 0).                                                       |
| month                | integer | query | 필터의 월 구성 요소(기본값 0).                                                      |
| day                  | integer | query | 필터의 일 구성 요소(기본값 0).                                                        |
| hour                 | integer | query | 필터의 시간 구성 요소(기본값 0).                                                       |
| minute               | integer | query | 필터의 분 구성 요소(기본값 0).                                                      |
| second               | integer | query | 필터의 초 구성 요소(기본값 0).                                                     |
| folder               | string  | query | 파일이 위치한 저장소 내 폴더 경로.                                               |
| storageName          | string  | query | Aspose Cloud 저장소 이름.                                                               |

### **응답**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP 상태 코드**

| 코드 | 의미                    | 설명                                      |
|------|-------------------------|--------------------------------------------------|
| 200  | OK                      | 필터가 성공적으로 적용됨; 응답에 작업 세부정보 포함. |
| 400  | 잘못된 요청              | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형). |
| 401  | 인증되지 않음           | 잘못되거나 누락된 JWT 토큰. |
| 413  | 페이로드 너무 큼         | 업로드된 파일이 크기 제한을 초과함. |
| 500  | 내부 서버 오류           | 예기치 않은 서버 오류. |

이 API는 삭제 작업의 결과를 나타내는 표준 HTTP 상태 코드를 반환합니다.

| 코드 | 의미                    | 설명                                      |
|------|-------------------------|--------------------------------------------------|
| 200  | OK                      | 날짜 필터가 성공적으로 삭제됨; 응답에 작업 상태 포함. |
| 400  | 잘못된 요청              | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형). |
| 401  | 인증되지 않음           | 잘못되거나 누락된 JWT 토큰. |
| 413  | 페이로드 너무 큼         | 업로드된 파일이 크기 제한을 초과함. |
| 500  | 내부 서버 오류           | 예기치 않은 서버 오류. |

## SDK를 사용하여 DeleteWorksheetDateFilter API 사용 방법

### DeleteWorksheetDateFilter API 사양

<a href="https://apireference.aspose.cloud/cells/#/AutoFilter/DeleteWorksheetDateFilter" rel="noopener noreferrer">OpenAPI 사양</a>은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하고 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API에 호출을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dateFilter?fieldIndex=0&dateTimeGroupingType=Year&year=1920" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 호출을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetDateFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetDateFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetDateFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetDateFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetDateFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetDateFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetDateFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetDateFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}