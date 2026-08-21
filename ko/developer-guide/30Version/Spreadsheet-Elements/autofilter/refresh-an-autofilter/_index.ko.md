---
title: "엑셀 워크시트에서 자동 필터 새로 고침"
second_title: "문서"
linktitle: "자동 필터 새로 고침"
type: docs
url: /autofilter/refresh/
aliases: [/refresh-an-autofilter/]
weight: 100
keywords: "Aspose.Cells, AutoFilter, 새로 고침, 엑셀, API, REST"
description: "Aspose.Cells Cloud REST API를 사용하여 엑셀 워크시트에 있는 기존 자동 필터를 새로 고침합니다. C#, Java, Python 등 다양한 언어에 대한 cURL 및 SDK 예제가 포함되어 있습니다."
ArticleTitle: "엑셀 워크시트에서 자동 필터 새로 고침"
---

### **새로 고침**(Refresh) 기능은 무엇을 하나요?

워크시트 데이터가 변경된 후(예: 행 추가 또는 삭제 후) 엔드포인트를 호출하면 현재 필터 기준이 다시 적용됩니다. 이 작업은 필터 정의를 수정하지 않고 단지 뷰를 업데이트하며 상태 응답을 반환합니다.

### REST API

이 REST API는 엑셀 워크시트의 자동 필터를 새로 고침합니다(API 버전 **v3.0**).

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/refresh
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 적용되며 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **응답**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP 상태 코드**

| 코드 | 의미                       | 설명                                             |
|------|---------------------------|--------------------------------------------------|
| 200  | OK (성공)                 | 필터가 성공적으로 적용됨; 응답에는 작업 세부 정보가 포함됩니다. |
| 400  | 잘못된 요청(Bad Request)  | 누락되었거나 유효하지 않은 매개변수(예: 지원되지 않는 파일 유형). |
| 401  | 인증되지 않음(Unauthorized) | 잘못되었거나 누락된 JWT 토큰. |
| 413  | 페이로드가 너무 큼(Payload Too Large) | 업로드된 파일이 크기 제한을 초과함. |
| 500  | 내부 서버 오류(Internal Server Error) | 예기치 않은 서버 오류. |

*오류 응답 예시*  

```json
// 400 Bad Request
{
    "Code": 400,
    "Message": "잘못된 매개변수: sheetName을 찾을 수 없습니다."
}

// 401 Unauthorized
{
    "Code": 401,
    "Message": "인증에 실패했습니다. JWT 토큰이 누락되었거나 유효하지 않습니다."
}

// 413 Payload Too Large
{
    "Code": 413,
    "Message": "업로드된 파일이 허용되는 최대 크기를 초과합니다."
}

// 500 Internal Server Error
{
    "Code": 500,
    "Message": "서버에서 예기치 않은 오류가 발생했습니다."
}
```

## SDK를 사용하여 PostWorksheetAutoFilterRefresh API 사용하는 방법

### PostWorksheetAutoFilterRefresh API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/AutoFilter/PostWorksheetAutoFilterRefresh)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API에 호출을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청(Request)" tabName12="응답(Response)" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/refresh" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your-jwt-token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용하기

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 호출을 수행하는 방법을 보여줍니다.
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetAutoFilterRefresh.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetAutoFilterRefresh.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetAutoFilterRefresh.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetAutoFilterRefresh.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetAutoFilterRefresh.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetAutoFilterRefresh.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetAutoFilterRefresh.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetAutoFilterRefresh.go" >}}

{{< /tab >}}

{{< /tabs >}}
---