---
title: "Excel 워크시트에서 하이퍼링크 업데이트 – Aspose.Cells Cloud API 가이드"
description: "Aspose.Cells Cloud REST API(v3.0)를 사용하여 Excel 워크시트의 기존 하이퍼링크를 업데이트하는 방법을 알아보세요. 엔드포인트, 매개변수, 요청 본문 스키마, cURL 예제, SDK 코드 스니펫, 오류 처리, 속도 제한 및 사전 요구 사항을 포함합니다."
keywords:
  - "Aspose.Cells"
  - "하이퍼링크 업데이트"
  - "Excel API"
  - "REST API"
  - "클라우드 스프레드시트"
  - "v3.0"
weight: 30
aliases:
  - /hyperlinks/update/
  - /update-hyperlinks-in-excel-worksheet/
---

# Excel 워크시트에서 하이퍼링크 업데이트  

**API 버전:** v3.0  

**PostWorksheetHyperlink** 작업은 0부터 시작하는 인덱스로 식별되는 워크시트 내 기존 하이퍼링크를 업데이트합니다.

---

## 목차
1. [사전 요구 사항](#prerequisites)  
2. [속도 제한](#rate-limiting)  
3. [엔드포인트](#endpoint)  
4. [매개변수](#parameters)  
   - [경로 매개변수](#path-parameters)  
   - [쿼리 매개변수](#query-parameters)  
   - [요청 본문 스키마](#request-body-schema)  
5. [응답](#responses)  
   - [성공 응답](#success-response)  
   - [오류 응답](#error-responses)  
6. [cURL 예제](#curl-example)  
7. [SDK 코드 샘플](#sdk-code-samples)  
8. [참고 자료](#see-also)  

---

## 사전 요구 사항 <a name="prerequisites"></a>

| 요구 사항 | 설명 |
|-----------|-------------|
| **인증** | JWT 토큰 기반 인증. 토큰 획득 방법은 [인증 가이드](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)를 참조하세요. |
| **스토리지** | 워크북은 지원되는 Aspose Cloud 스토리지(기본값은 **Default**)에 저장되어 있어야 합니다. |
| **권한** | JWT 토큰에는 대상 워크북을 읽고 쓸 수 있는 권한이 있어야 합니다. |
| **헤더** | 모든 요청에 대해 `Content-Type: application/json` 및 `Accept: application/json` 헤더가 필요합니다. |

---

## 속도 제한 <a name="rate-limiting"></a>

Aspose.Cells Cloud는 **액세스 토큰당 최대 60회/분**으로 요청 수를 제한합니다. 이 제한을 초과하면 HTTP **429 Too Many Requests** 오류가 반환됩니다. 제한이 발생하면 지수 백오프를 구현하거나 `Retry-After` 헤더를 준수하세요.

---

## 엔드포인트 <a name="endpoint"></a>

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
```

*파일 `name`의 워크시트 `sheetName`에서 `hyperlinkIndex`로 식별되는 하이퍼링크를 업데이트합니다.*

---

## 매개변수 <a name="parameters"></a>

### 경로 매개변수 <a name="path-parameters"></a>

| 이름              | 유형   | 필수 여부 | 설명 |
|-------------------|--------|----------|-------------|
| `name`            | string | ✅ | Excel 파일 이름(확장자 포함). |
| `sheetName`       | string | ✅ | 하이퍼링크가 포함된 워크시트 이름. |
| `hyperlinkIndex`  | integer| ✅ | 업데이트할 하이퍼링크의 0부터 시작하는 인덱스. |

### 쿼리 매개변수 <a name="query-parameters"></a>

| 이름           | 유형   | 필수 여부 | 설명 |
|----------------|--------|----------|-------------|
| `folder`       | string | ❌ | 워크북이 저장된 스토리지 내 폴더 경로. |
| `storageName`  | string | ❌ | 스토리지 서비스 이름(예: `Default`). |

### 요청 본문 스키마 <a name="request-body-schema"></a>

요청 본문에는 **`hyperlink`** 객체가 포함되어야 합니다. 변경하려는 필드만 제공하면 되며, 생략된 선택적 필드는 기존 값을 유지합니다.

| 필드            | 유형   | 필수 여부 | 설명 |
|-----------------|--------|----------|-------------|
| `Address`       | string | ✅ | 하이퍼링크의 대상 URL. |
| `Area`          | object | ✅ | 하이퍼링크가 배치된 셀 범위. `StartRow`, `StartColumn`, `EndRow`, `EndColumn`을 모두 포함해야 하며(모두 0부터 시작하는 정수). |
| `ScreenTip`     | string | ❌ | 마우스 오버 시 표시되는 툴팁. |
| `TextToDisplay` | string | ❌ | 셀 내에 표시되는 텍스트. |
| `link`          | object| ❌ | 하이퍼미디어 링크(`Href`, `Rel`, `Title`, `Type`). 일반적으로 요청 페이로드에서는 생략됩니다. |

**`Area` 객체 정의**

| 하위 필드       | 유형   | 필수 여부 | 설명 |
|-----------------|--------|----------|-------------|
| `StartRow`      | integer| ✅ | 0부터 시작하는 시작 행 인덱스. |
| `StartColumn`   | integer| ✅ | 0부터 시작하는 시작 열 인덱스. |
| `EndRow`        | integer| ✅ | 0부터 시작하는 종료 행 인덱스. |
| `EndColumn`     | integer| ✅ | 0부터 시작하는 종료 열 인덱스. |

---

## 응답 <a name="responses"></a>

### 성공 응답 <a name="success-response"></a>

| 필드       | 유형   | 설명 |
|------------|--------|-------------|
| `Code`     | integer| HTTP 상태 코드(성공 시 200). |
| `Status`   | string | 텍스트 상태(`OK`). |
| `Hyperlink`| object (선택 사항) | `link` 하위 객체 요청 시 반환되는 업데이트된 하이퍼링크 객체. |

**예시 JSON**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### 오류 응답 <a name="error-responses"></a>

| HTTP 코드 | 원인 | 예시 본문 |
|-----------|--------|--------------|
| **400** | 잘못된 요청 – 누락되거나 잘못된 매개변수. | `{ "Code":"400", "Message":"Invalid parameter value." }` |
| **401** | 인증 실패 – 누락되거나 잘못된 JWT 토큰. | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404** | 찾을 수 없음 – 워크북, 워크시트 또는 하이퍼링크가 존재하지 않음. | `{ "Code":"404", "Message":"File not found." }` |
| **429** | 요청 너무 많음 – 속도 제한 초과. | `{ "Code":"429", "Message":"Request limit exceeded. Retry later." }` |
| **500** | 내부 서버 오류 – 예기치 않은 서버 실패. | `{ "Code":"500", "Message":"An unexpected error occurred." }` |

---

## cURL 예제 <a name="curl-example"></a>

```bash
curl -L -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks/1" \
  -H "Authorization: Bearer <YOUR_JWT_TOKEN>" \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -d '{
        "hyperlink": {
          "Address": "https://www.msnbc.com/",
          "Area": {
            "StartRow": 1,
            "StartColumn": 6,
            "EndRow": 1,
            "EndColumn": 6
          },
          "ScreenTip": "MSNBC 홈페이지",
          "TextToDisplay": "MSNBC"
        },
        "folder": "samples",
        "storageName": "Default"
      }'
```

**응답**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*팁:* JSON 페이로드를 파일(예: `payload.json`)로 저장한 후 `--data @payload.json`을 사용해 보다 깔끔하게 복사·붙여넣기하세요.

---

## SDK 코드 샘플 <a name="sdk-code-samples"></a>

다음 스니펫은 공식 Aspose.Cells Cloud SDK를 사용하여 **PostWorksheetHyperlink**를 호출하는 방법을 보여줍니다. 플레이스홀더 값(`<YOUR_JWT_TOKEN>`, `<FILE_NAME>` 등)을 실제 데이터로 바꾸세요.

| 언어 | 샘플 |
|------|--------|
| **C#** | ```csharp\nvar api = new CellsApi("<client_id>", "<client_secret>");\nvar hyperlink = new Hyperlink {\n    Address = \"https://www.msnbc.com/\",\n    Area = new LinkArea { StartRow = 1, StartColumn = 6, EndRow = 1, EndColumn = 6 },\n    ScreenTip = \"MSNBC 홈페이지\",\n    TextToDisplay = \"MSNBC\"\n};\nvar response = api.PostWorksheetHyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, folder: \"samples\");\n``` |
| **Java** | ```java\nCellsApi api = new CellsApi(clientId, clientSecret);\nHyperlink hyperlink = new Hyperlink();\nhyperlink.setAddress(\"https://www.msnbc.com/\");\nLinkArea area = new LinkArea();\narea.setStartRow(1);\narea.setStartColumn(6);\narea.setEndRow(1);\narea.setEndColumn(6);\nhyperlink.setArea(area);\nhyperlink.setScreenTip(\"MSNBC 홈페이지\");\nhyperlink.setTextToDisplay(\"MSNBC\");\nCellsCloudResponse resp = api.postWorksheetHyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, \"samples\", null);\n``` |
| **Python** | ```python\nimport asposecellscloud\nfrom asposecellscloud.apis.cells_api import CellsApi\napi = CellsApi(client_id, client_secret)\nhyperlink = asposecellscloud.models.Hyperlink(\n    address=\"https://www.msnbc.com/\",\n    area=asposecellscloud.models.LinkArea(start_row=1, start_column=6, end_row=1, end_column=6),\n    screen_tip=\"MSNBC 홈페이지\",\n    text_to_display=\"MSNBC\"\n)\nresponse = api.post_worksheet_hyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, folder=\"samples\")\n``` |
| **Node.js** | ```javascript\nconst { CellsApi, Hyperlink, LinkArea } = require('asposecellscloud');\nconst api = new CellsApi(clientId, clientSecret);\nlet hyperlink = new Hyperlink({\n  address: 'https://www.msnbc.com/',\n  area: new LinkArea({ startRow: 1, startColumn: 6, endRow: 1, endColumn: 6 }),\n  screenTip: 'MSNBC 홈페이지',\n  textToDisplay: 'MSNBC'\n});\napi.postWorksheetHyperlink('test.xlsx', 'Sheet1', 1, hyperlink, { folder: 'samples' })\n  .then(resp => console.log(resp));\n``` |
| **Go** | ```go\nimport (\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3\"\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3/api\"\n)\nclient := api.NewCellsApiClient(clientId, clientSecret)\narea := asposecellscloud.LinkArea{StartRow: 1, StartColumn: 6, EndRow: 1, EndColumn: 6}\nhyperlink := asposecellscloud.Hyperlink{Address: \"https://www.msnbc.com/\", Area: &area, ScreenTip: \"MSNBC 홈페이지\", TextToDisplay: \"MSNBC\"}\nresp, _ := client.PostWorksheetHyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, \"samples\", \"\")\nfmt.Println(resp)\n``` |
| **PHP** | ```php\n<?php\nrequire_once('vendor/autoload.php');\nuse Aspose\Cells\CellsApi;\n$api = new CellsApi($clientId, $clientSecret);\n$hyperlink = new \\Aspose\\Cells\\Model\\Hyperlink();\n$hyperlink->setAddress('https://www.msnbc.com/');\n$area = new \\Aspose\\Cells\\Model\\LinkArea();\n$area->setStartRow(1);\n$area->setStartColumn(6);\n$area->setEndRow(1);\n$area->setEndColumn(6);\n$hyperlink->setArea($area);\n$hyperlink->setScreenTip('MSNBC 홈페이지');\n$hyperlink->setTextToDisplay('MSNBC');\n$response = $api->postWorksheetHyperlink('test.xlsx', 'Sheet1', 1, $hyperlink, 'samples');\nprint_r($response);\n?>\n``` |
| **Ruby** | ```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::CellsApi.new(client_id: CLIENT_ID, client_secret: CLIENT_SECRET)\nhyperlink = AsposeCellsCloud::Hyperlink.new(\n  address: 'https://www.msnbc.com/',\n  area: AsposeCellsCloud::LinkArea.new(start_row: 1, start_column: 6, end_row: 1, end_column: 6),\n  screen_tip: 'MSNBC 홈페이지',\n  text_to_display: 'MSNBC'\n)\nresult = api.post_worksheet_hyperlink('test.xlsx', 'Sheet1', 1, hyperlink, folder: 'samples')\nputs result\n``` |
| **Perl** | ```perl\nuse AsposeCellsCloud::CellsApi;\nmy $api = AsposeCellsCloud::CellsApi->new(client_id => $client_id, client_secret => $client_secret);\nmy $area = AsposeCellsCloud::LinkArea->new(startRow => 1, startColumn => 6, endRow => 1, endColumn => 6);\nmy $hyperlink = AsposeCellsCloud::Hyperlink->new(address => 'https://www.msnbc.com/', area => $area, screenTip => 'MSNBC 홈페이지', textToDisplay => 'MSNBC');\nmy $resp = $api->post_worksheet_hyperlink(name=>'test.xlsx', sheetName=>'Sheet1', hyperlinkIndex=>1, hyperlink=>$hyperlink, folder=>'samples');\nprint $resp->{Code}, \" \", $resp->{Status}, \"\\n\";\n``` |

*모든 SDK는 오픈 소스이며 [Aspose.Cells Cloud GitHub 저장소](https://github.com/aspose-cells-cloud)에서 확인할 수 있습니다.*

---

## 참고 자료 <a name="see-also"></a>

- **인증** – [JWT 토큰 시작하기](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- **스토리지 작업** – [파일 업로드](https://apireference.aspose.cloud/cells/#/Storage/UploadFile)  
- **기타 하이퍼링크 작업** – [하이퍼링크 추가](https://apireference.aspose.cloud/cells/#/Hyperlinks/PostWorksheetHyperlink) | [하이퍼링크 삭제](https://apireference.aspose.cloud/cells/#/Hyperlinks/DeleteWorksheetHyperlink)  
- **OpenAPI 명세서** – 엔드포인트 전체 정의: <https://apireference.aspose.cloud/cells/#/Hyperlinks/PostWorksheetHyperlink>  

---

*문서 최종 업데이트 날짜: 2026-07-30*