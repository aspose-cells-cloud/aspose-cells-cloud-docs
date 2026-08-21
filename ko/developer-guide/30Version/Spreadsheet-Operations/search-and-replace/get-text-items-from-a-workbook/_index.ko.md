---
title: "Excel 워크북에서 텍스트 항목 가져오기"
ArticleTitle: "Aspose.Cells Cloud API를 사용하여 Excel 워크북에서 텍스트 항목 가져오기"
second_title: "문서"
linktitle: "워크북에서 가져오기"
type: docs
url: /ko/workbook/get-text-items/
aliases: [  /ko/get-text-items-from-a-workbook/ ]
weight: 10
keywords: "Excel, Aspose.Cells Cloud, REST API, 스프레드시트, 텍스트 항목 가져오기, 워크북"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크북에서 텍스트 항목을 검색합니다. C#, Java, Python, PHP, Ruby, Go, Node.js, Perl, Swift SDK를 통해 사용 가능합니다."
---


## REST API

이 REST API는 Excel 파일의 워크북에서 **텍스트 항목**을 읽어옵니다.

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/textItems
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 위해 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.


### 요청 매개변수

| 매개변수 이름 | 유형   | 위치 | 설명                                            |
| -------------- | ------ | -------- | ------------------------------------------------------ |
| name           | string | path     | 워크북 파일의 이름입니다.                         |
| folder         | string | query    | 워크북이 위치한 스토리지의 폴더 경로입니다. |
| storageName    | string | query    | 스토리지 서비스의 이름입니다.                       |

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

| 코드 | 의미                     | 설명                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | 성공 (OK)                          | 필터가 성공적으로 적용되었으며, 응답에 작업 세부 정보가 포함됩니다. |
| 400  | 잘못된 요청 (Bad Request)                 | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형)가 있습니다. |
| 401  | 인증되지 않음 (Unauthorized)                | 잘못되었거나 누락된 JWT 토큰입니다. |
| 413  | 페이로드가 너무 큼 (Payload Too Large)           | 업로드된 파일이 크기 제한을 초과했습니다. |
| 500  | 내부 서버 오류 (Internal Server Error)       | 예기치 않은 서버 오류입니다. |
## SDK를 사용하여 GetWorkbookTextItems API 사용하는 방법

### GetWorkbookTextItems API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkbookTextItems)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예시는 cURL을 사용하여 Cloud API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/test.xlsx/textItems" -H "accept: application/json"
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

일반적인 HTTP 응답 코드:

| 코드 | 설명                                 |
|------|---------------------------------------------|
| 200  | 요청 성공; 텍스트 항목이 반환됩니다. |
| 401  | 인증되지 않음 – 토큰이 누락되었거나 유효하지 않습니다.    |
| 403  | 접근 거부 – 권한이 부족합니다.       |
| 404  | 찾을 수 없음 – 워크북 또는 리소스를 찾을 수 없습니다. |
| 500  | 내부 서버 오류 – 예기치 않은 실패입니다. |

### Aspose.Cells Cloud SDK 사용하기

이 예시는 API 버전 **v3.0**을 사용합니다. 최신 버전은 변경 로그를 참고하십시오. SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하십시오.

다음 코드 예시는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbookTextItems.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbookTextItems.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbookTextItems.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbookTextItems.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbookTextItems.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbookTextItems.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbookTextItems.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbookTextItems.go" >}}

{{< /tab >}}

{{< /tabs >}}