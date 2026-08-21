---
title: "Excel 워크시트에 사용자 정의 기준 추가"
second_title: "문서"
linktitle: "사용자 정의 필터 추가"
type: docs
url: /ko/autofilter/add-custom-filter/
aliases: [  /ko/filter-a-list-with-a-custom-criteria/ , /ko/autofilter/add-a-custom-filter/ ]
keywords: "Excel, 사용자 정의 필터, Aspose.Cells Cloud, REST API, 자동 필터, 워크시트, 사용자 정의 기준"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트에 사용자 정의 필터를 추가하는 방법을 알아보세요. 요청 세부 정보, cURL 예제, 여러 프로그래밍 언어의 SDK 코드 스니펫이 포함됩니다."
weight: 65
ArticleTitle: "Excel 워크시트에 사용자 정의 기준 추가 – Aspose.Cells Cloud API"
---

이 REST API는 **사용자 정의 기준**을 사용하여 목록을 필터링합니다.

## PutWorksheetCustomFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/custom
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 우수하며 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수:

| 매개변수 이름 | 유형    | 위치                     | 설명                                                                 |
|--------------|---------|--------------------------|---------------------------------------------------------------------|
| name         | string  | path                     | Excel 파일 이름.                                                    |
| sheetName    | string  | path                     | 필터링할 데이터가 포함된 워크시트 이름.                             |
| range        | string  | query                    | 필터를 적용할 셀 범위(예: `A1:B1`).                                |
| fieldIndex   | integer | query                    | 필터를 적용할 열의 0부터 시작하는 인덱스.                           |
| operatorType1| string  | query                    | 첫 번째 비교 연산자(예: `LessOrEqual`, `Equal`).                   |
| criteria1    | string  | query                    | 첫 번째 필터 값 또는 표현식.                                        |
| isAnd        | boolean | query                    | `true`인 경우 두 기준을 **AND**로 결합하고, 그렇지 않으면 **OR**로 결합합니다. |
| operatorType2| string  | query                    | 두 번째 비교 연산자(선택 사항).                                     |
| criteria2    | string  | query                    | 두 번째 필터 값 또는 표현식(선택 사항).                             |
| matchBlanks  | boolean | query                    | `true`인 경우 빈 셀이 필터 결과에 포함됩니다.                      |
| refresh      | boolean | query                    | `true`인 경우 필터 적용 후 워크시트를 강제로 새로 고침합니다.      |
| folder       | string  | query                    | 파일이 위치한 저장소의 폴더 경로.                                  |
| storageName  | string  | query                    | 저장소 서비스 이름.                                                |

### **응답**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP 상태 코드**

| 코드 | 의미                         | 설명                                                    |
|-----|-----------------------------|--------------------------------------------------------|
| 200 | OK                          | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함. |
| 400 | Bad Request                 | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식). |
| 401 | Unauthorized                | 잘못되거나 누락된 JWT 토큰.                            |
| 413 | Payload Too Large           | 업로드된 파일이 크기 제한을 초과함.                   |
| 500 | Internal Server Error       | 예기치 않은 서버 오류.                                 |

## SDK를 사용하여 PutWorksheetCustomFilter API 사용 방법

### PutWorksheetCustomFilter API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetCustomFilter)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

**cURL** 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/custom?range=A1:B1&fieldIndex=0&operatorType1=LessOrEqual&criteria1=1" \
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

SDK를 사용하면 개발 속도가 가장 빠릅니다. SDK는 저수준 세부 정보를 처리하므로 프로젝트 로직에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetCustomFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetCustomFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetCustomFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetCustomFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetCustomFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetCustomFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetCustomFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetCustomFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}

표준 필터 또는 날짜 필터 추가와 같은 기타 AutoFilter 작업은 AutoFilter 섹션 내의 관련 문서 페이지를 참조하세요.