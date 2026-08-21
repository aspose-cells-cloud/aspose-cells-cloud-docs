---
title: "차트 두 번째 값 축 업데이트"
ArticleTitle: "차트 두 번째 값 축 업데이트 – Aspose.Cells Cloud REST API"
type: docs
url: /charts/second-value-axis/update/
weight: 160
keywords: "Aspose.Cells, 차트 API, 두 번째 값 축, Excel, REST, 클라우드 SDK"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트의 차트 두 번째 값 축을 업데이트합니다. 요청 예시, 응답 코드 및 사전 조건이 포함됩니다."
---

이 REST API는 차트의 두 번째 값 축을 업데이트합니다.

**사전 조건:**  
- 유효한 JWT 액세스 토큰 (자세한 내용은 [인증 가이드](https://docs.aspose.cloud/cells/authentication/) 참조).  
- 대상 Excel 파일은 Aspose Cloud 스토리지에 저장되어 있어야 합니다(`folder` 및 선택적 `storageName` 제공).  
- API 버전 v3.0을 사용하며, 기본 URL은 `https://api.aspose.cloud/v3.0`이어야 합니다.

## PostChartSecondValueAxis API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondvalueaxis
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 위해 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름 | 유형    | 위치 | 설명                                              |
| ------------- | ------- | ---- | ------------------------------------------------- |
| name          | string  | path | Excel 파일 이름입니다.                            |
| sheetName     | string  | path | 차트가 포함된 워크시트 이름입니다.                |
| chartIndex    | integer | path | 수정할 차트의 0부터 시작하는 인덱스입니다.        |
| axis          | object  | body | 두 번째 값 축의 설정입니다.                       |
| folder        | string  | query| 파일이 위치한 스토리지 내 폴더 경로입니다.        |
| storageName   | string  | query| 스토리지 서비스 이름입니다.                       |

**요청 본문 예시(JSON):**

```json
{
  "IsAutomaticMajorUnit": true,
  "Maximum": 100,
  "Minimum": 0,
  "MajorUnit": 10,
  "MinorUnit": 2,
  "Title": {
    "Text": "보조 축"
  }
}
```

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Charts/PostChartSecondValueAxis)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예시는 cURL을 사용하여 클라우드 API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondvalueaxis" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**HTTP 상태 코드**

| 코드 | 의미                    | 설명                                             |
|------|-------------------------|--------------------------------------------------|
| 200  | OK                      | 필터가 성공적으로 적용됨; 응답에는 작업 세부정보가 포함됨. |
| 400  | Bad Request             | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식). |
| 401  | Unauthorized            | 잘못되거나 누락된 JWT 토큰.                         |
| 413  | Payload Too Large       | 업로드된 파일이 크기 제한을 초과함.                 |
| 500  | Internal Server Error   | 예기치 않은 서버 오류.                              |

**참고:**  
- [차트 두 번째 값 축 가져오기](https://docs.aspose.cloud/cells/charts/second-value-axis/get/)  
- [차트 값 축 업데이트](https://docs.aspose.cloud/cells/charts/value-axis/update/)

## 클라우드 SDK Family

SDK를 사용하는 것이 개발 속도를 높이는 가장 좋은 방법입니다. SDK는 저수준 세부 사항을 처리해주므로, 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하시기 바랍니다.

다음 코드 예시는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 요청을 보내는 방법을 보여줍니다:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// C# 예시: 두 번째 값 축 업데이트
var api = new CellsApi("clientId", "clientSecret");
var axis = new Axis { IsAutomaticMajorUnit = true, Maximum = 100 };
api.PostChartSecondValueAxis(name, sheetName, chartIndex, axis);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Java 예시: 두 번째 값 축 업데이트
CellsApi api = new CellsApi("clientId", "clientSecret");
Axis axis = new Axis();
axis.setIsAutomaticMajorUnit(true);
axis.setMaximum(100.0);
api.postChartSecondValueAxis(name, sheetName, chartIndex, axis);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
// PHP 예시: 두 번째 값 축 업데이트
$api = new CellsApi($clientId, $clientSecret);
$axis = new Axis();
$axis->setIsAutomaticMajorUnit(true);
$axis->setMaximum(100);
$api->postChartSecondValueAxis($name, $sheetName, $chartIndex, $axis);
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# Ruby 예시: 두 번째 값 축 업데이트
api = AsposeCellsCloud::ApiClient.new(client_id, client_secret)
axis = Axis.new(is_automatic_major_unit: true, maximum: 100)
api.post_chart_second_value_axis(name, sheet_name, chart_index, axis)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
# Python 예시: 두 번째 값 축 업데이트
api = asposecellscloud.ApiClient(client_id, client_secret)
axis = Axis(is_automatic_major_unit=True, maximum=100)
api.post_chart_second_value_axis(name, sheet_name, chart_index, axis)
```

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Post-ChartSecondValueAxis.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

```java
// Android(Java) 예시 – 위 Java 코드 예시와 동일합니다.
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```swift
// Swift 예시: 두 번째 값 축 업데이트
let api = CellsApi(clientId: "clientId", clientSecret: "clientSecret")
var axis = Axis()
axis.isAutomaticMajorUnit = true
axis.maximum = 100
api.postChartSecondValueAxis(name: name, sheetName: sheetName, chartIndex: chartIndex, axis: axis)
```

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
# Perl 예시: 두 번째 값 축 업데이트
my $api = AsposeCellsCloud::ApiClient->new(client_id => $client_id, client_secret => $client_secret);
my $axis = AsposeCellsCloud::Object::Axis->new(isAutomaticMajorUnit => 1, maximum => 100);
$api->post_chart_second_value_axis(name => $name, sheet_name => $sheet_name, chart_index => $chart_index, axis => $axis);
```

{{< /tab >}}

{{< tab tabNum="10" >}}

```go
// Go 예시: 두 번째 값 축 업데이트
api := cells.NewApiClient("clientId", "clientSecret")
axis := cells.Axis{IsAutomaticMajorUnit: true, Maximum: 100}
api.PostChartSecondValueAxis(name, sheetName, chartIndex, axis)
```

{{< /tab >}}

{{< /tabs >}}