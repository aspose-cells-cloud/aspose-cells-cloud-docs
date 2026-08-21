---
title: "차트 속성 업데이트"
type: docs
url: /charts/properties/update/
aliases: [/update-chart-properties/]
weight: 160
keywords: "Aspose.Cells, 차트, 업데이트, 엑셀, REST API, SDK"
description: "Aspose.Cells Cloud REST API(v3.0)를 사용하여 엑셀 워크북에서 차트 속성(종류, 제목, 범례 등)을 업데이트하는 방법을 배웁니다. 엔드포인트, 매개변수, cURL 예제, C#, Java, PHP, Ruby, Node.js, Perl, Go용 SDK 스니펫이 포함됩니다."
ArticleTitle: "차트 속성 업데이트 – Aspose.Cells Cloud REST API"
---

이 REST API는 차트 속성을 업데이트합니다.

### **보안 및 인증**

Aspose.Cells Cloud API는 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요하며, 안전하게 설계되었습니다.

## PostWorksheetChart API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}
```

### 요청 매개변수

| 매개변수 이름 | 유형    | 경로/쿼리 문자열/HTTP 본문 | 설명                                                 |
| ------------- | ------- | -------------------------- | ---------------------------------------------------- |
| name          | string  | path                       | 엑셀 파일의 이름입니다.                             |
| sheetName     | string  | path                       | 차트가 포함된 워크시트의 이름입니다.                |
| chartIndex    | integer | path                       | 업데이트할 차트의 0부터 시작하는 인덱스입니다.      |
| chart         | object  | body                       | 수정할 차트 속성을 정의하는 JSON 객체입니다.        |
| folder        | string  | query                      | 파일이 위치한 저장소의 폴더입니다.                  |
| storageName   | string  | query                      | 저장소 서비스의 이름입니다.                         |

### 요청 본문 스키마

**`chart`** 객체에는 수정할 수 있는 속성이 포함됩니다. 아래는 일반적으로 사용되는 필드를 포함한 예시 JSON입니다:

```json
{
  "Title": {
    "Text": "분기별 매출"
  },
  "ShowLegend": true,
  "Type": "Line",
  "DataLabels": {
    "ShowValue": true,
    "ShowPercentage": false
  },
  "ChartArea": {
    "BorderColor": "Blue",
    "FillColor": "White"
  }
}
```

> **참고:** 변경하려는 필드만 제공하면 됩니다. 생략된 속성은 기존 값을 유지합니다.

<a href="https://apireference.aspose.cloud/cells/#/Charts/PostWorksheetChart" target="_blank" rel="noopener noreferrer">OpenAPI 사양</a>은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API에 호출을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet4/charts/1" \
-d '{"Type": "line"}' \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt 토큰>"
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

## 응답

API는 작업 결과를 나타내는 JSON 객체를 반환합니다. 성공적인 업데이트는 다음과 같은 응답을 반환합니다:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**성공 상태 코드**

| HTTP 상태 코드 | 설명                                      |
| -------------- | ------------------------------------------- |
| 200            | OK – 차트 속성이 성공적으로 업데이트되었습니다. |

**응답 헤더**

| 헤더           | 설명                                                  |
| -------------- | ----------------------------------------------------- |
| `Content-Type` | `application/json` – 응답 본문이 JSON 형식임을 나타냅니다. |
| `X-RequestId`  | 요청의 고유 식별자(문제 해결 시 유용합니다).           |

가능한 오류 응답은 다음과 같습니다:

| HTTP 상태 코드 | 설명                                         |
| -------------- | ---------------------------------------------- |
| 400            | Bad Request – 잘못된 매개변수 또는 본문입니다. |
| 401            | Unauthorized – 토큰이 없거나 유효하지 않습니다.  |
| 404            | Not Found – 파일, 워크시트 또는 차트를 찾을 수 없습니다. |
| 500            | Internal Server Error                          |

다른 차트 관련 작업은 [차트 제목 업데이트](/charts/title/update/) 및 [차트 범례 업데이트](/charts/legend/update/)와 같은 관련 주제를 참조하십시오.

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 저장소</a>를 확인하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 호출을 수행하는 방법을 보여줍니다:

{{< tabs tabTotal="6" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Node.js" tabName5="Perl" tabName6="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-Charts-UpdateChartProperties-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-CellsChartsPostWorksheetChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-cells_charts_post_worksheet_chart-.rb" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-UpdateChartProperties-1.js" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-UpdateChartProperties-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "d554e51920e174943a60f4343a97e203" >}}

{{< /tab >}}

{{< /tabs >}}