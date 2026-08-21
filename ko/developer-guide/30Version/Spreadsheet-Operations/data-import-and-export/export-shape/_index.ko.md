---
title: "도형 내보내기"
second_title: "문서"
linktitle: "도형"
type: docs
url: /ko/export-excel-shape-to-different-formats/
aliases: [  /ko/export/excel-shape-to-different-formats/ ]
keywords: "도형 내보내기, Aspose.Cells Cloud, Excel 도형 내보내기, 이미지 형식, REST API, SDK"
description: "Aspose.Cells Cloud REST API 및 SDK를 사용하여 Excel 도형을 다양한 이미지 형식(PNG, GIF, JPEG, BMP, SVG, TIFF, EMF, WMF)으로 내보내는 방법을 알아보세요."
weight: 20
ArticleTitle: "도형 내보내기 – Aspose.Cells Cloud"
---

Excel에서 도형을 내보내면 다이어그램 콘텐츠를 다양한 플랫폼과 애플리케이션에서 재사용할 수 있습니다. **사전 요구 사항:** 유효한 JWT 액세스 토큰과 업로드할 원본 Excel 파일.

다음 형식으로 도형을 내보낼 수 있습니다: **PNG**, **GIF**, **JPEG**, **BMP**, **SVG**, **TIFF**, **EMF**, **WMF**.

## PostExport API

```http
PUT https://api.aspose.cloud/v3.0/cells/export
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 강화되어 있으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름 | 유형   | 경로/쿼리 문자열/HTTP 본문 | 필수 여부 | 설명 |
|--------------|--------|---------------------------|----------|------|
| file         | file   | formData                  | True     | 업로드할 파일 |
| objectType   | string | query                     | True     | 내보낼 개체의 유형입니다. 차트 내보내기의 경우 `chart`를 사용합니다. 유효한 값으로는 `shape`, `worksheet`, `picture` 등이 있습니다. |
| format       | string | query                     | True     | 원하는 출력 형식입니다. 지원되는 값: `png`, `jpeg`, `gif`, `bmp`, `svg`, `tiff`, `emf`, `wmf`, `pdf`. |

### **요청 예시**

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/export?objectType=shape&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### 응답

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet1_Shapes_0.tif",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    }
    // ... 추가 파일 객체 ...
  ]
}
```

*일반적으로 Base64 인코딩된 파일 페이로드 크기는 이미지 크기와 형식에 따라 수백 바이트에서 수메가바이트 범위입니다.*

**HTTP 상태 코드**

| 코드 | 의미               | 설명 |
|-----|--------------------|------|
| 200 | OK (성공)          | 도형이 성공적으로 내보내졌으며, 응답에 파일 목록이 포함됩니다. |
| 400 | Bad Request (잘못된 요청) | 누락되거나 잘못된 매개변수입니다. |
| 401 | Unauthorized (인증되지 않음) | 잘못되거나 누락된 액세스 토큰입니다. |
| 413 | Payload Too Large (ペイロードが大きすぎます) | 업로드된 파일이 크기 제한을 초과했습니다. |
| 500 | Internal Server Error (내부 서버 오류) | 예기치 않은 서버 오류입니다. |

## SDK를 사용한 PostExport API 활용 방법

### PostExport API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/LightCells/PostExport)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

**cURL** 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예시는 cURL을 사용하여 Cloud API를 호출하는 방법을 보여줍니다.

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/export?objectType=shape&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### Aspose.Cells Cloud SDK 사용

SDK를 사용하는 것은 Aspose.Cells Cloud에 대해 개발하는 가장 빠른 방법입니다. SDK는 저수준 세부 사항을 추상화하여 비즈니스 로직에 집중할 수 있도록 합니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하세요.

다음 코드 예시는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportShape.go" >}}

{{< /tab >}}

{{< /tabs >}}