---
title: "워크시트 내보내기 – Aspose.Cells Cloud"
second_title: "문서"
linktitle: "워크시트"
type: docs
url: /ko/export-excel-worksheet-to-different-formats/
aliases: [  /ko/export/excel-worksheet-to-different-formats/ ]
keywords: "Aspose.Cells, 워크시트 내보내기, Excel API, PDF, CSV, TIFF, ODS, 이미지 형식"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트를 PDF, CSV, TIFF 등 다양한 형식으로 내보내는 방법을 알아보세요. cURL 예제, 필요한 인증, 매개변수 세부 정보 및 응답 처리를 포함합니다."
weight: 20
ArticleTitle: "Excel 워크시트를 다양한 형식으로 내보내기 – Aspose.Cells Cloud"
---

워크시트는 다음과 같은 형식으로 내보낼 수 있습니다:

- **XLS** – [XLS 형식 세부 정보](https://docs.fileformat.com/spreadsheet/xls/)
- **XLSX** – [XLSX 형식 세부 정보](https://docs.fileformat.com/spreadsheet/xlsx/)
- **XLSB** – [XLSB 형식 세부 정보](https://docs.fileformat.com/spreadsheet/xlsb/)
- **CSV** – [CSV 형식 세부 정보](https://docs.fileformat.com/spreadsheet/csv/)
- **TSV** – [TSV 형식 세부 정보](https://docs.fileformat.com/spreadsheet/tsv/)
- **XLSM** – [XLSM 형식 세부 정보](https://docs.fileformat.com/spreadsheet/xlsm/)
- **ODS** – [ODS 형식 세부 정보](https://docs.fileformat.com/spreadsheet/ods/)
- **TXT** – [TXT 형식 세부 정보](https://docs.fileformat.com/word-processing/txt/)
- **PDF** – [PDF 형식 세부 정보](https://docs.fileformat.com/pdf/)
- **OTS** – [OTS 형식 세부 정보](https://docs.fileformat.com/spreadsheet/ots/)
- **XPS** – [XPS 형식 세부 정보](https://docs.fileformat.com/page-description-language/xps/)
- **DIF** – [DIF 형식 세부 정보](https://docs.fileformat.com/spreadsheet/dif/)
- **PNG** – [PNG 형식 세부 정보](https://docs.fileformat.com/Image/png/)
- **JPEG** – [JPEG 형식 세부 정보](https://docs.fileformat.com/image/jpeg/)
- **BMP** – [BMP 형식 세부 정보](https://docs.fileformat.com/image/bmp/)
- **SVG** – [SVG 형식 세부 정보](https://docs.fileformat.com/page-description-language/svg/)
- **TIFF** – [TIFF 형식 세부 정보](https://docs.fileformat.com/image/tiff/)
- **EMF** – [EMF 형식 세부 정보](https://docs.fileformat.com/image/emf/)
- **NUMBERS** – [Numbers 형식 세부 정보](https://docs.fileformat.com/spreadsheet/numbers/)
- **FODS** – [FODS 형식 세부 정보](https://docs.fileformat.com/spreadsheet/fods/)

[전체 워크북 또는 차트를 내보내는 것과 같은 관련 내보내기 작업을 탐색해 보세요.](https://docs.aspose.cloud/cells/export-excel-workbook-to-different-formats/)

## PostExport API

```http
POST https://api.aspose.cloud/v3.0/cells/export
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 적용되며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름 | 유형    | 경로/쿼리 문자열/HTTP 본문 | 필수 여부 | 설명                                                                 |
|---------------|---------|-----------------------------|-----------|----------------------------------------------------------------------|
| file          | file    | formData                    | True      | 업로드할 파일                                                        |
| objectType    | string  | query                       | True      | 내보낼 개체의 유형입니다. 차트 내보내기에는 `chart`를 사용합니다. 다른 가능한 값으로는 `worksheet`, `picture` 등이 있습니다. |
| format        | string  | query                       | True      | 원하는 출력 형식입니다. 지원되는 값: `png`, `jpeg`, `gif`, `bmp`, `svg`, `tiff`, `emf`, `wmf`, `pdf`. |

### 응답

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet1.tif",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet2.tif",
      "FileSize": 10040,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet3.tif",
      "FileSize": 2824,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4.tif",
      "FileSize": 1350,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet5.tif",
      "FileSize": 12978,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet6.tif",
      "FileSize": 7002,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet7.tif",
      "FileSize": 11532,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet1.tif",
      "FileSize": 382,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet2.tif",
      "FileSize": 382,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3.tif",
      "FileSize": 130084,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet4.tif",
      "FileSize": 120062,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

### **오류 처리**

요청이 실패하면 `Code` 및 `Message` 필드를 포함하는 JSON 오류 객체가 API에서 반환됩니다. 일반적인 HTTP 상태 코드로는 **401 Unauthorized**(토큰 누락 또는 유효하지 않음) 및 **400 Bad Request**(유효하지 않은 매개변수)가 있습니다.

**HTTP 상태 코드**

| 코드 | 의미                       | 설명                                             |
|------|----------------------------|--------------------------------------------------|
| 200  | OK                         | 필터가 성공적으로 적용되었으며, 응답에 작업 세부 정보가 포함됩니다. |
| 400  | Bad Request                | 누락되었거나 유효하지 않은 매개변수(예: 지원되지 않는 파일 유형). |
| 401  | Unauthorized               | 유효하지 않거나 누락된 JWT 토큰. |
| 413  | Payload Too Large          | 업로드된 파일이 크기 제한을 초과합니다. |
| 500  | Internal Server Error      | 예기치 않은 서버 오류. |

**참고 사항**

- 업로드 가능한 최대 파일 크기는 50 MB입니다.  
- API는 단일 요청에서 여러 워크시트를 내보내는 것을 지원하며, 각 워크시트는 `Files` 배열 내 개별 파일로 반환됩니다.  
- 대용량 워크북의 경우 비동기 처리를 지원하며, 작업 상태를 폴링하기 위해 `202 Accepted` 응답을 사용할 수 있습니다.

## SDK를 사용하여 PostExport API 사용 방법

### 사전 요구 사항

API를 호출하기 전에 Aspose.Cells Cloud 인증 흐름을 사용하여 유효한 JWT 액세스 토큰을 획득해야 합니다. 각 요청의 `Authorization` 헤더에 토큰이 포함되어 있어야 합니다. SDK는 클라이언트 자격 증명으로 구성된 경우 자동으로 토큰 획득을 처리합니다.

### PostExport API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/LightCells/PostExport)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

**cURL** 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API를 호출하는 방법을 보여줍니다.

```bash
# 워크시트를 TIFF 형식으로 내보내기
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=worksheet&format=tiff" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -F "File=@MyWorkbook.xlsx"
```

### Aspose.Cells Cloud SDK 사용

SDK를 사용하는 것은 Aspose.Cells Cloud에 대한 개발을 수행하는 가장 빠른 방법입니다. SDK는 저수준 세부 정보를 추상화하여 비즈니스 로직에 집중할 수 있도록 합니다. 지원되는 SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 방문하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}
---