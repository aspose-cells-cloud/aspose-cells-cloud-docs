---
title: "워크시트에 차트 추가"
type: docs
url: /ko/charts/add/
aliases: [  /ko/add-a-chart-in-a-worksheet/ ]
weight: 20
description: "Aspose.Cells Cloud API v3.0을 사용하여 Excel 워크시트에 차트를 추가하는 방법을 학습합니다. 엔드포인트, 매개변수, cURL 예제, SDK 스니펫이 포함됩니다."
keywords:
  - "Aspose.Cells 차트 추가"
  - "Aspose.Cells 차트 추가 API"
  - "차트 API REST"
  - "Aspose.Cells SDK 예제"
ArticleTitle: "워크시트에 차트 추가 – Aspose.Cells Cloud API 가이드"
---

이 REST API는 워크시트에 새 차트를 추가합니다.

**사전 조건**  
이 작업을 호출하기 전에 유효한 JWT 액세스 토큰을 가져오고, 대상 워크북이 지정된 폴더 또는 저장소 위치에 저장되어 있는지 확인하십시오.

## PutWorksheetAddChart API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이며 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름           | 유형    | 위치 | 설명                                                                                                                                                                              |
| ----------------------- | ------- | ------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**                | string  | path   | 워크북 이름.                                                                                                                                                                           |
| **sheetName**           | string  | path   | 워크시트 이름.                                                                                                                                                                          |
| **chartType**           | string  | query  | 차트 유형(차트 리소스의 **Type** 속성 참조). 지원되는 차트 유형은 **Bar**, **Column**, **Line**, **Pie**, **Scatter**, **Area**, **Doughnut**, **Radar** 등이 있습니다. |
| **upperLeftRow**        | integer | query  | 차트 영역의 왼쪽 상단 행 인덱스(0부터 시작).                                                                                                                                        |
| **upperLeftColumn**     | integer | query  | 차트 영역의 왼쪽 상단 열 인덱스(0부터 시작).                                                                                                                                     |
| **lowerRightRow**       | integer | query  | 차트 영역의 오른쪽 하단 행 인덱스(0부터 시작).                                                                                                                                       |
| **lowerRightColumn**    | integer | query  | 차트 영역의 오른쪽 하단 열 인덱스(0부터 시작).                                                                                                                                    |
| **area**                | string  | query  | 차트에 표시할 데이터가 포함된 범위(예: `A1:B5`).                                                                                                                                  |
| **isVertical**          | boolean | query  | 차트 방향이 수직인지 여부를 나타냅니다.                                                                                                                                     |
| **categoryData**        | string  | query  | 범주 축 데이터가 포함된 범위(예: `D1:E10`).                                                                                                                                          |
| **isAutoGetSerialName** | boolean | query  | **true**인 경우 시리즈 이름이 자동으로 생성됩니다.                                                                                                                                   |
| **title**               | string  | query  | 차트 제목.                                                                                                                                                                      |
| **folder**              | string  | query  | 워크북이 포함된 폴더.                                                                                                                                                       |
| **storageName**         | string  | query  | 저장소 이름.                                                                                                                                                                     |
| **dataLabels**          | boolean | query  | **true**인 경우 데이터 라벨을 표시합니다.                                                                                                                                                          |
| **dataLabelsPosition**  | string  | query  | 데이터 라벨 위치(예: `Above`).                                                                                                                                                 |
| **pivotTableSheet**     | string  | query  | 피벗 테이블이 포함된 시트 이름.                                                                                                                                         |
| **pivotTableName**      | string  | query  | 피벗 테이블 이름.                                                                                                                                                                 |

### **응답**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP 상태 코드**

| 코드 | 의미                         | 설명                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함 |
| 400  | Bad Request                 | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형) |
| 401  | Unauthorized                | 잘못되거나 누락된 JWT 토큰 |
| 413  | Payload Too Large           | 업로드된 파일이 크기 제한을 초과함 |
| 500  | Internal Server Error       | 예기치 않은 서버 오류 |

## PutWorksheetAddChart API를 SDK와 함께 사용하는 방법

### PutWorksheetAddChart API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetAddChart)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API에 요청하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/charts?chartType=Bar&area=B1:F2&title=SalesState" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
# 이 작업에는 요청 본문이 필요하지 않습니다
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

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 개발 속도가 가장 빨라집니다. SDK는 저수준 세부 정보를 추상화하여 프로젝트 작업에 집중할 수 있도록 해줍니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 요청하는 방법을 보여줍니다:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Objective C" tabName8="Perl" tabName9="Android" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-AddChart-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-AddChart-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PutWorksheetAddChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-add_new_chart_to_worksheet-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddChartToWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-AddChart-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-AddChart-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Examples-Android-chart-AddChart-AddChart.jave" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "7fa79c30fca0c594c18c0f3937b6bcc9" >}}

{{< /tab >}}

{{< /tabs >}}