---
title: "모든 워크시트 가져오기"
second_title: "문서"
linktitle: "모든"
type: docs
url: /ko/worksheets/get-all/
aliases: [/get-worksheet-count/]
keywords: "Aspose.Cells, 클라우드 API, 워크시트 가져오기, Excel, REST, SDK"
description: "Aspose.Cells Cloud REST API(v3.0)를 사용하여 Excel 워크북에 포함된 워크시트 목록을 검색합니다. cURL 예제, SDK 스니펫 및 응답 형식을 포함합니다."
weight: 10
---

이 REST API는 워크북에 포함된 워크시트에 대한 정보를 반환합니다.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets
```

### **요청 매개변수**

| 매개변수 이름 | 유형   | 위치 | 설명                               |
| -------------- | ------ | ---- | ---------------------------------- |
| name           | string | path | Excel 문서의 이름입니다.           |
| folder         | string | query| 문서가 포함된 폴더입니다.          |
| storageName    | string | query| 사용할 저장소의 이름입니다.        |

[OpenAPI 사양서](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheets)는 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells Cloud 서비스에 접근할 수 있습니다. 아래 예제는 워크시트를 검색하기 위한 GET 요청을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Worksheets": {
    "WorksheetList": [
      {
        "link": {
          "Href": "/Sheet1",
          "Rel": "self"
        }
      },
      {
        "link": {
          "Href": "/Sheet2",
          "Rel": "self"
        }
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## 오류 처리

이 엔드포인트에서 반환되는 일반적인 HTTP 상태 코드:

| 코드 | 의미                 | 설명                                     |
| ---- | ------------------- | ---------------------------------------- |
| 400  | 잘못된 요청(Bad Request) | 필수 매개변수 누락(예: `name`).        |
| 401  | 인증되지 않음(Unauthorized) | 유효하지 않거나 누락된 JWT 토큰.       |
| 404  | 찾을 수 없음(Not Found) | 지정된 워크북이 존재하지 않습니다.         |
| 500  | 내부 서버 오류(Internal Server Error) | 예기치 않은 서버 조건.             |

오류 응답은 JSON 형식으로 반환됩니다. 예:

```json
{
  "Code": "401",
  "Message": "Invalid access token."
}
```

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheets.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheets.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheets.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheets.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheets.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheets.go" >}}

{{< /tab >}}

{{< /tabs >}}