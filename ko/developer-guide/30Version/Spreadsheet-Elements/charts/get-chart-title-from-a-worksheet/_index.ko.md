---
title: "워크시트에서 차트 제목 가져오기"
type: docs
url: /charts/title/get/
aliases: [/get-chart-title-from-a-worksheet/]
weight: 120
keywords:
  - "Aspose.Cells Cloud"
  - "차트 제목"
  - "Excel"
  - "REST API"
  - "차트 제목 가져오기"
  - "cURL"
  - "SDK"
  - "Excel 차트 자동화"
  - "GET 차트 제목"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트의 차트 제목을 검색하는 방법을 알아보세요. 엔드포인트, 매개변수, 인증, 샘플 cURL 및 SDK 코드를 포함합니다."
ArticleTitle: "워크시트에서 차트 제목 가져오기"
---

이 REST API는 Excel 워크북의 워크시트에 저장된 차트의 제목을 검색합니다.

**필수 조건**: 이 엔드포인트를 호출하려면 `Cells.Read` 범위가 있는 유효한 Aspose.Cells Cloud OAuth2/JWT 액세스 토큰이 필요합니다. 워크북은 이미 지정된 저장소 위치에 업로드되어 있어야 합니다.

## GetWorksheetChartTitle API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 구현되었으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름 | 유형    | 위치 | 설명                                     |
| ------------- | ------- | ---- | ---------------------------------------- |
| name          | string  | path | 워크북 파일 이름입니다.                  |
| sheetName     | string  | path | 차트가 포함된 워크시트 이름입니다.      |
| chartIndex    | integer | path | 차트의 0부터 시작하는 인덱스입니다.      |
| folder        | string  | query | 워크북이 저장된 폴더 경로입니다.         |
| storageName   | string  | query | 저장소 서비스 이름입니다.                |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChartTitle)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

**cURL** 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/charts/0/title" \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt 토큰>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Title": {
    "Text": "1분기 매출",
    "Font": {
      "Name": "Arial",
      "Size": 12,
      "IsBold": true
    }
  }
}
```

{{< /tab >}}

{{< /tabs >}}

**응답 필드**

| 필드                | 설명                                            |
| ------------------- | ----------------------------------------------- |
| `Title.Text`        | 차트 제목으로 표시되는 실제 텍스트입니다.        |
| `Title.Font.Name`   | 제목에 사용되는 글꼴 패밀리입니다(예: _Arial_). |
| `Title.Font.Size`   | 포인트 단위의 글꼴 크기입니다.                  |
| `Title.Font.IsBold` | 제목 텍스트가 굵게 표시되는지 여부를 나타냅니다. |

**응답 상태 코드**

| 코드 | 설명 |
|------|------|
| 200 OK | 차트 제목이 성공적으로 검색되었습니다. |
| 401 Unauthorized | 인증에 실패했거나 토큰이 누락되었거나 유효하지 않습니다. |
| 404 Not Found | 지정된 워크북, 워크시트 또는 차트가 존재하지 않습니다. |
| 500 Internal Server Error | 예기치 않은 서버 오류가 발생했습니다. |

**참고**: 차트 인덱스는 0부터 시작하며, 차트가 실제로 존재하는지 확인해야 합니다. 워크북이 업로드되지 않은 경우, 먼저 해당 API를 사용하여 업로드해야 합니다.

**스크립트에서 제목 추출 방법(`jq` 사용)**

```bash
# JSON 응답이 response.json에 저장되었다고 가정
title=$(jq -r '.Title.Text' response.json)
echo "차트 제목: $title"
```

## 클라우드 SDK 패밀리

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// C# 예제: Aspose.Cells Cloud SDK 사용
var config = new Configuration
{
    AccessToken = "<jwt 토큰>",
    BasePath = "https://api.aspose.cloud"
};
var api = new ChartsApi(config);
var response = api.GetWorksheetChartTitle("Book1.xlsx", "Sheet1", 0, folder: "", storageName: "");
Console.WriteLine(response.Title.Text);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Java 예제: Aspose.Cells Cloud SDK 사용
Configuration config = new Configuration();
config.setAccessToken("<jwt 토큰>");
config.setBasePath("https://api.aspose.cloud");
ChartsApi api = new ChartsApi(config);
ChartTitleResponse response = api.getWorksheetChartTitle("Book1.xlsx", "Sheet1", 0, "", "");
System.out.println(response.getTitle().getText());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
// PHP 예제: Aspose.Cells Cloud SDK 사용
$config = new Aspose\Cells\Configuration();
$config->setAccessToken('<jwt 토큰>');
$config->setHost('https://api.aspose.cloud');
$apiInstance = new Aspose\Cells\Api\ChartsApi($config);
$response = $apiInstance->getWorksheetChartTitle('Book1.xlsx', 'Sheet1', 0, '', '');
echo $response->getTitle()->getText();
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# Ruby 예제: Aspose.Cells Cloud SDK 사용
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.access_token = '<jwt 토큰>'
config.host = 'https://api.aspose.cloud'

api_instance = AsposeCellsCloud::ChartsApi.new
result = api_instance.get_worksheet_chart_title('Book1.xlsx', 'Sheet1', 0, '', '')
puts result.title.text
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
# Python 예제: Aspose.Cells Cloud SDK 사용
from asposecellscloud import ChartsApi, Configuration

config = Configuration()
config.access_token = "<jwt 토큰>"
config.host = "https://api.aspose.cloud"

api_instance = ChartsApi(config)
response = api_instance.get_worksheet_chart_title("Book1.xlsx", "Sheet1", 0, "", "")
print(response.title.text)
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```javascript
// Node.js 예제: Aspose.Cells Cloud SDK 사용
const { ChartsApi, Configuration } = require('asposecellscloud');

let config = new Configuration();
config.accessToken = "<jwt 토큰>";
config.basePath = "https://api.aspose.cloud";

let apiInstance = new ChartsApi(config);
apiInstance.getWorksheetChartTitle("Book1.xlsx", "Sheet1", 0, "", "", (error, data) => {
    if (error) console.error(error);
    else console.log(data.title.text);
});
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```java
// Android(Java) 예제: Aspose.Cells Cloud SDK 사용
Configuration config = new Configuration();
config.setAccessToken("<jwt 토큰>");
config.setBasePath("https://api.aspose.cloud");
ChartsApi api = new ChartsApi(config);
ChartTitleResponse response = api.getWorksheetChartTitle("Book1.xlsx", "Sheet1", 0, "", "");
Log.d("ChartTitle", response.getTitle().getText());
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```swift
// Swift 예제: Aspose.Cells Cloud SDK 사용
import AsposeCellsCloud

let config = Configuration()
config.accessToken = "<jwt 토큰>"
config.host = "https://api.aspose.cloud"

let api = ChartsApi(configuration: config)
api.getWorksheetChartTitle(name: "Book1.xlsx", sheetName: "Sheet1", chartIndex: 0, folder: "", storageName: "") { result, error in
    if let title = result?.title?.text {
        print("차트 제목: \(title)")
    }
}
```

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
# Perl 예제: Aspose.Cells Cloud SDK 사용
use AsposeCellsCloud::ChartsApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new();
$config->{access_token} = '<jwt 토큰>';
$config->{host} = 'https://api.aspose.cloud';

my $api_instance = AsposeCellsCloud::ChartsApi->new($config);
my $result = $api_instance->get_worksheet_chart_title('Book1.xlsx', 'Sheet1', 0, '', '');
print $result->{title}{text}, "\n";
```

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "e1b22ed45ca780faa3231c3a8c60ddd4" >}}

{{< /tab >}}

{{< /tabs >}}

차트 제목을 업데이트하거나 삭제하는 것과 같은 보다 고급 시나리오에 대해서는 각 SDK의 문서를 참조할 수도 있습니다.

**참고 자료**: [차트 제목 업데이트](/charts/title/put/), [차트 제목 삭제](/charts/title/delete/).