---
title: "Aspose.Cells Cloud 웹 API - 스프레드시트를 다른 형식으로 변환 - 무료 온라인 도구"
second_title: "문서"
ArticleTitle: "스프레드시트를 다른 형식으로 변환하는 방법: 단계별 가이드"
linktype: "스프레드시트 변환"
type: docs
url: /ko/convert-spreadsheet/
keywords: "Aspose, Aspose.Cells, 스프레드시트 변환, Excel을 PDF로, Excel API, 클라우드 파일 변환"
description: "Aspose.Cells Cloud API를 사용해 스프레드시트 파일을 다른 형식으로 변환합니다."
weight: 100
---

Aspose.Cells Cloud 웹 API를 사용하여 로컬 스프레드시트/Excel 파일을 다른 형식으로 변환합니다.

## **스프레드시트 변환 API**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 우수하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **요청 파라미터:**

| 파라미터 이름   | 유형   | 경로/쿼리 문자열/HTTP 본문 | 설명                                                                                      |
| :------------- | :----- | :------------------------- | :------------------------------------------------------------------------------------------|
| Spreadsheet    | 파일   | FormData                   | 변환할 스프레드시트 파일을 업로드합니다.                                                     |
| format         | 문자열 | 쿼리                       | (필수) 원하는 출력 형식(예: “XLSX”, “PDF”, “CSV”)을 지정합니다.                                |
| outPath        | 문자열 | 쿼리                       | (선택 사항) 변환된 워크북을 저장할 폴더 경로입니다. 기본값은 null입니다.                          |
| outStorageName | 문자열 | 쿼리                       | 출력 파일 저장소 이름을 지정합니다.                                                             |
| fontsLocation  | 문자열 | 쿼리                       | 스프레드시트에 사용자 지정 글꼴을 사용합니다.                                                    |
| region         | 문자열 | 쿼리                       | 스프레드시트 지역 설정을 지정합니다.                                                             |
| password       | 문자열 | 쿼리                       | 보호된 스프레드시트 파일을 열기 위한 비밀번호입니다.                                              |

### **응답**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**성공 상태**

- **200 OK** – 변환이 성공적으로 완료되었으며, 응답 본문에 변환된 파일 스트림이 포함됩니다.
- `Content-Type` 헤더는 요청한 출력 형식의 MIME 유형을 반영합니다(예: PDF의 경우 `application/pdf`).

**HTTP 상태 코드**

| 코드 | 의미                  | 설명                                                             |
| ---- | --------------------- | ---------------------------------------------------------------- |
| 200  | OK                    | 필터가 성공적으로 적용되었으며, 응답에 작업 세부 정보가 포함됩니다. |
| 400  | 잘못된 요청            | 누락되거나 잘못된 파라미터(예: 지원되지 않는 파일 형식)가 있습니다.   |
| 401  | 인증되지 않음          | 잘못되거나 누락된 JWT 토큰입니다.                                  |
| 413  | 요청 본문이 너무 큼     | 업로드한 파일이 크기 제한을 초과합니다.                             |
| 500  | 내부 서버 오류         | 예기치 않은 서버 오류가 발생했습니다.                                |

## 변환 가능한 형식

| **출력 형식**                                                                                          | **설명**                                                                                                                   |
| :----------------------------------------------------------------------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------- |
| <a href="https://docs.fileformat.com/spreadsheet/xls/" rel="noopener noreferrer">XLS</a>               | Excel 95/5.0 - 2003 워크북.                                                                                                 |
| <a href="https://docs.fileformat.com/spreadsheet/xlsx/" rel="noopener noreferrer">XLSX</a>             | Office Open XML SpreadsheetML 파일 형식.                                                                                    |
| <a href="https://docs.fileformat.com/spreadsheet/xlsb/" rel="noopener noreferrer">XLSB</a>             | Excel 이진 워크북.                                                                                                          |
| <a href="https://docs.fileformat.com/spreadsheet/xlsm/" rel="noopener noreferrer">XLSM</a>             | Excel 매크로 사용 가능 워크북.                                                                                               |
| <a href="https://docs.fileformat.com/spreadsheet/xlt/" rel="noopener noreferrer">XLT</a>               | Excel 97 - Excel 2003 템플릿.                                                                                               |
| <a href="https://docs.fileformat.com/spreadsheet/xltx/" rel="noopener noreferrer">XLTX</a>             | Excel 템플릿.                                                                                                               |
| <a href="https://docs.fileformat.com/spreadsheet/xltm/" rel="noopener noreferrer">XLTM</a>             | Excel 매크로 사용 가능 템플릿.                                                                                                |
| <a href="https://docs.fileformat.com/spreadsheet/xlam/" rel="noopener noreferrer">XLAM</a>             | Excel에 새 기능을 추가하는 데 사용되는 Excel 매크로 사용 가능 애드인 파일입니다.                                              |
| <a href="https://docs.fileformat.com/spreadsheet/csv/" rel="noopener noreferrer">CSV</a>               | CSV(쉼표로 구분된 값) 파일.                                                                                                  |
| <a href="https://docs.fileformat.com/spreadsheet/tsv/" rel="noopener noreferrer">TSV</a>               | TSV(탭으로 구분된 값) 파일.                                                                                                  |
| <a href="https://docs.fileformat.com/word-processing/txt/" rel="noopener noreferrer">TXT</a>           | 구분 기호가 있는 일반 텍스트 파일.                                                                                            |
| <a href="https://docs.fileformat.com/web/html/" rel="noopener noreferrer">HTML</a>                     | HTML 형식.                                                                                                                  |
| <a href="https://docs.fileformat.com/web/mhtml/" rel="noopener noreferrer">MHTML</a>                   | MHTML 파일.                                                                                                                 |
| <a href="https://docs.fileformat.com/spreadsheet/ods/" rel="noopener noreferrer">ODS</a>               | ODS(OpenDocument 스프레드시트).                                                                                             |
| SpreadsheetML                                                                                          | Excel 2003 XML 파일.                                                                                                        |
| <a href="https://docs.fileformat.com/spreadsheet/numbers/" rel="noopener noreferrer">Numbers</a>       | Apple의 “Numbers” 애플리케이션으로 작성된 문서로, macOS 및 iOS용 iWork 스위트의 일부입니다.                                   |
| <a href="https://docs.fileformat.com/web/json/" rel="noopener noreferrer">JSON</a>                     | JavaScript 객체 표현(JSON).                                                                                                 |
| <a href="https://docs.fileformat.com/spreadsheet/dif/" rel="noopener noreferrer">DIF</a>               | 데이터 교환 형식(DIF).                                                                                                       |
| <a href="https://docs.fileformat.com/database/dbf/" rel="noopener noreferrer">DBF</a>                  | .dbf 확장자를 가진 파일은 dBASE 데이터베이스 관리 시스템에서 사용하는 데이터베이스 파일입니다.                                |
| <a href="https://docs.fileformat.com/pdf/" rel="noopener noreferrer">PDF</a>                           | Adobe Portable Document Format.                                                                                            |
| <a href="https://docs.fileformat.com/page-description-language/xps/" rel="noopener noreferrer">XPS</a> | XML Paper Specification 형식.                                                                                              |
| <a href="https://docs.fileformat.com/page-description-language/svg/" rel="noopener noreferrer">SVG</a> | 확장 가능한 벡터 그래픽스(SCALABLE VECTOR GRAPHICS) 형식.                                                                   |
| <a href="https://docs.fileformat.com/image/tiff/" rel="noopener noreferrer">TIFF</a>                   | 태그ged 이미지 파일 형식(TAGGED IMAGE FILE FORMAT).                                                                       |
| <a href="https://docs.fileformat.com/image/png/" rel="noopener noreferrer">PNG</a>                     | 포터블 네트워크 그래픽스(PORTABLE NETWORK GRAPHICS) 형식.                                                                   |
| <a href="https://docs.fileformat.com/image/bmp/" rel="noopener noreferrer">BMP</a>                     | 비트맵 이미지 형식.                                                                                                         |
| <a href="https://docs.fileformat.com/image/emf/" rel="noopener noreferrer">EMF</a>                     | 향상된 메타파일(ENHANCED METAFILE) 형식.                                                                                    |
| <a href="https://docs.fileformat.com/image/jpeg/" rel="noopener noreferrer">JPEG</a>                   | JPEG은 손실 압축 방식으로 저장되는 이미지 형식입니다.                                                                        |
| <a href="https://docs.fileformat.com/image/gif/" rel="noopener noreferrer">GIF</a>                     | 그래픽스 교환 포맷(GRAPHICS INTERCHANGE FORMAT).                                                                           |
| <a href="https://docs.fileformat.com/word-processing/md/" rel="noopener noreferrer">MARKDOWN</a>       | 마크다운(Markdown) 문서를 나타냅니다.                                                                                        |
| <a href="https://docs.fileformat.com/spreadsheet/sxc/" rel="noopener noreferrer">SXC</a>               | OpenOffice 및 StarOffice에서 사용하는 XML 기반 형식입니다.                                                                   |
| <a href="https://docs.fileformat.com/spreadsheet/fods/" rel="noopener noreferrer">FODS</a>             | 평면 XML로 저장되는 Open Document 형식입니다.                                                                                |
| <a href="https://docs.fileformat.com/word-processing/docx/" rel="noopener noreferrer">DOCX</a>         | XML과 이진 파일을 결합한 Microsoft Word 문서용 널리 알려진 형식입니다.                                                         |
| <a href="https://docs.fileformat.com/presentation/pptx/" rel="noopener noreferrer">PPTX</a>            | PPTX 형식은 Microsoft PowerPoint의 Open XML 프레젠테이션 파일 형식을 기반으로 합니다.                                         |
| <a href="https://docs.fileformat.com/database/sql/" rel="noopener noreferrer">SqlScript</a>            | 구조화된 쿼리 언어(Structured Query Language).                                                                              |
| <a href="https://docs.fileformat.com/web/xhtml/" rel="noopener noreferrer">XHtml</a>                   | XHTML은 XML 기반의 마크업을 사용하는 텍스트 기반 파일 형식으로, HTML 4.0의 재구성 버전을 사용합니다.                           |
| <a href="https://docs.fileformat.com/ebook/epub/" rel="noopener noreferrer">Epub</a>                   | .epub 확장자를 가진 파일은 출판사와 사용자 모두를 위한 표준 디지털 출판 형식인 전자책(e-book) 형식입니다.                       |
| <a href="https://docs.fileformat.com/web/xml/" rel="noopener noreferrer">Xml</a>                       | XML은 확장 가능한 마크업 언어(XML, Extensible Markup Language)를 의미하며, HTML과 유사하지만 태그를 사용해 개체를 정의합니다. |
| <a href="https://docs.fileformat.com/spreadsheet/ots/" rel="noopener noreferrer">Ots</a>               | Open Document 템플릿 시트(OTS, Open Document Template Sheet) 파일입니다.                                                     |
| <a href="https://docs.fileformat.com/ebook/azw3/" rel="noopener noreferrer">AZW3</a>                   | AZW는 아마존에서 Kindle 장치용으로 개발한 디지털 전자책 파일 형식입니다. AZW3은 Kindle Format 8(KF8)이라고도 합니다.          |

## 변환 스프레드시트 API를 어디에 사용해야 할까요?

- **레거시 시스템 마이그레이션**: 수천 개의 레거시 XLS 파일을 현대 시스템용 XLSX로 변환합니다.
- **아카이브 표준화**: 다양한 스프레드시트 형식(XLS, XLSM, ODS, CSV)을 단일 형식으로 정규화하여 아카이브합니다.
- **오피스 스위트 상호 운용성**: Excel 파일을 LibreOffice, Google 시트, Apple Numbers와 호환되는 형식으로 변환합니다.
- **데이터 소스 정규화**: 다양한 스프레드시트 형식을 CSV 또는 JSON으로 변환하여 데이터베이스에 삽입합니다.
- **웹 게시**: 재무 모델을 HTML로 변환하여 웹에 표시합니다.

## 왜 변환 스프레드시트 API를 사용해야 할까요?

- **개발자 친화적**: Aspose.Cells Cloud는 다양한 언어로 SDK 라이브러리를 제공하여 빠른 개발을 가능하게 하며, 포괄적인 문서도 함께 제공됩니다. 사용자 정의 차트 렌더링 솔루션을 구축하는 것에 비해 개발 작업량을 크게 줄여줍니다.
- **비용 효율적**: 워크북을 먼저 업로드하지 않고도 테이블 데이터를 변환할 수 있어 저장 공간을 절약하고 비용을 줄입니다.
- **포괄적인 형식 지원**: 20개 이상의 스프레드시트 형식 간 변환이 가능합니다.
- **데이터 정확성 및 서식 보존.**

## SDK를 사용해 변환 스프레드시트 API를 어떻게 사용하나요?

다음 코드 예제는 다양한 SDK를 사용하여 변환 스프레드시트 API를 사용하는 방법을 보여줍니다.

### 변환 스프레드시트 API 사양

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertSpreadsheet" rel="noopener noreferrer">변환 스프레드시트 API 사양</a>은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하여 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용해 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용해 클라우드 API에 요청하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert?format=pdf \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/file.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="file.pdf"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 저수준 세부 정보를 추상화하여 간결한 코드로 스프레드시트 파일을 다른 형식으로 변환할 수 있어 개발 속도가 가장 빠릅니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorkbook.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorkbook.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorkbook.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorkbook.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorkbook.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorkbook.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorkbook.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorkbook.go" >}}
{{</tab>}}
{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebAPI",
  "name": "Convert Spreadsheet",
  "description": "Convert a spreadsheet file to another format using Aspose.Cells Cloud.",
  "url": "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet",
  "documentation": "https://docs.aspose.cloud/cells/convert-spreadsheet/",
  "targetPlatform": "Web",
  "authenticationType": "OAuth2",
  "operation": [
    {
      "@type": "HttpOperation",
      "httpMethod": "PUT",
      "urlTemplate": "/cells/convert/spreadsheet",
      "description": "Convert a spreadsheet to the specified format."
    }
  ]
}
</script>

---