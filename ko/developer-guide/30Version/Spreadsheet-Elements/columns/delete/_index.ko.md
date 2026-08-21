---
title: "Aspose.Cells Cloud API를 사용하여 Excel 워크시트에서 열 삭제하기"
description: "Aspose.Cells Cloud REST API를 통해 Excel 워크시트에서 하나 이상의 열을 삭제하는 방법을 배워보세요. 인증, 요청 구문, 매개변수, 응답, 오류 처리, SDK 예제가 포함됩니다."
keywords: ["Aspose.Cells", "열 삭제", "Excel API", "REST", "클라우드", "워크시트", "열"]
date: 2026-07-30
api_version: "v3.0"
---

# Excel 워크시트에서 열 삭제하기

**엔드포인트**: `DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}`  

이 작업은 워크시트에서 단일 열 또는 열 범위를 제거합니다. 열 삭제 후 셀 참조(수식 포함)를 자동으로 업데이트할 수 있습니다.

---

## 목차
1. [필수 조건](#필수-조건)  
2. [인증](#인증)  
3. [요청 URL 및 HTTP 메서드](#요청-url-및-http-메서드)  
4. [매개변수](#매개변수)  
   - [경로 매개변수](#경로-매개변수)  
   - [쿼리 매개변수](#쿼리-매개변수)  
5. [cURL 예제](#curl-예제)  
6. [응답](#응답)  
7. [오류 코드](#오류-코드)  
8. [SDK 샘플](#sdk-샘플)  
9. [추가 참고 사항](#추가-참고-사항)  

---

## 필수 조건
- Aspose Cloud 인증 플로우를 통해 얻은 유효한 **JWT 액세스 토큰**.  
- 워크북(`{name}`)은 이미 Aspose Cloud 스토리지에 업로드되었거나(`folder`/`storageName` 쿼리 매개변수를 통해 접근 가능해야 함).

---

## 인증
모든 Aspose.Cells Cloud 요청은 **Bearer 토큰** 인증이 필요합니다.

```http
Authorization: Bearer <access_token>
```

JWT 토큰 획득 방법에 대한 자세한 내용은 [인증 가이드](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)를 참조하세요.

---

## 요청 URL 및 HTTP 메서드
```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}
```

- **`{name}`** – 워크북 파일 이름(예: `test.xlsx`).  
- **`{sheetName}`** – 워크시트 이름(예: `Sheet1`).  
- **`{columnIndex}`** – 삭제할 첫 번째 열의 0부터 시작하는 인덱스.

---

## 매개변수

| 이름               | 위치   | 유형     | 필수 여부 | 설명 |
|--------------------|--------|----------|-----------|------|
| **name**           | path   | string   | ✅ 예      | 워크북 파일 이름. |
| **sheetName**      | path   | string   | ✅ 예      | 워크시트 이름. |
| **columnIndex**    | path   | integer  | ✅ 예      | 삭제할 첫 번째 열의 0부터 시작하는 인덱스. |
| **startColumn**    | query  | integer  | ❌ 아니요  | 삭제를 시작할 0부터 시작하는 인덱스. 생략 시 `columnIndex`로 기본 설정됨. |
| **totalColumns**   | query  | integer  | ❌ 아니요  | 삭제할 열의 수. 생략 시 `columnIndex`로 지정된 열만 삭제됨. |
| **updateReference**| query  | boolean  | ❌ 아니요  | `true`인 경우, 삭제 후 워크북 전체에서 셀 참조(수식 포함)를 업데이트함. |
| **folder**         | query  | string   | ❌ 아니요  | 워크북이 포함된 폴더 경로. |
| **storageName**    | query  | string   | ❌ 아니요  | Aspose Cloud 스토리지 서비스 이름. |

> **참고** – 저수준 API 사양에 표시된 `columns` 매개변수는 더 표현력 있는 `startColumn` 및 `totalColumns` 쿼리 매개변수로 대체되었습니다. 후속 호환성을 위해 두 방식 모두 허용됩니다.

---

## cURL 예제

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/1?startColumn=1&totalColumns=1&updateReference=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

### 설명
- `test.xlsx`의 `Sheet1`에서 열 **B**(`columnIndex = 1`)를 삭제합니다.  
- `startColumn=1` 및 `totalColumns=1`은 단일 열 삭제를 지정합니다.  
- `updateReference=true`는 수식 및 기타 참조가 자동으로 조정되도록 보장합니다.

---

## 응답

| HTTP 코드 | 설명 | 예시 |
|-----------|------|------|
| **200** | 성공 – 열이 삭제됨. | `{ "Code": 200, "Status": "OK" }` |
| **400** | 잘못된 요청 – 누락되거나 유효하지 않은 매개변수. | `{ "Code": 400, "Message": "Invalid totalColumns value." }` |
| **401** | 인증 실패 – 누락되거나 유효하지 않은 JWT 토큰. | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404** | 없음 – 워크북 또는 워크시트가 존재하지 않음. | `{ "Code": 404, "Message": "Worksheet 'Sheet1' not found." }` |
| **500** | 내부 서버 오류 – 서버에서 예기치 않은 조건 발생. | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

응답 본문은 일반적인 **`CellsCloudResponse`** 모델을 따릅니다.

---

**HTTP 상태 코드**

| 코드 | 의미                         | 설명                                             |
|------|------------------------------|--------------------------------------------------|
| 200  | OK                           | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함. |
| 400  | Bad Request                  | 누락되거나 유효하지 않은 매개변수(예: 지원되지 않는 파일 유형). |
| 401  | Unauthorized                 | 유효하지 않거나 누락된 JWT 토큰. |
| 413  | Payload Too Large            | 업로드된 파일이 크기 제한을 초과함. |
| 500  | Internal Server Error        | 예기치 않은 서버 오류. |
---

## SDK 샘플

아래는 가장 인기 있는 SDK에 대한 실행 가능한 스니펫입니다. 플레이스홀더 값(`<YOUR_ACCESS_TOKEN>`, `<WORKBOOK>` 등)을 고유한 데이터로 대체하세요.

| 언어 | 샘플 |
|------|------|
| **C#** | <details><summary>코드 보기</summary> <br>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\nusing System;\n\nvar config = new Configuration { AccessToken = "<YOUR_ACCESS_TOKEN>", BaseUrl = "https://api.aspose.cloud" };\nvar api = new CellsApi(config);\n\nvar response = api.DeleteWorksheetColumns(name: "test.xlsx",\n                                         sheetName: "Sheet1",\n                                         columnIndex: 1,\n                                         startColumn: 1,\n                                         totalColumns: 1,\n                                         updateReference: true);\nConsole.WriteLine($"Status: {response.Status}");\n```</details> |
| **Java** | <details><summary>코드 보기</summary> <br>```java\nimport com.aspose.cloud.cells.api.CellsApi;\nimport com.aspose.cloud.cells.model.CellsCloudResponse;\nimport com.aspose.cloud.cells.Configuration;\n\nConfiguration config = new Configuration();\nconfig.setAccessToken("<YOUR_ACCESS_TOKEN>");\nconfig.setBaseUrl("https://api.aspose.cloud");\nCellsApi api = new CellsApi(config);\n\nCellsCloudResponse resp = api.deleteWorksheetColumns("test.xlsx", "Sheet1", 1, 1, 1, true, null, null);\nSystem.out.println("Status: " + resp.getStatus());\n```</details> |
| **Python** | <details><summary>코드 보기</summary> <br>```python\nimport asposecellscloud\nfrom asposecellscloud.rest import ApiException\n\nconfig = asposecellscloud.Configuration()\nconfig.access_token = '<YOUR_ACCESS_TOKEN>'\nconfig.host = 'https://api.aspose.cloud'\napi_instance = asposecellscloud.CellsApi(asposecellscloud.ApiClient(config))\n\ntry:\n    resp = api_instance.delete_worksheet_columns(name='test.xlsx',\n                                                 sheet_name='Sheet1',\n                                                 column_index=1,\n                                                 start_column=1,\n                                                 total_columns=1,\n                                                 update_reference=True)\n    print('Status:', resp.status)\nexcept ApiException as e:\n    print('Exception when calling CellsApi->delete_worksheet_columns:', e)\n```</details> |
| **Node.js** | <details><summary>코드 보기</summary> <br>```javascript\nconst { CellsApi, Configuration } = require('asposecellscloud');\n\nlet config = new Configuration({\n    accessToken: '<YOUR_ACCESS_TOKEN>',\n    basePath: 'https://api.aspose.cloud'\n});\nlet api = new CellsApi(config);\n\napi.deleteWorksheetColumns('test.xlsx', 'Sheet1', 1, {\n    startColumn: 1,\n    totalColumns: 1,\n    updateReference: true\n}).then(res => {\n    console.log('Status:', res.status);\n}).catch(err => {\n    console.error(err);\n});\n```</details> |
| **Go** | <details><summary>코드 보기</summary> <br>```go\npackage main\n\nimport (\n    \"context\"\n    \"fmt\"\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3\"\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3/api\"\n)\n\nfunc main() {\n    cfg := asposecellscloud.NewConfiguration()\n    cfg.AccessToken = \"<YOUR_ACCESS_TOKEN>\"\n    cfg.BasePath = \"https://api.aspose.cloud\"\n    client := api.NewAPIClient(cfg)\n    resp, _, err := client.CellsApi.DeleteWorksheetColumns(context.Background(), \"test.xlsx\", \"Sheet1\", 1,\n        &api.DeleteWorksheetColumnsOpts{StartColumn: optional.NewInt32(1), TotalColumns: optional.NewInt32(1), UpdateReference: optional.NewBool(true)})\n    if err != nil {\n        fmt.Println(\"Error:\", err)\n        return\n    }\n    fmt.Println(\"Status:\", resp.Status)\n}\n```</details> |
| **Ruby** | <details><summary>코드 보기</summary> <br>```ruby\nrequire 'aspose_cells_cloud'\n\nconfig = AsposeCellsCloud::Configuration.new do |c|\n  c.access_token = '<YOUR_ACCESS_TOKEN>'\n  c.host = 'https://api.aspose.cloud'\nend\napi = AsposeCellsCloud::CellsApi.new\n\nbegin\n  resp = api.delete_worksheet_columns('test.xlsx', 'Sheet1', 1,\n    start_column: 1,\n    total_columns: 1,\n    update_reference: true)\n  puts \"Status: #{resp.status}\"\nrescue AsposeCellsCloud::ApiError => e\n  puts \"Exception: #{e}\"\nend\n```</details> |
| **PHP** | <details><summary>코드 보기</summary> <br>```php\n<?php\nrequire_once('vendor/autoload.php');\nuse Aspose\\Cells\\Cloud\\Api\\CellsApi;\nuse Aspose\\Cells\\Cloud\\Configuration;\n\n$config = new Configuration();\n$config->setAccessToken('<YOUR_ACCESS_TOKEN>');\n$config->setHost('https://api.aspose.cloud');\n$apiInstance = new CellsApi($config);\n\ntry {\n    $result = $apiInstance->deleteWorksheetColumns('test.xlsx', 'Sheet1', 1, [\n        'startColumn' => 1,\n        'totalColumns' => 1,\n        'updateReference' => true\n    ]);\n    echo \"Status: \" . $result->getStatus();\n} catch (Exception $e) {\n    echo 'Exception when calling CellsApi->deleteWorksheetColumns: ', $e->getMessage();\n}\n?>\n```</details> |
| **Perl** | <details><summary>코드 보기</summary> <br>```perl\n#!/usr/bin/perl\nuse strict;\nuse warnings;\nuse AsposeCellsCloud::Api::CellsApi;\nuse AsposeCellsCloud::Configuration;\n\nmy $config = AsposeCellsCloud::Configuration->new(\n    access_token => '<YOUR_ACCESS_TOKEN>',\n    host => 'https://api.aspose.cloud'\n);\nmy $api = AsposeCellsCloud::Api::CellsApi->new($config);\n\nmy $response = $api->delete_worksheet_columns(\n    name => 'test.xlsx',\n    sheet_name => 'Sheet1',\n    column_index => 1,\n    start_column => 1,\n    total_columns => 1,\n    update_reference => JSON::true\n);\nprint \"Status: \", $response->{Status}, \"\\n\";\n```</details> |

*모든 SDK는 `access_token`이 설정되면 자동으로 필요한 `Authorization` 헤더를 추가합니다.*

---

## 추가 참고 사항

### 보안 헤더(프로덕션 환경 권장)
문서 페이지를 제공할 때 보안을 강화하기 위해 다음 HTTP 응답 헤더를 포함하세요:

```
Content-Security-Policy: default-src 'self'; script-src 'self' https://www.googletagmanager.com https://menu-new.containerize.com; style-src 'self' 'unsafe-inline'; img-src 'self' data:;
X-Content-Type-Options: nosniff
X-Frame-Options: SAMEORIGIN
Referrer-Policy: strict-origin-when-cross-origin
```

### 성능 팁
- 타사 분석 스크립트(`gtag.js`, `containerize.js`)는 `async` 속성으로 로드하거나 페이지 렌더링 후 지연 로드하세요.  
- 사용자 지정 JavaScript/CSS 번들을 압축하세요.  
- 렌더링 차단되는 작은 SVG 아이콘은 사전 로드하세요:

```html
<link rel="preload" href="/cells/icons/caret-down.svg" as="image" type="image/svg+xml">
```

### SEO 개선(JSON‑LD)

```json
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Delete Column from Excel Worksheet using Aspose.Cells Cloud API",
  "description": "Learn how to delete one or more columns from an Excel worksheet via Aspose.Cells Cloud REST API.",
  "author": { "@type": "Organization", "name": "Aspose" },
  "datePublished": "2023-01-01",
  "url": "https://docs.aspose.cloud/cells/columns/delete/",
  "keywords": ["Aspose.Cells", "Delete Column", "Excel", "REST API"]
}
```

HTML 헤드에 `<script type="application/ld+json">` 블록으로 스니펫을 배치하세요.

### 접근성
- 장식용 이미지는 모두 `alt=""`를 사용하거나 `aria-hidden="true"`로 숨김 처리됨.  
- Open Graph 이미지 메타 태그에 완전성을 위해 `alt` 속성이 추가됨.

---

## 참고 자료
- [DeleteWorksheetColumns OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Cells/DeleteWorksheetColumns)  
- [인증 개요](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- [GitHub의 Aspose.Cells Cloud SDK](https://github.com/aspose-cells-cloud)  

---
---