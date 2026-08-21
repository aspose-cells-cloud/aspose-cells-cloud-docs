---
title: "엑셀 워크시트에서 텍스트 항목 가져오기"
second_title: "문서"
linktitle: "워크시트에서 텍스트 항목 가져오기"
type: docs
url: /ko/worksheets/get-text-items/
aliases: [  /ko/get-text-items-from-a-worksheet/ ]
weight: 20
keywords: "Aspose.Cells, 클라우드 API, 엑셀, 워크시트, 텍스트 항목, REST"
description: "Aspose.Cells Cloud REST API를 사용하여 엑셀 파일의 특정 워크시트에서 모든 텍스트 항목을 검색합니다. 샘플 cURL, SDK 코드, 인증 단계 및 응답 스키마가 포함됩니다."
ArticleTitle: "엑셀 워크시트에서 텍스트 항목 가져오기"
---

## REST API

이 REST API는 엑셀 파일 내 워크시트의 텍스트 항목을 읽습니다.

```
https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{worksheet}/textItems
```

### 보안 및 인증
Aspose.Cells Cloud API는 [JWT 토큰 기반 인증](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)이 필요하며, 안전하게 설계되었습니다.

### 요청 파라미터


| 파라미터 이름 | 유형   | 위치 | 필수 여부 | 설명                                      |
| -------------- | ------ | -------- | -------- | ---------------------------------------------- |
| name           | string | path     | 예       | 워크북 파일 이름.                            |
| sheetName      | string | path     | 예       | 워크시트 이름.                         |
| folder         | string | query    | 아니요       | 워크북이 포함된 폴더 경로. |
| storageName    | string | query    | 아니요       | Aspose Cloud 스토리지 이름.              |

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
| 200  | 성공 (OK)                          | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보가 포함됨. |
| 400  | 잘못된 요청 (Bad Request)                 | 누락되거나 잘못된 파라미터(예: 지원되지 않는 파일 유형). |
| 401  | 인증되지 않음 (Unauthorized)                | 잘못되거나 누락된 JWT 토큰. |
| 413  | 페이로드가 너무 큼 (Payload Too Large)           | 업로드된 파일이 크기 제한을 초과함. |
| 500  | 내부 서버 오류 (Internal Server Error)       | 예상치 못한 서버 오류. |

## SDK를 사용하여 GetWorksheetTextItems API 사용하는 방법

### GetWorksheetTextItems API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetTextItems){:target="_blank" rel="noopener noreferrer"}은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예시는 cURL을 사용하여 Cloud API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/sheet1/textItems" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
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

### Aspose.Cells Cloud SDK 사용하기

SDK는 저수준 세부 사항을 처리하여 프로젝트 작업에 집중할 수 있도록 통합을 간소화합니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud){:target="_blank" rel="noopener noreferrer"}를 참조하세요.

다음 코드 예시는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 요청을 보내는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetTextItems.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetTextItems.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetTextItems.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetTextItems.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetTextItems.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetTextItems.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetTextItems.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetTextItems.go" >}}

{{< /tab >}}

{{< /tabs >}}