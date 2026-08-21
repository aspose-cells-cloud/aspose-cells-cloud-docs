---
title: "모든 하이퍼링크 가져오기 – Aspose.Cells Cloud REST API"
type: docs
url: /hyperlinks/get-all/
aliases:
  [/get-hyperlink-from-excel-worksheet/, /get-hyperlinks-from-excel-worksheet/]
keywords: "Aspose.Cells, 모든 하이퍼링크 가져오기, Excel API, REST API, 클라우드 SDK, cURL 예제, 스프레드시트 하이퍼링크"
description: "Aspose.Cells Cloud REST API(v3.0)를 사용하여 Excel 파일의 워크시트에서 모든 하이퍼링크를 검색합니다. HTTPS 엔드포인트, 필수 매개변수, cURL 예제, 응답 스키마 및 SDK 코드 예제가 포함됩니다."
weight: 10
ArticleTitle: "모든 하이퍼링크 가져오기 – Aspose.Cells Cloud REST API 문서"
---

이 REST API는 Excel 워크북의 특정 워크시트에서 **모든 하이퍼링크**를 검색합니다.

## 보안 및 인증

Aspose.Cells Cloud API는 보안이 강화되어 있으며, [JWT 토큰 기반 인증](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)이 필요합니다.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks
```

### 요청 매개변수

| 매개변수 이름 | 유형   | 위치 | 필수 여부 | 기본값 | 설명                             |
| ------------- | ------ | ---- | --------- | ------ | -------------------------------- |
| name          | string | path | 예       | –      | Excel 문서의 이름입니다.         |
| sheetName     | string | path | 예       | –      | 워크시트의 이름입니다.           |
| folder        | string | query| 아니요   | –      | 문서가 포함된 폴더입니다.        |
| storageName   | string | query| 아니요   | –      | 사용할 스토리지 서비스의 이름입니다. |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Hyperlinks/GetWorksheetHyperlinks)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예제는 cURL을 사용하여 API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Hyperlinks": {
    "Count": 4,
    "HyperlinkList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/1",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/2",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/3",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      }
    ],
    "link": null
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

JSON 응답은 `Hyperlinks` 객체를 포함합니다.

- **Count** – 워크시트 내 하이퍼링크의 총 개수입니다.
- **HyperlinkList** – 각 항목이 `link` 객체를 포함하는 배열입니다. `Href` 속성은 하이퍼링크 주소를 저장하며, `Rel`, `Title`, `Type`은 추가 메타데이터를 제공합니다(간단한 링크의 경우 일반적으로 `null`입니다).

### 오류 응답

| HTTP 코드 | 이유                                               | 예제 본문                                                           |
| --------- | -------------------------------------------------- | ------------------------------------------------------------------- |
| **400**   | 잘못된 요청 – 누락되거나 잘못된 매개변수입니다.   | `{ "Code":"400", "Message":"Invalid parameter value." }`            |
| **401**   | 인증되지 않음 – 누락되거나 잘못된 JWT 토큰입니다. | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**   | 찾을 수 없음 – 워크북 또는 워크시트가 존재하지 않습니다. | `{ "Code":"404", "Message":"File not found." }`                     |
| **500**   | 내부 서버 오류 – 예기치 않은 서버 오류입니다.      | `{ "Code":"500", "Message":"An unexpected error occurred." }`       |

## 클라우드 SDK 패밀리

SDK를 사용하면 이 기능을 통합하는 가장 빠른 방법입니다. SDK는 저수준 세부 사항을 처리하므로 비즈니스 로직에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetHyperlinks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetHyperlinks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetHyperlinks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetHyperlinks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetHyperlinks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetHyperlinks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetHyperlinks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetHyperlinks.go" >}}

{{< /tab >}}

{{< /tabs >}}