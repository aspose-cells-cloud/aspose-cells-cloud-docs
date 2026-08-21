---
title: "Excel 워크시트에서 가시성 사용하는 방법"
second_title: "문서"
linktitle: "가시성"
type: docs
url: /ko/worksheets/panes/
keywords: "Aspose.Cells Cloud, 워크시트 숨기기 API, 워크시트 표시 API, Excel 워크시트 가시성, REST API Excel, Aspose.Cells v3.0"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트를 프로그래밍 방식으로 숨기거나 표시하는 방법을 배워보세요. 요청 URL, cURL 및 .NET SDK 예제, 오류 처리, 버전별 참고 사항이 포함됩니다."
weight: 20
---

## Excel 워크시트에서 가시성 사용하기

*워크시트 가시성*은 시트를 최종 사용자에게 표시할지 여부를 정의합니다. Aspose.Cells Cloud를 사용하면 간단한 REST 호출을 통해 워크시트를 숨기거나 표시할 수 있습니다. 사용되는 API 엔드포인트는 다음과 같습니다:

* **워크시트 숨기기** – `PUT /cells/{fileName}/worksheets/{sheetName}/visibility`  
* **워크시트 표시** – `PUT /cells/{fileName}/worksheets/{sheetName}/visibility`

> **지원되는 API 버전:** **v3.0** (2026년 3월 기준)

### 사전 요구 사항
1. 활성화된 **Aspose.Cells Cloud** 계정.  
2. 유효한 **클라이언트 ID** 및 **클라이언트 시크릿**(또는 OAuth 2.0 액세스 토큰).  
3. 워크북(`{fileName}`)이 이미 Aspose 클라우드 저장소에 업로드되어 있어야 합니다.  

---

## 워크시트 숨기기

### 요청
```http
PUT https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/visibility
Authorization: Bearer {access_token}
Content-Type: application/json

{
  "Visible": false
}
```

### 응답
```json
{
  "Code": 200,
  "Status": "OK",
  "Worksheet": {
    "Name": "{sheetName}",
    "Index": 2,
    "Visible": false
  }
}
```

### cURL 예제
```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet2/visibility" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Content-Type: application/json" \
     -d '{ "Visible": false }'
```

### .NET SDK 예제
```csharp
var api = new CellsApi("client_id", "client_secret");
var request = new Visibility { Visible = false };
var response = api.PutWorksheetVisibility("MyWorkbook.xlsx", "Sheet2", request);
Console.WriteLine($"워크시트 숨김 처리됨: {response.Worksheet.Visible}");
```

### 일반적인 오류
| HTTP 코드 | 설명                                      | 해결 방법                                               |
|----------|------------------------------------------|----------------------------------------------------------|
| 400      | 잘못된 JSON 본문 또는 `Visible` 누락      | 요청 본문에 유효한 JSON 및 키가 포함되어 있는지 확인하세요. |
| 401      | 인증 실패 – 토큰 누락 또는 만료             | OAuth 토큰을 새로고침하고 헤더에 포함하세요.             |
| 404      | 워크시트 또는 파일을 찾을 수 없음           | `{fileName}` 및 `{sheetName}`이 올바른지 확인하세요.     |
| 409      | 워크시트가 이미 숨겨져 있음                | 요청을 보내기 전에 현재 가시성 상태를 확인하세요.        |

---

## 워크시트 표시

### 요청
```http
PUT https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/visibility
Authorization: Bearer {access_token}
Content-Type: application/json

{
  "Visible": true
}
```

### 응답
```json
{
  "Code": 200,
  "Status": "OK",
  "Worksheet": {
    "Name": "{sheetName}",
    "Index": 2,
    "Visible": true
  }
}
```

### cURL 예제
```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet2/visibility" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Content-Type: application/json" \
     -d '{ "Visible": true }'
```

### .NET SDK 예제
```csharp
var api = new CellsApi("client_id", "client_secret");
var request = new Visibility { Visible = true };
var response = api.PutWorksheetVisibility("MyWorkbook.xlsx", "Sheet2", request);
Console.WriteLine($"워크시트 표시됨: {response.Worksheet.Visible}");
```

### 일반적인 오류
| HTTP 코드 | 설명                                      | 해결 방법                                               |
|----------|------------------------------------------|----------------------------------------------------------|
| 400      | 잘못된 JSON 본문 또는 `Visible` 누락      | `"Visible": true`가 포함된 올바른 JSON 페이로드를 제공하세요. |
| 401      | 인증 실패 – 토큰 누락 또는 만료             | 액세스 토큰을 재생성하고 다시 시도하세요.                 |
| 404      | 워크시트 또는 파일을 찾을 수 없음           | 저장소에 파일 및 시트 이름이 존재하는지 확인하세요.       |
| 409      | 워크시트가 이미 표시되어 있음               | 조치가 필요 없습니다. 워크시트가 이미 표시되어 있습니다.  |

---

## 관련 작업
> *프리즈 창* | *창 분할* | *확대/축소* – 추가 워크시트 레이아웃 제어는 해당 페이지를 참조하세요.

---

## 자주 묻는 질문

<dl>
  <dt>Aspose.Cells Cloud API를 사용하여 워크시트를 숨기는 방법은?</dt>
  <dd>`/cells/{fileName}/worksheets/{sheetName}/visibility`에 `PUT` 요청을 보내고 JSON 본문에 `{ "Visible": false }`를 포함하세요. 유효한 OAuth 2.0 베어러 토큰을 포함해야 합니다. `200 OK` 응답으로 업데이트된 워크시트 객체가 반환됩니다.</dd>

  <dt>워크시트를 표시한 후 어떤 응답을 받게 되나요?</dt>
  <dd>API는 `"Visible": true`가 포함된 워크시트 객체가 포함된 `200 OK` 응답을 반환합니다. 응답에는 워크시트의 `Name`, `Index`, `Visible` 속성이 포함됩니다.</dd>

  <dt>단일 요청으로 여러 워크시트를 숨길 수 있나요?</dt>
  <dd>아니요. 가시성 엔드포인트는 `{sheetName}`으로 식별되는 단일 워크시트에만 작동합니다. 여러 시트를 숨기려면 클라이언트 코드에서 각 이름을 반복 처리해야 합니다.</dd>
</dl>

---

*Aspose Docs 팀 작성 – 15년 이상 Excel 워크플로 자동화 전문.*