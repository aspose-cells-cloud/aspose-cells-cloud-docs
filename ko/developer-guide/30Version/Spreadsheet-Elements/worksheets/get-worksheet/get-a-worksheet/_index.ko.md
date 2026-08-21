---
title: "Aspose.Cells Cloud API로 워크시트 내보내기 – 형식, cURL 및 SDK 샘플"
second_title: "문서"
linktitle: "워크시트 내보내기"
type: docs
url: /ko/worksheets/get-worksheet/
keywords: "Aspose.Cells Cloud 워크시트 가져오기, 워크시트 내보내기, Excel API, REST, CSV, PDF, PNG, JPEG, GIF, BMP, TIFF, EMF, XPS, OTS, XLS, XLSX, XLSB, XLSM, ODS, FODS, Numbers, 클라우드 API"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 파일에서 단일 워크시트를 내보내는 방법을 알아보세요. 엔드포인트, 매개변수, 수정된 cURL 예제, 인증 세부 정보, 오류 처리 및 C#, Java, Python 등 다양한 언어의 SDK 스니펫이 포함됩니다."
weight: 10
ArticleTitle: "Aspose.Cells Cloud API로 워크시트 내보내기 – 형식, cURL 및 SDK 샘플"
---

이 REST API를 사용하면 Excel 파일에서 워크시트를 다양한 파일 형식으로 **내보낼** 수 있습니다.

**요약** – **워크시트 가져오기**(Get Worksheet) 엔드포인트를 사용하여 워크북에서 선택한 형식으로 단일 워크시트를 다운로드하세요.

다음 형식으로 내보낼 수 있습니다:

| 형식    | 확장자     | MIME 유형                                                         |
| ------- | --------- | ----------------------------------------------------------------- |
| XLS     | .xls      | application/vnd.ms-excel                                          |
| XLSX    | .xlsx     | application/vnd.openxmlformats-officedocument.spreadsheetml.sheet |
| XLSB    | .xlsb     | application/vnd.ms-excel.sheet.binary.macroEnabled.12             |
| CSV     | .csv      | text/csv                                                          |
| TSV     | .tsv      | text/tab-separated-values                                         |
| XLSM    | .xlsm     | application/vnd.ms-excel.sheet.macroEnabled.12                    |
| ODS     | .ods      | application/vnd.oasis.opendocument.spreadsheet                    |
| TXT     | .txt      | text/plain                                                        |
| PDF     | .pdf      | application/pdf                                                   |
| OTS     | .ots      | application/vnd.oasis.opendocument.spreadsheet-template           |
| XPS     | .xps      | application/vnd.ms-xpsdocument                                    |
| DIF     | .dif      | application/x-dif                                                 |
| PNG     | .png      | image/png                                                         |
| JPEG    | .jpeg     | image/jpeg                                                        |
| GIF     | .gif      | image/gif                                                         |
| BMP     | .bmp      | image/bmp                                                         |
| WMF     | .wmf      | image/wmf                                                         |
| TIFF    | .tiff     | image/tiff                                                        |
| EMF     | .emf      | image/emf                                                         |
| NUMBERS | .numbers  | application/vnd.apple.numbers                                     |
| FODS    | .fods     | application/vnd.oasis.opendocument.spreadsheet-flat-xml           |

## 보안 및 인증
Aspose.Cells Cloud API는 [JWT 토큰 기반 인증](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)이 필요합니다.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

### **요청 매개변수**

| 매개변수 이름            | 유형     | 위치   | 설명                                                              |
| ------------------------ | ------- | ------ | ----------------------------------------------------------------- |
| **name**                 | string  | path   | **필수.** Excel 파일 이름입니다.                                 |
| **sheetName**            | string  | path   | **필수.** 내보낼 워크시트 이름입니다.                            |
| **format**               | string  | query  | 내보낼 워크시트의 대상 파일 형식(예: `pdf`, `png`)입니다.         |
| **verticalResolution**   | integer | query  | 해상도를 지원하는 형식(PNG, JPEG 등)의 이미지 DPI입니다.          |
| **horizontalResolution** | integer | query  | 해상도를 지원하는 형식의 수평 DPI입니다.                          |
| **area**                 | string  | query  | 내보낼 셀 범위(예: `A1:D10`)입니다.                               |
| **pageIndex**            | integer | query  | 워크시트가 페이지로 나뉘어 있을 때 내보낼 페이지의 인덱스입니다.  |
| **folder**               | string  | query  | 소스 파일이 위치한 저장소 내 폴더 경로입니다.                     |
| **storageName**          | string  | query  | Aspose Cloud 저장소 이름입니다.                                   |

<a href="https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet" target="_blank" rel="noopener noreferrer">OpenAPI 사양</a>은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1?format=gif" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```http
HTTP/1.1 200 OK
Content-Type: image/gif
Content-Disposition: attachment; filename="Sheet1.gif"

<이진 데이터>
```

{{< /tab >}}

{{< /tabs >}}

## 오류 처리

API는 표준 HTTP 상태 코드를 반환합니다. 일반적인 응답은 다음과 같습니다:

| 상태 코드 | 의미                                                         | 예시 JSON 본문                             |
| --------- | ------------------------------------------------------------ | ------------------------------------------ |
| **200**   | 성공 – 워크시트 스트림이 반환됩니다.                         | `{ "stream": "..." }`                      |
| **400**   | 잘못된 요청 – 누락되었거나 잘못된 매개변수입니다.            | `{ "error": "Invalid format parameter." }` |
| **401**   | 인증되지 않음 – 잘못되거나 누락된 JWT 토큰입니다.            | `{ "error": "Authentication failed." }`    |
| **404**   | 찾을 수 없음 – 지정된 파일 또는 워크시트가 존재하지 않습니다. | `{ "error": "Worksheet not found." }`      |
| **500**   | 내부 서버 오류 – 서버에서 예기치 않은 조건이 발생했습니다.   | `{ "error": "Unexpected error." }`         |

클라이언트 코드에서 이러한 응답을 적절히 처리하여 사용자에게 적절한 피드백을 제공하세요.

## 클라우드 SDK 패밀리

SDK를 사용하면 개발 속도를 최대한 빠르게 할 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

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