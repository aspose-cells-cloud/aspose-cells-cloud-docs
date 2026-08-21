---
title: "엑셀 워크시트에 아이콘 필터 추가"
second_title: "문서"
linktitle: "아이콘 필터 추가"
type: docs
url: /ko/autofilter/add-icon-filter/
aliases: [  /ko/add-an-icon-filter/ , /ko/autofilter/add-an-icon-filter/ ]
keywords: "Aspose.Cells Cloud, Excel, 아이콘 필터, 자동 필터, REST API"
description: "Aspose.Cells Cloud REST API를 사용하여 엑셀 워크시트에 아이콘 필터를 추가하는 방법을 알아보세요. 요청 세부 정보, cURL 예제, SDK 코드 예제, 오류 처리 방법을 제공합니다."
weight: 65
ArticleTitle: "엑셀 워크시트에 아이콘 필터 추가 – Aspose.Cells Cloud 문서"
---

## REST API

이 REST API는 **Aspose.Cells Cloud REST API**를 사용하여 엑셀 워크시트에 **아이콘 필터**를 추가합니다.

**배경 설명:** 아이콘 필터는 셀의 값에 따라 시각적 아이콘 집합을 적용하여 데이터 추세를 빠르게 시각적으로 분석할 수 있도록 합니다. 일반적인 사용 사례로는 성과 지표 강조 표시, 상태 표시기 설정, 또는 엑셀 워크시트 내에서 교통 신호등 아이콘을 사용하여 값을 범주화하는 작업 등이 있습니다.


```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/iconFilter
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 위해 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.


### 요청 매개변수:

| 매개변수 이름 | 유형     | 위치   | 설명 |
|---------------|----------|--------|------|
| name          | string   | Path   | 워크북 이름. |
| sheetName     | string   | Path   | 워크시트 이름. |
| range         | string   | Query  | 필터를 적용할 셀 범위(예: `A1:B1`). |
| fieldIndex    | integer  | Query  | 필터를 적용할 열의 0부터 시작하는 인덱스. |
| iconSetType   | string   | Query  | 사용할 아이콘 집합. 허용되는 값: `Arrows3`, `ArrowsGray3`, `Flags3`, `Signs3`, `Symbols3`, `Symbols32`, `TrafficLights31`, `TrafficLights32`, `Arrows4`, `ArrowsGray4`, `Rating4`, `RedToBlack4`, `TrafficLights4`, `Arrows5`, `ArrowsGray5`, `Quarters5`, `Rating5`, `Stars3`, `Boxes5`, `Triangles3`, `None`, `CustomSet`, `Smilies3`, `ColorSmilies3`. |
| iconId        | integer  | Query  | 선택한 아이콘 집합 내에서 특정 아이콘의 식별자. |
| matchBlanks   | boolean  | Query  | 빈 셀을 포함할지 여부(`true` 또는 `false`). |
| refresh       | boolean  | Query  | 필터 적용 후 필터를 새로 고칠지 여부(`true` 또는 `false`). |
| folder        | string   | Query  | 원본 워크북이 위치한 폴더. |
| storageName   | string   | Query  | 워크북이 저장된 저장소 이름. |

### **응답**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP 상태 코드**

| 코드 | 의미                           | 설명 |
|------|--------------------------------|------|
| 200  | 성공                           | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보가 포함됨. |
| 400  | 잘못된 요청                     | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식). |
| 401  | 인증되지 않음                   | 잘못되거나 누락된 JWT 토큰. |
| 413  | 페이로드가 너무 큼              | 업로드된 파일이 크기 제한을 초과함. |
| 500  | 내부 서버 오류                  | 예기치 않은 서버 오류. |
## SDK를 사용하여 PutWorksheetIconFilter API 사용하는 방법

### PutWorksheetIconFilter API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetIconFilter)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/iconFilter?range=A1:B1&fieldindex=0&iconsettype=ArrowsGray3&iconid=1" \
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

가능한 응답 상태 코드:

| 코드 | 설명 |
|------|------|
| 200 | 필터가 성공적으로 적용됨. |
| 400 | 잘못된 요청 – 누락되거나 잘못된 매개변수. |
| 401 | 인증되지 않음 – 잘못되거나 누락된 인증 토큰. |
| 404 | 워크북, 워크시트 또는 지정된 범위를 찾을 수 없음. |
| 500 | 내부 서버 오류. |
{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용하기

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 처리해 주므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetIconFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetIconFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetIconFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetIconFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetIconFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetIconFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetIconFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetIconFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}

기타 자동 필터 기능은 **[색상 필터 추가](/autofilter/add-color-filter/)**, **[날짜 필터 추가](/autofilter/add-date-filter/)**, **[자동 필터 지우기](/autofilter/clear-autofilter/)** 문서를 참조하세요.