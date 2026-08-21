---
title: "OLE 개체를 이미지로 변환 – Aspose.Cells Cloud REST API"
description: "Excel 워크시트에 포함된 OLE 개체를 검색하여 PNG, JPEG, TIFF, GIF, EMF 또는 BMP 형식으로 변환합니다. Aspose.Cells Cloud REST API를 사용합니다."
keywords:
  - "OLE 개체 이미지 변환"
  - "Aspose.Cells Cloud"
  - "REST API"
  - "Excel"
  - "OLE"
  - "이미지 변환"
  - "PNG"
  - "JPEG"
  - "TIFF"
  - "GIF"
  - "EMF"
  - "BMP"
weight: 40
---

# OLE 개체를 이미지로 변환

워크시트에 포함된 OLE 개체를 검색하여 요청한 이미지 형식으로 반환합니다.

---

## 사전 요구 사항

이 엔드포인트를 호출하기 전에 다음 사항을 확인하십시오:

1. **Aspose.Cells Cloud 계정** – [Aspose Cloud 포털](https://dashboard.aspose.cloud/)에서 가입합니다.  
2. **클라우드 저장소에 업로드된 워크북** – **파일 업로드** API 또는 Aspose Cloud UI를 사용합니다.  
3. **JWT 액세스 토큰** – [인증 가이드](/total/getting-started/rest-api-overview/authenticating-api-requests/)에 따라 토큰을 획득합니다.  

---

## 보안 및 인증

모든 Aspose.Cells Cloud API는 **JWT 토큰 기반 인증**을 요구합니다. 토큰을 `Authorization` 헤더에 포함시킵니다:

```http
Authorization: Bearer <jwt-token>
```

HTTPS 엔드포인트만 지원되며, `http://`는 절대 사용하지 마십시오.

---

## 요청

### HTTP 메서드
`GET`

### 엔드포인트
```
https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}?format={format}
```

### 경로 매개변수

| 이름           | 유형   | 필수 여부 | 설명                                    |
|----------------|--------|-----------|-----------------------------------------|
| `name`         | 문자열 | ✅        | 워크북 파일 이름(예: `Book1.xlsx`).     |
| `sheetName`    | 문자열 | ✅        | OLE 개체가 포함된 워크시트 이름.        |
| `objectNumber` | 정수   | ✅        | OLE 개체의 0부터 시작하는 인덱스.        |

### 쿼리 매개변수

| 이름          | 유형   | 필수 여부 | 설명                                                                 |
|---------------|--------|-----------|----------------------------------------------------------------------|
| `format`      | 문자열 | ❌        | 원하는 이미지 형식(`png`, `jpeg`, `tiff`, `gif`, `emf`, `bmp`). 생략 시 기본값은 `png`입니다. |
| `folder`      | 문자열 | ❌        | 워크북이 위치한 폴더 경로.                                           |
| `storageName` | 문자열 | ❌        | 스토리지 서비스 이름(예: `MyCloud`).                                |

---

## 요청 예시(cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>"
```

*`<jwt-token>`을 유효한 JWT 토큰으로 바꾸세요.*

---

## 응답

| 상태 코드 | 콘텐츠 형식                  | 설명                                |
|-----------|------------------------------|-------------------------------------|
| `200`     | `image/png` (또는 요청한 형식) | OLE 개체를 나타내는 이진 이미지 데이터. |
| `400`     | `application/json`           | 잘못된 요청 매개변수.               |
| `401`     | `application/json`           | 인증 실패(누락/잘못된 JWT).         |
| `404`     | `application/json`           | 지정된 워크북, 워크시트 또는 OLE 개체를 찾을 수 없습니다. |
| `500`     | `application/json`           | 서버 측 오류.                       |

### 이진 페이로드 처리

API는 원본 이미지 바이트를 반환합니다. 다음과 같이 처리할 수 있습니다:

* **파일로 직접 저장** (Linux/macOS 예시):

  ```bash
  curl -o oleobject.png "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
       -H "Authorization: Bearer <jwt-token>"
  ```

* **디버깅 또는 JSON 내 포함을 위해 Base64로 인코딩**:

  ```bash
  curl -s "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
       -H "Authorization: Bearer <jwt-token>" | base64
  ```

  *예시(Base64 출력 단축):*

  ```
  iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAABG0lEQVR42mNkY…
  ```

---

## 오류 응답

| HTTP 상태 코드 | 코드                   | 메시지                                 |
|----------------|------------------------|----------------------------------------|
| `400`          | `InvalidParameter`     | 하나 이상의 요청 매개변수가 유효하지 않습니다. |
| `401`          | `AuthenticationFailed` | JWT 토큰이 누락되었거나 유효하지 않습니다.   |
| `404`          | `PropertyNotFound`     | 요청한 워크북, 워크시트 또는 OLE 개체가 존재하지 않습니다. |
| `500`          | `InternalError`        | 서버에서 예기치 않은 오류가 발생했습니다. |

---

## SDK 예제

다음 코드 스니펫은 공식 SDK를 사용하여 이 작업을 호출하는 방법을 보여줍니다. `YOUR_JWT_TOKEN` 및 기타 자리표시자를 실제 값으로 바꾸세요.

| 언어     | 예제 |
|----------|------|
| **C#** | <details><summary>코드 보기</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model.Requests;\n\nvar config = new Configuration { AccessToken = \"YOUR_JWT_TOKEN\" };\nvar api = new OleObjectsApi(config);\nvar request = new GetWorksheetOleObjectRequest(\n    name: \"Embedded_OleObject_Sample_Book1.xlsx\",\n    sheetName: \"Sheet1\",\n    objectNumber: 0,\n    format: \"png\"\n);\nvar stream = api.GetWorksheetOleObject(request);\nusing var file = File.Create(\"oleobject.png\");\nstream.CopyTo(file);\n```</details> |
| **Java** | <details><summary>코드 보기</summary>```java\nimport com.aspose.cells.cloud.ApiException;\nimport com.aspose.cells.cloud.api.OleObjectsApi;\nimport com.aspose.cells.cloud.model.*;\nimport com.aspose.cells.cloud.model.requests.*;\nimport java.io.FileOutputStream;\nimport java.io.InputStream;\n\nOleObjectsApi api = new OleObjectsApi();\napi.getApiClient().setAccessToken(\"YOUR_JWT_TOKEN\");\nGetWorksheetOleObjectRequest req = new GetWorksheetOleObjectRequest(\n    \"Embedded_OleObject_Sample_Book1.xlsx\",\n    \"Sheet1\",\n    0,\n    \"png\",\n    null,\n    null\n);\nInputStream stream = api.getWorksheetOleObject(req);\ntry (FileOutputStream out = new FileOutputStream(\"oleobject.png\")) {\n    stream.transferTo(out);\n}\n```</details> |
| **Python** | <details><summary>코드 보기</summary>```python\nfrom asposecellscloud import CellsApi, GetWorksheetOleObjectRequest\n\napi = CellsApi()\napi.api_client.configuration.access_token = \"YOUR_JWT_TOKEN\"\nrequest = GetWorksheetOleObjectRequest(\n    name=\"Embedded_OleObject_Sample_Book1.xlsx\",\n    sheet_name=\"Sheet1\",\n    object_number=0,\n    format=\"png\"\n)\nstream = api.get_worksheet_ole_object(request)\nwith open('oleobject.png', 'wb') as f:\n    f.write(stream.read())\n```</details> |
| **Node.js** | <details><summary>코드 보기</summary>```javascript\nconst { CellsApi, GetWorksheetOleObjectRequest } = require('asposecellscloud');\n\nconst api = new CellsApi();\napi.apiClient.configuration.accessToken = 'YOUR_JWT_TOKEN';\n\nconst request = new GetWorksheetOleObjectRequest({\n    name: 'Embedded_OleObject_Sample_Book1.xlsx',\n    sheetName: 'Sheet1',\n    objectNumber: 0,\n    format: 'png'\n});\napi.getWorksheetOleObject(request).then(stream => {\n    const fs = require('fs');\n    const writeStream = fs.createWriteStream('oleobject.png');\n    stream.pipe(writeStream);\n});\n```</details> |
| **Go** | <details><summary>코드 보기</summary>```go\npackage main\nimport (\n    \"io\"\n    \"os\"\n    cells \"github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3\"\n)\nfunc main() {\n    cfg := cells.NewConfiguration()\n    cfg.AccessToken = \"YOUR_JWT_TOKEN\"\n    api := cells.NewOleObjectsApi(cfg)\n    req := cells.GetWorksheetOleObjectRequest{\n        Name:         \"Embedded_OleObject_Sample_Book1.xlsx\",\n        SheetName:    \"Sheet1\",\n        ObjectNumber: 0,\n        Format:       \"png\",\n    }\n    stream, _, err := api.GetWorksheetOleObject(req)\n    if err != nil { panic(err) }\n    out, _ := os.Create(\"oleobject.png\")\n    defer out.Close()\n    io.Copy(out, stream)\n}\n```</details> |
| **PHP** | <details><summary>코드 보기</summary>```php\n<?php\nrequire_once 'vendor/autoload.php';\nuse Aspose\\Cells\\Cloud\\Api\\OleObjectsApi;\nuse Aspose\\Cells\\Cloud\\Model\\Requests\\GetWorksheetOleObjectRequest;\n\n$config = new \\Aspose\\Cells\\Cloud\\Configuration();\n$config->setAccessToken('YOUR_JWT_TOKEN');\n$apiInstance = new OleObjectsApi($config);\n$request = new GetWorksheetOleObjectRequest(\n    'Embedded_OleObject_Sample_Book1.xlsx',\n    'Sheet1',\n    0,\n    'png'\n);\n$stream = $apiInstance->getWorksheetOleObject($request);\nfile_put_contents('oleobject.png', $stream);\n?>\n```</details> |
| **Ruby** | <details><summary>코드 보기</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::OleObjectsApi.new\napi.api_client.config.access_token = 'YOUR_JWT_TOKEN'\nrequest = AsposeCellsCloud::GetWorksheetOleObjectRequest.new(\n  name: 'Embedded_OleObject_Sample_Book1.xlsx',\n  sheet_name: 'Sheet1',\n  object_number: 0,\n  format: 'png'\n)\nstream = api.get_worksheet_ole_object(request)\nFile.open('oleobject.png', 'wb') { |f| f.write(stream) }\n```\n</details> |
| **Perl** | <details><summary>코드 보기</summary>```perl\nuse AsposeCellsCloud::Api::OleObjectsApi;\nuse AsposeCellsCloud::Object::GetWorksheetOleObjectRequest;\n\nmy $api = AsposeCellsCloud::Api::OleObjectsApi->new();\n$api->{api_client}->{config}->{access_token} = 'YOUR_JWT_TOKEN';\nmy $req = AsposeCellsCloud::Object::GetWorksheetOleObjectRequest->new(\n    name => 'Embedded_OleObject_Sample_Book1.xlsx',\n    sheet_name => 'Sheet1',\n    object_number => 0,\n    format => 'png'\n);\nmy $stream = $api->get_worksheet_ole_object(request => $req);\nopen my $fh, '>', 'oleobject.png' or die $!;\nbinmode $fh;\nprint $fh $stream;\nclose $fh;\n```</details> |

*(SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)에서 확인할 수 있습니다.)*

---

## 관련 작업

- **OLE 개체 추가** – `POST /cells/{name}/worksheets/{sheetName}/oleobjects`
- **OLE 개체 업데이트** – `PUT /cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}`
- **OLE 개체 삭제** – `DELETE /cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}`
- **OLE 개체 목록 조회** – `GET /cells/{name}/worksheets/{sheetName}/oleobjects`

자세한 내용은 해당 API 참조 페이지를 참고하세요.

---

## 추가 리소스

- **OpenAPI 사양** – <https://apireference.aspose.cloud/cells/#/OleObjects/GetWorksheetOleObject>
- **인증 가이드** – <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>
- **SDK 저장소** – <https://github.com/aspose-cells-cloud>
- **성능 및 접근성** – Lighthouse 및 axe‑core 감사를 실행하여 최적의 로드 시간과 WCAG 2.1 AA 준수를 보장하세요.

---