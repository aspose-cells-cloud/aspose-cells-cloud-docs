---
title: "워크시트에서 차트 범례 표시"
type: docs
url: /ko/charts/legend/show/
aliases: [  /ko/show-chart-legend-in-a-worksheet/ ]
weight: 100
keywords: "Aspose.Cells Cloud, 차트 범례 API, Excel 차트 범례, REST PUT 차트 범례, Aspose API v3.0"
description: "Aspose.Cells Cloud REST API(v3.0)를 사용하여 Excel 워크시트에 차트 범례를 표시하는 방법을 알아보세요. 엔드포인트 세부 정보, 매개변수, cURL 예제, SDK 스니펫 포함."
---

이 REST API는 Excel 워크북의 워크시트에 있는 차트에 **범례**(데이터 시리즈를 식별하는 설명 상자)를 표시할 수 있도록 해줍니다.

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
```

### 요청 매개변수

| 매개변수 이름 | 유형    | 위치   | 설명                                     |
| ------------- | ------- | ------ | ---------------------------------------- |
| name          | string  | path   | 워크북 파일 이름.                        |
| sheetName     | string  | path   | 차트가 포함된 워크시트 이름.             |
| chartIndex    | integer | path   | 차트의 0부터 시작하는 인덱스.            |
| folder        | string  | query  | 워크북이 포함된 폴더.                    |
| storageName   | string  | query  | 스토리지 서비스의 이름.                  |

[OpenAPI 스펙](https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetChartLegend)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

인증은 **Authorization** 헤더에 제공된 Bearer JWT 토큰으로 수행됩니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용해 호출을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

이 API는 다음 HTTP 상태 코드를 반환할 수 있습니다:

- **200 OK** – 범례가 성공적으로 표시되었습니다.
- **400 Bad Request** – 잘못된 매개변수.
- **401 Unauthorized** – 인증 실패.
- **404 Not Found** – 지정된 워크북, 워크시트 또는 차트가 존재하지 않습니다.
- **500 Internal Server Error** – 예기치 않은 서버 오류가 발생했습니다.

{{< /tab >}}

{{< /tabs >}}

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리해주므로, 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스로 호출을 수행하는 방법을 보여줍니다:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-ShowChartLegend-1.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-ShowChartLegend-show-chart-legend.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PutWorksheetChartLegend-.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-show_legend_in_chart-.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ShowChartLegendInAWorksheet.py" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-ShowChartLegend-1.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-ShowChartLegend-show-chart-legend.java" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-ShowChartLegend-1.pl" >}}
{{< /tab >}}

{{< tab tabNum="10" >}}
{{< gist "aspose-cells-cloud-gists" "f9f1d14e3b6985c0a44ec7acdd4f56b2" >}}
{{< /tab >}}

{{< /tabs >}}