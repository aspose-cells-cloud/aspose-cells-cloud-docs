---
title: "Excel 워크시트에서 열 숨기기"
second_title: "문서"
linktitle: "숨기기"
type: docs
url: /columns/hide/
aliases:
  - /hide-columns-in-excel-worksheet/
  - /hide-columns-in-an-excel-worksheet/
keywords: "Aspose.Cells Cloud, 열 숨기기 API, Excel 열 숨기기, REST API 열 숨기기, Aspose.Cells SDK, 스프레드시트 자동화"
description: "Aspose.Cells Cloud REST API(v3.0)를 사용해 Excel 워크시트에서 하나 이상의 열을 숨기는 방법을 배워보세요. 엔드포인트, 매개변수, cURL 예제, SDK 코드 예제, 오류 처리를 포함합니다."
weight: 40
---

이 REST API는 워크시트에서 열을 숨깁니다.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/hide
```

### 요청 매개변수

| 매개변수 이름   | 유형    | 위치   | 설명                                                           |
| -------------- | ------- | ------ | ------------------------------------------------------------- |
| name           | string  | path   | 워크북 파일의 이름입니다.                                        |
| sheetName      | string  | path   | 열을 숨길 워크시트의 이름입니다.                               |
| startColumn    | integer | query  | 숨길 첫 번째 열의 0부터 시작하는 인덱스입니다.                         |
| totalColumns   | integer | query  | **startColumn**에서 시작하여 연속으로 숨길 열의 수입니다. |
| folder         | string  | query  | 워크북이 포함된 폴더의 경로입니다.                        |
| storageName    | string  | query  | 파일이 위치한 스토리지 서비스의 이름입니다.                |

[OpenAPI 사양서](https://apireference.aspose.cloud/cells/#/Cells/PostHideWorksheetColumns)는 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

**cURL** 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스를 쉽게 호출할 수 있습니다. 아래 예제는 cURL을 사용해 열을 숨기는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/hide?startColumn=1&totalColumns=1" \
     -H "accept: application/json" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**가능한 응답 코드**

| HTTP 코드 | 의미                                  | 예시 JSON (오류)                                     |
| --------- | ------------------------------------ | --------------------------------------------------- |
| 200       | 성공                                 | `{ "Code": 200, "Status": "OK" }`                  |
| 400       | 잘못된 요청 (예: 잘못된 매개변수)      | `{ "Code": 400, "Message": "Invalid column range." }` |
| 401       | 인증되지 않음 (누락/잘못된 토큰)       | `{ "Code": 401, "Message": "Invalid access token." }` |
| 404       | 찾을 수 없음 (워크북 또는 워크시트)    | `{ "Code": 404, "Message": "File not found." }`     |
| 500       | 내부 서버 오류                        | `{ "Code": 500, "Message": "Unexpected error." }`   |

{{< /tab >}}

{{< /tabs >}}

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 가장 빠른 개발 방법입니다. SDK는 저수준 세부 사항을 추상화하여 비즈니스 로직에 집중할 수 있도록 해줍니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostHideWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostHideWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostHideWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostHideWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostHideWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostHideWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostHideWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostHideWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}