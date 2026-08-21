---
title: "Aspose.Cells Cloud API – Excel 워크시트에서 차트 제목 설정"
type: docs
url: /ko/chart/title/add/
aliases: [  /ko/set-chart-title-in-excel-worksheet/ ]
weight: 30
keywords: "Aspose.Cells Cloud, 차트 제목 API, Excel 차트 제목, REST API, SDK 예제"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트에서 차트 제목을 추가하거나 업데이트하는 방법을 알아보세요. cURL, SDK 샘플, 필요한 매개변수, 인증 단계 및 오류 처리를 포함합니다."
---

기존 차트 제목을 추가하거나 기존 제목을 표시합니다.

## PutWorksheetChartTitle API

```http
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 위해 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름 | 유형    | 위치   | 설명                           |
| ------------- | ------- | ------ | ------------------------------ |
| name          | string  | path   | 워크북 이름.                   |
| sheetName     | string  | path   | 워크시트 이름.                 |
| chartIndex    | integer | path   | 차트의 인덱스.                 |
| title           | string  | body   | 차트 제목 텍스트.              |
| folder        | string  | query  | 워크북이 포함된 폴더.          |
| storageName   | string  | query  | 스토리지 이름.                 |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetChartTitle)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/title" \
  -d '{"Text":"Sales Chart"}' \
  -X PUT \
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

**오류 응답**

| HTTP 코드 | 예시 페이로드                                                                          | 설명                                                     |
| --------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------- |
| 400       | `{ "Code": "400", "Message": "Invalid request payload." }`                             | 요청 본문이 잘못되었거나 필수 필드가 누락되었습니다.     |
| 401       | `{ "Code": "401", "Message": "Authentication failed. Invalid or expired JWT token." }` | 베어러 토큰이 누락되었거나, 유효하지 않거나, 만료되었습니다. |
| 404       | `{ "Code": "404", "Message": "Workbook, worksheet, or chart not found." }`             | 지정된 리소스가 존재하지 않습니다.                         |
| 500       | `{ "Code": "500", "Message": "Internal server error." }`                               | 서버에서 예기치 않은 오류가 발생했습니다.                |

## 클라우드 SDK 패밀리

SDK를 사용하면 개발 속도가 가장 빠릅니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 작업에 집중할 수 있도록 합니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-SetChartTitle-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-SetChartTitle-set-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PutWorksheetChartTitle-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-add_chart_title-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SetChartTitle.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-SetChartTitle-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-SetChartTitle-set-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-SetChartTitle-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "728d523e11f8751f5f601bafb04ab86f" >}}

{{< /tab >}}

{{< /tabs >}}