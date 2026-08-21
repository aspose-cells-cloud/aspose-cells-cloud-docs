---
title: "워크시트 하이퍼링크 삭제"
type: docs
url: /ko/hyperlinks/delete/
description: "Aspose.Cells Cloud API를 사용하여 인덱스로 워크시트 하이퍼링크를 삭제합니다. 필요한 매개변수, 인증 방법 및 C#, Java, Python 등 다양한 언어의 코드 예제를 확인하세요."
keywords: "Aspose.Cells, 클라우드, 하이퍼링크 삭제, Excel API, REST, 워크시트 하이퍼링크"
ArticleTitle: "워크시트 하이퍼링크 삭제 – Aspose.Cells Cloud API 문서"
weight: 40
---

이 REST API는 Excel 워크시트에서 인덱스를 기준으로 워크시트 하이퍼링크를 삭제합니다.

## 보안 및 인증
Aspose.Cells Cloud API는 보안이 적용되며, [JWT 토큰 기반 인증](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)이 필요합니다.

### REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
```

### 요청 매개변수

| 매개변수 이름       | 유형     | 위치   | 필수 여부 | 설명                                                          |
| ------------------ | ------- | ------ | -------- | ------------------------------------------------------------- |
| **name**           | string  | path   | ✅       | Excel 문서 이름.                                              |
| **sheetName**      | string  | path   | ✅       | 워크시트 이름.                                                |
| **hyperlinkIndex** | integer | path   | ✅       | 삭제할 하이퍼링크의 0부터 시작하는 인덱스.                     |
| **folder**         | string  | query  | ❌       | 문서가 포함된 폴더(기본값: 루트).                             |
| **storageName**    | string  | query  | ❌       | 스토리지 서비스 이름(생략 시 기본 스토리지 사용).              |

#### 응답 코드

| 상태 코드                     | 설명                                                      | 예시 응답 본문                                      |
| ----------------------------- | --------------------------------------------------------- | -------------------------------------------------- |
| **200 OK**                    | 하이퍼링크가 성공적으로 삭제되었습니다.                   | `{"Code":200,"Status":"OK"}`                       |
| **400 Bad Request**           | 누락되거나 유효하지 않은 매개변수.                         | `{"Code":400,"Message":"Invalid hyperlinkIndex."}` |
| **401 Unauthorized**          | 인증 토큰이 누락되었거나 유효하지 않습니다.                 | `{"Code":401,"Message":"Invalid access token."}`   |
| **404 Not Found**             | 파일, 워크시트 또는 하이퍼링크 인덱스가 존재하지 않습니다.  | `{"Code":404,"Message":"Resource not found."}`     |
| **500 Internal Server Error** | 예기치 않은 서버 오류.                                    | `{"Code":500,"Message":"Internal server error."}`  |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Hypelinks/DeleteWorksheetHyperlink)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예제는 cURL을 사용해 API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test1.xlsx/worksheets/Sheet1/hyperlinks/0" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## 클라우드 SDK 패밀리

SDK를 사용하면 개발 속도가 가장 빠릅니다. SDK가 저수준 세부 사항을 처리해주므로, 프로젝트 개발에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다. 신뢰성을 위해 인라인 스니펫을 제공하며, 원본 Gist로의 링크는 참고용으로 유지됩니다.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// ExampleDeleteWorksheetHyperlink.cs
// 출처: https://gist.github.com/aspose-cells-cloud-gists/8a5b324fdf3e574dbd747c1a1e24b05d
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new CellsApi("<client_id>", "<client_secret>");
var response = apiInstance.DeleteWorksheetHyperlink(
    name: "test1.xlsx",
    sheetName: "Sheet1",
    hyperlinkIndex: 0,
    folder: null,
    storageName: null);
Console.WriteLine(response.Status);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Example_DeleteWorksheetHyperlink.java
// 출처: https://gist.github.com/aspose-cells-cloud-gists/c59aa5c02f735466a5e34751cee73f5f
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.*;

CellsApi api = new CellsApi("<client_id>", "<client_secret>");
ApiResponse<Void> response = api.deleteWorksheetHyperlink(
    "test1.xlsx",
    "Sheet1",
    0,
    null,
    null);
System.out.println("Status: " + response.getStatusCode());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
// Example_DeleteWorksheetHyperlink.php
// 출처: https://gist.github.com/aspose-cells-cloud-gists/84283c8ba766ed815f47e6dfb0891152
require_once('vendor/autoload.php');

$config = new Aspose\Cells\Configuration();
$config->setAppSid('<client_id>');
$config->setAppKey('<client_secret>');

$apiInstance = new Aspose\Cells\Api\CellsApi($config);
$response = $apiInstance->deleteWorksheetHyperlink(
    "test1.xlsx",
    "Sheet1",
    0,
    null,
    null);
echo $response->getStatusCode();
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# Example_DeleteWorksheetHyperlink.rb
// 출처: https://gist.github.com/aspose-cells-cloud-gists/36ed8b8727561b92692939513d365fca
require 'aspose_cells_cloud'

api = AsposeCellsCloud::CellsApi.new('<client_id>', '<client_secret>')
result = api.delete_worksheet_hyperlink('test1.xlsx', 'Sheet1', 0)
puts result.status
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```javascript
// Example_DeleteWorksheetHyperlink.ts (Node.js)
// 출처: https://gist.github.com/aspose-cells-cloud-gists/e82de2e4189bc27ae92abf73c36b4df0
const AsposeCellsCloud = require("asposecellscloud");
const api = new AsposeCellsCloud.CellsApi("<client_id>", "<client_secret>");

api
  .deleteWorksheetHyperlink("test1.xlsx", "Sheet1", 0, null, null)
  .then(() => console.log("Hyperlink deleted"))
  .catch((err) => console.error(err));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```python
# Example_DeleteWorksheetHyperlink.py
// 출처: https://gist.github.com/aspose-cells-cloud-gists/61e922de11e6e7144db88adcad6501c1
from asposecellscloud import CellsApi, Configuration

config = Configuration(app_sid='<client_id>', app_key='<client_secret>')
api = CellsApi(config)

api.delete_worksheet_hyperlink('test1.xlsx', 'Sheet1', 0)
print('Hyperlink deleted')
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
# Example_DeleteWorksheetHyperlink.pl
// 출처: https://gist.github.com/aspose-cells-cloud-gists/f82a3a00251e34ff8766116282c8c9ca
use AsposeCellsCloud::CellsApi;

my $api_instance = AsposeCellsCloud::CellsApi->new('<client_id>', '<client_secret>');
my $result = $api_instance->delete_worksheet_hyperlink(
    name => 'test1.xlsx',
    sheet_name => 'Sheet1',
    hyperlink_index => 0);
print "Status: $result->{status}\n";
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go
// Example_DeleteWorksheetHyperlink.go
// 출처: https://gist.github.com/aspose-cells-cloud-gists/2b824d4e13644368d12682856aa49185
package main

import (
    "fmt"
    "github.com/asposecellscloud/asposecellscloud-go/v3"
)

func main() {
    config := asposecellscloud.NewConfiguration("<client_id>", "<client_secret>")
    api := asposecellscloud.NewAPIClient(config).CellsApi
    _, err := api.DeleteWorksheetHyperlink("test1.xlsx", "Sheet1", 0, nil, nil)
    if err != nil {
        fmt.Println(err)
    } else {
        fmt.Println("Hyperlink deleted")
    }
}
```

{{< /tab >}}

{{< /tabs >}}