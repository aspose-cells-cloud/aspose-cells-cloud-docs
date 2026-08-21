---
title: "워크시트에서 차트 가져오기"
type: docs
url: /charts/get/
aliases: [/get-chart-from-a-worksheet/]
weight: 10
keywords: "Aspose.Cells Cloud, 차트 가져오기, 워크시트, REST API, Excel, 차트 API, 차트 검색, Excel 차트"
description: "Aspose.Cells Cloud REST API를 사용하여 워크시트에서 차트 정보(메타데이터 및 내보내기 형식 포함)를 검색합니다."
ArticleTitle: "워크시트에서 차트 가져오기 – Aspose.Cells Cloud API"
---

이 REST API는 차트 정보를 검색합니다.

**사전 요구 사항** – 이 엔드포인트를 호출하려면 유효한 Aspose.Cells Cloud 계정, 활성화된 저장소 위치, JWT 액세스 토큰이 필요합니다. API 요청을 수행하기 전에 인증 가이드의 지침에 따라 토큰을 획득하십시오.

## GetWorksheetChart API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartNumber}
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이며 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름 | 유형    | 위치 | 설명                                    |
| -------------- | ------- | ---- | ----------------------------------------- |
| name           | string  | path | Excel 파일 이름.                         |
| sheetName      | string  | path | 차트가 포함된 워크시트 이름.             |
| chartNumber    | integer | path | 검색할 차트의 0부터 시작하는 인덱스.     |
| format         | string  | query | 원하는 내보내기 형식(예: png, jpeg).      |
| folder         | string  | query | 문서가 저장된 폴더 경로.                 |
| storageName    | string  | query | 저장소 서비스 이름.                       |


### **응답**

```json
{
  "Code": 200,
  "Status": "OK",
  "Chart": {
    "Name": "Chart 1",
    "Type": "Bar",
    "Top": 50,
    "Left": 100,
    "Width": 400,
    "Height": 300,
    "DataRange": "A1:B5",
    "ShowLegend": true,
    "Format": "png"
  }
}
```

**HTTP 상태 코드**

| 코드 | 의미                       | 설명                                             |
|------|----------------------------|--------------------------------------------------|
| 200  | OK                         | 필터가 성공적으로 적용되었으며, 응답에 작업 세부 정보가 포함됨. |
| 400  | Bad Request                | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형). |
| 401  | Unauthorized               | 유효하지 않거나 누락된 JWT 토큰. |
| 413  | Payload Too Large          | 업로드된 파일이 크기 제한을 초과함. |
| 500  | Internal Server Error      | 예기치 않은 서버 오류. |
## SDK를 사용한 GetWorksheetChart API 사용 방법

### GetWorksheetChart API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChart)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API에 요청하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Chart": {
    "Name": "Chart 1",
    "Type": "Bar",
    "Top": 50,
    "Left": 100,
    "Width": 400,
    "Height": 300,
    "DataRange": "A1:B5",
    "ShowLegend": true,
    "Format": "png"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 요청하는 방법을 보여줍니다:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-GetChart-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-GetChart-get-chart-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetWorksheetChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_worksheet_charts_info-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetChartAreaFromWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-GetChart-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-GetChart-get-chart-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-GetChart-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "6fbcaeac3bd9fe1d22319418799757bd" >}}

{{< /tab >}}

{{< /tabs >}}
---