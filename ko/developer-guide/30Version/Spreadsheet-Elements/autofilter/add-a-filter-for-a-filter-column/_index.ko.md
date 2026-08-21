---
title: "Excel 워크시트에 필터 추가"
second_title: "문서"
linktitle: "필터 추가"
type: docs
url: /autofilter/add-filter/
aliases: [/add-a-filter-for-a-filter-column/]
keywords: "Aspose.Cells, 클라우드, Excel, 자동 필터, 필터 추가, REST API, SDK"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트의 열에 자동 필터를 추가하는 방법을 알아보세요. cURL 및 SDK 샘플, 매개변수 가이드 포함."
weight: 60
ArticleTitle: "Aspose.Cells Cloud를 사용하여 Excel 워크시트에 필터 추가"
---

**필수 조건:** 이 API를 호출하기 전에 유효한 JWT 토큰을 획득하고, 대상 워크북이 지정된 저장소에 업로드되었는지 확인하며, 해당 파일에 접근할 수 있는 권한이 있어야 합니다. 명령줄 예제를 실행하려면 최신 버전의 cURL(7.68 이상)을 사용하는 것을 권장합니다.

이 REST API는 Excel 워크시트의 특정 열에 대해 필터를 추가합니다.

## PutWorksheetFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filter
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 위해 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>을 요구합니다.

### 요청 매개변수

| 매개변수 이름 | 유형    | 위치   | 설명 |
|--------------|--------|--------|------|
| name         | string | Path   | 워크북 이름입니다. |
| sheetName    | string | Path   | 워크시트 이름입니다. |
| range        | string | Query  | 필터가 적용될 셀 범위입니다(예: `A1:B1`). |
| fieldIndex   | integer| Query  | 필터를 적용할 열의 0부터 시작하는 인덱스입니다. |
| criteria     | string | Query  | 필터 조건입니다(예: 값 또는 표현식). |
| matchBlanks  | boolean| Query  | 필터에 빈 셀을 포함하려면 `true`로 설정하고, 그렇지 않으면 `false`로 설정합니다. |
| refresh      | boolean| Query  | 필터 적용 후 필터를 새로 고치려면 `true`로 설정하고, 그렇지 않으면 `false`로 설정합니다. |
| folder       | string | Query  | 원본 워크북이 저장된 폴더입니다. |
| storageName  | string | Query  | 저장소 서비스 이름입니다. |

### **응답**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP 상태 코드**

| 코드 | 의미                      | 설명 |
|-----|--------------------------|-----|
| 200 | OK                       | 필터가 성공적으로 적용되었으며, 응답에 작업 세부 정보가 포함됩니다. |
| 400 | Bad Request              | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형)가 포함되었습니다. |
| 401 | Unauthorized             | 잘못되거나 누락된 JWT 토큰입니다. |
| 413 | Payload Too Large        | 업로드된 파일이 크기 제한을 초과했습니다. |
| 500 | Internal Server Error    | 예기치 않은 서버 오류입니다. |

## SDK를 사용하여 PutWorksheetFilter API 사용하는 방법

### PutWorksheetFilter API 사양

<a href="https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetFilter" target="_blank" rel="noopener noreferrer">OpenAPI 사양</a>은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filter?range=A1:B1&fieldIndex=0&criteria=Year" \
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

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 개발 속도가 가장 빠릅니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}