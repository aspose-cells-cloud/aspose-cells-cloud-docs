---
title: "Excel 워크시트에서 모든 피벗 테이블 삭제"
description: "Aspose.Cells Cloud REST API를 사용하여 지정된 워크시트에서 모든 피벗 테이블을 삭제합니다."
keywords: "Aspose.Cells, 피벗 테이블, 삭제, REST API, Excel"
date: 2026-07-30
api_version: "v3.0"
---

# Excel 워크시트에서 모든 피벗 테이블 삭제

## 개요
이 작업은 Excel 파일 내 지정된 워크시트에서 **모든** 피벗 테이블을 제거합니다. 워크시트의 분석을 재설정하거나 단일 호출로 사용하지 않는 피벗 테이블을 정리해야 할 때 유용합니다.

## 사전 요구 사항
API를 호출하기 전에 다음 단계를 완료했는지 확인하십시오:

1. **Aspose Cloud 계정** – 아직 계정이 없다면 Aspose Cloud 계정을 생성합니다.  
2. **JWT 토큰** – 인증을 위한 JSON 웹 토큰(JWT)을 생성합니다. 자세한 내용은 [인증 가이드](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)를 참조하십시오.  
3. **스토리지 설정** – 대상 Excel 파일을 Aspose Cloud 스토리지 또는 연결된 외부 스토리지에 업로드합니다. 파일이 위치한 **폴더** 및 **스토리지 이름**(해당하는 경우)을 기록합니다.

## 인증
Aspose.Cells Cloud API는 **JWT 토큰 기반 인증**을 요구합니다. 각 요청의 `Authorization` 헤더에 토큰을 포함시킵니다:

```
Authorization: Bearer <jwt token>
```

## HTTP 요청

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### 경로 매개변수
| 이름 | 유형 | 필수 여부 | 설명 |
|------|--------|----------|-------------|
| `name` | string | 예 | Excel 파일 이름(예: `Sample.xlsx`). |
| `sheetName` | string | 예 | 모든 피벗 테이블을 제거할 워크시트 이름(예: `Sheet1`). |

### 쿼리 매개변수
| 이름 | 유형 | 필수 여부 | 설명 |
|------|--------|----------|-------------|
| `folder` | string | 아니요 | 파일이 위치한 폴더. |
| `storageName` | string | 아니요 | 사용할 스토리지 이름(파일이 기본 스토리지에 없을 경우). |

## 요청 예시(cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables?folder=SampleFolder&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

## 성공 응답
서비스는 작업 상태를 나타내는 표준 `CellsCloudResponse` 객체를 반환합니다.

```json
{
  "Code": 200,
  "Status": "OK"
}
```

## 오류 처리

| HTTP 상태 코드 | 의미 | 예제 페이로드 |
|-------------|---------|-----------------|
| **400** | 잘못된 요청 – 누락되었거나 유효하지 않은 매개변수 | `{ "Code": 400, "Message": "필수 매개변수 'name'이 누락되었습니다." }` |
| **401** | 인증 실패 – 유효하지 않거나 만료된 JWT | `{ "Code": 401, "Message": "유효하지 않은 인증 토큰입니다." }` |
| **404** | 찾을 수 없음 – 파일 또는 워크시트가 존재하지 않음 | `{ "Code": 404, "Message": "워크시트를 찾을 수 없습니다." }` |
| **500** | 내부 서버 오류 – 예기치 않은 실패 | `{ "Code": 500, "Message": "예기치 않은 오류가 발생했습니다." }` |

## SDK 예제

다음 코드 스니펫은 여러 Aspose.Cells Cloud SDK를 사용하여 작업을 호출하는 방법을 보여줍니다.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// API 클라이언트 초기화
var apiInstance = new CellsApi("<client-id>", "<client-secret>");

// 요청 매개변수 구성
string name = "Sample_Pivot_Table_Example.xls";
string sheetName = "Sheet2";
string folder = "SampleFolder";
string storageName = "MyStorage";

try
{
    var response = apiInstance.DeleteWorksheetPivotTables(name, sheetName, folder, storageName);
    Console.WriteLine($"응답 코드: {response.Code}, 상태: {response.Status}");
}
catch (Exception e)
{
    Console.WriteLine("CellsApi.DeleteWorksheetPivotTables 호출 시 예외 발생: " + e.Message);
}
```

### Java

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.*;

public class DeletePivotTables {
    public static void main(String[] args) {
        CellsApi api = new CellsApi("<client-id>", "<client-secret>");
        String name = "Sample_Pivot_Table_Example.xls";
        String sheetName = "Sheet2";
        String folder = "SampleFolder";
        String storageName = "MyStorage";

        try {
            CellsCloudResponse result = api.deleteWorksheetPivotTables(name, sheetName, folder, storageName);
            System.out.println("코드: " + result.getCode() + ", 상태: " + result.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### Python

```python
import asposecellscloud_sdk
from asposecellscloud_sdk import CellsApi, ApiException

# API 클라이언트 구성
configuration = asposecellscloud_sdk.Configuration()
configuration.api_key['client_id'] = '<client-id>'
configuration.api_key['client_secret'] = '<client-secret>'

api_instance = CellsApi(asposecellscloud_sdk.ApiClient(configuration))

name = 'Sample_Pivot_Table_Example.xls'
sheet_name = 'Sheet2'
folder = 'SampleFolder'
storage_name = 'MyStorage'

try:
    response = api_instance.delete_worksheet_pivot_tables(name, sheet_name, folder, storage_name)
    print(f'코드: {response.code}, 상태: {response.status}')
except ApiException as e:
    print("CellsApi->delete_worksheet_pivot_tables 호출 시 예외 발생: %s\n" % e)
```

### Node.js

```javascript
const { CellsApi, Configuration } = require('asposecellscloud-sdk');

const config = new Configuration({
    clientId: '<client-id>',
    clientSecret: '<client-secret>'
});
const apiInstance = new CellsApi(config);

const name = 'Sample_Pivot_Table_Example.xls';
const sheetName = 'Sheet2';
const folder = 'SampleFolder';
const storageName = 'MyStorage';

apiInstance.deleteWorksheetPivotTables(name, sheetName, folder, storageName)
    .then(result => {
        console.log(`코드: ${result.code}, 상태: ${result.status}`);
    })
    .catch(err => {
        console.error('오류:', err);
    });
```

*추가 SDK(Go, PHP, Ruby, Swift, Perl, Android)는 [Aspose.Cells Cloud SDK 저장소](https://github.com/aspose-cells-cloud)에서 사용할 수 있습니다.*

## 참고 자료
- [특정 피벗 테이블 삭제](https://docs.aspose.cloud/cells/pivot-tables/delete-specific/)
- [워크시트의 모든 피벗 테이블 가져오기](https://docs.aspose.cloud/cells/pivot-tables/get-all/)
- [인증 개요](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)
- [DeleteWorksheetPivotTables에 대한 OpenAPI 스펙](https://apireference.aspose.cloud/cells/#/PivotTables/DeleteWorksheetPivotTables)

--- 

*문서 최종 업데이트일: 2026-07-30. 모든 콘텐츠는 UTF-8로 인코딩됩니다.*