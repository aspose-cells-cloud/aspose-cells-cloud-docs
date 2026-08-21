---
title: "Excel 워크시트에서 셀 서식 지우기"
type: docs
url: /clear-cells-formatting-in-excel-worksheet/
weight: 100
keywords: "Aspose.Cells Cloud, Excel, 셀 서식 지우기, REST API, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트의 셀 서식을 지웁니다. 요청 세부 정보, cURL 예제, 여러 언어의 SDK 코드 스니펫을 포함합니다."
ArticleTitle: "Excel 워크시트에서 셀 서식 지우기 - Aspose.Cells Cloud API"
---

**참고:** 모든 Aspose.Cells Cloud API 호출은 **HTTPS**를 통해 이루어져야 합니다. HTTP 엔드포인트는 더 이상 사용되지 않으며 브라우저에서 차단될 수 있습니다.

- **메서드:** POST  
- **엔드포인트:** `https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/clearformats`

이 REST API는 Excel 파일에서 셀 서식을 지우며, Aspose.Cells Cloud 스위트의 일부로 Excel 워크시트의 셀 서식을 지우는 데 사용됩니다.

## PostClearFormats API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/clearformats
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 위해 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **응답**

```json
{
    "Status":"OK",
    "Code":200
}
```

**응답 스키마**

| 필드   | 유형    | 설명                                           |
|--------|---------|------------------------------------------------|
| Code   | 정수    | API에서 반환된 HTTP 상태 코드(예: 200)            |
| Status | 문자열  | 작업 결과 (`OK`는 성공을 나타냄)                 |

**HTTP 상태 코드**

| 코드 | 의미                         | 설명                                              |
|------|-----------------------------|---------------------------------------------------|
| 200  | OK                          | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함 |
| 400  | 잘못된 요청                   | 누락되었거나 유효하지 않은 매개변수(예: 지원되지 않는 파일 형식) |
| 401  | 인증되지 않음                 | 유효하지 않거나 누락된 JWT 토큰                   |
| 413  | 페이로드가 너무 큼            | 업로드된 파일이 크기 제한을 초과함                 |
| 500  | 내부 서버 오류                | 예기치 않은 서버 오류                              |

## SDK를 사용하여 PostClearFormats API 사용하는 방법

### PostClearFormats API 사양

<a href="https://apireference.aspose.cloud/cells/#/Cells/PostClearFormats" rel="noopener noreferrer">OpenAPI 사양</a>은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 아래 예제는 cURL을 사용하여 Cloud API에 호출을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/clearformats?range=a1%3Aa10&startRow=1&startColumn=1&endRow=10&endColumn=10" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

### Aspose.Cells Cloud SDK 사용

SDK를 사용하는 것이 개발 속도를 높이는 가장 빠른 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostClearFormats.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostClearFormats.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostClearFormats.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostClearFormats.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostClearFormats.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostClearFormats.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostClearFormats.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostClearFormats.go" >}}

{{< /tab >}}

{{< /tabs >}}

**참고 자료**

- [셀 내용 및 스타일 지우기](https://docs.aspose.cloud/cells/clear-contents-and-styles)  
- [셀 스타일 설정](https://docs.aspose.cloud/cells/set-cell-style)