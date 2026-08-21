---
title: "워크시트에서 모든 차트 삭제하기"
type: docs
url: /charts/clear/
aliases: [/delete-all-charts-from-a-worksheet/]
weight: 30
keywords: "Aspose.Cells, 클라우드, 삭제, 모든 차트, 워크시트, REST API, DELETE, SDK"
description: "Aspose.Cells Cloud REST API(v3.0)를 사용하여 워크시트의 모든 차트를 삭제하는 방법을 배웁니다. 엔드포인트, 매개변수, cURL 샘플, SDK 코드 스니펫, 인증 단계, 오류 처리가 포함됩니다."
ArticleTitle: "Aspose.Cells Cloud API를 사용하여 워크시트에서 모든 차트 삭제하기"
---

이 REST API는 지정된 워크시트에서 모든 차트를 삭제합니다.

**배경** – 워크시트의 시각적 레이아웃을 초기화하거나, 오래된 시각화를 교체하거나, 이전 차트 데이터를 유지하지 않고 워크북을 재사용 준비를 하려는 경우, 워크시트에서 모든 차트를 제거하는 것이 유용합니다.

API를 호출하기 전에 다음 전제 조건이 충족되었는지 확인하세요:

- 인증을 위한 유효한 JWT 토큰이 존재해야 합니다.  
- 워크북 파일이 지정된 저장소 위치 및 폴더에 존재해야 합니다.  
- API 버전 **v3.0**을 사용 중이어야 합니다.

## DeleteWorksheetClearCharts API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts
```

### **보안 및 인증**

Aspose.Cells Cloud API는 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>을 요구하는 보안 API입니다.

### 요청 매개변수

| 매개변수 이름 | 유형   | 위치 | 설명                              |
| ------------- | ------ | ---- | --------------------------------- |
| name          | string | path | 워크북 파일의 이름입니다.          |
| sheetName     | string | path | 워크시트의 이름입니다.             |
| folder        | string | query | 워크북이 저장된 폴더입니다.       |
| storageName   | string | query | 저장소의 이름입니다.              |

**요청 헤더**

| 헤더            | 설명                             |
|-----------------|----------------------------------|
| Authorization   | Bearer `<jwt token>`             |
| Accept          | `application/json`               |
| Content-Type    | `application/json` (본문 없음)   |

**요청 본문**

DELETE 작업은 **요청 본문이 필요 없습니다**.

**응답**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP 상태 코드**

| 코드 | 의미                         | 설명                                                   |
|------|------------------------------|--------------------------------------------------------|
| 200  | OK                           | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함. |
| 400  | Bad Request                  | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형). |
| 401  | Unauthorized                 | 잘못되거나 누락된 JWT 토큰.                             |
| 413  | Payload Too Large            | 업로드된 파일이 크기 제한을 초과함.                    |
| 500  | Internal Server Error        | 예기치 않은 서버 오류.                                  |

*예시 오류 응답*

```json
// 400 Bad Request
{
    "Code": 400,
    "Message": "Invalid parameter: 'sheetName' is required."
}

// 401 Unauthorized
{
    "Code": 401,
    "Message": "Authentication failed. Invalid JWT token."
}

// 413 Payload Too Large
{
    "Code": 413,
    "Message": "The request payload exceeds the maximum allowed size."
}

// 500 Internal Server Error
{
    "Code": 500,
    "Message": "An unexpected error occurred on the server."
}
```

## SDK를 사용하여 DeleteWorksheetClearCharts API 사용하는 방법

### DeleteWorksheetClearCharts API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetClearCharts)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예제는 cURL을 사용하여 클라우드 API로 요청을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/charts" \
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

### Aspose.Cells Cloud SDK 사용하기

워크시트에서 **모든 차트를 삭제**해야 할 때 SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리해 주므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스로 요청을 수행하는 방법을 보여줍니다:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-DeleteAllCharts-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-DeleteAllCharts-delete-all-charts.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetClearCharts-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-clear_the_charts-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteAllChartsFromAWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-DeleteAllCharts-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-DeleteAllCharts-delete-all-charts.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-DeleteAllCharts-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "1775c5a8985efa819486b7ede2c34bfc" >}}

{{< /tab >}}

{{< /tabs >}}
---