---
title: "Excel 워크시트의 모든 도형 가져오기"
second_title: "문서"
linktitle: "get-all"
type: docs
url: /shapes/get-all/
aliases: [/get-all-shapes-inside-the-worksheet/]
keywords: "Aspose.Cells, 클라우드 API, Excel 도형, 도형 가져오기, REST, SDK"
description: "Aspose.Cells Cloud REST API를 사용하여 워크시트에서 모든 도형(차트, 이미지, 텍스트 상자 등)을 검색합니다. cURL 예제, SDK 코드 스니펫, 인증 단계 및 오류 처리 방법을 포함합니다."
ArticleTitle: "Excel 워크시트의 모든 도형 가져오기"
weight: 10
---

이 REST API는 Excel 워크시트의 모든 도형을 검색할 수 있도록 지원합니다.

## 보안 및 인증
Aspose.Cells Cloud API는 안전하며, [JWT 토큰 기반 인증](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)이 필요합니다.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes
```

### 요청 파라미터

| 파라미터 이름   | 유형   | 위치   | 설명                                                                                                    |
| --------------- | ------ | ------ | ------------------------------------------------------------------------------------------------------- |
| **name**        | string | path   | Excel 파일 이름.                                                                                        |
| **sheetName**   | string | path   | 워크시트 이름.                                                                                          |
| **folder**      | string | query  | 문서가 위치한 폴더.                                                                                     |
| **storageName** | string | query  | 사용할 스토리지 서비스 이름.                                                                            |
| **include**     | string | query  | `details`로 설정하면 전체 도형 속성을 반환하고, 그렇지 않으면 `link` 객체만 반환합니다.                 |

> **선택 사항**: 파일이 루트 스토리지에 저장된 경우 `folder`, `storageName`, `include` 파라미터는 생략 가능합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 접근할 수 있습니다. 아래 예제는 선택적 쿼리 파라미터를 포함한 요청을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes?folder=Samples&storageName=MyStorage" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Shapes": {
    "ShapeList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      },
      {
        "link": {
          "Href": "/1",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      },
      {
        "link": {
          "Href": "/2",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      },
      {
        "link": {
          "Href": "/3",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes",
      "Rel": "self",
      "Type": null,
      "Title": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### 응답 필드

`Shapes` 객체는 `Shape` 항목 목록을 포함합니다. 각 도형은 다음 속성을 포함합니다(`include=details` 플래그를 사용한 경우에만 해당하며, 그렇지 않으면 `link` 객체만 반환됩니다).

| 속성       | 유형   | 설명                                                                     |
| ---------- | ------ | ------------------------------------------------------------------------ |
| **Name**   | string | 도형에 할당된 이름(예: "Chart 1")                                        |
| **Type**   | string | 도형 유형(예: `Chart`, `Picture`, `TextBox`)                             |
| **Top**    | number | 워크시트 상단 가장자리부터 도형까지의 거리(포인트 단위)                   |
| **Left**   | number | 워크시트 왼쪽 가장자리부터 도형까지의 거리(포인트 단위)                   |
| **Width**  | number | 도형의 너비(포인트 단위)                                                  |
| **Height** | number | 도형의 높이(포인트 단위)                                                  |
| **Link**   | object | 하이퍼링크 정보(`Href`, `Rel`, `Type`, `Title`)                          |

## 오류 처리

| HTTP 상태 코드 | 설명                                         | 예시 오류 본문                                                    |
| -------------- | -------------------------------------------- | ---------------------------------------------------------------- |
| **400**        | 잘못된 요청 — 잘못된 형식의 파라미터.         | `{ "Code": 400, "Message": "Invalid parameter value." }`         |
| **401**        | 인증되지 않음 — 토큰 누락 또는 유효하지 않은 토큰. | `{ "Code": 401, "Message": "Access token is missing or invalid." }` |
| **404**        | 없음 — 워크북 또는 워크시트가 존재하지 않음.   | `{ "Code": 404, "Message": "File or worksheet not found." }`     |
| **500**        | 내부 서버 오류 — 예기치 않은 조건.            | `{ "Code": 500, "Message": "An unexpected error occurred." }`    |

성공적인 요청은 위의 응답 예시와 같이 `Shapes` 객체를 포함한 **HTTP 200** 상태 코드를 반환합니다.

이 API는 JWT 토큰당 **분당 150회 요청** 제한을 적용합니다. 이 제한을 초과할 경우 **HTTP 429** 상태 코드와 `Retry-After` 헤더가 반환되며, 이 헤더는 재시도 가능한 시점을 나타냅니다.

## 클라우드 SDK 패밀리

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 처리해주므로, 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetShapes.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetShapes.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetShapes.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetShapes.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetShapes.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetShapes.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetShapes.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetShapes.go" >}}

{{< /tab >}}

{{< /tabs >}}