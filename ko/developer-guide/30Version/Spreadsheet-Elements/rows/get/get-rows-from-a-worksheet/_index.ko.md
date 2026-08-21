---
title: "Excel 워크시트에서 행 정보 가져오기"
second_title: "문서"
linktitle: "행"
type: docs
url: /ko/rows/get/rows/
aliases: [  /ko/get-row-from-a-worksheet/ ]
keywords: "Aspose.Cells Cloud, 행 가져오기 API, Excel 워크시트 행, REST API, cURL 예제, SDK 예제, .NET, Java, Python"
description: "Aspose.Cells Cloud REST API(v3.0)를 사용하여 Excel 워크시트에서 행 정보를 검색하는 방법을 알아보세요. C#, Java, Python 등 다양한 언어에 대한 엔드포인트, 매개변수, 인증, cURL 및 SDK 코드 예제가 포함되어 있습니다."
weight: 10
ArticleTitle: "Excel 워크시트에서 행 정보 가져오기 – Aspose.Cells Cloud API 문서"
---

이 REST API는 Excel 워크시트에서 행 정보를 검색합니다.

**사전 요구 사항**  
이 엔드포인트를 호출하려면 `Authorization` 헤더에 유효한 JWT 토큰을 제공해야 합니다. 토큰은 Aspose.Cloud 인증 흐름을 사용하여 획득해야 하며, Cells 작업에 필요한 범위를 포함해야 합니다. 이 API는 v3.0 버전 관리 체계를 따르며, 표준 속도 제한 정책의 적용을 받습니다.

## GetWorksheetRows API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 위해 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>을 요구합니다.

### **요청 매개변수**

| 매개변수 이름 | 유형   | 위치 | 설명                |
| -------------- | ------ | ---- | ------------------- |
| name           | string | path | 워크북 이름.        |
| sheetName      | string | path | 워크시트 이름.      |
| folder         | string | query | 워크북 폴더.       |
| storageName    | string | query | 저장소 이름.       |

[OpenAPI 사양서](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetRows)는 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

**cURL** 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 아래 예제는 cURL을 사용하여 클라우드 API로 요청을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Rows": {
    "MaxRow": 20,
    "RowsCount": 17,
    "RowsList": [
      { "link": { "Href": "/0", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/1", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/2", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/3", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/4", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/5", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/6", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/7", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/8", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/9", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/10", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/11", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/12", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/13", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/14", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/15", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/16", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/17", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/18", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/19", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/20", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/21", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/22", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/23", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/24", "Rel": "self", "Title": null, "Type": null } }
    ],
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/cells/rows",
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

**응답 코드**

| 코드 | 의미                    | 설명                                                                 |
|------|-------------------------|----------------------------------------------------------------------|
| 200  | OK (성공)               | 요청이 성공했으며, 행 정보가 반환됩니다.                              |
| 400  | Bad Request (잘못된 요청) | 요청이 잘못된 형식입니다(예: 필수 매개변수 누락).                      |
| 401  | Unauthorized (인증 실패) | 유효하지 않거나 누락된 JWT 토큰입니다.                                |
| 404  | Not Found (찾을 수 없음) | 지정된 워크북 또는 워크시트가 존재하지 않습니다.                        |
| 500  | Internal Server Error (내부 서버 오류) | 서버에서 예기치 않은 오류가 발생했습니다.                          |

## Cloud SDK Family

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK가 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스로 요청을 수행하는 방법을 보여줍니다:

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```java
curl -X GET "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows" -H "accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Rows": {
    "MaxRow": 20,
    "RowsCount": 17,
    "RowsList": [
      { "link": { "Href": "/0", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/1", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/2", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/3", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/4", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/5", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/6", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/7", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/8", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/9", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/10", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/11", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/12", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/13", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/14", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/15", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/16", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/17", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/18", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/19", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/20", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/21", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/22", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/23", "Rel": "self", "Title": null, "Type": null } },
      { "link": { "Href": "/24", "Rel": "self", "Title": null, "Type": null } }
    ],
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/cells/rows",
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

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK가 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. 아래는 워크시트 행을 검색하기 위한 언어별 코드 예제입니다.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}