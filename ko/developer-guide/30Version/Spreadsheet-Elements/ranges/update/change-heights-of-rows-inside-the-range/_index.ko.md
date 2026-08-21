---
title: "Excel에서 범위의 행 높이 설정 – Aspose.Cells Cloud API (v3.0)"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트 내 특정 범위의 행 높이를 변경합니다. 엔드포인트, 파라미터, cURL 예제, 샘플 응답, 여러 언어의 SDK 스니펫이 포함됩니다."
keywords: "Aspose.Cells, 행 높이, 범위, Excel, REST API, v3.0, SDK, cURL"
date: 2026-07-30
type: docs
weight: 76
aliases:
  - /change-heights-of-rows-inside-the-range/
---

# Excel에서 범위의 행 높이 설정

이 작업은 Aspose Cloud 스토리지에 저장된 워크시트의 지정된 범위에 대해 행 높이를 업데이트합니다.

## 사전 요구 사항 / 인증

**Cells.ReadWrite** 범위(scope)로 Aspose Cloud OAuth 서비스에서 JWT 액세스 토큰을 받아야 합니다.

각 요청의 `Authorization` 헤더에 토큰을 포함하세요:

```http
Authorization: Bearer <jwt token>
```

토큰이 없으면 **Aspose Cloud 인증 가이드**에 따라 요청하세요.

## HTTP 요청

| 메서드 | URI |
|--------|-----|
| **POST** | `https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/rowHeight` |

### 경로 파라미터

| 이름 | 유형 | 설명 |
|------|------|-------------|
| `name` | `string` | **필수.** 클라우드에 저장된 Excel 파일의 이름입니다. |
| `sheetName` | `string` | **필수.** 대상 범위를 포함하는 워크시트 이름입니다. |

### 쿼리 파라미터

| 이름 | 유형 | 필수 여부 | 설명 |
|------|------|----------|-------------|
| `value` | `number` | **예** | 범위에 적용할 원하는 행 높이(포인트 단위)입니다. |
| `folder` | `string` | 아니요 | 파일이 위치한 스토리지 내 폴더 경로입니다. |
| `storageName` | `string` | 아니요 | 스토리지 서비스 이름(여러 스토리지가 구성된 경우). |

### 요청 본문 (JSON)

본문에는 영향을 받는 행을 정의하는 **Range** 객체가 포함되어야 합니다.

```json
{
  "FirstRow": 0,
  "RowCount": 1,
  "FirstColumn": 0,
  "ColumnCount": 0
}
```

#### Range JSON 스키마

| 속성 | 유형 | 필수 여부 | 설명 |
|------|------|----------|-------------|
| `FirstRow` | integer | **예** | 범위 내 첫 번째 행의 0부터 시작하는 인덱스입니다. |
| `RowCount` | integer | **예** | 높이가 적용될 행의 개수입니다. |
| `FirstColumn` | integer | 아니요 | 첫 번째 열의 0부터 시작하는 인덱스(행 높이 설정 시 선택 사항). |
| `ColumnCount` | integer | 아니요 | 범위가 차지하는 열의 개수(선택 사항). |

행 높이 작업에 사용되는 속성은 위에 나열된 것만 있으며, 추가 필드는 무시됩니다.

## 샘플 요청

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/rowHeight?value=15&folder=Documents&storageName=MyStorage" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "FirstRow": 9,
        "RowCount": 1
      }'
```

### 샘플 응답 (성공)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**HTTP 상태 코드**

| 코드 | 의미                     | 설명                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함. |
| 400  | Bad Request                 | 누락되거나 잘못된 파라미터(예: 지원되지 않는 파일 유형). |
| 401  | Unauthorized                | 잘못되거나 누락된 JWT 토큰. |
| 413  | Payload Too Large           | 업로드된 파일이 크기 제한을 초과함. |
| 500  | Internal Server Error       | 예기치 않은 서버 오류. |

모든 응답은 숫자형 `Code`와 사람이 읽을 수 있는 `Status`(또는 오류 발생 시 `Message`)를 포함합니다. 오류 발생 시 추가로 `ErrorDetails`가 제공될 수 있습니다.

## SDK 예제

다음 스니펫은 공식 Aspose.Cells Cloud SDK를 사용하여 **범위의 행 높이 설정**을 호출하는 방법을 보여줍니다.

| 언어 | 예제 |
|------|------|
| **C#** | <details><summary>코드 보기</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar api = new RangesApi(configuration);\nvar range = new Range { FirstRow = 9, RowCount = 1 };\nawait api.PostWorksheetCellsRangeRowHeightAsync("test.xlsx", "Sheet1", range, 15);\n```</details> |
| **Java** | <details><summary>코드 보기</summary>```java\nimport com.aspose.cloud.cells.api.RangesApi;\nimport com.aspose.cloud.cells.model.Range;\n\nRangesApi api = new RangesApi(config);\nRange range = new Range().firstRow(9).rowCount(1);\napi.postWorksheetCellsRangeRowHeight("test.xlsx", "Sheet1", range, 15.0, null, null);\n```</details> |
| **Python** | <details><summary>코드 보기</summary>```python\nfrom asposecellscloud import RangesApi, ApiClient, Configuration\n\nconfig = Configuration()\nconfig.access_token = '<jwt token>'\napi = RangesApi(ApiClient(config))\nrange = {'FirstRow': 9, 'RowCount': 1}\napi.post_worksheet_cells_range_row_height('test.xlsx', 'Sheet1', range, value=15)\n```</details> |
| **Node.js** | <details><summary>코드 보기</summary>```javascript\nconst { RangesApi, Configuration } = require('asposecellscloud');\nconst config = new Configuration();\nconfig.accessToken = '<jwt token>';\nconst api = new RangesApi(config);\nconst range = { FirstRow: 9, RowCount: 1 };\napi.postWorksheetCellsRangeRowHeight('test.xlsx', 'Sheet1', range, 15)\n  .then(() => console.log('Row height set'))\n  .catch(err => console.error(err));\n```</details> |
| **PHP** | <details><summary>코드 보기</summary>```php\nuse Aspose\Cells\Configuration;\nuse Aspose\Cells\Api\RangesApi;\n\n$config = new Configuration();\n$config->setAccessToken('<jwt token>');\n$api = new RangesApi($config);\n$range = ['FirstRow' => 9, 'RowCount' => 1];\n$api->postWorksheetCellsRangeRowHeight('test.xlsx', 'Sheet1', $range, 15);\n```</details> |
| **Ruby** | <details><summary>코드 보기</summary>```ruby\nrequire 'aspose_cells_cloud'\nconfig = AsposeCellsCloud::Configuration.new\nconfig.access_token = '<jwt token>'\napi = AsposeCellsCloud::RangesApi.new\nrange = { 'FirstRow' => 9, 'RowCount' => 1 }\napi.post_worksheet_cells_range_row_height('test.xlsx', 'Sheet1', range, value: 15)\n```</details> |
| **Go** | <details><summary>코드 보기</summary>```go\nimport (\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3\"\n    \"context\"\n)\n\ncfg := asposecellscloud.NewConfiguration()\ncfg.AccessToken = \"<jwt token>\"\napi := asposecellscloud.NewRangesApi(cfg)\nrangeBody := map[string]interface{}{ \"FirstRow\": 9, \"RowCount\": 1 }\n_, err := api.PostWorksheetCellsRangeRowHeight(context.Background(), \"test.xlsx\", \"Sheet1\", rangeBody, 15, nil, nil)\nif err != nil { panic(err) }\n```</details> |
| **Perl** | <details><summary>코드 보기</summary>```perl\nuse AsposeCellsCloud::Api::RangesApi;\nmy $api = AsposeCellsCloud::Api::RangesApi->new({ access_token => '<jwt token>' });\nmy $range = { FirstRow => 9, RowCount => 1 };\n$api->post_worksheet_cells_range_row_height('test.xlsx', 'Sheet1', $range, 15);\n```</details> |

> **참고:** SDK는 액세스 토큰이 구성된 경우 자동으로 필요한 `Authorization: Bearer` 헤더를 추가합니다.

## 참조

- **OpenAPI 사양** – 이 작업의 상세 계약서: <https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeRowHeight>
- **Aspose.Cells Cloud SDK 저장소** – 소스 코드 및 추가 언어 바인딩: <https://github.com/aspose-cells-cloud>
- **인증 가이드** – JWT 토큰 획득 방법: <https://docs.aspose.cloud/cells/authentication/>