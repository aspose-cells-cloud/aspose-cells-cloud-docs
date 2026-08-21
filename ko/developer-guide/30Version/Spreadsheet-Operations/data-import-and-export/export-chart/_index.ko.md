---
title: "엑셀 차트 내보내기"
second_title: "문서"
linktype: "차트"
type: docs
url: /export-excel-chart-to-different-formats/
aliases: [/export/excel-chart-to-different-formats/]
description: "Aspose.Cells Cloud REST API 또는 SDK를 사용하여 엑셀 차트 객체를 PNG, JPEG, PDF, SVG, TIFF, EMF, WMF 등 일반적인 형식으로 내보냅니다. 인증, cURL 예제 및 여러 언어의 코드 예제가 포함됩니다."
keywords: "Aspose.Cells, 차트 내보내기, 엑셀 차트 내보내기, REST API, cURL, PDF, PNG, JPEG, SVG, TIFF, EMF, WMF, SDK, 차트 형식, Aspose Cells Cloud"
weight: 20
ArticleTitle: "엑셀 차트 내보내기 – 문서"
---

워크북에서 차트 객체를 다양한 이미지 및 문서 형식으로 내보내는 것은 보고서 작성 및 게시에 일반적으로 요구되는 작업입니다. Aspose.Cells Cloud는 차트를 PNG, JPEG, PDF, SVG, TIFF, EMF, WMF 등 일반적인 형식으로 직접 변환하는 간단한 REST 엔드포인트를 제공합니다.

차트는 다음 형식으로 내보낼 수 있습니다: [PNG](https://docs.fileformat.com/Image/png/), [GIF](https://docs.fileformat.com/image/gif/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [WMF](https://docs.fileformat.com/image/Wmf/), [PDF](https://docs.fileformat.com/pdf/).

**사전 요구 사항:**  
- 활성 구독이 있는 유효한 Aspose.Cells Cloud 계정  
- 인증 플로우를 통해 획득한 OAuth 2.0 Bearer 토큰(JWT)  
- 업로드할 워크북 파일(최대 크기 < 50 MB)  

## **REST API**

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름 | 유형   | 경로/쿼리 문자열/HTTP 본문 | 필수 여부 | 설명                                                                                                                     |
|---------------|--------|-----------------------------|-----------|--------------------------------------------------------------------------------------------------------------------------|
| file          | 파일   | formData                    | 예        | 업로드할 파일                                                                                                            |
| objectType    | 문자열 | query                       | 예        | 내보낼 객체 유형. 차트 내보내기의 경우 `chart`를 사용합니다. 다른 가능한 값으로는 `worksheet`, `picture` 등이 있습니다. |
| format        | 문자열 | query                       | 예        | 원하는 출력 형식. 지원되는 값: `png`, `jpeg`, `gif`, `bmp`, `svg`, `tiff`, `emf`, `wmf`, `pdf`.                         |

### **응답**

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_0.tif",
      "FileSize": 10040,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_1.tif",
      "FileSize": 12978,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_2.tif",
      "FileSize": 7002,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_3.tif",
      "FileSize": 11532,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet6_Charts_0.tif",
      "FileSize": 8270,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3_Charts_0.tif",
      "FileSize": 42570,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3_Charts_1.tif",
      "FileSize": 12102,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3_Charts_2.tif",
      "FileSize": 8290,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

**HTTP 상태 코드**

| 코드 | 의미                      | 설명                                                     |
|------|---------------------------|----------------------------------------------------------|
| 200  | OK (성공)                 | 필터가 성공적으로 적용되었으며, 응답에 작업 세부 정보가 포함됩니다. |
| 400  | Bad Request (잘못된 요청) | 매개변수 누락 또는 유효하지 않음(예: 지원되지 않는 파일 형식).     |
| 401  | Unauthorized (인증 안 됨)  | 유효하지 않거나 누락된 JWT 토큰.                             |
| 413  | Payload Too Large         | 업로드된 파일이 크기 제한을 초과했습니다.                      |
| 500  | Internal Server Error     | 예기치 않은 서버 오류입니다.                                 |

## SDK를 사용하여 PostExport API 사용하는 방법

### PostExport API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/LightCells/PostExport)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

모든 요청은 `Authorization` 헤더에 유효한 OAuth 2.0 Bearer 토큰을 포함해야 합니다. 아래 예제는 **cURL**을 사용하여 API를 호출하고 multipart/form‑data를 통해 워크북을 업로드하는 방법을 보여줍니다.

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=chart&format=tiff" \
  -H "Authorization: Bearer {access_token}" \
  -H "Accept: multipart/form-data" \
  -H "Content-Type: multipart/form-data" \
  -H "x-aspose-client: Containerize.Swagger" \
  -F "File=@/path/to/your/workbook.xlsx"
```

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportChart.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportChart.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportChart.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportChart.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportChart.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportChart.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportChart.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportChart.go" >}}

{{< /tab >}}

{{< /tabs >}}