---
title: "가로 페이지 나누기 가져오기"
second_title: "문서"
linktitle: "가로 페이지 나누기 가져오기"
type: docs
url: /page-breaks/get-horizontal-page-breaks/
aliases: [/get-horizontal-page-breaks-inside-worksheet/]
keywords: "가로 페이지 나누기, Aspose.Cells Cloud, REST API, Excel 워크시트, SDK"
description: "Aspose.Cells Cloud API를 통해 Excel 워크시트에서 가로 페이지 나누기를 가져옵니다. 엔드포인트, 매개변수, cURL 예제, 응답 형식, C#, Java, Python 등 다양한 언어의 SDK 코드 스니펫이 포함됩니다."
ArticleTitle: "가로 페이지 나누기 가져오기 - Aspose.Cells Cloud API 문서"
weight: 10
---

**가로 페이지 나누기** – 지정된 행 이후에 인쇄된 페이지가 새 페이지로 시작되도록 강제하는 행 기반 나누기입니다. 이 REST API는 이러한 가로 페이지 나누기를 가져옵니다.

## 보안 및 인증

Aspose.Cells Cloud API는 안전하며 [JWT 토큰 기반 인증](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)이 필요합니다.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks
```

### 요청 매개변수

| 매개변수 이름 | 유형   | 위치   | 설명                                                         |
| ------------- | ------ | ------ | ------------------------------------------------------------ |
| name          | string | path   | Excel 파일 이름입니다.                                       |
| sheetName     | string | path   | 워크시트 이름입니다.                                         |
| folder        | string | query  | 파일이 위치한 저장소의 폴더 경로입니다. _(선택 사항)_      |
| storageName   | string | query  | 저장소 이름입니다. _(선택 사항)_                            |

<a href="https://apireference.aspose.cloud/cells/#/PageBreaks/GetHorizontalPageBreaks" rel="noopener" title="GetHorizontalPageBreaks에 대한 OpenAPI 사양">OpenAPI 사양</a>은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 요청을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예제는 cURL을 사용해 Cloud API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/horizontalpagebreaks" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "HorizontalPageBreaks": {
    "HorizontalPageBreakList": [
      {
        "Row": 6,
        "EndColumn": 16383,
        "StartColumn": 0
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/HorizontalPageBreaks",
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

## 오류 처리

| HTTP 상태 코드 | 설명                                                   | 예제 JSON                                             |
| -------------- | ------------------------------------------------------ | ----------------------------------------------------- |
| 400            | 잘못된 요청 – 누락되었거나 잘못된 매개변수입니다.      | `{ "Code": 400, "Message": "Invalid parameter." }`   |
| 401            | 인증되지 않음 – JWT 토큰이 누락되었거나 잘못되었습니다.| `{ "Code": 401, "Message": "Authentication failed." }`|
| 404            | 찾을 수 없음 – 지정된 파일 또는 워크시트가 없습니다.  | `{ "Code": 404, "Message": "Resource not found." }`  |
| 500            | 내부 서버 오류 – 서버에서 예기치 않은 조건이 발생했습니다. | `{ "Code": 500, "Message": "Server error." }`        |

## 클라우드 SDK 패밀리

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetHorizontalPageBreaks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetHorizontalPageBreaks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetHorizontalPageBreaks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetHorizontalPageBreaks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetHorizontalPageBreaks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetHorizontalPageBreaks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetHorizontalPageBreaks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetHorizontalPageBreaks.go" >}}

{{< /tab >}}

{{< /tabs >}}