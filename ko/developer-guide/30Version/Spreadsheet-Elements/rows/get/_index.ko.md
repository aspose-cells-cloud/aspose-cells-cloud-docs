---
title: "Aspose.Cells Cloud API를 사용하여 Excel 워크시트에서 단일 행 가져오기"
description: "Aspose Cloud 스토리지에 저장된 Excel 워크시트에서 특정 행을 가져오는 방법을 알아보세요. Aspose.Cells Cloud REST API를 사용하며, 요청 구문, 매개변수, 응답 스키마, 샘플 cURL 및 SDK 코드(C#, Java, Python)가 포함됩니다."
keywords: "Aspose.Cells Cloud, 행 가져오기, Excel API, 스프레드시트 REST, C# SDK, Java SDK, Python SDK"
date: 2026-07-30
api_version: "v3.0"
---

# Excel 워크시트에서 단일 행 가져오기

**엔드포인트**: `GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/rows/{rowIndex}`  

Aspose Cloud 스토리지에 저장된 워크시트에서 행을 가져옵니다. 이 작업에는 **읽기**(Read) 범위가 포함된 유효한 OAuth 2.0 액세스 토큰이 필요합니다.

---

## 목차
1. [사전 요구 사항](#prerequisites)  
2. [HTTP 요청](#http-request)  
3. [매개변수](#parameters)  
   - [경로 매개변수](#path-parameters)  
   - [쿼리 매개변수](#query-parameters)  
4. [cURL 예제](#curl-example)  
5. [응답](#response)  
   - [성공 스키마](#success-schema)  
   - [상태 코드](#status-codes)  
6. [SDK 코드 샘플](#sdk-code-samples)  
   - [C#](#c)  
   - [Java](#java)  
   - [Python](#python)  
7. [관련 작업](#related-operations)  
8. [참고 사항 및 제한 사항](#notes--limits)  

---

## 사전 요구 사항
- 활성 구독이 있는 **Aspose Cloud 계정**  
- **읽기**(Read) 범위가 포함된 **OAuth 2.0 액세스 토큰**  
- 대상 워크북이 이미 Aspose Cloud 스토리지에 존재해야 합니다  

---

## HTTP 요청
```http
GET /cells/{name}/worksheets/{sheetName}/rows/{rowIndex}?folder={folder}&storageName={storageName} HTTP/1.1
Host: api.aspose.cloud
Authorization: Bearer {access_token}
Accept: application/json
```

*기본 URL*: `https://api.aspose.cloud/v3.0`

---

## 매개변수

### 경로 매개변수
| 이름        | 유형     | 필수 여부 | 설명                                      |
|-------------|----------|-----------|-------------------------------------------|
| `name`      | string   | ✅        | 워크북 파일 이름(예: `MyWorkbook.xlsx`)   |
| `sheetName` | string   | ✅        | 워크시트 이름(예: `Sheet1`)               |
| `rowIndex`  | integer  | ✅        | 가져올 행의 0부터 시작하는 인덱스           |

### 쿼리 매개변수 *(선택 사항)*
| 이름            | 유형     | 필수 여부 | 설명                                           |
|-----------------|----------|-----------|------------------------------------------------|
| `folder`        | string   | ❌        | 워크북이 위치한 클라우드 스토리지 폴더 경로     |
| `storageName`   | string   | ❌        | 스토리지 서비스 이름(사용자 지정 스토리지 사용 시) |

---

## cURL 예제
```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/rows/5?folder=Docs&storageName=MyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

---

## 응답

### 성공 스키마 (`200 OK`)
```json
{
  "Code": 200,
  "Status": "OK",
  "Row": {
    "Index": 5,
    "Height": 15.0,
    "Style": { /* 스타일 객체 */ },
    "Cells": [
      { "ColumnIndex": 0, "Value": "A6", "DataType": "String" },
      { "ColumnIndex": 1, "Value": 123, "DataType": "Number" }
      /* ...추가 셀... */
    ]
  }
}
```

### 상태 코드
| 코드 | 의미 |
|------|------|
| **200** | 행을 성공적으로 가져왔습니다. |
| **401** | 인증 실패 – 액세스 토큰 누락 또는 유효하지 않음 |
| **404** | 워크북, 워크시트 또는 행을 찾을 수 없음 |
| **500** | 내부 서버 오류 |

### 오류 예제 (`401 Unauthorized`)
```json
{
  "Code": 401,
  "Message": "액세스 토큰이 누락되었거나 유효하지 않습니다."
}
```

---

## SDK 코드 샘플

### C#  
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var clientId = "YOUR_CLIENT_ID";
var clientSecret = "YOUR_CLIENT_SECRET";

var api = new CellsApi(clientId, clientSecret);
var response = api.CellsRows_GetWorksheetRow(
    name: "MyWorkbook.xlsx",
    sheetName: "Sheet1",
    rowIndex: 5,
    folder: "Docs",
    storageName: null   // 선택 사항
);

Console.WriteLine($"행 {response.Row.Index}이(가) {response.Row.Cells.Count}개 셀과 함께 가져와졌습니다.");
```

### Java  
```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.RowResponse;

CellsApi api = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");
RowResponse response = api.cellsRowsGetWorksheetRow(
    "MyWorkbook.xlsx",
    "Sheet1",
    5,
    "Docs",
    null   // storageName – 선택 사항
);

System.out.println("행 인덱스: " + response.getRow().getIndex());
System.out.println("셀 수: " + response.getRow().getCells().size());
```

### Python  
```python
from asposecellscloud import CellsApi, ApiException
from asposecellscloud.models import RowResponse

client_id = "YOUR_CLIENT_ID"
client_secret = "YOUR_CLIENT_SECRET"

api = CellsApi(client_id, client_secret)

try:
    response = api.cells_rows_get_worksheet_row(
        name="MyWorkbook.xlsx",
        sheet_name="Sheet1",
        row_index=5,
        folder="Docs",
        storage_name=None
    )
    print(f"행 {response.row.index}이(가) {len(response.row.cells)}개 셀과 함께 가져와졌습니다.")
except ApiException as e:
    print("CellsApi->cells_rows_get_worksheet_row 호출 시 예외 발생:", e)
```

---

## 관련 작업
| 작업 | 설명 |
|------|------|
| **행 추가** | `POST /cells/{name}/worksheets/{sheetName}/rows` – 워크시트에 새 행을 삽입합니다. |
| **행 삭제** | `DELETE /cells/{name}/worksheets/{sheetName}/rows/{rowIndex}` – 기존 행을 제거합니다. |
| **여러 행 가져오기** | `GET /cells/{name}/worksheets/{sheetName}/rows` – 행 컬렉션을 가져옵니다. |
| **행 개요** | `/cells/rows/` – 행 관련 엔드포인트에 대한 일반 문서입니다. |

---

## 참고 사항 및 제한 사항
- **요청 제한**: 계정당 분당 100개의 요청  
- **지원되는 형식**: XLS, XLSX, CSV, ODS  
- 행 인덱스는 **0부터 시작**하며, 첫 번째 행은 `0`입니다.  
- 이 엔드포인트를 호출하기 전에 워크북이 지정된 `folder`에 업로드되어 있어야 합니다.  

---