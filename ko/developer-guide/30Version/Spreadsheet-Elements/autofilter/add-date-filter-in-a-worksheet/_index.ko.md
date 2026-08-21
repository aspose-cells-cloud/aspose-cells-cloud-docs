---
title: "Excel 워크시트에 날짜 필터 추가"
second_title: "문서"
linktitle: "날짜 필터 추가"
type: docs
url: /autofilter/add-date-filter/
aliases:
  - /add-date-filter-in-a-worksheet/
  - /autofilter/add-a-date-filter/
description: "Aspose.Cells Cloud REST API(v3.0)를 사용하여 Excel 워크시트에 날짜 필터를 추가하는 방법을 배웁니다. cURL 예제, SDK 스니펫(C#, Java, Python 등), 매개변수 및 오류 처리를 포함합니다."
weight: 65
ArticleTitle: "Excel 워크시트에 날짜 필터 추가 | Aspose.Cells Cloud API"
keywords: "Aspose.Cells, Excel 날짜 필터, AutoFilter API, REST API, 클라우드 SDK, cURL, 스프레드시트 자동화"
---

이 REST API는 Excel 워크시트에 **날짜 필터**를 추가합니다.

**필수 조건:** 유효한 JWT 토큰이 있어야 하며, 대상 워크북이 지정된 저장소 위치에 이미 존재해야 합니다. 이 요청은 JSON 본문을 필요로 하지 않습니다.

## PutWorksheetDateFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dateFilter
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 위해 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>을 요구합니다.

### 요청 매개변수


| 매개변수 이름             | 유형     | 위치   | 설명                                                                                                                                                      |
| ------------------------ | ------- | ------ | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**                 | string  | Path   | 워크북 이름.                                                                                                                                              |
| **sheetName**            | string  | Path   | 워크시트 이름.                                                                                                                                            |
| **range**                | string  | Query  | 필터를 적용할 Excel 범위(예: `A1:B1`).                                                                                                                    |
| **fieldIndex**           | integer | Query  | 필터링할 열의 0부터 시작하는 인덱스.                                                                                                                      |
| **dateTimeGroupingType** | string  | Query  | 날짜/시간 필터의 그룹화 유형. 허용되는 값은 `Day`, `Hour`, `Minute`, `Month`, `Second`, `Year`입니다. 값은 대소문자를 구분하며, 기본값은 `Day`입니다. |
| **year**                 | integer | Query  | 필터 값의 연도 구성 요소.                                                                                                                                 |
| **month**                | integer | Query  | 필터 값의 월 구성 요소.                                                                                                                                   |
| **day**                  | integer | Query  | 필터 값의 일 구성 요소.                                                                                                                                   |
| **hour**                 | integer | Query  | 필터 값의 시간 구성 요소.                                                                                                                                 |
| **minute**               | integer | Query  | 필터 값의 분 구성 요소.                                                                                                                                   |
| **second**               | integer | Query  | 필터 값의 초 구성 요소.                                                                                                                                   |
| **matchBlanks**          | boolean | Query  | 빈 셀 포함 여부(`true` 또는 `false`).                                                                                                                     |
| **refresh**              | boolean | Query  | 적용 후 필터 새로고침 여부(`true` 또는 `false`).                                                                                                          |
| **folder**               | string  | Query  | 원본 워크북의 폴더 경로.                                                                                                                                  |
| **storageName**          | string  | Query  | 저장소 서비스 이름.                                                                                                                                       |

*PUT 요청은 요청 본문을 필요로 하지 않으며, 모든 매개변수는 쿼리 문자열을 통해 제공됩니다.*

### **응답**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP 상태 코드**

| 코드 | 의미                         | 설명                                                                 |
|------|-----------------------------|---------------------------------------------------------------------|
| 200  | OK                          | 필터가 성공적으로 적용됨; 응답에는 작업 세부 정보가 포함됩니다.         |
| 400  | Bad Request                 | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형).               |
| 401  | Unauthorized                | 잘못되거나 누락된 JWT 토큰.                                           |
| 413  | Payload Too Large           | 업로드된 파일이 크기 제한을 초과함.                                    |
| 500  | Internal Server Error       | 예기치 않은 서버 오류.                                                |

## SDK를 사용하여 PutWorksheetDateFilter API 사용하는 방법

### PutWorksheetDateFilter API 사양

<a href="https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetDateFilter" rel="noopener noreferrer">OpenAPI 사양</a>은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

**cURL** 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예제는 cURL을 사용하여 클라우드 API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dateFilter?range=A1:B1&fieldIndex=0&dateTimeGroupingType=Year&year=1920&refresh=true" \
-X PUT \
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

SDK를 사용하면 개발 속도가 가장 빠릅니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetDateFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetDateFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetDateFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetDateFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PutWorksheetDateFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetDateFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetDateFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetDateFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}