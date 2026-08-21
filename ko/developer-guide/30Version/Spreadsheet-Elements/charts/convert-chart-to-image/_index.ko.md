---
title: "Excel 차트를 이미지로 변환 – Aspose.Cells Cloud REST API"
type: docs
url: /charts/to-image/
aliases: [/convert-charts-to-image/]
weight: 50
keywords: "Aspose.Cells Cloud, 차트를 이미지로, Excel 차트 변환, REST API, 이미지 형식, PNG, JPEG, BMP, TIFF, GIF"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 차트 객체를 PNG, JPEG, BMP, TIFF 또는 GIF 이미지로 변환하는 방법을 알아보세요. 엔드포인트 세부 정보, 매개변수, cURL 예제, SDK 스니펫, 응답 예제 및 오류 처리가 포함됩니다."
ArticleTitle: "Excel 차트를 이미지로 변환 – Aspose.Cells Cloud REST API"
---

이 REST API는 **Aspose.Cells Cloud**를 사용하여 **Excel 차트**를 이미지로 변환하는 방법을 설명합니다.

## PutWorksheetAddChart API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartNumber}?format={format}
```

지원되는 이미지 형식은 `png`, `jpeg`, `bmp`, `tiff`, `gif`입니다.

### **보안 및 인증**

Aspose.Cells Cloud API는 보안적이며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름 | 유형    | 위치 | 설명                   |
| ------------- | ------- | ---- | ----------------------- |
| name          | string  | path | 문서 이름.             |
| sheetName     | string  | path | 워크시트 이름.         |
| chartNumber   | integer | path | 차트 번호.             |
| format        | string  | query | 내보낼 파일 형식.      |
| folder        | string  | query | 문서 폴더.             |
| storageName   | string  | query | 스토리지 이름.         |

### **응답**

이 엔드포인트는 요청된 형식의 이미지 파일을 바이너리 스트림(예: `byte[]`)으로 반환합니다. 응답의 `Content-Type` 헤더는 선택한 이미지 형식에 따라 `image/png`, `image/jpeg` 등으로 설정됩니다.

**HTTP 상태 코드**

| 코드 | 의미                    | 설명                                           |
|------|-------------------------|-----------------------------------------------|
| 200  | OK (성공)               | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함 |
| 400  | Bad Request (잘못된 요청) | 누락되거나 유효하지 않은 매개변수(예: 지원되지 않는 파일 유형) |
| 401  | Unauthorized (인증되지 않음) | 잘못되거나 누락된 JWT 토큰 |
| 413  | Payload Too Large (페이로드가 너무 큼) | 업로드된 파일이 크기 제한을 초과함 |
| 500  | Internal Server Error (내부 서버 오류) | 예기치 않은 서버 오류 |

## SDK를 사용한 PutWorksheetAddChart API 사용 방법

### PutWorksheetAddChart API 사양

<a href="https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChart" rel="noopener noreferrer">OpenAPI 사양</a>은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0?format=jpg" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your_jwt_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```text
byte[]
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 처리해주므로, 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Node.js" tabName5="Python" tabName6="Android" tabName7="Objective C" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-ConvertChartToImage-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetWorksheetChartWithFormat-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_chart_in_specified_format-.rb" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-ConvertChartToImage-1.js" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ConvertChartToImage.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-ConvertChartToImage-convert-chart-to-image.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

예제는 곧 제공될 예정입니다.

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-ConvertChartToImage-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "d22256010a610e1351ab15969a7adeef" >}}

{{< /tab >}}

{{< /tabs >}}