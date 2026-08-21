---
title: "그림 내보내기"
second_title: "문서"
linktitle: "그림"
type: docs
url: /export-excel-picture-to-different-formats/
aliases: [/export/excel-picture-to-different-formats/]
keywords: "그림 내보내기, Aspose.Cells Cloud, REST API, Excel, 이미지 형식, PNG, GIF, JPEG, BMP, SVG, TIFF, EMF, WMF"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 그림을 다양한 이미지 형식으로 내보냅니다. 이 서비스는 C#, Java, PHP, Ruby, Node.js, Python, Perl, Go, Swift 등 여러 언어의 SDK를 지원합니다."
weight: 20
---

다음 형식으로 그림을 내보낼 수 있습니다: [PNG](https://docs.fileformat.com/Image/png/), [GIF](https://docs.fileformat.com/image/gif/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), 그리고 [WMF](https://docs.fileformat.com/image/Wmf/).

## REST API


```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 우수하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.


### 요청 매개변수

| 매개변수         | 위치       | 유형   | 필수 여부 | 설명                                                                  |
| --------------- | --------- | ------ | -------- | --------------------------------------------------------------------- |
| `file`          | Form‑data | 파일   | 예        | OLE 개체를 포함한 Excel 워크북 (`.xlsx`, `.xls` 등)                  |
| `outputFormat`  | 쿼리      | 문자열 | 예        | 내보낼 개체의 대상 형식 (`pdf`, `png`, `jpeg`, `docx`, `pptx`)      |
| `objectType`    | 쿼리      | 문자열 | 예        | 고정 값 `oleobject`                                                  |


### 응답

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet6_Pictures_0.tif",
      "FileSize": 21680,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet6_Pictures_1.tif",
      "FileSize": 21286,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet2_Pictures_0.tif",
      "FileSize": 130084,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet2_Pictures_1.tif",
      "FileSize": 120062,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

**HTTP 상태 코드**

| 코드 | 의미                        | 설명                                                 |
|------|-----------------------------|------------------------------------------------------|
| 200  | OK (성공)                   | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함 |
| 400  | Bad Request (잘못된 요청)   | 누락되거나 잘못된 매개변수 (예: 지원되지 않는 파일 형식) |
| 401  | Unauthorized (인증되지 않음) | 잘못되었거나 누락된 JWT 토큰                          |
| 413  | Payload Too Large (ペイロード가 너무 큼) | 업로드된 파일이 크기 제한을 초과함                   |
| 500  | Internal Server Error (내부 서버 오류) | 예기치 않은 서버 오류 발생                            |

## SDK를 사용한 PostExport API 사용 방법

### PostExport API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/LightCells/PostExport)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

**cURL** 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API에 요청을 보내는 방법을 보여줍니다.


```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=picture&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 가장 효율적으로 높일 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 로직에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportPicture.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportPicture.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportPicture.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportPicture.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportPicture.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportPicture.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportPicture.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportPicture.go" >}}
{{< /tab >}}

{{< /tabs >}}