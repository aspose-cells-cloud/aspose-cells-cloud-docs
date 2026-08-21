---
title: "수직 페이지 나누기 가져오기"
second_title: "문서"
linktitle: "수직 페이지 나누기 가져오기"
type: docs
url: /ko/page-breaks/get-vertical-page-breaks/
aliases: [  /ko/get-vertical-page-breaks-inside-worksheet/ ]
keywords: "Aspose.Cells, 수직 페이지 나누기, Excel API, 클라우드 스프레드시트, REST API"
description: "Aspose.Cells Cloud REST API(v3.0)를 사용하여 Excel 워크시트에서 수직 페이지 나누기를 검색합니다. HTTPS 엔드포인트, 필수 매개변수, cURL 예제, 응답 세부정보, 오류 처리 및 SDK 샘플 포함."
weight: 20
---

이 REST API는 워크시트에서 **수직** 페이지 나누기를 검색합니다.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks
```

### 요청 매개변수

| 매개변수 이름 | 유형   | 위치   | 설명                                           | 필수 여부 |
| ------------- | ------ | ------ | ---------------------------------------------- | --------- |
| `name`        | string | path   | Excel 파일의 이름.                             | 예        |
| `sheetName`   | string | path   | 나누기를 읽어올 워크시트의 이름.               | 예        |
| `folder`      | string | query  | 파일이 저장된 스토리지 폴더.                   | 아니요    |
| `storageName` | string | query  | 사용할 Aspose Cloud 스토리지의 이름.           | 아니요    |

[OpenAPI 사양서](https://apireference.aspose.cloud/cells/#/PageBreaks/GetVerticalPageBreaks)는 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

**cURL**을 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용해 클라우드 API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/verticalpagebreaks" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "VerticalPageBreaks": {
    "VerticalPageBreakList": [
      {
        "Column": 3,
        "EndRow": 1048575,
        "StartRow": 0
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/VerticalPageBreaks",
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

### 응답 세부정보

| 필드                    | 유형   | 설명                                                                                 |
| ----------------------- | ------ | ------------------------------------------------------------------------------------ |
| `VerticalPageBreakList` | array  | 수직 페이지 나누기 객체의 컬렉션.                                                    |
| `Column`                | int    | 나누기가 발생하는 열 인덱스(0부터 시작).                                              |
| `StartRow`              | int    | 나누기 범위의 첫 번째 행(0부터 시작).                                                 |
| `EndRow`                | int    | 나누기 범위의 마지막 행(0부터 시작, 일반적으로 마지막 행을 나타내는 `1048575`).        |
| `link.Href`             | string | 리소스에 대한 자기 참조 URL(HTTPS).                                                  |
| `Code`                  | int    | 서비스에서 반환된 HTTP 상태 코드.                                                     |
| `Status`                | string | HTTP 상태에 대한 텍스트 설명.                                                         |

### 오류 처리

| HTTP 코드 | 의미                  | 일반적인 원인                               |
| --------- | --------------------- | ------------------------------------------- |
| 401       | 인증되지 않음         | JWT 토큰 누락 또는 유효하지 않은 토큰.      |
| 404       | 찾을 수 없음          | 지정된 파일 또는 워크시트가 존재하지 않음.  |
| 400       | 잘못된 요청           | 잘못되거나 형식이 잘못된 쿼리 매개변수.     |
| 500       | 내부 서버 오류        | 예기치 않은 서버 측 조건.                   |

추가 세부 정보는 JSON 응답의 `Code` 및 `Status` 필드를 확인하십시오.

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 Aspose.Cells Cloud에 가장 빠르게 개발하는 방법입니다. SDK는 저수준 세부 사항을 추상화하여 비즈니스 로직에 집중할 수 있도록 합니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하십시오.

다음 코드 예제는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetVerticalPageBreaks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetVerticalPageBreaks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetVerticalPageBreaks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetVerticalPageBreaks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetVerticalPageBreaks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetVerticalPageBreaks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetVerticalPageBreaks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetVerticalPageBreaks.go" >}}

{{< /tab >}}

{{< /tabs >}}