---
title: "조건부 서식 지우기"
type: docs
url: /ko/conditional-formattings/clear/
aliases: [  /ko/clear-all-condition-formattings/ ]
keywords: "Aspose.Cells Cloud, REST API, 조건부 서식 지우기, Excel, 워크시트, JWT, v3.2"
description: "Aspose.Cells Cloud API(v3.2)를 사용하여 워크시트에서 모든 조건부 서식 규칙을 삭제합니다. 요청 구문, 필수 매개변수, 인증 단계 및 여러 SDK에서의 샘플 코드를 확인하세요."
weight: 80
---

이 REST API는 워크시트에서 모든 조건부 서식 규칙을 지웁니다.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.2/cells/{name}/worksheets/{sheetName}/conditionalFormattings
```

### 요청 매개변수

| 매개변수 이름   | 유형   | 위치   | 설명                                                              |
| --------------- | ------ | ------ | ----------------------------------------------------------------- |
| **name**        | string | path   | 워크북 파일의 이름(예: `Book1.xlsx`).                             |
| **sheetName**   | string | path   | 조건부 서식을 제거할 워크시트의 이름.                             |
| **folder**      | string | query  | _(선택 사항)_ 워크북이 위치한 저장소의 폴더 경로.                 |
| **storageName** | string | query  | _(선택 사항)_ 저장소 서비스의 이름.                               |

[OpenAPI 사양서](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormattings)는 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 이를 통해 웹 브라우저에서 직접 REST 요청을 수행할 수 있습니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예시는 cURL을 사용하여 클라우드 API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.2/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

### 오류 응답

| HTTP 코드 | 원인                                               | 예시 본문                                                            |
| --------- | -------------------------------------------------- | ------------------------------------------------------------------- |
| **400**   | 잘못된 요청 – 누락되거나 잘못된 매개변수.          | `{ "Code":"400", "Message":"Invalid parameter value." }`            |
| **401**   | 인증 실패 – 누락되거나 잘못된 JWT 토큰.           | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**   | 없음 – 워크북 또는 워크시트가 존재하지 않음.       | `{ "Code":"404", "Message":"File not found." }`                     |
| **500**   | 내부 서버 오류 – 예기치 않은 서버 오류.            | `{ "Code":"500", "Message":"An unexpected error occurred." }`       |

## SDK 예제

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 요청을 보내는 방법을 보여줍니다:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-ClearConditionFormattings-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-clear-all-formatting.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-delete_worksheet_conditional_formattings-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-ClearConditionFormattings-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-ClearConditionFormattings-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "63fda1be9e5149f83edca47ce58dac87" >}}

{{< /tab >}}

{{< /tabs >}}