---
title: "Aspose.Cells Cloud API – 워크시트에서 목록 개체(표) 가져오기"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트에서 ListObject(표)를 검색합니다. 여러 형식(PDF, CSV, JSON 등)으로 직접 내보내는 기능을 지원합니다."
keywords:
  - Aspose.Cells
  - Cloud API
  - Excel
  - ListObject
  - Table
  - REST
  - SDK
type: docs
slug: /list-objects/get/
weight: 9
---

# Aspose.Cells Cloud API – 워크시트에서 목록 개체(표) 가져오기

Excel 워크북의 특정 워크시트에서 **목록 개체**(일명 *표*)를 검색합니다. 선택적 `format` 쿼리 매개변수를 사용하여 표를 원하는 형식으로 직접 내보낼 수도 있습니다.

---

## 사전 요구 사항

| 요구 사항 | 세부 정보 |
|-----------|-----------|
| **인증** | 유효한 **JWT**(Bearer) 토큰이 필요합니다. [인증 가이드](/authentication/)에 설명된 **OAuth2** 인증 흐름을 통해 토큰을 획득할 수 있습니다. |
| **스토리지** | 워크북은 Aspose Cloud 스토리지 위치에 저장되어 있어야 합니다. 파일이 기본이 아닌 스토리지에 있는 경우, `storageName` 쿼리 매개변수를 지정하세요. |
| **속도 제한** | API는 표준 Aspose Cloud 속도 제한 정책을 따릅니다(기본값 = 계정당 1분당 100개 요청). |
| **SDK(선택 사항)** | 공식 SDK(C#, Java, Python 등)를 사용하면 요청 구성 및 응답 처리가 간편해집니다. 아래 **SDK 샘플** 섹션을 참조하세요. |

---

## 요청

### HTTP GET

```
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}
```

| 매개변수 | 유형 | 위치 | 필수 | 설명 |
|----------|------|--------|--------|-------------|
| **name** | `string` | 경로(Path) | ✔️ | Excel 파일 이름(확장자 포함). |
| **sheetName** | `string` | 경로(Path) | ✔️ | 목록 개체가 포함된 워크시트 이름. |
| **listobjectindex** | `integer` | 경로(Path) | ✔️ | 검색할 목록 개체의 0부터 시작하는 인덱스. |
| **format** | `string` | 쿼리(Query) | ❌ | 원하는 내보내기 형식(예: `pdf`, `csv`, `json`). |
| **folder** | `string` | 쿼리(Query) | ❌ | 워크북이 저장된 폴더 경로. |
| **storageName** | `string` | 쿼리(Query) | ❌ | 사용할 Aspose Cloud 스토리지 이름. |

#### 참고 사항

* 모든 호출은 **반드시** HTTPS를 통해 이루어져야 합니다.  
* `format` 매개변수가 제공되면, 응답 본문은 내보낸 파일 스트림입니다(예: `application/pdf`).  
* `format` 없이 요청하면, API는 ListObject의 JSON 설명을 반환합니다.

---

## cURL 예제

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/1?format=csv" \
  -X GET \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your_jwt_token>"
```

*`<your_jwt_token>`을 인증 엔드포인트에서 획득한 유효한 JWT로 바꾸세요.*

---

## 성공 응답 (JSON)

**`format`을 생략하면**, API는 ListObject를 설명하는 JSON 페이로드를 반환합니다.

```json
{
  "ListObject": {
    "AutoFilter": {
      "FilterColumns": [],
      "Range": "B2:F11",
      "Sorter": {
        "CaseSensitive": false,
        "HasHeaders": false,
        "KeyList": [],
        "SortLeftToRight": false
      }
    },
    "DisplayName": "Table3",
    "StartColumn": 1,
    "StartRow": 1,
    "EndColumn": 5,
    "EndRow": 10,
    "ListColumns": [
      {
        "Name": "Column1",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 1,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$B$2:$B$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column2",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 2,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$C$2:$C$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column3",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 3,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$D$2:$D$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column4",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 4,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$E$2:$E$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column5",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 5,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$F$2:$F$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      }
    ],
    "ShowHeaderRow": true,
    "ShowTableStyleColumnStripes": false,
    "ShowTableStyleFirstColumn": false,
    "ShowTableStyleLastColumn": false,
    "ShowTableStyleRowStripes": true,
    "ShowTotals": false,
    "TableStyleName": "None",
    "TableStyleType": "None",
    "link": {
      "Href": "api-qa.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/0",
      "Rel": "self"
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

**`format`이 제공되면**, 응답 본문은 요청된 파일 유형의 이진 스트림입니다(예: `Content-Type: text/csv`).

---

## 오류 처리

| HTTP 코드 | 의미 | 예시 JSON |
|-----------|---------|--------------|
| **400** | 잘못된 요청 – 누락되었거나 유효하지 않은 매개변수. | `{"Code":400,"Message":"Invalid format parameter."}` |
| **401** | 인증되지 않음 – 누락되었거나 유효하지 않은 JWT 토큰. | `{"Code":401,"Message":"Authentication failed."}` |
| **404** | 찾을 수 없음 – 워크북, 워크시트 또는 목록 개체가 존재하지 않음. | `{"Code":404,"Message":"ListObject not found."}` |
| **500** | 내부 서버 오류. | `{"Code":500,"Message":"Unexpected server error."}` |

### 일반적인 실수 주의점 (참고)

* **0부터 시작하는 인덱스** – `listobjectindex`는 **0**에서 시작합니다. 인덱스 `1`을 요청하면 워크시트의 두 번째 표가 반환됩니다.  
* **폴더 및 스토리지** – 워크북이 하위 폴더에 저장된 경우, `folder` 쿼리 매개변수를 포함해야 합니다(예: `?folder=Reports/2024`).  
* **내보내기 형식** – Aspose.Cells 변환 엔진이 지원하는 형식만 허용됩니다(`pdf`, `xlsx`, `csv`, `json` 등). 지원되지 않는 값을 지정하면 **400** 오류가 발생합니다.

---

## SDK 샘플

다음 스니펫은 공식 Aspose.Cells Cloud SDK를 사용하여 엔드포인트를 호출하는 방법을 보여줍니다. 플레이스홀더 값(`<YOUR_CLIENT>`, `<YOUR_JWT>` 등)을 실제 설정으로 바꾸세요.

<details>
<summary>💻 C#</summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// API 클라이언트 초기화
var apiInstance = new ListObjectsApi();

// 요청 빌드
var request = new GetWorksheetListObjectRequest(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    listobjectindex: 1,
    format: null,               // 예: "csv"로 내보내기
    folder: null,
    storageName: null
);

// 실행
var response = apiInstance.GetWorksheetListObject(request);
Console.WriteLine(response);
```
</details>

<details>
<summary>☕ Java</summary>

```java
import com.aspose.cells.cloud.api.ListObjectsApi;
import com.aspose.cells.cloud.model.*;
import com.aspose.cells.cloud.model.requests.*;

public class GetWorksheetListObjectExample {
    public static void main(String[] args) throws ApiException {
        ListObjectsApi apiInstance = new ListObjectsApi();

        GetWorksheetListObjectRequest request = new GetWorksheetListObjectRequest(
                "Book1.xlsx",   // name
                "Sheet1",       // sheetName
                1,              // listobjectindex
                null,           // format
                null,           // folder
                null            // storageName
        );

        ListObjectResponse result = apiInstance.getWorksheetListObject(request);
        System.out.println(result);
    }
}
```
</details>

<details>
<summary>🐍 Python</summary>

```python
from asposecellscloud.apis.list_objects_api import ListObjectsApi
from asposecellscloud.models import GetWorksheetListObjectRequest

api = ListObjectsApi()

request = GetWorksheetListObjectRequest(
    name="Book1.xlsx",
    sheet_name="Sheet1",
    listobjectindex=1,
    format=None,
    folder=None,
    storage_name=None
)

response = api.get_worksheet_list_object(request)
print(response)
```
</details>

<details>
<summary>🟢 Node.js (TypeScript)</summary>

```typescript
import { ListObjectsApi, GetWorksheetListObjectRequest } from "@asposecellscloud/asposecellscloud";

const api = new ListObjectsApi();

const request = new GetWorksheetListObjectRequest({
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    listobjectindex: 1,
    format: undefined,
    folder: undefined,
    storageName: undefined
});

api.getWorksheetListObject(request)
   .then(response => console.log(response))
   .catch(err => console.error(err));
```
</details>

<details>
<summary>🐘 PHP</summary>

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

use Aspose\Cells\Cloud\Api\ListObjectsApi;
use Aspose\Cells\Cloud\Model\Requests\GetWorksheetListObjectRequest;

$listObjectsApi = new ListObjectsApi();

$request = new GetWorksheetListObjectRequest(
    "Book1.xlsx",   // name
    "Sheet1",       // sheetName
    1,              // listobjectindex
    null,           // format
    null,           // folder
    null            // storageName
);

$response = $listObjectsApi->getWorksheetListObject($request);
print_r($response);
?>
```
</details>

<details>
<summary>💎 Ruby</summary>

```ruby
require 'aspose_cells_cloud'

api_instance = AsposeCellsCloud::ListObjectsApi.new

request = AsposeCellsCloud::GetWorksheetListObjectRequest.new(
  name: 'Book1.xlsx',
  sheet_name: 'Sheet1',
  listobjectindex: 1,
  format: nil,
  folder: nil,
  storage_name: nil
)

result = api_instance.get_worksheet_list_object(request)
puts result
```
</details>

<details>
<summary>🦪 Go</summary>

```go
package main

import (
    "fmt"
    cells "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/api"
)

func main() {
    cfg := cells.NewConfiguration()
    cfg.AddDefaultHeader("Authorization", "Bearer <your_jwt>")
    client := api.NewAPIClient(cfg)

    request := api.GetWorksheetListObjectRequest{
        Name:            "Book1.xlsx",
        SheetName:       "Sheet1",
        Listobjectindex: 1,
        Format:          nil,
        Folder:          nil,
        StorageName:     nil,
    }

    result, _, err := client.ListObjectsApi.GetWorksheetListObject(request)
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    fmt.Printf("%+v\n", result)
}
```
</details>

---

## 참고 자료

| 관련 엔드포인트 | 설명 |
|------------------|-------------|
| **목록 개체 추가** | `POST /cells/{name}/worksheets/{sheetName}/listobjects` – 새 표 생성. |
| **목록 개체 업데이트** | `PUT /cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}` – 표 속성 수정. |
| **목록 개체 삭제** | `DELETE /cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}` – 표 제거. |
| **모든 목록 개체 나열** | `GET /cells/{name}/worksheets/{sheetName}/listobjects` – 워크시트의 모든 표 나열. |

---

## 참조

* **OpenAPI 명세서** – <https://apireference.aspose.cloud/cells/#/ListObjects/GetWorksheetListObject>  
* **인증 가이드** – <https://docs.aspose.cloud/cells/authentication/>  
* **GitHub 저장소(SDK)** – <https://github.com/aspose-cells-cloud>  

---
---