---
title: "Aspose.Cells Cloud – Excel 워크북을 PDF, CSV, HTML 등 다양한 형식으로 변환하기 (GET /cells/{name})"
second_title: "문서"
linktitle: "Excel 변환"
type: docs
url: /ko/get-different-formats-files/
aliases:
  - /export-excel-workbook-to-different-file-formats/
  - /export-different-formats/
keywords: "Aspose.Cells, Excel 변환, Excel 변환하기, PDF, CSV, HTML, ODS, JSON, 이미지 형식, 스프레드시트 내보내기, API, REST"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크북을 다양한 형식(PDF, CSV, HTML, PNG 등)으로 가져오는 방법을 알아보세요. cURL, SDK 예제, 인증 및 응답 세부 정보 포함."
weight: 10
ArticleTitle: "Aspose.Cells Cloud – Excel 워크북을 PDF, CSV, HTML 등 다양한 형식으로 변환하기 (GET /cells/{name})"
---

이 REST API는 Excel 워크북을 다른 형식으로 가져옵니다.

## GetWorkBook API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}
```

### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **쿼리 파라미터**

| 파라미터 이름           | 유형     | 설명                                                                                                                                                      | 기본값 |
| ---------------------- | -------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | ------ |
| format                 | string   | 대상 파일 형식(예: CSV, XLS, HTML, MHTML, ODS, PDF, XML, TXT, TIFF, XLSB, XLSM, XLSX, XLTM, XLTX, XPS, PNG, JPG, GIF, EMF, BMP, MD, Numbers, WMF, SVG 등). | –      |
| password               | string   | Excel 파일을 열기 위해 필요한 비밀번호.                                                                                                                   | –      |
| isAutoFit              | bool     | 행 및 열 너비를 자동으로 조정합니다.                                                                                                                       | false  |
| onlySaveTable          | bool     | **true**로 설정 시 테이블 데이터만 저장됩니다. `true` 또는 `false`를 허용합니다.                                                                          | false  |
| outPath                | string   | 결과를 저장할 경로. 단일 파일의 경우 파일 이름과 확장자를 포함하고, 다중 파일의 경우 폴더만 지정합니다.                                                     | –      |
| outStorageName         | string   | 출력 파일이 저장될 스토리지 이름.                                                                                                                          | –      |
| checkExcelRestriction  | bool     | 셀 또는 관련 개체를 수정할 때 Excel 제한 사항을 확인합니다.                                                                                               | false  |
| region                 | string   | 워크북에 적용할 지역 설정.                                                                                                                                 | –      |
| pageWideFitOnPerSheet  | bool     | PDF로 변환 시 각 워크시트에 페이지 너비를 맞춥니다.                                                                                                        | false  |
| pageTallFitOnPerSheet  | bool     | PDF로 변환 시 각 워크시트에 페이지 높이를 맞춥니다.                                                                                                       | false  |
| onePagePerSheet        | bool     | 워크시트당 하나의 PDF 페이지를 생성합니다.                                                                                                                | false  |
| folder                 | string   | 원본 워크북이 위치한 폴더 경로.                                                                                                                            | –      |
| storageName            | string   | 소스 파일이 위치한 스토리지 이름.                                                                                                                          | –      |

### 응답

**성공 (200)** 

- `format` 쿼리 파라미터를 생략하면 API는 워크북 구조 정보를 포함하는 **[워크북](/cells/workbook/)** 객체를 반환합니다.

- `format` 쿼리 파라미터에 파일 유형을 지정하면 API는 요청한 형식으로 변환된 파일을 반환합니다.

```http
HTTP/1.1 200 OK
Content-Type: application/pdf
Content-Disposition: attachment; filename="book1.pdf"
Content-Length: 123456

(바이너리 PDF 데이터)
```

**HTTP 상태 코드**

| 코드 | 의미                         | 설명                                                         |
|------|------------------------------|--------------------------------------------------------------|
| 200  | OK                           | 필터가 성공적으로 적용되었으며, 응답에 작업 세부 정보가 포함됩니다. |
| 400  | Bad Request                  | 누락되거나 유효하지 않은 파라미터(예: 지원되지 않는 파일 형식). |
| 401  | Unauthorized                 | 유효하지 않거나 누락된 JWT 토큰.                             |
| 413  | Payload Too Large            | 업로드된 파일이 크기 제한을 초과했습니다.                    |
| 500  | Internal Server Error        | 예기치 않은 서버 오류.                                        |

> **참고:**  
> - 대규모 워크북은 변환에 더 오랜 시간이 걸릴 수 있으므로 요청 타임아웃을 늘리는 것을 고려하세요.  
> - 일부 형식(예: `ODS`)은 매크로와 같은 특정 Excel 기능을 지원하지 않습니다.

## SDK를 사용하여 GetWorkBook API 사용하기

> **사전 조건:**  
> - Aspose.Cells 인증 흐름을 통해 얻은 유효한 **JWT 액세스 토큰**.  
> - 소스 워크북은 지원되는 Aspose 스토리지에 저장되어 있거나 요청에 직접 제공되어야 합니다.  
> - API 버전(`v3.0`)이 최신 릴리스 버전과 일치하는지 확인하세요.

### GetWorkBook API 사양

<a href="https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook" rel="noopener noreferrer">OpenAPI 사양</a>은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

### 예제 요청

**cURL** 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 액세스할 수 있습니다. 다음 예제는 필요한 인증 헤더가 포함된 올바른 GET 요청을 보여줍니다.

{{< tabs tabTotal="1" tabID="11" tabName11="Request" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=pdf" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger"
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 가장 빠르게 개발할 수 있습니다. SDK는 저수준 세부 정보를 추상화하여 프로젝트 작업에 집중할 수 있도록 합니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}

**참고 자료**

- <a href="https://apireference.aspose.cloud/cells/#/Workbook/ConvertWorkbook" rel="noopener noreferrer">워크북 변환 (POST)</a>  
- <a href="https://apireference.aspose.cloud/cells/#/Workbook/SaveAs" rel="noopener noreferrer">다른 이름으로 저장 (GET)</a>

---

_최종 업데이트: 2024-12-01_

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Aspose.Cells Cloud – Excel 워크북을 PDF, CSV, HTML 등 다양한 형식으로 변환하기 (GET /cells/{name})",
  "description": "Excel 워크북을 PDF, CSV, HTML 등 다양한 형식으로 변환하는 Aspose.Cells Cloud GET /cells/{name} 엔드포인트에 대한 문서입니다.",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2024-12-01",
  "keywords": "Aspose.Cells, Excel 변환, PDF, CSV, HTML, API, REST, 클라우드",
  "url": "https://docs.aspose.cloud/cells/get-different-formats-files/",
  "publisher": {
    "@type": "Organization",
    "name": "Aspose"
  }
}
</script>