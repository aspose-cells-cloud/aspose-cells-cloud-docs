---
title: "엑셀 워크시트에서 셀 병합하는 방법 – Aspose.Cells Cloud API (v3.0)"
type: docs
url: /ko/merge-cells-in-excel-worksheet/
weight: 110
keywords: "셀 병합, Aspose.Cells, 클라우드 API, 엑셀"
description: "Aspose.Cells Cloud REST API를 사용해 엑셀 워크시트에서 셀을 병합하는 가이드로, cURL 및 SDK 예제를 포함합니다."
ArticleTitle: "엑셀 워크시트에서 셀 병합하는 방법 – Aspose.Cells Cloud API (v3.0)"
---

Aspose.Cells Cloud REST API는 지정된 행과 열 범위에 해당하는 직사각형 셀 블록을 하나의 셀로 병합합니다.

**사전 요구 사항**  
- 인증을 위한 유효한 JWT 토큰  
- 워크북은 이미 지정된 스토리지 폴더에 존재해야 합니다.  
- Aspose.Cloud 계정에서 스토리지 구성(폴더 및 스토리지 이름)이 설정되어 있어야 합니다.

## PostWorksheetMerge API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/merge
```

### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 이름            | 유형     | 위치   | 설명                                                  |
|-----------------|----------|--------|-------------------------------------------------------|
| name            | string   | path   | 워크북 이름.                                           |
| sheetName       | string   | path   | 워크시트 이름.                                         |
| startRow        | integer  | query  | 병합 시작 행의 0부터 시작하는 인덱스(0 = 첫 번째 행).    |
| startColumn     | integer  | query  | 병합 시작 열의 0부터 시작하는 인덱스(0 = 첫 번째 열).    |
| totalRows       | integer  | query  | 병합할 행 수.                                          |
| totalColumns    | integer  | query  | 병합할 열 수.                                          |
| folder          | string   | query  | 워크북이 포함된 폴더.                                  |
| storageName     | string   | query  | 스토리지 이름.                                         |

*이 작업에는 요청 본문이 필요하지 않습니다.*

## **응답**

CellsCloudResponse를 반환합니다.

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP 상태 코드**

| 코드 | 의미                      | 설명                                                    |
|------|---------------------------|---------------------------------------------------------|
| 200  | OK                        | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함.     |
| 400  | Bad Request               | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식).  |
| 401  | Unauthorized              | 잘못되거나 누락된 JWT 토큰.                               |
| 413  | Payload Too Large         | 업로드된 파일이 크기 제한을 초과함.                       |
| 500  | Internal Server Error     | 예기치 않은 서버 오류.                                    |

## SDK를 사용하여 PostWorksheetMerge API 사용하는 방법

### PostWorksheetMerge API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetMerge)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 요청을 수행할 수 있도록 합니다.

**cURL 명령줄 도구**를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용해 클라우드 API로 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/merge?startRow=10&startColumn=10&totalRows=10&totalColumns=10" \
  -X POST \
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

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 처리해 주므로, 프로젝트 핵심 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스로 요청을 보내는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetMerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetMerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetMerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetMerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetMerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetMerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetMerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetMerge.go" >}}

{{< /tab >}}

{{< /tabs >}}
---