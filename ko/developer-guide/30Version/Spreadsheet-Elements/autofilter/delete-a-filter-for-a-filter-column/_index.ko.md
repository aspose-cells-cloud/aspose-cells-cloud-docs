---
title: "엑셀 워크시트에서 필터 삭제하기 – Aspose.Cells Cloud API"
second_title: "문서"
linktitle: "필터 삭제"
type: docs
url: /ko/delete-filter/
aliases: [/delete-a-filter-for-a-filter-column/, /delete-auto-filter/]
keywords: "Aspose.Cells Cloud 필터 삭제, 엑셀, REST API, SDK"
description: "Aspose.Cells Cloud REST API, cURL, SDK(C#, Java, Python 등)를 사용하여 엑셀 워크시트에서 자동필터를 삭제하는 방법을 알아보세요. 엔드포인트, 매개변수, 인증 및 샘플 코드 포함."
weight: 100
---

## REST API

이 REST API는 엑셀 워크시트의 **자동필터**(AutoFilter)를 삭제합니다.

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filter
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 강화되어 있으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름            | 유형    | 위치   | 필수 여부 | 설명                                                                 |
| ------------------------ | ------- | ------ | --------- | -------------------------------------------------------------------- |
| **name**                 | string  | Path   | 예        | 워크북 이름.                                                         |
| **sheetName**            | string  | Path   | 예        | 워크시트 이름.                                                       |
| **range**                | string  | Query  | 아니요    | 필터를 적용할 셀 범위 (예: `A1:C10`).                                |
| **fieldIndex**           | integer | Query  | 예        | 필터가 적용될 열의 0부터 시작하는 인덱스.                            |
| **dateTimeGroupingType** | string  | Query  | 아니요    | 날짜/시간 값 그룹화 방식: `Day`, `Hour`, `Minute`, `Month`, `Second`, `Year`. |
| **year**                 | integer | Query  | 아니요    | 날짜 그룹화를 위한 연도 구성 요소.                                   |
| **month**                | integer | Query  | 아니요    | 날짜 그룹화를 위한 월 구성 요소.                                     |
| **day**                  | integer | Query  | 아니요    | 날짜 그룹화를 위한 일 구성 요소.                                     |
| **hour**                 | integer | Query  | 아니요    | 날짜 그룹화를 위한 시 구성 요소.                                     |
| **minute**               | integer | Query  | 아니요    | 날짜 그룹화를 위한 분 구성 요소.                                     |
| **second**               | integer | Query  | 아니요    | 날짜 그룹화를 위한 초 구성 요소.                                     |
| **matchBlanks**          | boolean | Query  | 아니요    | `true` / `false` — 빈 셀을 필터에 포함할지 여부.                    |
| **refresh**              | boolean | Query  | 아니요    | `true` / `false` — 삭제 후 워크시트를 새로 고칠지 여부.             |
| **folder**               | string  | Query  | 아니요    | 원본 워크북 폴더.                                                    |
| **storageName**          | string  | Query  | 아니요    | 스토리지 이름.                                                       |

### **응답**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP 상태 코드**

| 코드 | 의미               | 설명                                                      |
|------|--------------------|-----------------------------------------------------------|
| 200  | OK                 | 필터가 성공적으로 적용됨; 응답에는 작업 세부 정보 포함.   |
| 400  | Bad Request        | 누락되거나 잘못된 매개변수 (예: 지원되지 않는 파일 유형). |
| 401  | Unauthorized       | 잘못되거나 누락된 JWT 토큰.                               |
| 413  | Payload Too Large  | 업로드된 파일이 크기 제한을 초과함.                       |
| 500  | Internal Server Error | 예기치 않은 서버 오류.                                  |

## SDK를 사용하여 DeleteWorksheetFilter API 사용하는 방법

### DeleteWorksheetFilter API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/AutoFilter/DeleteWorksheetFilter)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.


cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예시는 cURL을 사용하여 Cloud API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filter?fieldIndex=0&dateTimeGroupingType=Year" \
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

### Aspose.Cells Cloud SDK 사용하기

SDK를 사용하면 개발 속도를 가장 효율적으로 높일 수 있습니다. SDK는 저수준 세부 사항을 처리해주므로, 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}

---