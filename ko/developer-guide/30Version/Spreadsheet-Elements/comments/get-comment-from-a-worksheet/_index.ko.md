---
title: "워크시트 코멘트 가져오기 – Aspose.Cells Cloud API 문서"
type: docs
url: /ko/comments/get/
aliases: [  /ko/get-comment-from-a-worksheet/ ]
keywords: "Aspose.Cells, 워크시트 코멘트, API, GET, Excel"
description: "Aspose.Cells Cloud API(v3.0)를 사용하여 셀 이름으로 워크시트 코멘트를 검색하는 방법을 알아보세요. 요청 URL, 파라미터, cURL 예제, 응답 세부 정보, SDK 코드 스니펫 포함."
weight: 10
ArticleTitle: "워크시트 코멘트 가져오기 – Aspose.Cells Cloud API 문서"
---

이 REST API는 **Aspose.Cells Cloud**를 사용하여 셀 이름으로 워크시트 코멘트를 검색합니다.

**필수 조건:** 이 작업을 호출하려면 `Authorization` 헤더에 유효한 JWT 액세스 토큰(`Bearer <jwt token>`)을 포함해야 합니다. 토큰은 [인증 가이드](/cells/authentication/)에 설명된 Aspose.Cells Cloud 인증 흐름을 통해 획득할 수 있습니다.

## GetWorksheetComment API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 위해 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 파라미터

| 파라미터 이름 | 타입   | 위치 (URL 경로 / 쿼리 문자열) | 설명                                                              |
| ------------- | ------ | ----------------------------- | ----------------------------------------------------------------- |
| name          | string | URL 경로                      | Excel 파일 이름.                                                  |
| sheetName     | string | URL 경로                      | 코멘트를 포함하는 워크시트 이름.                                  |
| cellName      | string | URL 경로                      | 코멘트를 검색할 셀 주소(예: **A1**).                              |
| folder        | string | 쿼리 문자열                   | 문서가 저장된 폴더 경로.                                          |
| storageName   | string | 쿼리 문자열                   | 스토리지 서비스 이름.                                             |

<a href="https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetComment" rel="noopener noreferrer">OpenAPI 사양</a>은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 요청을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/A1" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Comment": {
    "CellName": "A1",
    "Author": "roy.wang",
    "HtmlNote": "",
    "Note": "Aspose.Cells Cloud.",
    "AutoSize": "True",
    "IsVisible": "True",
    "Width": 30,
    "Height": 10,
    "TextHorizontalAlignment": "Bottom",
    "TextOrientationType": "TopToBottom",
    "TextVerticalAlignment": "Bottom"
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**응답:** API는 다음 필드를 포함하는 `Comment` 객체를 포함하는 JSON 객체를 반환합니다:

| 필드                        | 타입    | 설명                                                    |
| -------------------------- | ------- | ------------------------------------------------------- |
| `CellName`                 | string  | 셀의 주소(예: **A1**).                                   |
| `Author`                   | string  | 코멘트 작성자의 이름.                                   |
| `HtmlNote`                 | string  | HTML 형식의 코멘트 내용(있는 경우).                      |
| `Note`                     | string  | 일반 텍스트 형태의 코멘트.                              |
| `AutoSize`                 | boolean | 코멘트 박스가 자동 크기 조정되는지 여부.                 |
| `IsVisible`                | boolean | 코멘트가 표시되는지 여부.                               |
| `Width`                    | integer | 코멘트 박스의 너비(문자 단위).                           |
| `Height`                   | integer | 코멘트 박스의 높이(문자 단위).                           |
| `TextHorizontalAlignment` | string  | 텍스트의 수평 정렬(예: **Bottom**).                      |
| `TextOrientationType`      | string  | 텍스트의 방향(예: **TopToBottom**).                      |
| `TextVerticalAlignment`    | string  | 텍스트의 수직 정렬(예: **Bottom**).                      |

## 일반적인 오류

- **401 Unauthorized(인증되지 않음)** – JWT 토큰이 유효하고 만료되지 않았으며 `Authorization` 헤더에 올바르게 설정되었는지 확인하세요.
- **404 Not Found(찾을 수 없음)** – 파일 이름, 워크시트 이름 및 셀 주소가 올바르고, 파일이 지정된 폴더/스토리지에 존재하는지 확인하세요.
- **500 Internal Server Error(내부 서버 오류)** – 요청 페이로드의 데이터 형식이 올바른지 확인하고 서비스가 정상 작동 중인지 확인하세요.

**HTTP 상태 코드**

| 코드 | 의미                         | 설명                                                |
|------|-----------------------------|-----------------------------------------------------|
| 200  | OK                          | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함. |
| 400  | Bad Request(잘못된 요청)     | 누락되거나 잘못된 파라미터(예: 지원되지 않는 파일 형식). |
| 401  | Unauthorized(인증되지 않음)   | 잘못되거나 누락된 JWT 토큰.                          |
| 413  | Payload Too Large(페이로드 너무 큼) | 업로드된 파일이 크기 제한을 초과함.                  |
| 500  | Internal Server Error(내부 서버 오류) | 예기치 않은 서버 오류.                               |

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetComments.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetComments.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetComments.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetComments.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetComments.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetComments.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetComments.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetComments.go" >}}

{{< /tab >}}

{{< /tabs >}}