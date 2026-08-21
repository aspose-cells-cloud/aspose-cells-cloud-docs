---
title: "Excel 워크시트에서 범위 콘텐츠 가져오기"
second_title: "문서"
linktitle: "가져오기"
type: docs
url: /ko/ranges/get/
keywords: "Aspose.Cells, Excel, API, get, range, spreadsheet, REST"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트에서 범위 콘텐츠를 검색하는 방법을 알아보세요. 요청 구문 및 샘플 코드 포함."
weight: 20
ArticleTitle: "Excel 워크시트에서 범위 콘텐츠 가져오기 – Aspose.Cells Cloud API"
---

## Excel 워크시트에서 범위 콘텐츠 가져오기 작업

- [이름이 지정된 범위를 기반으로 셀 데이터 가져오기](/cells/ranges/get/values/)
- [Excel 워크북에서 이름이 지정된 범위 가져오기](/cells/ranges/get/name/)

**필수 조건**

- 유효한 Aspose Cloud 액세스 토큰(또는 OAuth용 `client_id`/`client_secret`)
- Excel 파일이 대상 저장 폴더에 업로드되어 있어야 함
- Aspose.Cells Cloud SDK 버전 3.0 이상

**범위 가져오기(Get Range)** 작업은 워크시트에서 지정된 범위의 콘텐츠를 반환합니다.  
이 작업은 JSON 형식(또는 요청 시 다른 형식)으로 범위 데이터를 반환하는 간단한 `GET` 요청입니다.

**요청 개요**

| 요소 | 값 |
|------|-----|
| **HTTP 메서드** | `GET` |
| **엔드포인트** | `https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}` |
| **경로 매개변수** | `fileName` – Excel 파일 이름(확장자 포함) <br> `sheetName` – 워크시트 이름 <br> `rangeName` – 범위 이름(예: `A1:B10`) |
| **쿼리 매개변수**(선택 사항) | `folder` – 저장 폴더 <br> `storage` – 저장소 이름 <br> `outFormat` – 응답 형식(예: `json`, `xml`) |
| **헤더** | `Authorization: Bearer <access_token>` <br> `Accept: application/json` |

**샘플 cURL**

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/ranges/A1:B10?folder=Samples&storage=MyStorage" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Accept: application/json"
```

**샘플 C\#**

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

var apiInstance = new CellsApi("client_id", "client_secret");
var request = new GetRangeRequest(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    rangeName: "A1:B10",
    folder: "Samples",
    storage: "MyStorage"
);
var response = apiInstance.GetRange(request);
Console.WriteLine(response);
```

**샘플 Java**

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.requests.GetRangeRequest;

CellsApi api = new CellsApi("client_id", "client_secret");
GetRangeRequest request = new GetRangeRequest(
        "Book1.xlsx",
        "Sheet1",
        "A1:B10",
        "Samples",
        "MyStorage",
        null,
        null);
var response = api.getRange(request);
System.out.println(response);
```

**샘플 Python**

```python
from asposecellscloud import CellsApi, GetRangeRequest

api = CellsApi(client_id="client_id", client_secret="client_secret")
request = GetRangeRequest(
    name="Book1.xlsx",
    sheet_name="Sheet1",
    range_name="A1:B10",
    folder="Samples",
    storage="MyStorage"
)
response = api.get_range(request)
print(response)
```

**응답 스키마(JSON)**

```json
{
  "Code": 200,
  "Status": "OK",
  "Range": {
    "ColumnCount": 2,
    "RowCount": 1,
    "FirstRow": 0,
    "FirstColumn": 0,
    "Values": [
      ["Value1", "Value2"]
    ]
  }
}
```

**HTTP 상태 코드**

| 코드 | 의미 | 설명 |
|------|------|------|
| 200  | OK | 필터가 성공적으로 적용됨; 응답에는 작업 세부 정보가 포함됨 |
| 400  | 잘못된 요청 | 매개변수 누락 또는 유효하지 않음(예: 지원되지 않는 파일 형식) |
| 401  | 인증되지 않음 | 유효하지 않거나 누락된 JWT 토큰 |
| 413  | 페이로드가 너무 큼 | 업로드된 파일이 크기 제한을 초과함 |
| 500  | 내부 서버 오류 | 예기치 않은 서버 오류 발생 |

- `200 OK` – 범위가 성공적으로 검색됨  
- `400 Bad Request` – 매개변수 누락 또는 유효하지 않음  
- `401 Unauthorized` – 유효하지 않거나 누락된 액세스 토큰  
- `404 Not Found` – 지정된 파일, 워크시트 또는 범위를 찾을 수 없음  
- `500 Internal Server Error` – 예기치 않은 서버 오류 발생  

**오류 응답 예시**

```json
// 400 Bad Request
{
  "Code": 400,
  "Message": "요청 매개변수가 유효하지 않거나 누락되었습니다."
}
```

```json
// 401 Unauthorized
{
  "Code": 401,
  "Message": "유효하지 않거나 누락된 액세스 토큰입니다."
}
```

```json
// 404 Not Found
{
  "Code": 404,
  "Message": "지정된 파일, 워크시트 또는 범위를 찾을 수 없습니다."
}
```

**참고**

- [이름이 지정된 범위를 기반으로 셀 데이터 가져오기](/cells/ranges/get/values/)  
- [Excel 워크북에서 이름이 지정된 범위 가져오기](/cells/ranges/get/name/)  
- [범위 콘텐츠 업데이트](/cells/ranges/update/)  
- [범위 삭제](/cells/ranges/delete/)  
---