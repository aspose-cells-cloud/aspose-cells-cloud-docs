---
title: "Excel 워크시트에서 자동 크기 조정(Autofit) 사용하기"
second_title: "문서"
linktitle: "자동 크기 조정"
type: docs
url: /ko/worksheets/autofit/
aliases: [/autofit-rows-and-columns-of-worksheet/]
keywords: "자동 크기 조정, 열, 행, Aspose.Cells, 클라우드, Excel, API, 크기 조정"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트의 행과 열을 자동으로 크기 조정하는 방법을 알아보세요. cURL, .NET, Java, Python 예제 포함."
weight: 20
ArticleTitle: "Excel 워크시트에서 자동 크기 조정(Autofit) 사용하기 – Aspose.Cells Cloud API"
---

## Excel 워크시트에서 자동 크기 조정(Autofit) 사용하기

- [Excel 워크시트에서 열을 자동 크기 조정하는 방법](/ko/cells/worksheets/autofit/column/)
- [Excel 워크시트에서 여러 열을 자동 크기 조정하는 방법](/ko/cells/worksheets/autofit/columns/)
- [Excel 워크시트에서 행을 자동 크기 조정하는 방법](/ko/cells/worksheets/autofit/row/)
- [Excel 워크시트에서 여러 행을 자동 크기 조정하는 방법](/ko/cells/worksheets/autofit/rows/)

**사전 요구 사항**  
자동 크기 조정(Autofit) 작업을 사용하기 전에 다음이 필요합니다:

1. 유효한 **클라이언트 ID**(Client Id) 및 **클라이언트 시크릿**(Client Secret)이 있는 Aspose.Cells Cloud 계정  
2. Aspose Cloud 스토리지에 업로드된 워크북(또는 공개 URL로 접근 가능한 워크북)  
3. 수정하려는 워크시트 이름

**API 참조**

| 작업 | HTTP 메서드 | 엔드포인트 | 필수 파라미터 | 요청 본문 | 샘플 응답 | 상태 코드 |
|-------|-------------|----------|------------------|-------------|----------------|------------|
| **열** 자동 크기 조정 | POST | `/cells/worksheets/{sheetName}/autofit/column` | `sheetName` (path) <br> `columnIndex` (query) | *없음* | `{ "code": 200, "status": "OK", "message": "Column autofitted." }` | 200, 400, 401, 404, 500 |
| **열들** 자동 크기 조정 | POST | `/cells/worksheets/{sheetName}/autofit/columns` | `sheetName` (path) <br> `startColumn`, `endColumn` (query) | *없음* | `{ "code": 200, "status": "OK", "message": "Columns autofitted." }` | 200, 400, 401, 404, 500 |
| **행** 자동 크기 조정 | POST | `/cells/worksheets/{sheetName}/autofit/row` | `sheetName` (path) <br> `rowIndex` (query) | *없음* | `{ "code": 200, "status": "OK", "message": "Row autofitted." }` | 200, 400, 401, 404, 500 |
| **행들** 자동 크기 조정 | POST | `/cells/worksheets/{sheetName}/autofit/rows` | `sheetName` (path) <br> `startRow`, `endRow` (query) | *없음* | `{ "code": 200, "status": "OK", "message": "Rows autofitted." }` | 200, 400, 401, 404, 500 |

**코드 예제**

*cURL*

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/worksheets/MySheet/autofit/columns?startColumn=0&endColumn=5" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json"
```

*.NET (C#)*

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// 인증
var apiInstance = new CellsApi("{client_id}", "{client_secret}");

// 열 자동 크기 조정 호출
var response = apiInstance.PostWorksheetAutofitColumns(
    name: "Workbook.xlsx",
    sheetName: "Sheet1",
    startColumn: 0,
    endColumn: 5,
    folder: "",
    storageName: ""
);
Console.WriteLine(response.Status);
```

*Java*

```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.*;

CellsApi api = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");

// 행 자동 크기 조정
PostWorksheetAutofitRowsResponse resp = api.postWorksheetAutofitRows(
    "Workbook.xlsx",
    "Sheet1",
    0,   // startRow
    10,  // endRow
    "",  // folder
    ""   // storageName
);
System.out.println(resp.getStatus());
```

*Python*

```python
from asposecellscloud import CellsApi, ApiClient, Configuration

config = Configuration()
config.client_id = "YOUR_CLIENT_ID"
config.client_secret = "YOUR_CLIENT_SECRET"
api_client = ApiClient(configuration=config)
api = CellsApi(api_client)

# 단일 열 자동 크기 조정
response = api.post_worksheet_autofit_column(
    name="Workbook.xlsx",
    sheet_name="Sheet1",
    column_index=2,
    folder="",
    storage_name=""
)
print(response.status)
```

이 코드 스니펫은 다음을 수행하는 방법을 보여줍니다:

1. **클라이언트 ID** 및 **클라이언트 시크릿**을 사용하여 Aspose.Cells Cloud에 인증  
2. 열 또는 행에 대해 적절한 자동 크기 조정(Autofit) 엔드포인트 호출  
3. 작업이 성공적으로 완료되었음을 확인하는 응답 처리

**다음 단계**

자동 크기 조정(Autofit) 호출이 완료된 후, 업데이트된 워크북을 다운로드할 수 있습니다:

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/Workbook.xlsx" \
     -H "Authorization: Bearer {access_token}" \
     -o UpdatedWorkbook.xlsx
```

특정 범위를 대상으로 하려면 `startColumn`, `endColumn`, `startRow`, `endRow` 파라미터를 자유롭게 조정하세요.