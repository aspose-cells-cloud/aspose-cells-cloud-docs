---
title: 세로 page break 삭제 – Aspose.Cells Cloud REST API
description: Aspose.Cells Cloud REST API(v3.0)를 사용하여 Excel 워크시트에서 세로 page break를 제거합니다. 요청 구문, 매개변수, 예제, 응답 코드, SDK 스니펫이 포함됩니다.
keywords: 세로 page break 삭제, Aspose.Cells Cloud, REST API
slug: delete-vertical-page-break
api_version: v3.0
---

# 세로 page break 삭제

Aspose.Cells Cloud REST API를 사용하여 Excel 워크북의 워크시트에서 세로 page break를 삭제합니다.

---

## 사전 요구 사항

* `Authorization` 헤더에 **JWT 인증 토큰**을 제공해야 합니다.  
* 워크북(`{name}`)은 지정된 **폴더** 또는 **스토리지**에 저장되어 API 클라이언트가 접근할 수 있어야 합니다.

---

## HTTP 요청

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks/{index}
```

| 매개변수 | 유형 | 위치 | 필수 여부 | 설명 |
|---------|------|------|----------|------|
| **name**      | string | path   | 예 | Excel 파일의 이름입니다. |
| **sheetName** | string | path   | 예 | page break가 포함된 워크시트의 이름입니다. |
| **index**     | integer| path   | 예 | 삭제할 세로 page break의 0부터 시작하는 인덱스입니다. |
| **folder**    | string | query  | 아니요 | 파일이 저장된 폴더 경로입니다. |
| **storageName**| string| query  | 아니요 | 스토리지 서비스의 이름입니다. |

---

## 요청 예제

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/verticalpagebreaks/0?folder=Docs&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>"
```

---

## 성공 응답

| 코드 | 설명 |
|------|------|
| **200** | 세로 page break가 성공적으로 삭제되었습니다. |

**예제 페이로드**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

---

## 오류 응답

| HTTP 코드 | 설명 |
|-----------|------|
| **401** | 인증되지 않음 – 토큰이 누락되었거나 유효하지 않습니다. |
| **404** | 찾을 수 없음 – 지정된 파일, 워크시트 또는 page-break 인덱스가 존재하지 않습니다. |
| **400** | 잘못된 요청 – 요청 구문이 잘못되었거나 매개변수가 유효하지 않습니다. |
| **500** | 내부 서버 오류 – 예기치 않은 조건이 발생했습니다. |

**오류 페이로드 예제**

*401 – 인증되지 않음*

```json
{
  "Code": 401,
  "Message": "Invalid authentication token."
}
```

*404 – 찾을 수 없음*

```json
{
  "Code": 404,
  "Message": "The specified file, worksheet, or page‑break index was not found."
}
```

*400 – 잘못된 요청*

```json
{
  "Code": 400,
  "Message": "The request parameters are invalid or malformed."
}
```

*500 – 내부 서버 오류*

```json
{
  "Code": 500,
  "Message": "An unexpected server error occurred."
}
```

---

## SDK 코드 예제

다음 예제는 다양한 Aspose.Cells Cloud SDK를 사용하여 **DeleteVerticalPageBreak** 작업을 호출하는 방법을 보여줍니다.

<details><summary>**C#**</summary>

```csharp
// Install-Package Aspose.Cells-Cloud
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new CellsApi("client_id", "client_secret");
string name = "Book1.xlsx";
string sheetName = "Sheet1";
int index = 0;
string folder = "Docs";
string storageName = "MyStorage";

try
{
    var response = apiInstance.DeleteVerticalPageBreak(name, sheetName, index, folder, storageName);
    Console.WriteLine($"Status: {response.Status}");
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling CellsApi.DeleteVerticalPageBreak: " + e.Message );
}
```

</details>

<details><summary>**Java**</summary>

```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.CellsCloudResponse;

public class DeleteVerticalPageBreak {
    public static void main(String[] args) {
        CellsApi api = new CellsApi("client_id", "client_secret");
        String name = "Book1.xlsx";
        String sheetName = "Sheet1";
        int index = 0;
        String folder = "Docs";
        String storageName = "MyStorage";

        try {
            CellsCloudResponse resp = api.deleteVerticalPageBreak(name, sheetName, index, folder, storageName);
            System.out.println("Status: " + resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

</details>

<details><summary>**Python**</summary>

```python
from asposecellscloud import CellsApi, ApiClient, Configuration

config = Configuration()
config.client_id = "client_id"
config.client_secret = "client_secret"
api_client = ApiClient(configuration=config)
api = CellsApi(api_client)

name = "Book1.xlsx"
sheet_name = "Sheet1"
index = 0
folder = "Docs"
storage_name = "MyStorage"

try:
    response = api.delete_vertical_page_break(name, sheet_name, index, folder, storage_name)
    print("Status:", response.status)
except Exception as e:
    print("Error:", e)
```

</details>

<details><summary>**Node.js**</summary>

```javascript
const { CellsApi, ApiClient, Configuration } = require('asposecellscloud');

const config = new Configuration();
config.clientId = "client_id";
config.clientSecret = "client_secret";

const api = new CellsApi(new ApiClient(config));

const name = "Book1.xlsx";
const sheetName = "Sheet1";
const index = 0;
const folder = "Docs";
const storageName = "MyStorage";

api.deleteVerticalPageBreak(name, sheetName, index, folder, storageName)
  .then(response => console.log('Status:', response.status))
  .catch(error => console.error('Error:', error));
```

</details>

<details><summary>**Go**</summary>

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3"
)

func main() {
    config := asposecellscloud.NewConfiguration()
    config.ClientId = "client_id"
    config.ClientSecret = "client_secret"

    api := asposecellscloud.NewAPIClient(config).CellsApi
    name := "Book1.xlsx"
    sheetName := "Sheet1"
    index := int32(0)
    folder := "Docs"
    storageName := "MyStorage"

    resp, _, err := api.DeleteVerticalPageBreak(name, sheetName, index, folder, storageName)
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    fmt.Println("Status:", resp.Status)
}
```

</details>

*(PHP, Ruby, Perl 및 기타 언어에 대한 SDK 스니펫도 동일한 패턴으로 제공되며 공식 GitHub 저장소에서 확인할 수 있습니다.)*

---

## 관련 리소스

* **OpenAPI 사양** – [DeleteVerticalPageBreak](https://apireference.aspose.cloud/cells/#/PageBreaks/DeleteVerticalPageBreak)  
* **Aspose.Cells Cloud SDK** – <https://github.com/aspose-cells-cloud>  
* **인증 가이드** – <https://docs.aspose.cloud/cells/authentication/>  

--- 

*문서 최종 업데이트 날짜: 2026‑07‑30*