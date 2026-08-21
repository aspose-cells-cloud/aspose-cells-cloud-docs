---
title: "Excel 워크시트에서 이름이 지정된 범위 이동하기"
second_title: "문서"
linktitle: "이동"
type: docs
url: /ranges/move/
aliases: [/move-a-named-range-with-an-excel-worksheet/]
keywords: "Aspose.Cells Cloud, 이름이 지정된 범위 이동, Excel 워크시트, REST API, 범위 이동, SDK 예제"
description: "Aspose.Cells Cloud REST API v3.0을 사용하여 Excel 워크시트 내에서 이름이 지정된 범위를 이동하는 방법을 배워보세요. 엔드포인트 세부 정보, 인증, 예제 및 SDK 코드 예제가 포함되어 있습니다."
weight: 20
ArticleTitle: "Aspose.Cells Cloud API를 사용하여 Excel 워크시트에서 이름이 지정된 범위 이동하기"
---

이름이 지정된 범위를 이동하는 작업은 프로그래밍 방식으로 데이터를 재정리해야 할 때 흔히 발생합니다. 이 섹션에서는 Aspose.Cells Cloud REST API를 사용하여 정의된 범위를 동일한 워크시트 내의 새 위치로 이동하는 방법을 설명합니다.

이 REST API는 Excel 워크시트에서 지정된 범위를 대상 범위로 이동합니다.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/moveto
```

### 인증
이 API는 Aspose Cloud OAuth 흐름을 통해 얻은 **Bearer JWT 토큰**이 필요합니다. 토큰은 `Authorization` 헤더에 포함해야 합니다:

```
Authorization: Bearer <jwt token>
```

토큰은 **Cells** 범위(scope)를 가지고 있어야 합니다.

### 사전 조건
- 워크북 파일은 Aspose Cloud 스토리지에 저장되어 있어야 합니다.  
- 파일이 루트 디렉터리에 있지 않은 경우, 스토리지 이름(`storageName`)과 폴더 경로(`folder`)를 제공해야 합니다.  
- API 버전 **v3.0**을 지원하는 최신 Aspose.Cells Cloud SDK 버전을 사용해야 합니다.

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 강화되어 있으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 이름              | 유형     | 위치   | 설명 |
|-------------------|----------|--------|------|
| **name**          | string   | path   | 워크북 파일 이름 |
| **sheetName**     | string   | path   | 워크시트 이름 |
| **destRow**       | integer  | query  | 대상 범위의 시작 행 인덱스 (0부터 시작) |
| **destColumn**    | integer  | query  | 대상 범위의 시작 열 인덱스 (0부터 시작) |
| **range**         | object   | body   | 이동할 원본 범위의 정의 |
| **folder**        | string   | query  | 워크북이 저장된 폴더 경로 |
| **storageName**   | string   | query  | Aspose Cloud 스토리지 이름 |

### 요청 본문

| 필드            | 유형     | 필수 여부 | 설명 |
|-----------------|----------|-----------|------|
| **ColumnCount** | integer  | 아니요    | 원본 범위의 열 개수 |
| **ColumnWidth** | integer  | 아니요    | 각 열의 너비(포인트 단위) |
| **FirstColumn** | integer  | 아니요    | 원본 범위의 첫 번째 열 인덱스 (0부터 시작) |
| **FirstRow**    | integer  | 아니요    | 원본 범위의 첫 번째 행 인덱스 (0부터 시작) |
| **Name**        | string   | 아니요    | 범위 이름(이름이 지정된 범위인 경우) |
| **RefersTo**    | string   | 아니요    | 범위를 정의하는 A1 스타일 참조 식 |
| **RowCount**    | integer  | 아니요    | 원본 범위의 행 개수 |
| **RowHeight**   | integer  | 아니요    | 각 행의 높이(포인트 단위) |
| **Worksheet**   | string   | 아니요    | 원본 범위가 포함된 워크시트 |

### 워크플로우

1. 워크북을 Aspose Cloud 스토리지에 **업로드**합니다(기존에 없는 경우).  
2. OAuth 엔드포인트를 사용하여 JWT 토큰을 **생성**합니다.  
3. 원본 범위를 설명하는 JSON 페이로드를 **구성**합니다.  
4. 필요한 경로, 쿼리 매개변수 및 JSON 본문과 함께 `moveto` 엔드포인트를 **호출**합니다.  
5. 응답을 **확인**합니다. 성공적인 호출은 `200 OK` 상태 코드를 반환합니다.

### 예제 요청 / 응답

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/moveto?destRow=20&destColumn=20" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{ 
  "ColumnCount": 7,
  "ColumnWidth": 19,
  "FirstColumn": 0,
  "FirstRow": 9,
  "Name": "MyRange",
  "RefersTo": "A10:G10",
  "RowCount": 1,
  "RowHeight": 15,
  "Worksheet": "Sheet1"
}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

오류가 발생하면 응답에 선택적 `ErrorMessage` 필드가 포함되어 실패에 대한 추가 세부 정보를 제공합니다.

**HTTP 상태 코드**

| 코드 | 의미                         | 설명 |
|------|------------------------------|------|
| 200  | OK                           | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함 |
| 400  | Bad Request                  | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식) |
| 401  | Unauthorized                 | 잘못되거나 누락된 JWT 토큰 |
| 413  | Payload Too Large            | 업로드된 파일이 크기 제한을 초과함 |
| 500  | Internal Server Error        | 예기치 않은 서버 오류 |

**응답 스키마**

| 필드 | 유형 | 설명 |
|------|------|------|
| **Code** | integer | API에서 반환되는 HTTP 유사 상태 코드(예: 200) |
| **Status** | string | 결과에 대한 텍스트 설명(예: "OK") |
| **ErrorMessage** | string (선택 사항) | 호출 실패 시 사람이 읽을 수 있는 오류 세부 정보 |

## Cloud SDK Family

SDK를 사용하면 개발 속도를 최대한 높일 수 있습니다. SDK는 저수준 세부 사항을 처리해주므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeMoveTo.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeMoveTo.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeMoveTo.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeMoveTo.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeMoveTo.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeMoveTo.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeMoveTo.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeMoveTo.go" >}}

{{< /tab >}}

{{< /tabs >}}