---
title: "워크시트 영역을 PNG, PDF, CSV로 내보내기 – Aspose.Cells Cloud API"
second_title: "문서"
linktitle: "영역"
type: docs
url: /worksheets/area-to-different-formats/
aliases: [/get-worksheet-for-area/]
keywords: "Aspose.Cells, 워크시트 영역 내보내기, PNG, PDF, CSV, 엑셀 변환, REST API, SDK"
description: "Aspose.Cells Cloud REST API 또는 SDK(C#, Java, Python 등)를 사용해 엑셀 워크시트의 특정 셀 범위를 PNG, PDF, CSV 및 20개 이상의 다른 형식으로 내보내는 방법을 알아보세요."
weight: 230
ArticleTitle: "Aspose.Cells Cloud API로 워크시트 영역을 PNG, PDF, CSV로 내보내기 – 완전 가이드"
---

[GET /cells/{name}/worksheets/{sheetName}](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet) API를 사용하면 워크시트의 지정된 영역을 다양한 파일 형식으로 변환할 수 있습니다. 지원되는 형식: [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/), [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [GIF](https://docs.fileformat.com/image/gif/), [BMP](https://docs.fileformat.com/image/bmp/), [WMF](https://docs.fileformat.com/image/wmf/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

이 가이드에서는 Aspose.Cells Cloud API를 사용해 엑셀 워크시트의 **특정 셀 범위**를 PNG, PDF, CSV 및 20개 이상의 추가 형식으로 내보내는 방법을 설명합니다. 전체 워크시트 내보내기 또는 워크시트북 변환과 관련된 작업은 **[전체 워크시트 내보내기](https://docs.aspose.cloud/cells/worksheets/worksheet-to-different-formats/)** 및 **[워크시트북을 PDF로 변환](https://docs.aspose.cloud/cells/workbook/convert-to-pdf/)** 페이지를 참조하세요.

## REST API

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetWithFormat)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

### 요청 매개변수

| 매개변수               | 유형    | 필수 여부 | 설명                                           |
|------------------------|---------|-----------|------------------------------------------------|
| `name`                 | string  | 예        | 워크시트북 파일 이름.                          |
| `sheetName`            | string  | 예        | 대상 워크시트 이름.                            |
| `format`               | string  | 예        | 원하는 출력 형식(png, pdf, csv 등).            |
| `area`                 | string  | 아니요    | 내보낼 셀 범위(예: `B3:K8`).                    |
| `verticalResolution`   | int     | 아니요    | 래스터 형식의 수직 DPI.                        |
| `horizontalResolution` | int     | 아니요    | 래스터 형식의 수평 DPI.                        |
| `folder`               | string  | 아니요    | 파일이 포함된 클라우드 스토리지 폴더.          |
| `storage`              | string  | 아니요    | 스토리지 서비스 이름.                          |

### 성공 응답

* **200 OK** – 요청된 파일을 바이너리 형식(PNG, PDF, CSV 등)으로 반환합니다.

### 오류 응답

| 상태 코드 | 설명                                                |
|-----------|-----------------------------------------------------|
| 400       | 잘못된 요청 – 누락되었거나 잘못된 매개변수.         |
| 401       | 인증 실패 – 인증 토큰이 누락되었거나 잘못됨.        |
| 404       | 찾을 수 없음 – 지정된 워크시트북 또는 워크시트가 존재하지 않음. |
| 500       | 내부 서버 오류 – 서버에서 예기치 않은 조건 발생.    |

**예시 오류 페이로드**

```json
{
  "error": {
    "code": "InvalidParameter",
    "message": "'area' 매개변수가 잘못된 형식입니다. 예상 형식: B3:K8."
  }
}
```

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용해 클라우드 API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1?format=png&verticalResolution=100&horizontalResolution=90&area=B3%3AK8&folder=DotnetFiles" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt 토큰>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

변환된 이미지(바이너리 PNG)

{{< /tab >}}

{{< /tabs >}}

## 클라우드 SDK 패밀리

SDK를 사용하면 개발 속도가 가장 빠릅니다. SDK는 저수준 세부 정보를 추상화하여 프로젝트 로직에 집중할 수 있게 해줍니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCellAreaWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCellAreaWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCellAreaWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCellAreaWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCellAreaWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCellAreaWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCellAreaWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCellAreaWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}
---