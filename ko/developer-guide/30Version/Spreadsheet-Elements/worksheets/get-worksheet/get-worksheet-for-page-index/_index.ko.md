---
title: "워크시트 페이지 내보내기 – Aspose.Cells Cloud API 참조"
ArticleTitle: "워크시트 페이지 내보내기 – Aspose.Cells Cloud API 참조"
second_title: "문서"
linktype: "page"
type: docs
url: /ko/worksheets/page-to-different-formats/
aliases: [  /ko/get-worksheet-for-page-index/ ]
keywords: "Aspose.Cells Cloud, 워크시트 페이지 내보내기, PDF, PNG, CSV, REST API, JWT 인증, 파일 형식"
description: "Aspose.Cells Cloud REST API를 사용해 특정 워크시트 페이지를 PDF, PNG, CSV 등 다양한 형식으로 내보내는 방법을 알아보세요. cURL 요청, 매개변수 가이드, 다양한 언어의 SDK 샘플을 포함합니다."
weight: 240
---

특정 워크시트 페이지를 내보내는 기능은 전체 워크북을 다운로드하지 않고 보고서의 인쇄 가능한 스냅샷, 차트 이미지 또는 데이터 추출물을 얻고자 할 때 유용합니다. 이 엔드포인트는 단일 페이지를 하위 워크플로우에 가장 적합한 형식으로 가져올 수 있도록 합니다.

[GET /cells/{name}/worksheets/{sheetName}](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet) API를 사용하면 워크시트의 특정 페이지를 다양한 파일 형식으로 변환할 수 있습니다. 지원되는 형식: [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/), [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [GIF](https://docs.fileformat.com/image/gif/), [BMP](https://docs.fileformat.com/image/bmp/), [WMF](https://docs.fileformat.com/image/wmf/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

## REST API

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

> **사전 요구 사항** – 유효한 JWT 인증 토큰과 `folder` 매개변수로 지정한 클라우드 폴더에 저장된 워크북이 필요합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예시는 cURL을 사용해 클라우드 API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1?format=png&verticalResolution=100&horizontalResolution=90&pageIndex=1&folder=DotnetFiles" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

**응답** – 서비스는 요청한 형식으로 페이지를 반환합니다. 이미지 형식(png, jpeg, gif 등)의 경우 바디는 바이너리 이미지를 포함하며, 문서 형식(pdf, xls, csv 등)의 경우 바디는 파일 내용을 포함합니다. 성공적인 호출은 HTTP 200을 반환합니다.

*PNG 응답 예시(기본64 인코딩된 일부 스니펫):*

```text
iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAABG0lEQVR42mNkYGBg+M+ABbJw
...
```

{{< /tab >}}

{{< /tabs >}}

**매개변수**

| 매개변수                 | 유형     | 설명                                                              | 기본값 |
| ------------------------ | ------- | ----------------------------------------------------------------- | ----- |
| `format`                 | string  | 출력 파일 형식(예: `pdf`, `png`, `csv`).                         | `pdf` |
| `verticalResolution`     | integer | 렌더링된 이미지의 수직 DPI.                                        | `100` |
| `horizontalResolution`   | integer | 렌더링된 이미지의 수평 DPI.                                       | `100` |
| `pageIndex`              | integer | 내보낼 워크시트 페이지의 0부터 시작하는 인덱스(`0` = 첫 번째 페이지). | `0`   |
| `folder`                 | string  | 원본 워크북이 위치한 클라우드 저장소 폴더.                         | —     |

**HTTP 상태 코드**

| 코드 | 의미                        | 설명                                             |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | 필터가 성공적으로 적용됨; 응답은 작업 세부 정보 포함. |
| 400  | Bad Request                 | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식). |
| 401  | Unauthorized                | 잘못되거나 누락된 JWT 토큰.                        |
| 413  | Payload Too Large           | 업로드된 파일이 크기 제한을 초과함.                |
| 500  | Internal Server Error       | 예기치 않은 서버 오류.                             |

**가능한 오류**

- **401 Unauthorized** – 잘못되거나 누락된 JWT 토큰.
- **404 Not Found** – 지정된 워크북 또는 워크시트가 존재하지 않음.
- **400 Bad Request** – 잘못된 매개변수 값(예: 지원되지 않는 `format`).
- **500 Internal Server Error** – 예기치 않은 서버 측 문제.

## 클라우드 SDK Family

SDK를 사용하면 개발 속도를 최대한 높일 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

아래 코드 예시는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

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