---
title: "목록 개체 내보내기"
second_title: "문서"
linktitle: "목록 개체"
type: docs
url: /ko/export-excel-listobject-to-different-formats/
aliases: [  /ko/export/excel-listobject-to-different-formats/ ]
keywords: "목록 개체 내보내기, Excel 목록 개체, Aspose.Cells Cloud, REST API, PDF, CSV, JSON, XLSX, ODS, PNG, TIFF, SDKs"
description: "Aspose.Cells Cloud REST API는 Excel 목록 개체를 다양한 파일 형식으로 내보낼 수 있도록 지원합니다. C#, Java, Python, Node.js, Go, PHP, Ruby, Perl, Swift 등 여러 프로그래밍 언어에서 사용 가능한 SDK가 제공됩니다."
weight: 20
---

다음 형식으로 내보낼 수 있습니다: [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/), [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 위해 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>을 요구합니다.


### 요청 매개변수

| 매개변수 이름 | 유형    | 경로/쿼리 문자열/HTTP 본문 | 필수 여부 | 설명 |
|---------------|---------|-----------------------------|-----------|------|
| file          | file    | formData                    | True      | 업로드할 파일 |
| objectType    | string  | query                       | True      | 내보낼 객체 유형입니다. 차트 내보낼 경우 `chart`를 사용합니다. 다른 가능한 값으로는 `worksheet`, `picture` 등이 있습니다. |
| format        | string  | query                       | True      | 원하는 출력 형식입니다. 지원되는 값: `png`, `jpeg`, `gif`, `bmp`, `svg`, `tiff`, `emf`, `wmf`, `pdf` |

### 응답

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet1_ListObjects_0.tif",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet2_ListObjects_0.tif",
      "FileSize": 10040,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet1_ListObjects_0.tif",
      "FileSize": 382,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```


**HTTP 상태 코드**

| 코드 | 의미                        | 설명 |
|------|-----------------------------|------|
| 200  | OK                          | 필터가 성공적으로 적용되었으며, 응답에 작업 세부 정보가 포함됩니다. |
| 400  | Bad Request                 | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식)입니다. |
| 401  | Unauthorized                | 잘못되거나 누락된 JWT 토큰입니다. |
| 413  | Payload Too Large           | 업로드된 파일이 크기 제한을 초과했습니다. |
| 500  | Internal Server Error       | 예기치 않은 서버 오류입니다. |

## SDK를 사용하여 PostExport API 사용하는 방법

### PostExport API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/LightCells/PostExport)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

**cURL** 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예시는 cURL을 사용하여 Cloud API에 요청을 보내는 방법을 보여줍니다.

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=listobject&format=tiff" \
-H "accept: multipart/form-data" \
-H "Content-Type: multipart/form-data" \
-H "x-aspose-client: Containerize.Swagger" \
-d '{"File":{}}'
```

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK가 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예시는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportListObject.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportListObject.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportListObject.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportListObject.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportListObject.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportListObject.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportListObject.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportListObject.go" >}}
{{< /tab >}}

{{< /tabs >}}