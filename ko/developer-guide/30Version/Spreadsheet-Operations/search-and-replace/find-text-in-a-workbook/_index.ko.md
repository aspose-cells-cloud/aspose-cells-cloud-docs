---
title: "Excel 워크북에서 텍스트 찾기"
second_title: "문서"
linktitle: "워크북에서 찾기"
type: docs
url: /ko/workbook/find-text/
aliases: [  /ko/find-text-in-a-workbook/ ]
weight: 30
keywords: "Aspose.Cells, 텍스트 찾기, Excel API, 워크북 검색"
description: "Aspose.Cells Cloud API를 사용하여 Excel 워크북(XLS‑X, ODS)에서 **텍스트를 검색**하는 방법을 알아보세요. cURL 예제, SDK 스니펫, 응답 스키마가 포함되어 있습니다. 지금 시작하세요."
ArticleTitle: "Aspose.Cells Cloud API를 사용하여 Excel 워크북에서 텍스트 찾기"
---

이 REST API는 Excel 워크북에서 텍스트를 검색합니다.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/findText
```

### **보안 및 인증**

Aspose.Cells Cloud API는 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름 | 유형   | 위치 | 설명                                               |
| ------------- | ------ | ---- | -------------------------------------------------- |
| name          | string | path | Excel 워크북의 이름입니다.                        |
| text          | string | query | 검색할 텍스트 문자열입니다.                       |
| folder        | string | query | 워크북이 포함된 폴더(선택 사항)입니다.            |
| storageName   | string | query | 워크북이 위치한 저장소 이름(선택 사항)입니다.      |

### **응답**

```json
{
  "Status":"OK",
  "Code":200,
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "Text": "string"
      }
    ]
  }
}
```

**HTTP 상태 코드**

| 코드 | 의미                     | 설명                                             |
|------|--------------------------|--------------------------------------------------|
| 200  | OK (성공)                | 필터가 성공적으로 적용되었으며, 응답에 작업 세부정보가 포함되어 있습니다. |
| 400  | 잘못된 요청              | 누락되거나 유효하지 않은 매개변수(예: 지원되지 않는 파일 유형)입니다. |
| 401  | 인증되지 않음            | 잘못되거나 누락된 JWT 토큰입니다.                 |
| 413  | 요청 페이로드가 너무 큼  | 업로드된 파일이 크기 제한을 초과했습니다.         |
| 500  | 내부 서버 오류           | 예기치 않은 서버 오류입니다.                      |

## SDK를 사용하여 PostWorkbooksTextSearch API 사용하는 방법

### PostWorkbooksTextSearch API 사양

<a href="https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbooksTextSearch" target="_blank" rel="noopener noreferrer">OpenAPI 사양</a>은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/findText?text=a" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <your_access_token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "Text": "string"
      }
    ]
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용

SDK를 사용하는 것이 가장 빠른 개발 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbooksTextSearch.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbooksTextSearch.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbooksTextSearch.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbooksTextSearch.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbooksTextSearch.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbooksTextSearch.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbooksTextSearch.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbooksTextSearch.go" >}}

{{< /tab >}}

{{< /tabs >}}
---