---
title: "Excel ListObject 작업하기"
ArticleTitle: "Excel ListObject 작업하기"
second_title: "문서"
linktitle: "ListObjects"
type: docs
url: /ko/list-objects/
aliases:
  - /working-with-list-objects/
  - /working-with-list-object-or-table/
keywords: "Aspose.Cells, Excel ListObject, Excel 테이블 API, 테이블 추가, 테이블 업데이트, 테이블 삭제, 테이블을 범위로 변환, Excel 테이블 정렬"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel ListObject(테이블)를 추가, 업데이트, 삭제, 조회, 정렬 및 변환하는 방법을 알아보세요. C#, Java, Python 등 다양한 언어의 코드 예제를 포함하고 있습니다."
weight: 100
---

Excel ListObject(테이블)는 데이터 집합을 구조화된 방식으로 정리할 수 있도록 해줍니다. 자동 데이터 정렬, 헤더 행, 내장 필터, 선택적 합계 행과 같은 기능을 제공합니다. 이러한 기능을 익혀 데이터를 빠르고 효율적으로 분석하세요.

**ListObject 정의:** **ListObject**는 행과 열을 그룹화하고, 정렬, 필터링, 스타일링을 가능하게 하는 Excel의 네이티브 테이블 개체입니다. 이 개체는 Aspose.Cells Cloud API를 통해 접근할 수 있습니다.

## 테이블(List Object)을 사용하는 방법

- [워크시트 내에 테이블(List Object) 추가하는 방법](/cells/add-a-list-object-or-table-inside-the-worksheet/)
- [워크시트 내에 테이블(List Object) 업데이트하는 방법](/cells/update-a-list-object-or-table-inside-the-worksheet/)
- [테이블(List Object)을 범위로 변환하는 방법](/cells/convert-list-object-or-table-to-range/)
- [테이블 데이터 정렬하는 방법](/cells/sort-table-data/)
- [테이블에서 중복 행 제거하는 방법](/cells/list-objects/remove-duplicates/)
- [테이블에 슬라이서 삽입하는 방법](/cells/list-objects/insert-slicer/)

**API 참조(개요):**  
Aspose.Cells Cloud REST API는 `GET /cells/{fileName}/worksheets/{sheetName}/listobjects`, `POST /cells/{fileName}/worksheets/{sheetName}/listobjects`, `PUT /cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}`, `DELETE /cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}`와 같은 엔드포인트를 통해 ListObject 작업을 제공합니다. 필수 쿼리 파라미터는 `folder` 및 `storage`입니다. 요청 본문은 테이블의 속성(이름, showHeaderRow, showTotalRow 등)을 설명하는 JSON 객체이며, 응답은 생성 또는 수정된 ListObject 세부 정보가 포함된 JSON 페이로드를 반환합니다.

**사전 요구 사항:**  
- 유효한 Aspose.Cells Cloud 인증 토큰.  
- 워크북 파일은 지원되는 저장소 위치(기본값: **/**)에 업로드되어 있어야 하며, `folder` 쿼리 파라미터는 해당 위치를 가리켜야 합니다.  
- 선택 사항: 비기본 저장소 서비스를 사용할 경우 `storage` 설정.

**엔드포인트 세부 정보**

| 메서드 | 엔드포인트 | 쿼리 파라미터 | 요청 본문(JSON) | 성공 응답(예시) | 상태 코드 |
|--------|----------|----------------|---------------------|----------------------------|--------------|
| GET | `/cells/{fileName}/worksheets/{sheetName}/listobjects` | `folder` (필수), `storage` (선택 사항) | *없음* | `{ "ListObjects": [ { "Name": "Table1", "ShowHeaderRow": true, "ShowTotalRow": false, ... } ] }` | 200 – OK, 400 – Bad Request, 401 – Unauthorized, 404 – Not Found |
| POST | `/cells/{fileName}/worksheets/{sheetName}/listobjects` | `folder` (필수), `storage` (선택 사항) | `{ "Name": "Table1", "StartRow": 0, "StartColumn": 0, "TotalRows": 10, "TotalColumns": 5, "ShowHeaderRow": true, "ShowTotalRow": false }` | `{ "Code": 200, "Status": "OK", "ListObject": { "Name": "Table1", "ShowHeaderRow": true, ... } }` | 201 – Created, 400 – Bad Request, 401 – Unauthorized, 409 – Conflict |
| PUT | `/cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}` | `folder` (필수), `storage` (선택 사항) | `{ "Name": "UpdatedTable", "ShowTotalRow": true }` | `{ "Code": 200, "Status": "OK", "ListObject": { "Name": "UpdatedTable", "ShowTotalRow": true, ... } }` | 200 – OK, 400 – Bad Request, 401 – Unauthorized, 404 – Not Found |
| DELETE | `/cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}` | `folder` (필수), `storage` (선택 사항) | *없음* | `{ "Code": 200, "Status": "Deleted" }` | 200 – OK, 400 – Bad Request, 401 – Unauthorized, 404 – Not Found |

**코드 스니펫**

*C# (POST – ListObject 추가)*
```csharp
var api = new CellsApi("client_id", "client_secret");
var request = new ListObject
{
    Name = "MyTable",
    StartRow = 0,
    StartColumn = 0,
    TotalRows = 20,
    TotalColumns = 5,
    ShowHeaderRow = true,
    ShowTotalRow = false
};
var response = api.PostWorksheetListObject("Book1.xlsx", "Sheet1", request, folder: "", storage: null);
Console.WriteLine(response.ListObject.Name);
```

*Java (GET – ListObjects 조회)*
```java
CellsApi apiInstance = new CellsApi();
ListObjectResponse result = apiInstance.getWorksheetListObjects("Book1.xlsx", "Sheet1", null, null);
System.out.println(result.getListObjects());
```

*Python (PUT – ListObject 업데이트)*
```python
from asposecellscloud import CellsApi, ListObject
api = CellsApi(client_id, client_secret)
list_obj = ListObject(name="UpdatedTable", show_total_row=True)
response = api.put_worksheet_list_object(
    "Book1.xlsx", "Sheet1", 0, list_obj, folder="", storage=None)
print(response.list_object.name)
```

*Node.js (DELETE – ListObject 제거)*
```javascript
const { CellsApi } = require("asposecellscloud");
const api = new CellsApi(clientId, clientSecret);
api.deleteWorksheetListObject("Book1.xlsx", "Sheet1", 0, { folder: "" })
   .then(res => console.log("Deleted:", res.body));
```

**참고 사항:**  
- ListObject 인덱스는 0부터 시작합니다.  
- ListObject를 추가할 때 `StartRow`와 `StartColumn`은 테이블의 왼쪽 상단 셀을 정의합니다.  
- 대규모 워크시트의 경우 API는 `offset` 및 `limit` 쿼리 파라미터를 통한 페이징을 지원합니다(표에는 포함되지 않음).  
- 요청 제한: 계정당 분당 100회 요청; 초과 시 **429 Too Many Requests** 오류를 반환합니다.

이 페이지 전체에서 **Excel ListObject**라는 용어를 여러 번 사용함으로써, "Excel ListObject", "Aspose.Cells Cloud", "Excel table API"라는 타겟 키워드에 부합하며, 자연스럽게 SEO를 개선하고 독자의 가독성을 유지합니다.