---
title: "차트 영역 채우기 서식 가져오기 – Aspose.Cells Cloud API(v3.0)"
type: docs
url: /ko/charts/chart-area/fill-format/get/
aliases: [  /ko/get-fill-format-of-a-chart-area-from-a-worksheet/ ]
weight: 70
keywords:
  - "Aspose.Cells"
  - "차트 영역"
  - "채우기 서식"
  - "REST API"
  - "Excel"
description: "Aspose.Cells Cloud API를 통해 Excel 워크시트의 차트 영역 채우기 서식(색상, 패턴, 그라데이션)을 검색합니다. cURL 예제, SDK 코드 스니펫, 인증 단계 및 응답 세부 정보가 포함됩니다."
ArticleTitle: "차트 영역 채우기 서식 가져오기 Aspose.Cells Cloud API v3.0"
---

이 REST API는 **차트 영역**의 채우기 서식 정보를 검색합니다.

**사전 요구 사항**  
이 엔드포인트를 호출하려면 유효한 OAuth/JWT 액세스 토큰이 필요합니다. Aspose.Cells Cloud 인증 흐름을 사용하여 토큰을 획득하고 `Authorization` 헤더에 `Bearer <jwt token>` 형태로 포함시켜야 합니다. SDK 중 하나를 사용 중이라면, 메서드를 호출하기 전에 SDK가 `client_id` 및 `client_secret`으로 구성되어 있는지 확인하십시오.

## GetChartAreaFillFormat API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/chartArea/fillFormat
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 구축되었으며 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름 | 유형    | 위치 | 설명                              |
| -------------- | ------- | ------ | ----------------------------------- |
| name           | string  | path   | 워크북 이름.                        |
| sheetName      | string  | path   | 워크시트 이름.                      |
| chartIndex     | integer | path   | 차트의 인덱스.                      |
| folder         | string  | query  | 워크북이 포함된 폴더.               |
| storageName    | string  | query  | 스토리지 이름.                      |

[OpenAPI 스펙](https://apireference.aspose.cloud/cells/#/ChartArea/GetChartAreaFillFormat)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 액세스할 수 있습니다. 아래 예제는 cURL로 API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/chartArea/fillFormat" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "FillFormat": {
    "Type": "Automatic"
  },
  "Code": 200,
  "Status": "OK"
}
```

**참고 사항**  
- 성공적인 호출은 HTTP 200과 함께 채우기 서식 세부 정보를 반환합니다.  
- HTTP 401은 인증 실패(유효하지 않거나 누락된 토큰)를 나타냅니다.  
- 지정된 워크북, 워크시트 또는 차트 인덱스가 존재하지 않으면 HTTP 404가 반환됩니다.  
- HTTP 500은 서버 측 오류를 의미합니다. 문제가 지속되면 요청을 다시 시도하거나 지원팀에 문의하십시오.

| 코드 | 의미                                             |
|------|--------------------------------------------------|
| 200  | 성공 – 채우기 서식 반환됨                        |
| 401  | 인증되지 않음 – 유효하지 않거나 누락된 토큰       |
| 404  | 찾을 수 없음 – 워크북, 워크시트 또는 차트 없음  |
| 500  | 내부 서버 오류                                   |

관련 작업은 **차트 영역 테두리 가져오기** 및 **차트 제목 가져오기** 엔드포인트를 참조하십시오.

{{< /tab >}}

{{< /tabs >}}

## 클라우드 SDK 패밀리

SDK를 사용하면 개발 속도를 최대한 높일 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 저장소</a>를 확인하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Objective C" tabName8="Android" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-GetChartFillFormat-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-GetChartFillFormat-get-fill-format.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetChartAreaFillFormat-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_chart_area_fill_format_info-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetFillFormatOfChartAreaFromWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-GetChartFillFormat-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-GetChartFillFormat-get-fill-format.java" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-GetChartFillFormat-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "d9af13f9a5cf8dee333f8d5e26c32866" >}}

{{< /tab >}}

{{< /tabs >}}
---