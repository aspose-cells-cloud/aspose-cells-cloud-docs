---
title: Excel에서 열 그룹 해제 - Aspose.Cells Cloud API  
description: Aspose.Cells Cloud REST API(v3.0)을 사용하여 Excel 워크시트에서 열 그룹을 해제합니다. 엔드포인트, 매개변수, 인증, cURL 예제, 응답 형식, SDK 스니펫을 포함합니다.  
keywords: Aspose.Cells, 그룹 해제, 열, Excel, API, REST, 클라우드, SDK  
slug: columns/ungroup  
date: 2026-07-30  
---

# Excel에서 열 그룹 해제하기  

Aspose.Cells Cloud는 지정된 워크시트에서 열 그룹을 해제하는 **POST** 작업을 제공합니다. 이 페이지에서는 요청 형식, 필요한 매개변수, 인증 방법, 예제 호출 및 SDK 사용법을 자세히 설명합니다.

---  

## 사전 요구사항  

| 요구사항 | 필요 이유 |
|----------|-------------|
| **Aspose Cloud 계정** | Aspose.Cells Cloud 서비스에 접근하기 위해 필요합니다. |
| **JWT 액세스 토큰** | 모든 API 호출은 베어러 토큰으로 인증되어야 합니다. 자세한 내용은 [JWT 인증 가이드](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)를 참조하세요. |
| **Aspose Cloud 스토리지에 저장된 워크북** | API는 클라우드 스토리지(또는 연결된 외부 스토리지)에 있는 파일을 대상으로 작동합니다. |
| **워크시트 이름** | 대상 워크시트는 워크북에 존재해야 합니다. |

---  

## 인증  

모든 요청은 유효한 JWT 토큰을 포함하는 **Authorization** 헤더가 필요합니다:

```http
Authorization: Bearer <access_token>
```

이 토큰은 Aspose Cloud OAuth 흐름을 통해 획득됩니다. 토큰은 제한된 기간 동안 유효하며, 필요에 따라 갱신해야 합니다.

---  

## 엔드포인트  

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/ungroup
```

* `{name}` – **Path** – 워크북 파일 이름(예: `test.xlsx`).  
* `{sheetName}` – **Path** – 워크시트 이름(예: `Sheet1`).  

---  

## 매개변수  

### 경로 매개변수  

| 이름 | 유형 | 필수 여부 | 설명 |
|------|------|----------|-------------|
| `name` | string | 예 | 워크북 파일 이름입니다. |
| `sheetName` | string | 예 | 워크시트 이름입니다. |

### 쿼리 매개변수  

| 이름 | 유형 | 필수 여부 | 설명 |
|------|------|----------|-------------|
| `firstIndex` | integer | 예 | 그룹 해제할 첫 번째 열의 0부터 시작하는 인덱스입니다. |
| `lastIndex` | integer | 예 | 그룹 해제할 마지막 열의 0부터 시작하는 인덱스입니다. |
| `folder` | string | 아니요 | 워크북이 포함된 폴더 경로입니다. |
| `storageName` | string | 아니요 | 파일이 위치한 스토리지 서비스 이름입니다. |

---  

## 요청 예제(cURL)  

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/ungroup?firstIndex=1&lastIndex=5" \
     -H "Authorization: Bearer <access_token>" \
     -H "Accept: application/json"
```

*`<access_token>`을 유효한 JWT 토큰으로 대체하세요.*

---  

## 성공 응답  

```json
{
  "Code": 200,
  "Status": "OK",
  "Columns": {
    "FirstIndex": 1,
    "LastIndex": 5
  }
}
```

응답 객체(`CellsCloudResponse`)는 성공적으로 그룹이 해제된 열 범위를 포함합니다.

### 오류 응답  

요청이 실패할 경우, 서비스는 다음 필드를 포함하는 JSON 페이로드를 반환합니다:

| 필드 | 의미 |
|------|------|
| `Code` | HTTP 스타일 오류 코드(예: 400, 401)입니다. |
| `Status` | 오류에 대한 간단한 설명입니다. |
| `ErrorMessage` | 오류에 대한 자세한 설명입니다. |

---  

**HTTP 상태 코드**

| 코드 | 의미 | 설명 |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK | 필터가 성공적으로 적용되었으며, 응답에는 작업 세부 정보가 포함됩니다. |
| 400  | Bad Request | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형)입니다. |
| 401  | Unauthorized | 잘못되었거나 누락된 JWT 토큰입니다. |
| 413  | Payload Too Large | 업로드된 파일이 크기 제한을 초과했습니다. |
| 500  | Internal Server Error | 예기치 않은 서버 오류입니다. |
---  

## SDK 코드 예제  

아래는 가장 널리 사용되는 SDK에 대한 실행 가능한 스니펫입니다. 플레이스홀더 값(`<YourAccessToken>`, `<YourFileName>` 등)을 귀하의 실제 데이터로 대체하세요.

<details><summary>**C# (.NET)**</summary>  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

class Program
{
    static void Main()
    {
        var config = new Configuration
        {
            AccessToken = "<YourAccessToken>",
            BaseUrl = "https://api.aspose.cloud"
        };
        var cellsApi = new CellsApi(config);

        var response = cellsApi.PostUngroupWorksheetColumns(
            name: "test.xlsx",
            sheetName: "Sheet1",
            firstIndex: 1,
            lastIndex: 5,
            folder: null,
            storageName: null);

        Console.WriteLine($"Ungrouped columns: {response.Columns.FirstIndex} – {response.Columns.LastIndex}");
    }
}
```
</details>

<details><summary>**Java**</summary>  

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.CellsCloudResponse;
import com.aspose.cells.cloud.Configuration;

public class UngroupColumns {
    public static void main(String[] args) throws Exception {
        Configuration config = new Configuration();
        config.setAccessToken("<YourAccessToken>");
        config.setBaseUrl("https://api.aspose.cloud");
        CellsApi api = new CellsApi(config);

        CellsCloudResponse resp = api.postUngroupWorksheetColumns(
            "test.xlsx",
            "Sheet1",
            1,
            5,
            null,
            null);

        System.out.println("Ungrouped columns: " + resp.getColumns().getFirstIndex()
                           + " – " + resp.getColumns().getLastIndex());
    }
}
```
</details>

<details><summary>**Python**</summary>  

```python
from asposecellscloud import CellsApi, Configuration

config = Configuration()
config.access_token = "<YourAccessToken>"
config.base_url = "https://api.aspose.cloud"

api = CellsApi(config)

response = api.post_ungroup_worksheet_columns(
    name="test.xlsx",
    sheet_name="Sheet1",
    first_index=1,
    last_index=5,
    folder=None,
    storage_name=None)

print(f"Ungrouped columns: {response.columns.first_index} – {response.columns.last_index}")
```
</details>

<details><summary>**Node.js**</summary>  

```javascript
const { CellsApi, Configuration } = require('asposecellscloud');

const config = new Configuration({
    accessToken: "<YourAccessToken>",
    baseUrl: "https://api.aspose.cloud"
});

const api = new CellsApi(config);

api.postUngroupWorksheetColumns("test.xlsx", "Sheet1", 1, 5, null, null)
   .then(resp => {
       console.log(`Ungrouped columns: ${resp.columns.firstIndex} – ${resp.columns.lastIndex}`);
   })
   .catch(err => console.error(err));
```
</details>

<details><summary>**Go**</summary>  

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    config := sdk.NewConfiguration()
    config.AccessToken = "<YourAccessToken>"
    config.BasePath = "https://api.aspose.cloud"

    api := sdk.NewCellsApi(config)

    resp, _, err := api.PostUngroupWorksheetColumns(
        "test.xlsx",
        "Sheet1",
        1,
        5,
        nil,
        nil,
    )
    if err != nil {
        panic(err)
    }
    fmt.Printf("Ungrouped columns: %d – %d\n", resp.Columns.FirstIndex, resp.Columns.LastIndex)
}
```
</details>

> **참고:** PHP, Ruby, Perl 등 다른 언어의 SDK도 동일한 매개변수 순서를 따릅니다. 전체 예제는 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하세요.

---  

## 참고 자료  

* **OpenAPI 명세서:** <https://apireference.aspose.cloud/cells/#/Cells/PostUngroupWorksheetColumns>  
* **인증 가이드:** <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>  
* **SDK 저장소:** <https://github.com/aspose-cells-cloud>

---  

## 개정 이력  

| 날짜 | 작성자 | 변경 사항 |
|------|--------|--------|
| 2026‑07‑30 | AI Optimizer | UTF‑8 인코딩 수정, 사전 요구사항 추가, 메타 키워드 정리, 제목 계층 구조 개선, SDK 스니펫 삽입 |
| 2026‑07‑29 | Original | 초기 문서 초안 작성 |