---
title: "워크시트 코멘트 삭제 API – Aspose.Cells Cloud"
description: "Aspose.Cells Cloud REST API(v3.0)를 사용하여 Excel 워크시트의 특정 셀 코멘트를 삭제합니다. 엔드포인트, 매개변수, 요청/응답 예제, SDK 스니펫, 오류 처리를 포함합니다."
keywords: "Aspose.Cells, 코멘트 삭제, Excel API, REST, 워크시트 코멘트"
date: "2026-07-30"
lastModified: "2026-07-30"
---

# 워크시트 코멘트 삭제 API – Aspose.Cells Cloud

> **최종 업데이트일:** 2026년 7월 30일  

## 개요
**코멘트**는 Excel 워크시트의 특정 셀에 첨부된 텍스트 메모입니다.  
**워크시트 코멘트 삭제** 작업은 지정된 셀에서 코멘트를 제거합니다.

![Aspose.Cells Cloud – 워크시트 코멘트 삭제 예시](/cells/images/Aspose-image-for-open-graph.jpg "Aspose.Cells Cloud – 워크시트 코멘트 삭제 API")

## 인증
모든 Aspose.Cells Cloud 엔드포인트는 **JWT 토큰 기반 인증**이 필요합니다.  
`Authorization` 헤더에 토큰을 포함하세요:

```
Authorization: Bearer <jwt token>
```

JWT 토큰 획득 방법에 대한 자세한 내용은 [인증 가이드](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)를 참조하세요.

## 사전 요구 사항
- 유효한 JWT 액세스 토큰  
- 대상 워크북(`{name}`)이 지정된 스토리지 위치에 존재해야 합니다.  
- 선택 사항: 선호하는 언어에 대한 Aspose.Cells Cloud SDK 중 하나 설치

## HTTP 요청

### 엔드포인트
```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### 경로 매개변수
| 매개변수 | 유형   | 필수 여부 | 설명 |
|----------|--------|-----------|------|
| `name`      | 문자열 | ✅ | Excel 워크북의 이름(예: `test.xlsx`) |
| `sheetName` | 문자열 | ✅ | 코멘트가 포함된 워크시트의 이름 |
| `cellName`  | 문자열 | ✅ | 코멘트를 삭제할 셀의 주소(예: `A1`) |

### 쿼리 매개변수
| 매개변수      | 유형   | 필수 여부 | 설명 |
|---------------|--------|-----------|------|
| `folder`      | 문자열 | ❌ | 워크북이 저장된 폴더 경로. 생략 시 루트 폴더가 사용됩니다. |
| `storageName` | 문자열 | ❌ | 스토리지 서비스 이름(예: `MyCloud`). 생략 시 기본 스토리지가 사용됩니다. |

## 요청 예제

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/A1?folder=Docs&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

## 응답

### 성공 (200)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**HTTP 상태 코드**

| 코드 | 의미              | 설명 |
|------|-------------------|------|
| 200  | OK                | 필터가 성공적으로 적용되었으며, 응답에 작업 세부 정보가 포함됩니다. |
| 400  | 잘못된 요청       | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형) |
| 401  | 인증되지 않음     | 잘못되거나 누락된 JWT 토큰 |
| 413  | 페이로드가 너무 큼 | 업로드된 파일이 크기 제한을 초과함 |
| 500  | 내부 서버 오류    | 예기치 않은 서버 오류 |

### 오류 응답

| HTTP 코드 | 설명 | 예시 |
|-----------|------|------|
| 400 | 잘못된 요청 – 누락되거나 잘못된 매개변수 | `{ "Code": 400, "Message": "Invalid parameters." }` |
| 401 | 인증되지 않음 – 잘못되거나 누락된 토큰 | `{ "Code": 401, "Message": "Authentication required." }` |
| 404 | 찾을 수 없음 – 파일, 워크시트 또는 코멘트가 존재하지 않음 | `{ "Code": 404, "Message": "Resource not found." }` |
| 500 | 내부 서버 오류 – 서버에서 예기치 않은 조건 발생 | `{ "Code": 500, "Message": "Server error." }` |

## SDK 예제
다음은 가장 인기 있는 언어를 위한 즉시 실행 가능한 스니펫입니다. `<jwt token>`, `test.xlsx`, `Sheet1`, `A1`을 자신의 값으로 바꾸세요.

### C#
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using Aspose.Cells.Cloud.SDK.Client;

// Configure the API client
var config = new Configuration
{
    AccessToken = "<jwt token>",
    BasePath = "https://api.aspose.cloud"
};

var apiInstance = new WorksheetsApi(config);
try
{
    var result = apiInstance.DeleteWorksheetComment(
        name: "test.xlsx",
        sheetName: "Sheet1",
        cellName: "A1",
        folder: "Docs",
        storageName: "MyStorage"
    );
    Console.WriteLine("Comment deleted. Status: " + result.Status);
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling WorksheetsApi.DeleteWorksheetComment: " + e.Message);
}
```

### Java
```java
import com.aspose.cloud.cells.api.WorksheetsApi;
import com.aspose.cloud.cells.client.ApiException;
import com.aspose.cloud.cells.model.CellsCloudResponse;

public class DeleteWorksheetCommentExample {
    public static void main(String[] args) {
        WorksheetsApi api = new WorksheetsApi();
        api.getApiClient().setAccessToken("<jwt token>");
        try {
            CellsCloudResponse response = api.deleteWorksheetComment(
                "test.xlsx",
                "Sheet1",
                "A1",
                "Docs",
                "MyStorage"
            );
            System.out.println("Deleted comment, status: " + response.getStatus());
        } catch (ApiException e) {
            System.err.println("Exception when calling WorksheetsApi#deleteWorksheetComment");
            e.printStackTrace();
        }
    }
}
```

### PHP
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$config = new Aspose\Cells\Configuration();
$config->setAccessToken('<jwt token>');
$config->setHost('https://api.aspose.cloud');

$apiInstance = new Aspose\Cells\Api\WorksheetsApi(
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->deleteWorksheetComment(
        'test.xlsx',
        'Sheet1',
        'A1',
        'Docs',
        'MyStorage'
    );
    echo "Comment deleted. Status: " . $result->getStatus();
} catch (Exception $e) {
    echo 'Exception when calling WorksheetsApi->deleteWorksheetComment: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Ruby
```ruby
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.access_token = '<jwt token>'
config.host = 'https://api.aspose.cloud'

api_instance = AsposeCellsCloud::WorksheetsApi.new
begin
  result = api_instance.delete_worksheet_comment('test.xlsx', 'Sheet1', 'A1', 'Docs', 'MyStorage')
  puts "Comment deleted – status: #{result.status}"
rescue AsposeCellsCloud::ApiError => e
  puts "Exception when calling WorksheetsApi->delete_worksheet_comment: #{e}"
end
```

### Node.js (TypeScript)
```typescript
import { WorksheetsApi, Configuration } from "@asposecloud/cells-cloud";

const config = new Configuration({
    accessToken: "<jwt token>",
    basePath: "https://api.aspose.cloud"
});

const api = new WorksheetsApi(config);

api.deleteWorksheetComment("test.xlsx", "Sheet1", "A1", "Docs", "MyStorage")
    .then((response) => {
        console.log("Comment deleted. Status:", response.status);
    })
    .catch((error) => {
        console.error("Error deleting comment:", error);
    });
```

### Python
```python
from asposecellscloud.apis import WorksheetsApi
from asposecellscloud import Configuration, ApiClient

config = Configuration()
config.access_token = "<jwt token>"
config.host = "https://api.aspose.cloud"

api_client = ApiClient(configuration=config)
api = WorksheetsApi(api_client)

try:
    response = api.delete_worksheet_comment(
        name="test.xlsx",
        sheet_name="Sheet1",
        cell_name="A1",
        folder="Docs",
        storage_name="MyStorage"
    )
    print("Comment deleted. Status:", response.status)
except Exception as e:
    print("Exception when calling WorksheetsApi->delete_worksheet_comment:", e)
```

### Perl
```perl
use AsposeCellsCloud::Api::WorksheetsApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new(
    access_token => '<jwt token>',
    host => 'https://api.aspose.cloud'
);
my $api_instance = AsposeCellsCloud::Api::WorksheetsApi->new($config);

eval {
    my $result = $api_instance->delete_worksheet_comment(
        name        => 'test.xlsx',
        sheet_name  => 'Sheet1',
        cell_name   => 'A1',
        folder      => 'Docs',
        storage_name=> 'MyStorage'
    );
    print "Comment deleted. Status: " . $result->{status} . "\n";
};
if ($@) {
    warn "Exception when calling WorksheetsApi->delete_worksheet_comment: $@\n";
}
```

### Go
```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/api"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/config"
)

func main() {
    cfg := config.NewConfiguration()
    cfg.AccessToken = "<jwt token>"
    cfg.Host = "https://api.aspose.cloud"

    apiInstance := api.NewWorksheetsApi(cfg)

    result, _, err := apiInstance.DeleteWorksheetComment(
        "test.xlsx",   // name
        "Sheet1",      // sheetName
        "A1",          // cellName
        "Docs",        // folder (optional)
        "MyStorage",   // storageName (optional)
    )
    if err != nil {
        fmt.Printf("Error when calling DeleteWorksheetComment: %v\n", err)
        return
    }
    fmt.Printf("Comment deleted. Status: %s\n", result.Status)
}
```

## 관련 작업
- [워크시트 코멘트 추가](/comments/add/)  
- [워크시트 코멘트 업데이트](/comments/update/)  

## 속도 제한
Aspose.Cells Cloud은 계정당 기본 **분당 100개의 요청** 속도 제한을 적용합니다. 이 제한을 초과하면 HTTP 429 Too Many Requests가 반환됩니다. 지수 백오프를 구현하거나 `Retry-After` 헤더를 준수하여 제한을 피하세요.

## 참고 자료
- **OpenAPI 스펙:** <https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetComment>  
- **인증 가이드:** <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>  
- **SDK 저장소:** <https://github.com/aspose-cells-cloud>  
---