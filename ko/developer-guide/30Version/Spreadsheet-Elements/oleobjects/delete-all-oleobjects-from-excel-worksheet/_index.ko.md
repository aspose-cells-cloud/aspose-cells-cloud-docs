---
title: Excel 워크시트에서 모든 OLE 개체 삭제
description: Aspose.Cells Cloud REST API(v3.0)를 사용하여 Excel 워크시트에서 모든 OLE(개체 연결 및 임베딩) 개체를 제거하는 방법을 알아보세요. 엔드포인트, 매개변수, 요청/응답 예시, SDK 스니펫, 인증, 오류 처리 및 자주 묻는 질문(FAQ)이 포함되어 있습니다.
keywords: Aspose.Cells Cloud, OLE 개체 삭제, Excel API, REST API, 워크시트 OLE 삭제, 클라우드 SDK
api_version: v3.0
last_updated: 2024-11-01
weight: 60
---

# Excel 워크시트에서 모든 OLE 개체 삭제

**OleObjects – Clear**는 지정된 워크시트에서 모든 OLE(Object Linking and Embedding, 개체 연결 및 임베딩) 개체를 제거하되 셀 데이터는 그대로 유지합니다. 이 작업은 레거시 스프레드시트를 정리하거나 워크북을 재배포하기 전에 준비할 때 유용합니다.

---

## 사전 요구 사항

- 유효한 **Aspose Cloud JWT 액세스 토큰**(OAuth 2.0)  
- 대상 워크북은 Aspose Cloud 스토리지에 저장되어 있어야 하며, 그렇지 않을 경우 `folder`/`storageName` 매개변수를 사용하여 위치를 지정해야 합니다.  
- API 버전 **v3.0** 이상  

> **참고:** 이 작업은 *멱등성(idempotent)* 을 갖습니다. 즉, OLE 개체가 존재하지 않아도 요청을 보내면 성공적인 `200 OK` 응답이 반환됩니다.

---

## HTTP 요청

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects
```

### 경로 매개변수

| 이름          | 유형     | 필수 여부 | 설명                         |
|---------------|----------|-----------|------------------------------|
| `name`        | string   | ✔️        | 워크북 파일의 이름입니다.     |
| `sheetName`   | string   | ✔️        | 워크시트의 이름입니다.        |

### 쿼리 매개변수

| 이름            | 유형     | 필수 여부 | 설명                                           |
|-----------------|----------|-----------|------------------------------------------------|
| `folder`        | string   | 선택 사항 | 워크북이 위치한 폴더입니다.                   |
| `storageName`   | string   | 선택 사항 | 워크북이 저장된 스토리지 이름입니다.           |

**헤더**

| 헤더                 | 값                            |
|----------------------|-------------------------------|
| `Authorization`      | `Bearer <jwt token>` |
| `Accept`             | `application/json` |
| `Content-Type`       | `application/json` |

---

## 요청 예시(cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects?folder=Samples&storageName=MyStorage" \
     -X DELETE \
     -H "Authorization: Bearer <jwt token>" \
     -H "Accept: application/json" \
     -H "Content-Type: application/json"
```

*`<jwt token>`을 유효한 액세스 토큰으로 바꾸고, 필요에 따라 `folder`/`storageName`을 조정하세요.*

---

## 성공적인 응답

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**HTTP 상태 코드**

| 코드 | 의미                | 설명                                         |
|------|---------------------|----------------------------------------------|
| 200  | OK                  | 필터가 성공적으로 적용되었으며, 응답에 작업 세부 정보가 포함됩니다. |
| 400  | 잘못된 요청         | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식)가 있습니다. |
| 401  | 인증되지 않음       | 유효하지 않거나 누락된 JWT 토큰입니다.       |
| 413  | 요청 페이로드가 너무 큼 | 업로드된 파일이 크기 제한을 초과합니다.     |
| 500  | 내부 서버 오류      | 예기치 않은 서버 오류입니다.                 |
---

## SDK 샘플

다음 코드 스니펫은 공식 Aspose.Cells Cloud SDK를 사용하여 **DeleteWorksheetOleObjects**를 호출하는 방법을 보여줍니다. 자리표시자 값(`<YOUR_TOKEN>`, `<FILE_NAME>` 등)을 실제 데이터로 바꾸세요.

| 언어 | 샘플 |
|------|------|
| **C#** | <details><summary>C# 예제 보기</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar config = new Configuration { AccessToken = "<YOUR_TOKEN>", BasePath = "https://api.aspose.cloud" };\nvar api = new OleObjectsApi(config);\napi.DeleteWorksheetOleObjects(name: "Sample.xlsx", sheetName: "Sheet1", folder: "Samples", storageName: null);\n```</details> |
| **Java** | <details><summary>Java 예제 보기</summary>```java\nimport com.aspose.cells.cloud.api.OleObjectsApi;\nimport com.aspose.cells.cloud.client.ApiClient;\nimport com.aspose.cells.cloud.client.Configuration;\n\nConfiguration config = new Configuration();\nconfig.setAccessToken("<YOUR_TOKEN>");\nconfig.setBasePath("https://api.aspose.cloud");\nOleObjectsApi api = new OleObjectsApi(new ApiClient(config));\napi.deleteWorksheetOleObjects("Sample.xlsx", "Sheet1", "Samples", null);\n```</details> |
| **Python** | <details><summary>Python 예제 보기</summary>```python\nfrom asposecellscloud import ApiClient, Configuration, OleObjectsApi\n\nconfig = Configuration()\nconfig.access_token = '<YOUR_TOKEN>'\nconfig.host = 'https://api.aspose.cloud'\nclient = ApiClient(configuration=config)\napi = OleObjectsApi(client)\napi.delete_worksheet_ole_objects(name='Sample.xlsx', sheet_name='Sheet1', folder='Samples')\n```</details> |
| **Node.js** | <details><summary>Node.js 예제 보기</summary>```javascript\nconst { OleObjectsApi, Configuration } = require('asposecellscloud');\n\nlet config = new Configuration({ accessToken: '<YOUR_TOKEN>', basePath: 'https://api.aspose.cloud' });\nlet api = new OleObjectsApi(config);\napi.deleteWorksheetOleObjects('Sample.xlsx', 'Sheet1', { folder: 'Samples' })\n  .then(() => console.log('모든 OLE 개체가 삭제되었습니다.'))\n  .catch(err => console.error(err));\n```</details> |
| **Go** | <details><summary>Go 예제 보기</summary>```go\npackage main\nimport (\n    "context"\n    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"\n)\n\nfunc main() {\n    cfg := asposecellscloud.NewConfiguration()\n    cfg.AccessToken = "<YOUR_TOKEN>"\n    cfg.Host = "https://api.aspose.cloud"\n    api := asposecellscloud.NewOleObjectsApi(cfg)\n    _, err := api.DeleteWorksheetOleObjects(context.Background(), "Sample.xlsx", "Sheet1", map[string]interface{}{ "folder": "Samples" })\n    if err != nil { panic(err) }\n    println("모든 OLE 개체가 삭제되었습니다.")\n}\n```</details> |

*모든 지원 언어에 대한 전체 소스 파일은 [Aspose.Cells Cloud GitHub 저장소](https://github.com/aspose-cells-cloud)에서 확인할 수 있습니다.*

---

## 오류 및 처리

- **멱등성** – 이미 OLE 개체가 없는 워크시트에서 개체를 삭제하려고 해도 `200 OK` 응답이 반환됩니다.  
- **토큰 만료** – `401 Unauthorized` 오류가 발생하면 새 JWT 토큰을 발급받아 다시 시도하세요.  
- **잘못된 워크시트 이름** – 워크시트 이름이 워크북 내 실제 이름과 대소문자가 일치해야 합니다. 그렇지 않으면 `400 Bad Request`가 반환됩니다.  

일시적인 `500` 오류에 대해서는 지수 백오프 방식으로 재시도 로직을 구현하세요.

---

## 자주 묻는 질문(FAQ)

**Q1: `folder` 및 `storageName` 매개변수를 반드시 지정해야 하나요?**  
**A:** 아닙니다. 생략할 경우 Aspose Cloud는 기본 스토리지와 루트 폴더를 사용합니다.

**Q2: 특정 셀에서만 OLE 개체를 삭제할 수 있나요?**  
**A:** 이 엔드포인트는 워크시트 내 **모든** OLE 개체를 삭제합니다. 특정 개체만 제거하려면 *특정 OLE 개체 삭제* 작업을 사용하세요.

**Q3: 워크북이 편집 잠금 상태라면 어떻게 되나요?**  
**A:** API는 `400 Bad Request` 응답과 함께 파일이 잠겨 있다는 메시지를 반환합니다. 엔드포인트를 호출하기 전 해당 파일이 다른 곳에서 열려 있지 않은지 확인하세요.

**Q4: 워크북 크기에 제한이 있나요?**  
**A:** 서비스는 일반적인 Aspose Cloud 파일 크기 제한을 따르며, 현재 각 파일당 최대 2GB까지 허용됩니다. 더 큰 파일은 분할하거나 청크 단위로 처리해야 할 수 있습니다.

---

## 모범 사례

- **성능** – 문서 사이트에서 서드파티 스크립트를 로드할 때 `async` 또는 `defer` 속성을 사용하여 초기 페이지 로드 시간을 줄이세요.  
- **보안** – 새 탭에서 열리는 모든 외부 링크에 `rel="noopener noreferrer"`를 추가하세요.  
- **접근성** – 장식용 아이콘(예: 사이드바 내 캐리트-down 화살표)은 WCAG AA 표준을 충족하기 위해 `alt=""` 및 `role="presentation"`을 설정해야 합니다.  
- **일관성** – 인코딩 오류를 방지하기 위해 날짜 형식을 ISO-8601(`YYYY-MM-DD`)으로 유지하세요.  

---

## 관련 작업

- **OLE 개체 추가** – `POST /cells/{name}/worksheets/{sheetName}/oleobjects`  
- **특정 OLE 개체 삭제** – `DELETE /cells/{name}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  

하단의 내비게이션 링크를 사용하여 관련 API 작업 간에 이동할 수 있습니다.