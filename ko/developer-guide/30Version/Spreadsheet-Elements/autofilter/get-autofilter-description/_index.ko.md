---
---
title: "AutoFilter 가져오기"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트에서 AutoFilter 설명을 검색합니다."
keywords: "AutoFilter, Excel, Aspose.Cells Cloud, REST API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
type: docs
url: /cells/autofilter/get/
aliases:
  - /get-autofilter-description/
weight: 50
---

# 워크시트에서 AutoFilter 설명 검색하기

**버전:** v3.0  
**엔드포인트:** `GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter`

> **참고:** 모든 샘플 요청은 **HTTPS**를 사용합니다. JWT 토큰을 안전하지 않은 연결을 통해 전송하지 마십시오.

---

## 개요

**AutoFilter**를 사용하면 사용자가 열 값, 색상, 사용자 정의 기준 등을 기준으로 워크시트의 행을 필터링할 수 있습니다. 이 API는 필터 열, 범위, 정렬 세부 정보 등을 포함한 전체 AutoFilter 구성을 반환하여 프로그래밍 방식으로 필터 설정을 검사하거나 복제할 수 있도록 합니다.

---

## 사전 요구 사항

| 요구 사항 | 설명 |
|-----------|------|
| **인증** | 유효한 JWT 토큰이 필요합니다. [인증 가이드](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)를 참조하십시오. |
| **파일 위치** | 워크북은 Aspose Cloud 스토리지(또는 연결된 외부 스토리지)에 저장되어야 합니다. |
| **지원되는 형식** | Aspose.Cells에서 지원하는 모든 Excel 형식(예: `.xlsx`, `.xls`, `.xlsm`). |
| **SDK (옵션)** | SDK를 사용하려면 적절한 패키지를 설치하십시오(예: .NET의 경우 `dotnet add package Aspose.Cells-Cloud`). |

---

## 요청

### HTTP 요청

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter
```

### 경로 매개변수

| 매개변수 | 유형   | 설명 |
|---------|--------|------|
| `name`      | string | **필수.** 확장자를 포함한 워크북 파일 이름. |
| `sheetName` | string | **필수.** AutoFilter를 검색할 워크시트 이름. |

### 쿼리 매개변수

| 매개변수      | 유형   | 설명 |
|--------------|--------|------|
| `folder`      | string | 워크북이 위치한 스토리지 내 폴더 경로. |
| `storageName` | string | 사용할 스토리지 이름. |

### 보안

이 API는 **JWT 토큰 기반 인증**을 사용합니다. `Authorization` 헤더에 토큰을 포함하십시오:

```http
Authorization: Bearer <your_jwt_token>
```

---

## 요청 예시(cURL)

```bash
curl "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter?folder=MyFolder&storageName=MyStorage" \
  -X GET \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>"
```

---

## 응답

서비스는 `AutoFilter` 모델을 래핑하는 JSON 객체를 반환합니다.

### 성공 응답 스키마

```json
{
  "Status": "OK",
  "Code": 200,
  "AutoFilter": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "FilterColumns": [
      {
        "FieldIndex": 0,
        "FilterType": "string",
        "MultipleFilters": {
          "MatchBlank": true,
          "MultipleFilterList": [
            {}
          ]
        },
        "ColorFilter": {
          "FilterByFillColor": "string",
          "Pattern": "string",
          "Color": {
            "Color": { "A": 0, "R": 0, "G": 0, "B": 0 },
            "ColorIndex": 0,
            "IsShapeColor": true,
            "ThemeColor": { "ColorType": "string", "Tint": 0 },
            "Type": "string"
          },
          "ForegroundColorColor": {
            "Color": { "A": 0, "R": 0, "G": 0, "B": 0 },
            "ColorIndex": 0,
            "IsShapeColor": true,
            "ThemeColor": { "ColorType": "string", "Tint": 0 },
            "Type": "string"
          },
          "BackgroundColor": {
            "Color": { "A": 0, "R": 0, "G": 0, "B": 0 },
            "ColorIndex": 0,
            "IsShapeColor": true,
            "ThemeColor": { "ColorType": "string", "Tint": 0 },
            "Type": "string"
          }
        },
        "CustomFilters": [
          { "FilterOperatorType": "string" }
        ],
        "DynamicFilter": { "DynamicFilterType": "string" },
        "IconFilter": { "IconId": 0, "IconSetType": "string" },
        "Top10Filter": {
          "Criteria": "string",
          "IsPercent": true,
          "IsTop": true,
          "Items": 0
        },
        "Visibledropdown": "string"
      }
    ],
    "Range": "string",
    "Sorter": {
      "CaseSensitive": true,
      "HasHeaders": true,
      "KeyList": [
        { "Key": 0, "SortOrder": "string", "CustomList": "string" }
      ],
      "SortLeftToRight": true
    }
  }
}
```

### 응답 예시

```json
{
  "Status": "OK",
  "Code": 200,
  "AutoFilter": {
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter",
      "Rel": "self",
      "Title": "AutoFilter",
      "Type": "application/json"
    },
    "FilterColumns": [
      {
        "FieldIndex": 1,
        "FilterType": "Custom",
        "MultipleFilters": {
          "MatchBlank": false,
          "MultipleFilterList": [
            {
              "Operator": "Equals",
              "Criteria": "Approved"
            }
          ]
        },
        "ColorFilter": null,
        "CustomFilters": [],
        "DynamicFilter": null,
        "IconFilter": null,
        "Top10Filter": null,
        "Visibledropdown": "true"
      }
    ],
    "Range": "A1:C100",
    "Sorter": {
      "CaseSensitive": false,
      "HasHeaders": true,
      "KeyList": [
        {
          "Key": 1,
          "SortOrder": "Ascending",
          "CustomList": null
        }
      ],
      "SortLeftToRight": false
    }
  }
}
```

---

**HTTP 상태 코드**

| 코드 | 의미                         | 설명                                              |
|------|------------------------------|---------------------------------------------------|
| 200  | OK                           | 필터가 성공적으로 적용됨; 응답에는 작업 세부 정보가 포함됨. |
| 400  | Bad Request                  | 누락되었거나 잘못된 매개변수(예: 지원되지 않는 파일 형식). |
| 401  | Unauthorized                 | 잘못되었거나 누락된 JWT 토큰. |
| 413  | Payload Too Large            | 업로드된 파일이 크기 제한을 초과함. |
| 500  | Internal Server Error        | 예기치 않은 서버 오류. |
---

## SDK 예제

이 작업은 모든 Aspose.Cells Cloud SDK에서 사용할 수 있습니다. 아래는 실행 가능한 스니펫입니다.

| 언어 | 예제 |
|------|------|
| **C#** | <details><summary>코드 보기</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar apiInstance = new CellsApi();\nvar response = apiInstance.GetWorksheetAutoFilter(\"Book1.xlsx\", \"Sheet1\", folder: \"MyFolder\", storageName: \"MyStorage\");\nConsole.WriteLine(response.AutoFilter);\n```</details> |
| **Java** | <details><summary>코드 보기</summary>```java\nimport com.aspose.cells.cloud.api.CellsApi;\nimport com.aspose.cells.cloud.model.AutoFilterResponse;\n\nCellsApi api = new CellsApi();\nAutoFilterResponse resp = api.getWorksheetAutoFilter(\"Book1.xlsx\", \"Sheet1\", \"MyFolder\", \"MyStorage\");\nSystem.out.println(resp.getAutoFilter());\n```</details> |
| **Python** | <details><summary>코드 보기</summary>```python\nfrom asposecellscloud import CellsApi\n\napi = CellsApi()\nresp = api.get_worksheet_auto_filter(name='Book1.xlsx', sheet_name='Sheet1', folder='MyFolder', storage_name='MyStorage')\nprint(resp.auto_filter)\n```</details> |
| **Node.js** | <details><summary>코드 보기</summary>```javascript\nconst { CellsApi } = require('asposecellscloud');\nconst api = new CellsApi();\napi.getWorksheetAutoFilter('Book1.xlsx', 'Sheet1', { folder: 'MyFolder', storageName: 'MyStorage' })\n  .then(resp => console.log(resp.autoFilter))\n  .catch(err => console.error(err));\n```</details> |
| **PHP** | <details><summary>코드 보기</summary>```php\nuse Aspose\Cells\CellsApi;\nuse Aspose\Cells\Models\AutoFilterResponse;\n\n$api = new CellsApi();\n$response = $api->getWorksheetAutoFilter('Book1.xlsx', 'Sheet1', 'MyFolder', 'MyStorage');\nprint_r($response->getAutoFilter());\n```</details> |
| **Ruby** | <details><summary>코드 보기</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::CellsApi.new\nresp = api.get_worksheet_auto_filter('Book1.xlsx', 'Sheet1', folder: 'MyFolder', storage_name: 'MyStorage')\nputs resp.auto_filter\n```</details> |
| **Go** | <details><summary>코드 보기</summary>```go\nimport (\n    \"fmt\"\n    \"github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3\"\n)\n\napi := asposecellscloud.NewAPIClient()\nresp, _, err := api.CellsApi.GetWorksheetAutoFilter(context.Background(), \"Book1.xlsx\", \"Sheet1\", \"MyFolder\", \"MyStorage\")\nif err != nil { panic(err) }\nfmt.Println(resp.AutoFilter)\n```</details> |
| **Perl** | <details><summary>코드 보기</summary>```perl\nuse AsposeCellsCloud::CellsApi;\nmy $api = AsposeCellsCloud::CellsApi->new();\nmy $resp = $api->get_worksheet_auto_filter(name=>'Book1.xlsx', sheet_name=>'Sheet1', folder=>'MyFolder', storage_name=>'MyStorage');\nprint $resp->{autoFilter};\n```</details> |

SDK 전체 목록 및 설치 지침은 [Aspose.Cells Cloud GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하십시오.

---

## 참조

- [AutoFilter – OpenAPI 스펙](https://apireference.aspose.cloud/cells/#/AutoFilter/GetWorksheetAutoFilter)  
- [인증 가이드](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- [스토리지 작업](https://docs.aspose.cloud/cells/storage/)  

---
---