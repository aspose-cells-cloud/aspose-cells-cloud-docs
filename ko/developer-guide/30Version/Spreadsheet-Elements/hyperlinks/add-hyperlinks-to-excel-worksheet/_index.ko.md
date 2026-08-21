---
title: "워크시트에 하이퍼링크 추가"
type: docs
url: /hyperlinks/add/
aliases: [/add-hyperlinks-to-excel-worksheet/]
keywords: "Aspose.Cells, 하이퍼링크 추가, Excel REST API, 클라우드 SDK"
description: "Aspose.Cells Cloud v3.0 REST API를 사용하여 Excel 워크시트에 하이퍼링크를 추가하는 방법을 배워보세요. 엔드포인트, 전체 매개변수 가이드, cURL 예제, C#, Java, Python 등 다양한 언어의 SDK 스니펫을 포함합니다."
weight: 20
---

이 REST API는 Excel 워크시트에 하이퍼링크를 추가합니다.

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks
```

### 요청 매개변수

| 매개변수 이름 | 유형    | 위치 | 설명                                                                                      |
| ------------- | ------- | ---- | ----------------------------------------------------------------------------------------- |
| name          | string  | path | 문서 이름.                                                                                |
| sheetName     | string  | path | 워크시트 이름.                                                                            |
| firstRow      | integer | query | 하이퍼링크가 적용될 범위의 첫 번째 행 인덱스(0부터 시작).                                 |
| firstColumn   | integer | query | 하이퍼링크가 적용될 범위의 첫 번째 열 인덱스(0부터 시작).                                |
| totalRows     | integer | query | 하이퍼링크 범위가 포함하는 행 수.                                                         |
| totalColumns  | integer | query | 하이퍼링크 범위가 포함하는 열 수.                                                         |
| address       | string  | query | 하이퍼링크가 가리키는 대상 URL(URL 인코딩됨).                                             |
| folder        | string  | query | 문서가 위치한 폴더.                                                                       |
| storageName   | string  | query | 스토리지 이름.                                                                            |

요청은 동일한 필드(`Address`, `FirstRow`, `FirstColumn`, `TotalRows`, `TotalColumns`)를 포함하는 JSON 바디도 포함할 수 있습니다. 쿼리 문자열 매개변수 대신 페이로드를 선호할 경우 바디를 제공하는 것이 유용합니다.

### 오류 응답

| HTTP 코드 | 원인                                              | 예시 바디                                                           |
| --------- | ------------------------------------------------- | ------------------------------------------------------------------- |
| **400**   | 잘못된 요청 — 누락되거나 유효하지 않은 매개변수.   | `{ "Code":"400", "Message":"Invalid parameter value." }`            |
| **401**   | 인증되지 않음 — 누락되거나 유효하지 않은 JWT 토큰. | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**   | 찾을 수 없음 — 워크북 또는 워크시트가 존재하지 않음. | `{ "Code":"404", "Message":"File not found." }`                     |
| **500**   | 내부 서버 오류 — 예기치 않은 서버 실패.            | `{ "Code":"500", "Message":"An unexpected error occurred." }`       |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Hypelinks/PutWorksheetHyperlink)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API로 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks?firstRow=1&firstColumn=6&totalRows=1&totalColumns=1&address=https%3A%2F%2Fwww.msnbc.com%2F" \
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

요청이 실패하면 API는 표준 HTTP 오류 코드(예: 400 Bad Request, 401 Unauthorized, 404 Not Found, 500 Internal Server Error)와 함께 오류 메시지와 코드를 포함하는 JSON 페이로드를 반환합니다.

## 클라우드 SDK 패밀리

SDK를 사용하면 개발 속도가 가장 빠릅니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetHyperlink.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetHyperlink.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetHyperlink.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetHyperlink.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetHyperlink.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetHyperlink.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetHyperlink.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetHyperlink.go" >}}

{{< /tab >}}

{{< /tabs >}}