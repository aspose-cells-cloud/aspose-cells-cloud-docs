---
title: "Aspose.Cells Cloud API를 사용하여 Excel 워크시트에 동적 필터 추가"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트에 동적 필터(예: BelowAverage, Tomorrow, LastMonth 등)를 적용하는 방법을 알아보세요. 인증, 요청 구문, 매개변수, 응답 처리 및 여러 언어에 대한 SDK 예제가 포함되어 있습니다."
keywords: Aspose.Cells, 동적 필터, Excel API, REST, 자동 필터, 클라우드 SDK
slug: add-dynamic-filter
api_version: v3.0
---

## 개요

**PutWorksheetDynamicFilter** 작업은 Excel 워크시트의 지정된 범위에 동적 필터를 추가합니다.  
동적 필터는 날짜, 평균, 공백 등의 값을 자동으로 평가하여 사용자가 사용자 정의 수식을 작성하지 않고도 '스마트' 뷰를 만들 수 있도록 합니다.

## 사전 요구 사항

| 요구 사항              | 세부 정보                                                                                                                  |
| ---------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| **인증**               | `/connect/token` 엔드포인트에서 얻은 유효한 JWT 토큰이 필요합니다. `Authorization: Bearer <token>` 헤더에 포함해야 합니다. |
| **스토리지**           | 워크북은 Aspose Cloud 스토리지 위치(기본 또는 사용자 지정 스토리지)에 있어야 합니다.                                       |
| **지원되는 파일 형식** | `.xlsx`, `.xls`, `.xlsm`, `.xlsb`, `.csv` 등                                                                               |
| **권한**               | 대상 폴더/파일에 대한 읽기/쓰기 권한이 필요합니다.                                                                         |

## HTTP 요청

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dynamicFilter
```

### 경로 매개변수

| 매개변수    | 유형   | 필수 여부 | 설명                                         |
| ----------- | ------ | --------- | -------------------------------------------- |
| `name`      | string | ✅        | Excel 워크북의 이름(예: `Book1.xlsx`).       |
| `sheetName` | string | ✅        | 필터를 적용할 범위가 포함된 워크시트의 이름. |

### 쿼리 매개변수

| 매개변수            | 유형    | 필수 여부 | 설명                                                            |
| ------------------- | ------- | --------- | --------------------------------------------------------------- |
| `range`             | string  | ✅        | 필터를 적용할 셀 범위(예: `A1:B1`).                             |
| `fieldIndex`        | integer | ✅        | 동적 필터를 적용할 범위 내 컬럼의 0부터 시작하는 인덱스.        |
| `dynamicFilterType` | string  | ✅        | 적용할 동적 필터 유형( **지원되는 동적 필터 유형** 참조).       |
| `matchBlanks`       | boolean | ❌        | `true`인 경우, 빈 셀이 필터 결과에 포함됩니다. 기본값: `false`. |
| `refresh`           | boolean | ❌        | `true`인 경우, 필터 적용 후 자동 필터를 새로 고칩니다.          |
| `folder`            | string  | ❌        | 워크북이 위치한 스토리지 내 폴더 경로.                          |
| `storageName`       | string  | ❌        | 사용할 Aspose Cloud 스토리지의 이름.                            |

### 요청 본문

요청 본문은 빈 JSON 객체입니다:

```json
{}
```

## 지원되는 동적 필터 유형

| 값             | 의미                                    |
| -------------- | --------------------------------------- |
| `BelowAverage` | 해당 컬럼 평균보다 낮은 값을 가진 행.   |
| `AboveAverage` | 해당 컬럼 평균보다 높은 값을 가진 행.   |
| `Tomorrow`     | 내일 날짜와 일치하는 행.                |
| `Yesterday`    | 어제 날짜와 일치하는 행.                |
| `NextWeek`     | 다음 달력 주차에 속하는 날짜를 가진 행. |
| `LastMonth`    | 전월의 날짜를 가진 행.                  |
| `ThisYear`     | 올해의 날짜를 가진 행.                  |

## 예제 요청(cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dynamicFilter?range=A1:B1&fieldIndex=0&dynamicFilterType=BelowAverage&matchBlanks=true" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{}'   # PUT 요청은 빈 JSON 본문을 가집니다
```

## 예제 응답

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "동적 필터가 성공적으로 적용되었습니다."
}
```

**HTTP 상태 코드**

| 코드 | 의미                  | 설명                                                      |
| ---- | --------------------- | --------------------------------------------------------- |
| 200  | OK                    | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보가 포함됨. |
| 400  | Bad Request           | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식).  |
| 401  | Unauthorized          | 잘못되거나 누락된 JWT 토큰.                               |
| 413  | Payload Too Large     | 업로드된 파일이 크기 제한을 초과함.                       |
| 500  | Internal Server Error | 예기치 않은 서버 오류.                                    |

## SDK 예제

아래는 가장 인기 있는 SDK에 대한 실행 가능한 스니펫입니다. `YOUR_JWT_TOKEN`, `YOUR_FILE_NAME` 등의 자리 표시자를 실제 값으로 바꾸세요.

### C#

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

var apiInstance = new AutoFilterApi();
var name = "Book1.xlsx"; // string | 워크북 이름.
var sheetName = "Sheet1"; // string | 워크시트 이름.
var range = "A1:B1"; // string | 필터를 적용할 범위.
var fieldIndex = 0; // int? | 0부터 시작하는 컬럼 인덱스.
var dynamicFilterType = "BelowAverage"; // string | 동적 필터 유형.
var matchBlanks = true; // bool? | 빈 셀 포함 여부.
var refresh = true; // bool? | 적용 후 새로 고침 여부.
var folder = "myFolder"; // string (선택 사항)
var storageName = null; // string (선택 사항)

try
{
    var response = apiInstance.PutWorksheetDynamicFilter(name, sheetName, range, fieldIndex, dynamicFilterType, matchBlanks, refresh, folder, storageName);
    Console.WriteLine(response.Status);
}
catch (Exception e)
{
    Console.WriteLine("AutoFilterApi.PutWorksheetDynamicFilter 호출 시 예외 발생: " + e.Message );
}
```

### Java

```java
import com.aspose.cloud.cells.api.AutoFilterApi;
import com.aspose.cloud.cells.model.*;

public class PutWorksheetDynamicFilterExample {
    public static void main(String[] args) {
        AutoFilterApi api = new AutoFilterApi();
        String name = "Book1.xlsx";
        String sheetName = "Sheet1";
        String range = "A1:B1";
        Integer fieldIndex = 0;
        String dynamicFilterType = "BelowAverage";
        Boolean matchBlanks = true;
        Boolean refresh = true;
        String folder = "myFolder";
        String storageName = null;

        try {
            CellsCloudResponse resp = api.putWorksheetDynamicFilter(name, sheetName, range, fieldIndex,
                    dynamicFilterType, matchBlanks, refresh, folder, storageName);
            System.out.println(resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### Python

```python
from asposecellscloud import AutoFilterApi, ApiClient, Configuration

config = Configuration()
config.access_token = "<jwt token>"
api_client = ApiClient(configuration=config)
api = AutoFilterApi(api_client)

name = "Book1.xlsx"
sheet_name = "Sheet1"
range_ = "A1:B1"
field_index = 0
dynamic_filter_type = "BelowAverage"
match_blanks = True
refresh = True
folder = "myFolder"
storage_name = None

response = api.put_worksheet_dynamic_filter(
    name=name,
    sheet_name=sheet_name,
    range=range_,
    field_index=field_index,
    dynamic_filter_type=dynamic_filter_type,
    match_blanks=match_blanks,
    refresh=refresh,
    folder=folder,
    storage_name=storage_name
)

print(response.status)
```

### Node.js (TypeScript)

```typescript
import {
  AutoFilterApi,
  Configuration,
  CellsCloudResponse,
} from "@asposecloud/cells-sdk";

const config = new Configuration({
  accessToken: "<jwt token>",
});
const api = new AutoFilterApi(config);

(async () => {
  try {
    const resp: CellsCloudResponse = await api.putWorksheetDynamicFilter(
      "Book1.xlsx", // name
      "Sheet1", // sheetName
      "A1:B1", // range
      0, // fieldIndex
      "BelowAverage", // dynamicFilterType
      true, // matchBlanks
      true, // refresh
      "myFolder", // folder (선택 사항)
      undefined, // storageName (선택 사항)
    );
    console.log(resp.status);
  } catch (error) {
    console.error(error);
  }
})();
```

_(Ruby, PHP, Go, Perl용 유사 스니펫은 공식 SDK 저장소에서 제공됩니다.)_

## 관련 주제

- **표준 자동 필터 추가** – [표준 필터 추가](/autofilter/add-filter)
- **날짜 필터 추가** – [날짜 필터 추가](/autofilter/add-date-filter)
- **자동 필터 삭제** – [자동 필터 삭제](/autofilter/delete-filter)
- **워크시트 작업** – [워크시트 API 개요](/worksheets/)

## 참고 사항

- 원본 문서에서 사용된 모든 이미지는 접근성 측면에서 검토되었습니다. 장식용 아이콘은 `alt=""` 및 `role="presentation"`으로 표시되었으며, 기능적 아이콘은 설명적인 `alt` 텍스트를 유지했습니다.
- 메타 키워드는 빈 항목과 중복 항목을 제거하여 정리되었습니다.
- 이 페이지는 SEO 및 스크린 리더 탐색을 개선하기 위해 명확한 제목 계층 구조(H1은 프론트 매터에서 하나, H2는 주요 섹션, H3/H4는 하위 섹션)를 따릅니다.

---
