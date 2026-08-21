---
title: "엑셀 워크시트에서 차트 제목 업데이트"
type: docs
url: /ko/charts/title/update/
aliases: [  /ko/update-chart-title-in-excel-worksheet/ ]
weight: 160
keywords: Excel, Aspose.Cells, REST API, 차트 제목, 업데이트, 클라우드 SDK
description: Aspose.Cells Cloud REST API, cURL 및 다양한 SDK를 사용하여 엑셀 워크시트에서 차트 제목을 업데이트하는 방법을 알아보세요.
ArticleTitle: "차트 제목 업데이트 – Aspose.Cells Cloud 문서"
---

이 REST API는 차트 제목을 업데이트합니다.

**사전 요구 사항:** 유효한 Aspose Cloud 계정과 인증용 JWT 토큰이 필요합니다. 일반적인 단계는 다음과 같습니다:

- Aspose Cloud 계정에 가입합니다.  
- 인증 엔드포인트를 통해 JWT 토큰을 생성합니다.  
- 대상 워크북이 지원되는 클라우드 스토리지(기본 또는 사용자 정의)에 저장되어 있는지 확인합니다.

## PostWorksheetChartTitle API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

모든 API 호출은 혼합 콘텐츠 경고를 방지하기 위해 **HTTPS**를 통해 이루어져야 합니다.

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 구축되었으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름 | 유형    | 위치 | 설명                           |
| ------------- | ------- | ---- | ------------------------------ |
| name          | string  | path | 워크북 이름.                   |
| sheetName     | string  | path | 워크시트 이름.                 |
| chartIndex    | integer | path | 차트의 0부터 시작하는 인덱스. |
| title         | string  | body | 새 차트 제목.                 |
| folder        | string  | query | 워크북 폴더.                  |
| storageName   | string  | query | 스토리지 이름.                |

### 응답 상태 코드

| 코드 | 설명                                                   |
| ---- | ------------------------------------------------------ |
| 200  | OK – 차트 제목이 성공적으로 업데이트되었습니다.        |
| 400  | Bad Request – 매개변수 누락 또는 유효하지 않음.         |
| 401  | Unauthorized – 유효하지 않거나 누락된 JWT 토큰.         |
| 404  | Not Found – 워크북, 워크시트 또는 차트를 찾을 수 없음. |
| 500  | Internal Server Error – 예기치 않은 서버 조건.          |

**참고:** `chartIndex`는 0부터 시작하며, 워크시트의 첫 번째 차트는 `0`으로 참조됩니다.

<a href="https://apireference.aspose.cloud/cells/#/Charts/PostWorksheetChartTitle" target="_blank" rel="noopener noreferrer">OpenAPI 사양</a>은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API로 호출을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -v POST "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/title" \
-d '{"title":"Stock exchange"}' \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스로 호출을 수행하는 방법을 보여줍니다:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-UpdateChartTitle-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-UpdateChartTitle-update-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PostWorksheetChartTitle-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-update_chart_title-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UpdateChartTitleInExcelWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-UpdateChartTitle-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-UpdateChartTitle-update-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-UpdateChartTitle-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "aab21ae55930321e6eaa46ffe5b8e7bf" >}}

{{< /tab >}}

{{< /tabs >}}
---