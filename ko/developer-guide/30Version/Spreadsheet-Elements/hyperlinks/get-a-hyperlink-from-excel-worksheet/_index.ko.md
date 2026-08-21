---
title: "워크시트 하이퍼링크 가져오기"
type: docs
url: /hyperlinks/get/
keywords: "Aspose.Cells Cloud, 워크시트 하이퍼링크 가져오기, Excel 하이퍼링크 API, REST, JWT 인증, Excel 워크시트, API 엔드포인트"
description: "Aspose.Cells Cloud API(v3.0)를 사용하여 Excel 워크시트에서 특정 하이퍼링크를 검색합니다. 엔드포인트, 매개변수, cURL 예제, 인증 세부 정보, 오류 처리, SDK 스니펫을 포함합니다."
weight: 10
ArticleTitle: "Aspose.Cells Cloud API – 워크시트 하이퍼링크 가져오기"
---

이 REST API는 **Aspose.Cells 하이퍼링크 가져오기 API**를 사용하여 워크시트의 **하이퍼링크**를 검색합니다.

## 보안 및 인증

Aspose.Cells Cloud API는 보안이 우수하며 [JWT 토큰 기반 인증](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)이 필요합니다.  
엔드포인트를 호출하기 전에 클라이언트 ID와 비밀번호를 사용하여 JWT 액세스 토큰을 획득하고, 이를 `Authorization: Bearer <jwt token>` 헤더에 포함해야 합니다.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
```

### 요청 매개변수

| 매개변수 이름      | 유형    | 위치  | 설명                                      |
| ------------------ | ------- | ----- | ----------------------------------------- |
| name               | string  | path  | Excel 파일의 이름입니다.                  |
| sheetName          | string  | path  | 링크를 포함하는 워크시트의 이름입니다.    |
| hyperlinkIndex     | integer | path  | 검색할 하이퍼링크의 0부터 시작하는 인덱스입니다. |
| folder             | string  | query | 문서가 저장된 폴더입니다.                 |
| storageName        | string  | query | 스토리지 서비스의 이름입니다.             |

### 오류 응답

| HTTP 코드 | 이유                                                 | 예시 본문                                                            |
| --------- | ---------------------------------------------------- | -------------------------------------------------------------------- |
| **400**   | 잘못된 요청 – 누락되거나 유효하지 않은 매개변수입니다. | `{ "Code":"400", "Message":"Invalid parameter value." }`            |
| **401**   | 인증되지 않음 – 누락되거나 유효하지 않은 JWT 토큰입니다. | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**   | 찾을 수 없음 – 워크북 또는 워크시트가 존재하지 않습니다. | `{ "Code":"404", "Message":"File not found." }`                     |
| **500**   | 내부 서버 오류 – 예기치 않은 서버 실패입니다.         | `{ "Code":"500", "Message":"An unexpected error occurred." }`       |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Hyperlinks/GetWorksheetHyperlink)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API에 호출을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Hyperlink": {
    "Address": "https://docs.aspose.cloud/display/cellscloud/Get+Hyperlink+from+Excel+Worksheet",
    "Area": {
      "EndColumn": 0,
      "EndRow": 1,
      "StartColumn": 0,
      "StartRow": 1
    },
    "ScreenTip": null,
    "TextToDisplay": "https://docs.aspose.cloud/display/cellscloud/Get+Hyperlink+from+Excel+Worksheet",
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/hyperlinks/1",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetHyperlink.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetHyperlink.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetHyperlink.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetHyperlink.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetHyperlink.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetHyperlink.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetHyperlink.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetHyperlink.go" >}}

{{< /tab >}}

{{< /tabs >}}