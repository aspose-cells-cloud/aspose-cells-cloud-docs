---
title: "Aspose.Cells Cloud Web API – Excel 파일의 열기 비밀번호 설정/수정"
second_title: "종합 개발자 가이드"
ArticleTitle: "스프레드시트 보호 – 열기 비밀번호 및 수정 비밀번호 설정"
linktitle: "보호"
type: docs
url: /protection/
keywords: "Aspose.Cells, 클라우드, API, 스프레드시트, 보호, 열기 비밀번호, 읽기-쓰기 비밀번호, Excel"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크북을 열기 비밀번호 또는 읽기-쓰기 비밀번호로 보호하는 방법을 알아보세요. 요청 구문, 코드 예제, 오류 처리가 포함됩니다."
weight: 60
---

이 가이드에서는 Aspose.Cells Cloud Web API를 사용하여 스프레드시트의 **열기 비밀번호**와 **읽기-쓰기 비밀번호**를 설정, 수정 및 제거하는 방법을 배웁니다. 이러한 기능은 Excel 워크북 내의 민감한 데이터를 보호하는 데 도움이 됩니다.

**사전 요구 사항**  
- 유효한 API 키 및 SID가 있는 활성화된 Aspose.Cells Cloud 계정  
- 보호하려는 워크북은 Aspose Cloud 스토리지에 업로드되었거나 공개 URL을 통해 접근 가능해야 합니다  

**API 참조**  

| **HTTP 메서드** | **엔드포인트** | **쿼리/경로 매개변수** | **설명** |
|-----------------|--------------|----------------------------|-----------------|
| `PUT` | `/cells/{fileName}/protection` | `fileName` (경로) – 워크북 이름<br>`openPassword` (쿼리, 선택) – 파일 열기에 필요한 비밀번호<br>`readWritePassword` (쿼리, 선택) – 파일 수정에 필요한 비밀번호 | 지정된 워크북에 대해 열기 비밀번호 및/또는 읽기-쓰기 비밀번호를 설정하거나 업데이트합니다. |
| `DELETE` | `/cells/{fileName}/protection` | `fileName` (경로) – 워크북 이름 | 워크북을 보호하는 모든 비밀번호를 제거합니다. |

**요청 본문 예제 (JSON)**  

```json
{
  "OpenPassword": "MyOpenPwd123",
  "ReadWritePassword": "MyEditPwd456"
}
```

**응답 예제 (JSON)**  

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "워크북 보호가 성공적으로 업데이트되었습니다."
}
```

**HTTP 상태 코드**

| 코드 | 의미                     | 설명                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | 필터가 성공적으로 적용됨; 응답에는 작업 세부 정보가 포함됩니다. |
| 400  | Bad Request (잘못된 요청)   | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식) |
| 401  | Unauthorized (인증되지 않음) | 잘못되거나 누락된 JWT 토큰 |
| 413  | Payload Too Large (페이로드가 너무 큼) | 업로드된 파일이 크기 제한을 초과함 |
| 500  | Internal Server Error (내부 서버 오류) | 예기치 않은 서버 오류 |

**코드 예제**

*C# (Aspose.Cells Cloud SDK)*  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");
var request = new SetWorkbookProtectionRequest(
    name: "Sample.xlsx",
    openPassword: "MyOpenPwd123",
    readWritePassword: "MyEditPwd456"
);
apiInstance.SetWorkbookProtection(request);
```

*Python (Aspose.Cells Cloud SDK)*  

```python
import asposecellscloud
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.models import SetWorkbookProtectionRequest

api = CellsApi(client_id="YOUR_CLIENT_ID", client_secret="YOUR_CLIENT_SECRET")
request = SetWorkbookProtectionRequest(
    name="Sample.xlsx",
    open_password="MyOpenPwd123",
    read_write_password="MyEditPwd456"
)
api.set_workbook_protection(request)
```

**오류 처리**  
오류가 발생하면 API는 `Code`, `Message`, 그리고 선택적으로 `Description`을 포함하는 JSON 페이로드를 반환합니다. 상태 코드를 확인하고 애플리케이션 로직에 따라 적절히 처리하세요.

**관련 주제**  

- **[Aspose.Cells Cloud를 사용하여 비밀번호로 스프레드시트 보호하는 방법](https://docs.aspose.cloud/cells/protect-spreadsheet/).**  
- **[Aspose.Cells Cloud를 사용하여 비밀번호로 스프레드시트 보호를 해제하는 방법](https://docs.aspose.cloud/cells/unprotect-spreadsheet/).**  
---