---
title: "워크시트의 모든 주석 삭제"
description: "Aspose.Cells Cloud API를 사용하여 Excel 파일의 워크시트에서 모든 주석을 삭제합니다. DELETE 엔드포인트, 필수 매개변수, 인증 방법, 샘플 cURL 요청, 응답 형식, 오류 코드 및 SDK 예제를 알아봅니다."
keywords: "Aspose, Cells, 주석 삭제, 워크시트, API, REST, Excel, 클라우드"
url: /comments/clear/
aliases:
  - /delete-all-comments-in-a-worksheet/
weight: 50
---

# 워크시트의 모든 주석 삭제

**API 버전:** `v3.0`  
**리소스:** `Worksheets` → `DeleteWorksheetComments`  

Aspose.Cells Cloud는 지정된 워크시트에서 **모든** 주석을 제거하는 강력한 REST 엔드포인트를 제공합니다. 이 작업은 되돌릴 수 없으며, 실행 후 주석은 복구할 수 없습니다.

---

## 사전 요구 사항

| 요구 사항 | 세부 정보 |
|-----------|-----------|
| **인증** | `Authorization` 헤더에 유효한 JWT 액세스 토큰(`Bearer <jwt token>`)이 필요합니다. 토큰은 [OAuth2 인증 흐름](https://docs.aspose.cloud/cells/authentication/)을 통해 획득할 수 있습니다. |
| **스토리지** | 파일은 Aspose.Cells Cloud에서 접근 가능한 스토리지에 있어야 합니다(`storageName`을 생략하면 기본 스토리지를 사용합니다). |
| **권한** | 토큰은 대상 파일에 대한 읽기 및 쓰기 권한을 보유하고 있어야 합니다. |
| **SDK (선택사항)** | .NET, Java, PHP, Ruby, Node.js, Python, Perl, Go용 SDK가 제공됩니다(자세한 내용은 **SDK 예제** 섹션 참조). |

---

## HTTP 요청

### 엔드포인트

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments
```

### 경로 매개변수

| 이름          | 유형     | 설명 |
|---------------|----------|------|
| `name`        | string   | Excel 파일 이름(예: `test.xlsx`). |
| `sheetName`   | string   | 워크시트 이름(예: `Sheet1`). |

### 쿼리 매개변수

| 이름           | 유형     | 필수 여부 | 설명 |
|----------------|----------|-----------|------|
| `folder`       | string   | 선택사항  | 파일이 포함된 폴더 경로. |
| `storageName`  | string   | 선택사항  | 파일이 위치한 스토리지 이름. |

### 요청 헤더

| 헤더               | 값                                |
|--------------------|-----------------------------------|
| `Authorization`    | `Bearer <jwt token>`              |
| `Accept`           | `application/json`                |
| `Content-Type`     | `application/json`                |

---

## 요청 예시(cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments?folder=Documents&storageName=MyStorage" \
  -X DELETE \
  -H "Accept: application/json" \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

*`test.xlsx`, `Sheet1`, `Documents`, `MyStorage`, `<jwt token>`을 실제 값으로 대체하세요.*

---

## 응답

### 성공 (200)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

응답 본문은 `CellsCloudResponse` 모델을 따릅니다.

### 오류 응답

| HTTP 코드 | 의미                                 | 예시 응답 본문 |
|-----------|--------------------------------------|----------------|
| **400**   | 잘못된 요청 – 유효하지 않은 매개변수. | `{ "Code": 400, "Message": "Invalid request." }` |
| **401**   | 인증 실패 – 누락되거나 유효하지 않은 JWT 토큰. | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404**   | 찾을 수 없음 – 파일 또는 워크시트가 존재하지 않음. | `{ "Code": 404, "Message": "Resource not found." }` |
| **500**   | 내부 서버 오류. | `{ "Code": 500, "Message": "Server error." }` |

---

## SDK 예제

다음 스니펫은 공식 Aspose.Cells Cloud SDK(버전 3.13.0)를 사용해 엔드포인트를 호출하는 방법을 보여줍니다. 플레이스홀더 값(`<fileName>`, `<sheet>`, `<jwt token>` 등)을 실제 데이터로 대체하세요.

### C#  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new WorksheetsApi();
var name = "test.xlsx"; // string | 파일 이름.
var sheetName = "Sheet1"; // string | 워크시트 이름.
var folder = "Documents"; // string | 폴더 경로 (선택사항)
var storageName = "MyStorage"; // string | 스토리지 이름 (선택사항)

try
{
    var response = apiInstance.DeleteWorksheetComments(name, sheetName, folder, storageName);
    Console.WriteLine(response.Status);
}
catch (Exception e)
{
    Console.WriteLine("WorksheetsApi.DeleteWorksheetComments 호출 중 예외 발생: " + e.Message );
}
```

### Java  

```java
import com.aspose.cells.cloud.sdk.api.WorksheetsApi;
import com.aspose.cells.cloud.sdk.model.*;

public class DeleteWorksheetComments {
    public static void main(String[] args) {
        WorksheetsApi api = new WorksheetsApi();
        String name = "test.xlsx";
        String sheetName = "Sheet1";
        String folder = "Documents";
        String storageName = "MyStorage";

        try {
            CellsCloudResponse resp = api.deleteWorksheetComments(name, sheetName, folder, storageName);
            System.out.println(resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### PHP  

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

use Aspose\Cells\Cloud\Api\WorksheetsApi;

$apiInstance = new WorksheetsApi();
$name = "test.xlsx";
$sheetName = "Sheet1";
$folder = "Documents";
$storageName = "MyStorage";

try {
    $result = $apiInstance->deleteWorksheetComments($name, $sheetName, $folder, $storageName);
    echo $result->getStatus();
} catch (Exception $e) {
    echo 'WorksheetsApi->deleteWorksheetComments 호출 중 예외 발생: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Ruby  

```ruby
require 'aspose_cells_cloud'

api_instance = AsposeCellsCloud::WorksheetsApi.new
name = 'test.xlsx'
sheet_name = 'Sheet1'
folder = 'Documents'          # 선택사항
storage_name = 'MyStorage'    # 선택사항

begin
  result = api_instance.delete_worksheet_comments(name, sheet_name, folder, storage_name)
  puts result.status
rescue AsposeCellsCloud::ApiError => e
  puts "WorksheetsApi->delete_worksheet_comments 호출 중 예외 발생: #{e}"
end
```

### Node.js (TypeScript)  

```typescript
import { WorksheetsApi } from "@asposecloud/cells-sdk";

const api = new WorksheetsApi();
const name = "test.xlsx";
const sheetName = "Sheet1";
const folder = "Documents";
const storageName = "MyStorage";

api.deleteWorksheetComments(name, sheetName, folder, storageName)
    .then((response) => console.log(response.status))
    .catch((error) => console.error("오류:", error));
```

### Python  

```python
from asposecellscloud import WorksheetsApi

api_instance = WorksheetsApi()
name = "test.xlsx"
sheet_name = "Sheet1"
folder = "Documents"          # 선택사항
storage_name = "MyStorage"    # 선택사항

try:
    response = api_instance.delete_worksheet_comments(name, sheet_name, folder, storage_name)
    print(response.status)
except Exception as e:
    print("WorksheetsApi->delete_worksheet_comments 호출 중 예외 발생:", e)
```

### Perl  

```perl
use AsposeCellsCloud::Api::WorksheetsApi;

my $api_instance = AsposeCellsCloud::Api::WorksheetsApi->new();

my $name = 'test.xlsx';
my $sheet_name = 'Sheet1';
my $folder = 'Documents';
my $storage_name = 'MyStorage';

eval {
    my $result = $api_instance->delete_worksheet_comments(
        name => $name,
        sheet_name => $sheet_name,
        folder => $folder,
        storage_name => $storage_name
    );
    print $result->{status}, "\n";
};
if ($@) {
    print "WorksheetsApi->delete_worksheet_comments 호출 중 예외 발생: $@\n";
}
```

### Go  

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    cfg := sdk.NewConfiguration()
    cfg.AddDefaultHeader("Authorization", "Bearer <jwt token>")
    api := sdk.NewWorksheetsApi(cfg)

    name := "test.xlsx"
    sheetName := "Sheet1"
    folder := "Documents"
    storageName := "MyStorage"

    resp, _, err := api.DeleteWorksheetComments(name, sheetName, folder, storageName)
    if err != nil {
        fmt.Printf("오류: %v\n", err)
        return
    }
    fmt.Println(resp.Status)
}
```

---

## 참고 사항 및 제한 사항

* 이 작업은 지정된 워크시트의 **모든 주석을 삭제**합니다. 실행 전 주의가 필요하며, 되돌릴 수 없습니다.
* 요청 본문은 **받지 않으며**, 모든 필수 정보는 URL과 헤더를 통해 전달됩니다.
* 대상 파일이 **암호화되어 보호**되어 있거나 워크시트가 **읽기 전용**인 경우, 원인에 따라 API가 `400` 또는 `401` 오류를 반환합니다.
* 엔드포인트는 **Aspose Cloud Storage**에 저장된 파일뿐만 아니라, `storageName`을 통해 **Amazon S3**, **Azure Blob**, **Google Cloud Storage**도 지원합니다.

---

## 관련 리소스

* **OpenAPI 사양** – [DeleteWorksheetComments](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetComments)
* **인증 가이드** – [Aspose.Cells Cloud용 OAuth2](https://docs.aspose.cloud/cells/authentication/)
* **SDK 저장소** – <https://github.com/aspose-cells-cloud>
* **일반 워크시트 API** – <https://docs.aspose.cloud/cells/worksheets/>

---

*최종 업데이트: 2026-07-30*