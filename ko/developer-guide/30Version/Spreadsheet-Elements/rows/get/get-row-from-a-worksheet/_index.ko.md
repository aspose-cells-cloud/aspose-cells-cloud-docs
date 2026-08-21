---
title: "엑셀 워크시트에서 행 설명 가져오기"
second_title: "문서"
linktitle: "행"
type: docs
url: /ko/rows/get/row/
aliases: [  /ko/get-row-from-a-worksheet/ ]
keywords: "Aspose.Cells Cloud, 엑셀 행 API, 워크시트 행 가져오기, REST API, .NET SDK, Java SDK, Python SDK"
description: "Aspose.Cells Cloud REST API를 사용하여 엑셀 워크시트의 특정 행에 대한 자세한 정보(높이, 스타일, 숨김 상태 등)를 검색합니다. curl 예제, SDK 스니펫 및 오류 처리 포함."
weight: 10
ArticleTitle: "엑셀 워크시트에서 행 설명 가져오기 – Aspose.Cells Cloud API"
---

**필수 조건:**  
- 유효한 JWT 액세스 토큰을 획득하고 이를 `Authorization: Bearer <jwt token>` 헤더에 포함합니다.  
- 워크북이 Aspose Cloud 스토리지에 저장되어 있거나, 존재하는 폴더 경로를 지정합니다.  
- 엔드포인트 URL에 표시된 대로 API 버전 **v3.0**을 사용합니다.

이 REST API는 엑셀 워크시트에서 행 인덱스를 기반으로 행 데이터를 검색합니다.

## GetWorksheetRow API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/{rowIndex}
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 적용되며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **요청 매개변수**

| 매개변수 이름 | 유형    | 위치 | 설명                                                  |
| ------------- | ------- | ---- | ----------------------------------------------------- |
| name          | string  | path | 워크북 파일 이름입니다.                               |
| sheetName     | string  | path | 워크북 내 워크시트 이름입니다.                        |
| rowIndex      | integer | path | 검색할 행의 0부터 시작하는 인덱스입니다.              |
| folder        | string  | query| 워크북이 포함된 폴더입니다.                           |
| storageName   | string  | query| 워크북이 저장된 스토리지 이름입니다.                  |

[OpenAPI 명세서](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetRow)는 공개적으로 사용 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API에 요청을 수행하는 방법을 보여줍니다. 요청을 인증하려면 `Authorization: Bearer <jwt token>` 헤더를 포함하세요.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Row": {
    "GroupLevel": 0,
    "Height": 13.5,
    "Index": 0,
    "IsBlank": false,
    "IsHeightMatched": true,
    "IsHidden": false,
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    },
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/cells/rows/0",
      "Rel": "self"
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

**응답 스키마**

| 속성              | 유형    | 설명                                                           |
|-------------------|---------|----------------------------------------------------------------|
| `GroupLevel`      | integer | 행의 개요 수준(그룹화에 사용됨)입니다.                          |
| `Height`          | number  | 포인트 단위로 측정된 행의 높이입니다.                           |
| `Index`           | integer | 반환된 행의 0부터 시작하는 인덱스입니다.                        |
| `IsBlank`         | boolean | 행에 데이터가 포함되어 있는지 여부를 나타냅니다.                |
| `IsHeightMatched`| boolean | 행 높이가 기본 행 높이와 일치하면 `true`입니다.                 |
| `IsHidden`        | boolean | 행이 숨겨져 있으면 `true`입니다.                                |
| `Style`           | object  | 행에 대한 스타일 정보를 포함하는 개체입니다.                    |
| `link`            | object  | 행 리소스에 대한 하이퍼링크 참조입니다.                         |
| `Code`            | integer | 응답의 HTTP 상태 코드입니다.                                    |
| `Status`          | string  | 상태의 텍스트 설명(예: “OK”)입니다.                             |

{{< /tab >}}

{{< /tabs >}}

**참고 사항 / 오류 처리:** API는 다음과 같은 HTTP 상태 코드를 반환할 수 있습니다:

- **200** – 성공; 행 데이터가 반환됩니다.  
- **401** – 인증되지 않음; JWT 토큰이 누락되었거나 유효하지 않습니다.  
- **404** – 없음; 지정된 워크북, 워크시트 또는 행이 존재하지 않습니다.  
- **500** – 내부 서버 오류; 예기치 않은 조건이 발생했습니다.

| 코드 | 설명                                            | 해결 방법                              |
|------|-------------------------------------------------|----------------------------------------|
| 200  | 성공 – 행 데이터가 반환되었습니다.              | –                                      |
| 401  | 인증되지 않음 – JWT 토큰이 누락되었거나 유효하지 않습니다. | 유효한 JWT 토큰을 제공하세요.          |
| 404  | 없음 – 워크북, 워크시트 또는 행이 누락되었습니다. | 이름과 행 인덱스를 확인하세요.         |
| 500  | 내부 서버 오류 – 예기치 않은 조건이 발생했습니다. | Aspose 지원팀에 문의하세요.            |

오류 코드 전체 목록은 Aspose.Cells Cloud [오류 코드 문서](https://docs.aspose.cloud/cells/)를 참조하세요.

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 개발 속도를 가장 빠르게 할 수 있는 방법입니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 작업에 집중할 수 있도록 도와줍니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetRow.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetRow.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetRow.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetRow.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetRow.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetRow.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetRow.go" >}}

{{< /tab >}}

{{< /tabs >}}