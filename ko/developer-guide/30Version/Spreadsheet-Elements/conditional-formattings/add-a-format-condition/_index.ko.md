---
title: "서식 조건 추가"
type: docs
url: /ko/conditional-formattings/add-format-condition/
aliases: [  /ko/add-a-format-condition/ ]
keywords: "Aspose.Cells Cloud, 조건부 서식 API, 서식 조건 추가, Excel REST API, Cells API"
description: "Aspose.Cells Cloud REST API(v3.0)를 사용하여 Excel 워크시트에 서식 조건을 추가하는 방법을 알아보세요. 요청 구문, 매개변수, 안전한 cURL 예제, SDK 스니펫이 포함됩니다."
ArticleTitle: "서식 조건 추가 – Aspose.Cells Cloud API 문서"
weight: 50
---

이 REST API는 워크시트에 서식 조건을 추가합니다.

## 보안 및 인증
Aspose.Cells Cloud API는 [JWT 토큰 기반 인증](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)을 요구합니다.

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}
```

### 요청 매개변수

| 매개변수 이름 | 유형    | 위치 | 설명                                                              |
| -------------- | ------- | ------ | ------------------------------------------------------------------- |
| name           | string  | path   | Excel 워크북의 이름입니다.                                          |
| sheetName      | string  | path   | 서식이 적용될 범위를 포함하는 워크시트의 이름입니다.                |
| index          | integer | path   | 추가 또는 교체할 서식 조건의 0부터 시작하는 인덱스입니다.           |
| cellArea       | string  | query  | 조건이 적용될 셀 범위(예: `A1:C3`)입니다.                           |
| type           | string  | query  | 조건의 유형(예: `Expression`, `CellValue`)입니다.                  |
| operatorType   | string  | query  | 조건의 연산자(예: `Between`, `Equal`)입니다.                       |
| formula1       | string  | query  | 조건에서 사용되는 첫 번째 수식 또는 값입니다.                       |
| formula2       | string  | query  | 두 번째 수식 또는 값입니다(`Between`과 같은 일부 연산자에 필요).    |
| folder         | string  | query  | 워크북이 위치한 저장소의 폴더입니다.                                |
| storageName    | string  | query  | 저장소 서비스의 이름(예: `Default`)입니다.                          |

### 오류 응답

| HTTP 코드 | 이유                                           | 예시 본문                                                             |
| --------- | ---------------------------------------------- | --------------------------------------------------------------------- |
| **400**   | 잘못된 요청 – 누락되거나 잘못된 매개변수입니다. | `{ "Code":"400", "Message":"Invalid parameter value." }`             |
| **401**   | 인증되지 않음 – 누락되거나 잘못된 JWT 토큰입니다. | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**   | 없음 – 워크북 또는 워크시트가 존재하지 않습니다.  | `{ "Code":"404", "Message":"File not found." }`                      |
| **500**   | 내부 서버 오류 – 예기치 않은 서버 실패입니다.   | `{ "Code":"500", "Message":"An unexpected error occurred." }`       |

### 성공 응답

| HTTP 코드 | 이유                                          | 예시 본문                                |
| --------- | --------------------------------------------- | ----------------------------------------- |
| **200**   | 성공 – 조건이 성공적으로 추가 또는 업데이트되었습니다. | `{ "Code": "200", "Status": "OK" }` |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/PutWorksheetFormatCondition)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

**cURL**을 사용하여 Aspose.Cells API를 호출할 수 있습니다. 아래 예제는 빈 JSON 본문을 포함한 전체 요청을 보여줍니다.

### cURL 예제

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings/0?cellArea=A1:C3&type=Expression&operatorType=Between&formula1=v1&formula2=v2" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-AddFormatCondition-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-add-cells-area-for-format-condition.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-put_worksheet_format_condition-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-AddFormatCondition-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-AddFormatCondition-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "caa13d019b3c7c3b5c14110ccd217e99" >}}

{{< /tab >}}

{{< /tabs >}}