---
title: "셀 영역 삭제 – Aspose.Cells Cloud API 문서"
type: docs
url: /conditional-formattings/delete-cell-area/
aliases: [/remove-cell-area-from-conditional-formatting/]
keywords: "Aspose.Cells Cloud, 셀 영역 삭제, 조건부 서식 API, Excel REST API"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트의 조건부 서식에서 특정 셀 영역을 삭제합니다. ASP.NET, Java, Python 예제 포함."
ArticleTitle: "셀 영역 삭제 – Aspose.Cells Cloud API 문서"
weight: 70
---

이 REST API는 조건부 서식 규칙에서 셀 영역을 삭제합니다.

## 보안 및 인증
Aspose.Cells Cloud API는 보안이 보장되며, [JWT 토큰 기반 인증](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)이 필요합니다.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/area
```

### 요청 매개변수

| 매개변수 이름   | 유형    | 위치   | 설명                                                           |
| --------------- | ------- | ------ | ------------------------------------------------------------- |
| `name`          | string  | path   | Excel 파일의 이름입니다.                                      |
| `sheetName`     | string  | path   | 조건부 서식이 포함된 워크시트의 이름입니다.                   |
| `startRow`      | integer | query  | 삭제할 영역의 첫 번째 행(0부터 시작하는 인덱스)입니다.         |
| `startColumn`   | integer | query  | 삭제할 영역의 첫 번째 열(0부터 시작하는 인덱스)입니다.         |
| `totalRows`     | integer | query  | 삭제할 영역의 행 수입니다.                                     |
| `totalColumns`  | integer | query  | 삭제할 영역의 열 수입니다.                                     |
| `folder`        | string  | query  | 파일이 위치한 클라우드 스토리지의 폴더 경로(선택 사항).        |
| `storageName`   | string  | query  | 스토리지 서비스의 이름(선택 사항).                             |

### 오류 응답

| HTTP 상태 코드 | 코드            | 설명                                                   | 예시 JSON                                                    |
| -------------- | --------------- | ------------------------------------------------------ | ------------------------------------------------------------ |
| 400            | `BadRequest`    | 누락되거나 잘못된 매개변수입니다.                      | `{ "Code": "400", "Message": "Invalid request parameters." }` |
| 401            | `Unauthorized`  | 누락되거나 잘못된 JWT 토큰입니다.                      | `{ "Code": "401", "Message": "Authentication failed." }`      |
| 404            | `NotFound`      | 파일, 워크시트 또는 조건부 서식을 찾을 수 없습니다.   | `{ "Code": "404", "Message": "Resource not found." }`         |
| 500            | `InternalError` | 예기치 않은 서버 오류입니다.                           | `{ "Code": "500", "Message": "Internal server error." }`      |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormattingArea)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells Cloud 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 **셀 영역 삭제** 엔드포인트를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings/area?startRow=3&startColumn=3&totalRows=1&totalColumns=1" \
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

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 개발 속도를 높이는 가장 좋은 방법입니다. SDK는 저수준 세부 사항을 처리해주므로, 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud){:target="_blank" rel="noopener noreferrer"}를 확인하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-RemoveCellAreaFromConditionalFormatting-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-remove-cell-area-from-conditional-formatting.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-delete_worksheet_conditional_formatting_area-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-RemoveCellAreaFromConditionalFormatting-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-RemoveCellAreaFromConditionalFormatting-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "2bc4a93409f78b40b6bcf681c6a14bda" >}}

{{< /tab >}}

{{< /tabs >}}