---
title: "조건부 서식 삭제 – Aspose.Cells Cloud API 참조"
type: docs
url: /ko/conditional-formattings/delete/
aliases:
  - /remove-conditional-formatting/
keywords: "Aspose.Cells, 조건부 서식, 삭제, API, Excel, 클라우드"
description: "Aspose.Cells Cloud REST API를 사용하여 워크시트에서 조건부 서식 규칙을 제거합니다. 매개변수, 인증, 요청/응답 예시 및 SDK 스니펫 포함."
weight: 60
---

# 조건부 서식 삭제

## 개요
조건부 서식을 사용하면 특정 기준을 충족하는 셀에 시각적 스타일(예: 임계값보다 큰 값 강조 표시)을 적용할 수 있습니다. 자동화 시나리오에서는 기존 규칙을 제거해야 할 수 있습니다. 이 엔드포인트는 Aspose Cloud 저장소에 저장된 Excel 워크북의 워크시트에서 조건부 서식 규칙을 삭제합니다.

## 사전 요구 사항
- **Cells** 제품이 활성화된 **Aspose Cloud** 계정  
- OAuth 2.0 클라이언트 자격 증명 흐름을 통해 생성된 **JWT 액세스 토큰**  
- 워크북(`{name}`)이 지정된 **폴더** 및 **스토리지**(있는 경우)에 이미 존재해야 함  
- 아래 표시된 URL에서는 API 버전 **v3.0**(기본값)이 사용됨

## 인증
모든 Aspose.Cells Cloud 엔드포인트는 **JWT 토큰 기반 인증**이 필요합니다.

```http
Authorization: Bearer <access_token>
```

### 액세스 토큰 획득(cURL)

```bash
curl -X POST "https://api.aspose.cloud/connect/token" \
  -d "grant_type=client_credentials&client_id=<your_client_id>&client_secret=<your_client_secret>&scope=Cells"
```

**응답**

```json
{
  "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
  "token_type": "Bearer",
  "expires_in": 3600
}
```

모든 요청의 `Authorization` 헤더에 반환된 `access_token`을 사용합니다.

## HTTP 요청

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}
```

### 경로 매개변수

| 이름          | 유형     | 필수 여부 | 설명 |
|---------------|----------|-----------|------|
| `name`        | string   | 예        | 워크북 파일 이름(예: `Book1.xlsx`) |
| `sheetName`   | string   | 예        | 조건부 서식이 포함된 워크시트 이름 |
| `index`       | integer  | 예        | 삭제할 조건부 서식 규칙의 0부터 시작하는 인덱스 |

### 쿼리 매개변수

| 이름            | 유형     | 필수 여부 | 설명 |
|-----------------|----------|-----------|------|
| `folder`        | string   | 아니요    | 워크북이 위치한 클라우드 폴더 |
| `storageName`   | string   | 아니요    | Aspose Cloud 스토리지 서비스 이름 |

## 요청 예시(cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/conditionalFormattings/0?folder=MyFolder&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

### 성공 응답

```json
{
  "Code": "200",
  "Status": "OK"
}
```

**HTTP 상태 코드**

| 코드 | 의미                      | 설명 |
|------|---------------------------|------|
| 200  | OK                        | 필터가 성공적으로 적용됨. 응답은 작업 세부 정보 포함 |
| 400  | 잘못된 요청                 | 누락되었거나 잘못된 매개변수(예: 지원되지 않는 파일 유형) |
| 401  | 인증되지 않음              | 잘못되었거나 누락된 JWT 토큰 |
| 413  | 페이로드가 너무 큼         | 업로드된 파일이 크기 제한을 초과함 |
| 500  | 내부 서버 오류             | 예기치 않은 서버 오류 |

## 오류 응답

| HTTP 코드 | 이유 | 예시 본문 |
|-----------|------|------------|
| **400**   | 잘못된 요청 – 누락되었거나 잘못된 매개변수 | `{ "Code":"400", "Message":"Invalid parameter value." }` |
| **401**   | 인증되지 않음 – 누락되었거나 잘못된 JWT 토큰 | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**   | 찾을 수 없음 – 워크북 또는 워크시트가 존재하지 않음 | `{ "Code":"404", "Message":"File not found." }` |
| **500**   | 내부 서버 오류 – 예기치 않은 서버 실패 | `{ "Code":"500", "Message":"An unexpected error occurred." }` |

## SDK 예시
다음 스니펫은 공식 Aspose.Cells Cloud SDK를 사용하여 **조건부 서식 삭제** 작업을 호출하는 방법을 보여줍니다.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK;
using Aspose.Cells.Cloud.SDK.Requests;

// API 클라이언트 구성
var config = new Configuration
{
    ClientId = "<your_client_id>",
    ClientSecret = "<your_client_secret>"
};
var apiInstance = new ConditionalFormattingsApi(config);

// 조건부 서식 삭제
var request = new DeleteWorksheetConditionalFormattingRequest(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    folder: "MyFolder",
    storageName: null
);
apiInstance.DeleteWorksheetConditionalFormatting(request);
```

### Java

```java
import com.aspose.cells.cloud.sdk.api.*;
import com.aspose.cells.cloud.sdk.model.*;
import com.aspose.cells.cloud.sdk.requests.*;

ApiClient client = new ApiClient();
client.setAppKey("<your_client_id>");
client.setAppSid("<your_client_secret>");

ConditionalFormattingsApi api = new ConditionalFormattingsApi(client);

DeleteWorksheetConditionalFormattingRequest request = new DeleteWorksheetConditionalFormattingRequest(
        "Book1.xlsx",
        "Sheet1",
        0,
        "MyFolder",
        null);

api.deleteWorksheetConditionalFormatting(request);
```

### Node.js

```javascript
const { ConditionalFormattingsApi, DeleteWorksheetConditionalFormattingRequest } = require('asposecellscloud');

const config = {
    clientId: "<your_client_id>",
    clientSecret: "<your_client_secret>"
};

const apiInstance = new ConditionalFormattingsApi(config);

const request = new DeleteWorksheetConditionalFormattingRequest({
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    folder: "MyFolder",
    storageName: null
});

apiInstance.deleteWorksheetConditionalFormatting(request)
    .then(() => console.log('Conditional formatting deleted.'))
    .catch(err => console.error(err));
```

### Python

```python
from asposecellscloud import ConditionalFormattingsApi, DeleteWorksheetConditionalFormattingRequest, ApiClient

api_client = ApiClient(client_id="<your_client_id>", client_secret="<your_client_secret>")
api = ConditionalFormattingsApi(api_client)

request = DeleteWorksheetConditionalFormattingRequest(
    name="Book1.xlsx",
    sheetName="Sheet1",
    index=0,
    folder="MyFolder",
    storageName=None
)

api.delete_worksheet_conditional_formatting(request)
print("Conditional formatting removed.")
```

*(Ruby, Go, Perl 및 Swift용 추가 SDK 스니펫은 [GitHub 저장소](https://github.com/aspose-cells-cloud)에서 제공됩니다.)*

## 참고 자료
- **인증 가이드** – [JWT 토큰 기반 인증](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- **OpenAPI 사양** – 이 엔드포인트에 대한 상세 스키마 (새 탭에서 열림)  
  `<a href="https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormatting" target="_blank" rel="noopener noreferrer">OpenAPI Specification</a>`  
- **조건부 서식 개요** – 서식 규칙 생성, 업데이트 및 나열 방법 학습  
- **Aspose.Cells Cloud SDK** – 지원되는 언어 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud) 참조  

---  

*이 페이지는 표준 Aspose.Cells Cloud API 문서 템플릿을 따르며, 사전 요구 사항 섹션을 포함하고 접근성 및 SEO 모범 사례를 준수합니다.*