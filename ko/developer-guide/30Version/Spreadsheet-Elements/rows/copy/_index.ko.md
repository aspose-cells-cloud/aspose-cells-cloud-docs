---
title: "Excel 워크시트에서 행 복사하기"
description: "Aspose.Cells Cloud REST API(v3.0)를 사용하여 Excel 워크시트의 특정 전체 행에서 데이터와 서식을 복사합니다. 인증, 요청/응답 세부 정보, 오류 처리 및 SDK 예제가 포함됩니다."
api_version: "v3.0"
endpoint: "/cells/{name}/worksheets/{sheetName}/cells/rows/copy"
method: "POST"
weight: 30
---

# Excel 워크시트에서 행 복사하기 <span style="float:right;">v3.0</span>

워크시트의 특정 전체 행에서 데이터와 서식을 복사합니다.

---

## 사전 요구 사항

| # | 요구 사항 |
|---|-------------|
| 1 | 유효한 **JWT** 토큰. [인증 가이드](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)를 참조하세요. |
| 2 | 워크북(`{name}`)은 선택한 **폴더** / **스토리지**에 이미 존재해야 합니다. |
| 3 | 대상 워크시트(`{sheetName}`)는 워크북에 존재해야 합니다. |
| 4 | (선택사항) 파일이 기본 위치에 없을 경우 **폴더** 및 **storageName**을 확인합니다. |

---

## 엔드포인트

```
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/copy
```

*모든 경로 매개변수는 대소문자를 구분합니다.*

### 경로 매개변수

| 매개변수 | 유형   | 필수 여부 | 설명 |
|----------|--------|-----------|------|
| `name`    | string | ✅ | 워크북 파일 이름(예: `test.xlsx`). |
| `sheetName` | string | ✅ | 워크시트 이름(예: `Sheet1`). |

### 쿼리 매개변수

| 매개변수               | 유형    | 필수 여부 | 설명 |
|------------------------|---------|-----------|------|
| `sourceRowIndex`       | integer | ✅ | 소스 행의 0부터 시작하는 인덱스. |
| `destinationRowIndex`  | integer | ✅ | 행이 복사될 대상 위치의 0부터 시작하는 인덱스. |
| `rowNumber`            | integer | ✅ | 복사할 행 수. |
| `worksheet`            | string  | ❌ | 워크시트 식별자; 일반적으로 **sheetName**과 동일함. |
| `folder`               | string  | ❌ | 워크북이 포함된 폴더의 경로. |
| `storageName`          | string  | ❌ | 스토리지 서비스의 이름. |

---

## 요청 예시(cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/copy?sourceRowIndex=1&destinationRowIndex=12&rowNumber=10" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **참고**  
> `<jwt token>`을 인증 서비스에서 얻은 유효한 JWT 토큰으로 대체하세요.

---

## 성공 응답

| 코드 | 설명 |
|------|------|
| **200** | 행이 성공적으로 복사되었습니다. |

```json
{
  "Code": 200,
  "Status": "OK"
}
```

응답 본문은 `CellsCloudResponse` 인스턴스입니다.

---

## 오류 처리

| HTTP 코드 | 의미                                  | 예시 본문 |
|-----------|---------------------------------------|-----------|
| **400**   | 잘못된 요청 – 누락되거나 잘못된 매개변수. | `{ "Code": 400, "Message": "Invalid sourceRowIndex." }` |
| **401**   | 인증 실패 – 잘못되거나 누락된 JWT 토큰. | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404**   | 없음 – 워크북 또는 워크시트가 존재하지 않음. | `{ "Code": 404, "Message": "File not found." }` |
| **500**   | 내부 서버 오류 – 예기치 않은 서버 조건. | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

**처리 가이드라인**

* **400** – 모든 필수 쿼리 매개변수가 존재하고 올바르게 형식화되었는지 확인하세요.  
* **401** – JWT 토큰을 재생성하거나 갱신하세요.  
* **404** – 워크북 및 워크시트 이름을 확인하고, 파일이 지정된 폴더/스토리지에 존재하는지 확인하세요.  
* **500** – 잠시 후 재시도하세요. 문제가 지속될 경우 Aspose 지원팀에 문의하세요.

---

## SDK 예제

다음 코드 스니펫은 공식 Aspose.Cells Cloud SDK를 사용하여 **행 복사** 작업을 호출하는 방법을 보여줍니다.

| 언어 | 예제 |
|------|------|
| **C#**   | <details><summary>코드 보기</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar api = new CellsApi("clientId", "clientSecret");\nawait api.PostCopyWorksheetRowsAsync(name: "test.xlsx", sheetName: "Sheet1", sourceRowIndex: 1, destinationRowIndex: 12, rowNumber: 10);\n```</details> |
| **Java** | <details><summary>코드 보기</summary>```java\nCellsApi api = new CellsApi("clientId", "clientSecret");\napi.postCopyWorksheetRows("test.xlsx", "Sheet1", 1, 12, 10, null, null, null);\n```</details> |
| **Python** | <details><summary>코드 보기</summary>```python\nfrom asposecellscloud import CellsApi\napi = CellsApi(client_id='clientId', client_secret='clientSecret')\napi.post_copy_worksheet_rows(name='test.xlsx', sheet_name='Sheet1', source_row_index=1, destination_row_index=12, row_number=10)\n```</details> |
| **Node.js** | <details><summary>코드 보기</summary>```javascript\nconst { CellsApi } = require('asposecellscloud');\nconst api = new CellsApi('clientId', 'clientSecret');\nawait api.postCopyWorksheetRows('test.xlsx', 'Sheet1', 1, 12, 10);\n```</details> |
| **Go** | <details><summary>코드 보기</summary>```go\nimport \"github.com/asposecellscloud/aspose-cells-cloud-go/v3\"\napi := cells.NewCellsApiClient(\"clientId\", \"clientSecret\")\n_, err := api.PostCopyWorksheetRows(context.Background(), \"test.xlsx\", \"Sheet1\", 1, 12, 10, nil, nil, nil)\n```</details> |
| **PHP** | <details><summary>코드 보기</summary>```php\nuse Aspose\Cells\CellsApi;\n$api = new CellsApi('clientId', 'clientSecret');\n$api->postCopyWorksheetRows('test.xlsx', 'Sheet1', 1, 12, 10);\n```</details> |
| **Ruby** | <details><summary>코드 보기</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::CellsApi.new('clientId', 'clientSecret')\napi.post_copy_worksheet_rows('test.xlsx', 'Sheet1', 1, 12, 10)\n```</details> |
| **Perl** | <details><summary>코드 보기</summary>```perl\nuse Aspose::Cells::CellsApi;\nmy $api = Aspose::Cells::CellsApi->new('clientId', 'clientSecret');\n$api->postCopyWorksheetRows(name => 'test.xlsx', sheetName => 'Sheet1', sourceRowIndex => 1, destinationRowIndex => 12, rowNumber => 10);\n```</details> |

*전체 소스 파일은 [Aspose‑Cells‑Cloud GitHub 저장소](https://github.com/aspose-cells-cloud)에서 확인할 수 있습니다.*

---

## 참고 자료

- [Excel 워크시트에 행 추가하기](/rows/add/)  
- [Excel 워크시트에서 행 삭제하기](/rows/delete/)  
- [Excel 워크시트에서 행 업데이트하기](/rows/update/)  

---

*페이지 생성일: **{{DATE}}**. 이 API의 최신 버전은 [OpenAPI 사양서](https://apireference.aspose.cloud/cells/#/Cells/PostCopyWorksheetRows)를 참조하세요.*