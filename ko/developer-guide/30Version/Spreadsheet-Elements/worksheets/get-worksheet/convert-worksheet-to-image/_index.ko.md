---
title: "워크시트를 PDF, PNG, CSV 등으로 변환 – Aspose.Cells Cloud API"
second_title: "문서"
linktitle: "워크시트 변환"
type: docs
url: /ko/worksheets/conversion/
aliases:
  - /convert-worksheet-to-image/
  - /worksheets/to-image/
keywords: "Aspose.Cells, 워크시트 변환, REST API, cURL, SDK, PDF, PNG, CSV"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크북의 단일 워크시트를 PDF, PNG, CSV 및 15가지 이상의 다른 형식으로 변환하는 방법을 알아보세요. cURL 예제, SDK 스니펫 및 전체 매개변수 참조가 포함됩니다."
weight: 130
ArticleTitle: "워크시트를 PDF, PNG, CSV 등으로 변환 – Aspose.Cells Cloud API"
---

**워크시트 변환 API** – `GET /cells/{name}/worksheets/{sheetName}` 엔드포인트는 Excel 워크북 내부의 단일 워크시트(시트)를 다른 파일 형식으로 변환합니다.

> **사전 조건:** 이 엔드포인트를 호출하기 전에 유효한 JWT 토큰이 필요하며, 워크북은 Aspose Cloud 스토리지 지원 위치에 저장되어 있어야 합니다.

지원되는 **가져오기**(읽기) 가능 형식 (워크시트를 읽을 수 있음):

- XLS, XLSX, XLSB, CSV, TSV, XLSM, ODS, TXT

지원되는 **내보내기**(저장) 전용 형식 (워크시트를 저장할 수 있음):

- PDF, OTS, XPS, DIF, PNG, JPEG, BMP, SVG, TIFF, EMF, NUMBERS, FODS

## REST API

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetWithFormat)은 공개적으로 접근 가능한 인터페이스를 설명합니다.

### **요청 매개변수**

| 매개변수                 | 유형    | 필수 여부 | 기본값 | 허용 값                                                            | 설명                                              |
| ------------------------ | ------- | -------- | ------- | ------------------------------------------------------------------ | ------------------------------------------------- |
| **format**               | string  | Yes      | –       | pdf, png, jpeg, bmp, svg, tiff, emf, csv, txt, … (지원 목록 참조) | 대상 출력 형식.                                   |
| **verticalResolution**   | integer | No       | 96      | 72‑600                                                             | 이미지 출력 수직 DPI.                             |
| **horizontalResolution** | integer | No       | 96      | 72‑600                                                             | 이미지 출력 수평 DPI.                             |
| **password**             | string  | No       | –       | –                                                                  | 보호된 워크북을 열기 위한 비밀번호.               |
| **folder**               | string  | No       | –       | –                                                                  | 소스 워크북이 저장된 클라우드 폴더.               |
| **storage**              | string  | No       | –       | –                                                                  | 스토리지 이름 (예: "Default").                    |

### 응답

| 상태 코드 | 설명                                                                  | 반환 유형                  |
| --------- | --------------------------------------------------------------------- | -------------------------- |
| **200**   | 변환 성공 – 변환된 파일의 바이너리 스트림이 반환됨.                  | `application/octet-stream` |
| **400**   | 잘못된 요청 – 누락되거나 잘못된 매개변수.                             | JSON 오류 객체             |
| **401**   | 인증되지 않음 – 잘못되거나 누락된 JWT 토큰.                           | JSON 오류 객체             |
| **404**   | 찾을 수 없음 – 워크북 또는 워크시트가 존재하지 않음.                 | JSON 오류 객체             |
| **500**   | 내부 서버 오류 – 예기치 않은 실패.                                    | JSON 오류 객체             |

#### 예제 요청 (cURL)

```bash
curl -v "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1?format=png&verticalResolution=96&horizontalResolution=96" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

#### 예제 응답

```
변환된 이미지 (바이너리 스트림)
```

## 클라우드 SDK Family

SDK를 사용하면 개발 속도가 가장 빠릅니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}
---