---
title: "조건부 서식 규칙 가져오기"
type: docs
url: /conditional-formattings/get-all/
aliases: [/get-conditional-formattings-of-worksheet/]
keywords: "Aspose.Cells Cloud, REST API, Excel, 조건부 서식, 워크시트, 조건부 서식 API"
description: "Aspose.Cells Cloud REST API를 사용하여 워크시트에 적용된 모든 조건부 서식 규칙을 검색합니다. 요청 구문, 인증 단계, 매개변수, 간결한 응답 예시, 오류 처리를 포함합니다."
weight: 20
---

이 REST API는 워크시트에 적용된 조건부 서식 규칙을 검색합니다.

## 보안 및 인증
Aspose.Cells Cloud API는 보안이 적용되며 [JWT 토큰 기반 인증](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)이 필요합니다.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings
```

### 요청 매개변수

| 매개변수 이름 | 유형   | 위치   | 설명                                       |
| ------------- | ------ | ------ | ------------------------------------------ |
| name          | string | path   | Excel 파일 이름입니다.                    |
| sheetName     | string | path   | 워크시트 이름입니다.                      |
| folder        | string | query  | 파일이 저장된 폴더 경로입니다.            |
| storageName   | string | query  | 스토리지 서비스 이름입니다(선택 사항).   |

### 오류 응답

| HTTP 코드 | 이유                                       | 예시 본문                                                           |
| --------- | ------------------------------------------ | ------------------------------------------------------------------- |
| **400**   | 잘못된 요청 – 누락 또는 잘못된 매개변수.   | `{ "Code":"400", "Message":"Invalid parameter value." }`            |
| **401**   | 인증되지 않음 – 누락 또는 잘못된 JWT 토큰. | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**   | 찾을 수 없음 – 워크북 또는 워크시트가 없음. | `{ "Code":"404", "Message":"File not found." }`                     |
| **500**   | 내부 서버 오류 – 예기치 않은 서버 실패.     | `{ "Code":"500", "Message":"An unexpected error occurred." }`       |

<a href="https://apireference.aspose.cloud/cells/#/ConditionalFormattings/GetWorksheetConditionalFormattings" target="_blank">OpenAPI 스펙</a>은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예시는 cURL을 사용하여 Cloud API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Status": "OK",
  "ConditionalFormattings": {
    "Count": 1,
    "ConditionalFormattingList": [
      {
        "sqref": "A1:B10",
        "FormatConditions": [
          {
            "Priority": 1,
            "Type": "CellValue",
            "Operator": "GreaterThan",
            "Formula1": "100",
            "Style": {
              "Font": {
                "Color": { "A": 255, "R": 255, "G": 0, "B": 0 },
                "IsBold": true
              }
            }
          }
        ]
      }
    ]
  }
}
```

_위 예시는 응답 페이로드를 간결하게 유지하기 위해 가장 관련성이 높은 필드만 표시합니다._

**응답 매개변수**

| 매개변수                                | 유형     | 설명                                           |
|----------------------------------------|----------|------------------------------------------------|
| Status                                 | string   | 요청 결과 상태(예: **OK**)                      |
| ConditionalFormattings                 | object   | 조건부 서식 데이터를 담은 컨테이너              |
| ConditionalFormattings.Count           | integer  | 반환된 조건부 서식 규칙의 수                   |
| ConditionalFormattings.ConditionalFormattingList | array    | 조건부 서식 객체 목록                          |
| ConditionalFormattingList[].sqref      | string   | 서식이 적용되는 셀 범위(예: **A1:B10**)         |
| ConditionalFormattingList[].FormatConditions | array    | 해당 범위에 대한 포맷 조건 객체 모음            |
| FormatConditions[].Priority            | integer  | 조건의 평가 우선순위                           |
| FormatConditions[].Type                | string   | 조건 유형(예: **CellValue**)                   |
| FormatConditions[].Operator            | string   | 조건에 사용되는 연산자(예: **GreaterThan**)    |
| FormatConditions[].Formula1            | string   | 조건에 사용되는 첫 번째 수식 또는 값            |
| FormatConditions[].Style               | object   | 조건이 충족될 때 적용되는 스타일                |
| Style.Font.Color                       | object   | 글꼴의 RGBA 색상 정의                          |
| Style.Font.IsBold                      | boolean  | 글꼴이 굵은 글꼴인지 여부                       |

**HTTP 상태 코드**

| 코드 | 의미                      | 설명                                           |
|-----|---------------------------|----------------------------------------------|
| 200 | OK                       | 필터가 성공적으로 적용됨; 응답에 작업 세부정보 포함 |
| 400 | 잘못된 요청                | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형) |
| 401 | 인증되지 않음              | 잘못되거나 누락된 JWT 토큰                      |
| 413 | 페이로드가 너무 큼         | 업로드된 파일이 크기 제한을 초과함              |
| 500 | 내부 서버 오류             | 예기치 않은 서버 오류                            |

{{< /tab >}}

{{< /tabs >}}

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 <a href="https://github.com/aspose-cells-cloud" target="_blank">GitHub 저장소</a>를 확인하세요.

다음 코드 예시는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-GetWorksheetConditionalFormatting-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-get-conditional-formatting-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-get_worksheet_conditional_formattings-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-GetWorksheetConditionalFormatting-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-GetWorksheetConditionalFormatting-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "b2a10009556f14d1f939a8433925c5f6" >}}

{{< /tab >}}

{{< /tabs >}}
---