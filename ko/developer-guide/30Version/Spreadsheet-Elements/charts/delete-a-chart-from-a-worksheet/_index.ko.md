---
title: "워크시트에서 차트 삭제하기"
type: docs
url: /charts/delete/
aliases: [/delete-a-chart-from-a-worksheet/]
weight: 40
keywords:
  - "Aspose.Cells"
  - "REST API"
  - "Delete Chart"
  - "Worksheet"
  - "Excel"
  - "Cloud SDK"
  - "Chart Deletion"
  - "API Reference"
description: "Aspose.Cells Cloud REST API를 사용하여 0부터 시작하는 인덱스로 워크시트에서 차트를 삭제합니다."
ArticleTitle: "Aspose.Cells Cloud REST API를 사용하여 워크시트에서 차트 삭제하기"
---

이 REST API는 인덱스를 기준으로 워크시트의 차트를 삭제합니다.

관련 작업은 **[차트 추가](#)** 및 **[차트 조회](#)** 페이지를 참조하세요.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}
```

### 보안 및 인증

Aspose.Cells Cloud API는 보안이 확보되었으며, [JWT 토큰 기반 인증](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)이 필요합니다.

### 요청 매개변수

| 매개변수 이름 | 유형    | 위치 | 설명                                         |
| ------------ | ------- | ---- | -------------------------------------------- |
| name         | string  | path | 워크북 이름.                                 |
| sheetName    | string  | path | 워크시트 이름.                               |
| chartIndex   | integer | path | 삭제할 차트의 0부터 시작하는 인덱스.         |
| folder       | string  | query | 워크북이 포함된 폴더.                       |
| storageName  | string  | query | 사용할 스토리지 이름.                        |


### **응답**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP 상태 코드**

| 코드 | 의미                         | 설명                                             |
|------|------------------------------|--------------------------------------------------|
| 200  | OK                           | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함. |
| 400  | Bad Request                  | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형). |
| 401  | Unauthorized                 | 잘못되거나 누락된 JWT 토큰.                       |
| 413  | Payload Too Large            | 업로드된 파일이 크기 제한을 초과함.               |
| 500  | Internal Server Error        | 예기치 않은 서버 오류.                            |

## SDK를 사용하여 PutWorksheetAddChart API 사용하는 방법

### PutWorksheetAddChart API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetDeleteChart)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예시는 cURL을 사용하여 Cloud API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0" \
-X DELETE \
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

{{< /tab >}}

{{< /tabs >}}

API는 다음과 같은 상태 코드를 반환합니다:

| 코드 | 설명                                      |
|------|-------------------------------------------|
| 200  | 차트가 성공적으로 삭제됨                    |
| 400  | 잘못된 요청 (예: 잘못된 인덱스)            |
| 401  | 인증되지 않음 (누락되거나 잘못된 JWT 토큰) |
| 404  | 워크북, 워크시트, 또는 차트를 찾을 수 없음 |
| 500  | 서버 오류                                 |

**오류 처리:** 자세한 오류 정보는 OpenAPI 사양의 일반 오류 모델을 참조하세요.

### Aspose.Cells Cloud SDK 사용하기

SDK를 사용하면 개발 속도를 최대한 빠르게 할 수 있습니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 작업에 집중할 수 있도록 합니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예시는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-DeleteChart-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-DeleteOneChart-delete-single-chart.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetDeleteChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-delete_worksheet_chart_by_index-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteChartExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-DeleteChart-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-DeleteOneChart-delete-single-chart.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-DeleteChart-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "b858c32efd7b745ebb75d61898ec50e0" >}}

{{< /tab >}}

{{< /tabs >}}
---