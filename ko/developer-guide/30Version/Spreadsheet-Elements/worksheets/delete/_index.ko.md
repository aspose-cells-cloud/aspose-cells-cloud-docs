---
title: "Excel 워크시트 삭제 작업 방법"
second_title: "문서"
linktitle: "삭제"
type: docs
url: /ko/worksheets/delete/
keywords: "Aspose.Cells, 클라우드, REST API, 워크시트 삭제, Excel, C#, Java, Python"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크북에서 단일 또는 여러 워크시트를 삭제하는 방법을 알아보세요. C#, Java, Python 예제, 사전 준비 사항, 오류 처리 팁 및 관련 작업을 포함합니다."
weight: 20
ArticleTitle: "Aspose.Cells Cloud API로 Excel 워크북에서 워크시트 삭제하기"
---

## Excel 워크북에서 워크시트 삭제 작업하기

애플리케이션이 Excel 파일을 동적으로 생성하거나 수정할 때, 더 이상 필요하지 않은 워크시트를 제거해야 할 수 있습니다—예를 들어, 임시 보고서, 임시 시트, 오래된 데이터 등이 해당됩니다. Aspose.Cells Cloud API는 하나의 요청으로 단일 워크시트 또는 여러 워크시트를 쉽게 삭제할 수 있도록 지원합니다.

**API 참조**  

| 항목 | 세부 정보 |
|------|-----------|
| **HTTP 메서드** | `DELETE` |
| **엔드포인트** | `/cells/{fileName}/worksheets` |
| **경로 매개변수** | `fileName` – Excel 파일 이름 (필수) |
| **쿼리 매개변수** | `sheetName` – 삭제할 워크시트 이름 (선택 사항, 단일 워크시트 삭제 시 사용) <br> `folder` – 스토리지 내 소스 폴더 경로 (선택 사항) <br> `storage` – 사용할 스토리지 이름 (선택 사항) |
| **요청 본문** | *없음* |
| **성공 응답** | `200 OK` – 워크시트가 성공적으로 삭제되었습니다. 작업 상태를 담은 JSON 객체를 반환합니다. |
| **오류 응답** | `400 Bad Request` – 잘못된 매개변수 <br> `401 Unauthorized` – 인증 실패 <br> `404 Not Found` – 파일 또는 워크시트를 찾을 수 없음 <br> `500 Internal Server Error` – 서버 내부 오류 |

**요청**  

하나 이상의 워크시트를 삭제하려면 위의 엔드포인트로 `DELETE` 요청을 보내고, 필수 `fileName`과 선택적으로 단일 워크시트 삭제를 위한 `sheetName` 쿼리 매개변수를 포함해야 합니다. `sheetName`을 생략하면 워크북의 모든 워크시트가 삭제됩니다.

**매개변수**  

- `fileName` (문자열, 필수): 확장자를 포함한 Excel 파일 이름.  
- `sheetName` (문자열, 선택 사항): 삭제할 특정 워크시트 이름. 생략 시 API는 모든 워크시트를 삭제합니다.  
- `folder` (문자열, 선택 사항): 스토리지 내 파일이 위치한 폴더 경로.  
- `storage` (문자열, 선택 사항): 사용할 Aspose Cloud 스토리지 이름.

**응답**  

- **200 OK** – 예시 JSON:  
  ```json
  {
    "code": 200,
    "status": "OK",
    "message": "워크시트가 성공적으로 삭제되었습니다."
  }
  ```
- **400 Bad Request** – 잘못된 요청 매개변수.  
- **401 Unauthorized** – 인증 토큰 누락 또는 유효하지 않음.  
- **404 Not Found** – 지정된 파일 또는 워크시트가 존재하지 않음.  
- **500 Internal Server Error** – 예기치 않은 서버 오류.

**예제**  

*아래는 세 가지 인기 언어를 사용하여 삭제 엔드포인트를 호출하는 방법을 보여주는 짧은 코드 스니펫입니다.*

**C# 예제**  
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Client;
using Aspose.Cells.Cloud.SDK.Model;

var api = new CellsApi("client_id", "client_secret");
var fileName = "Sample.xlsx";
var sheetName = "TempSheet";

try
{
    var response = api.DeleteWorksheet(fileName, sheetName);
    Console.WriteLine($"상태: {response.Status}");
}
catch (Exception ex)
{
    Console.WriteLine($"오류: {ex.Message}");
}
```

**Java 예제**  
```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.ResponseMessage;

public class DeleteWorksheetDemo {
    public static void main(String[] args) throws Exception {
        CellsApi api = new CellsApi("client_id", "client_secret");
        String fileName = "Sample.xlsx";
        String sheetName = "TempSheet";

        try {
            ResponseMessage response = api.deleteWorksheet(fileName, sheetName, null, null);
            System.out.println("상태: " + response.getStatus());
        } catch (Exception e) {
            System.err.println("오류: " + e.getMessage());
        }
    }
}
```

**Python 예제**  
```python
from asposecellscloud import CellsApi, ApiException

api = CellsApi(client_id="client_id", client_secret="client_secret")
file_name = "Sample.xlsx"
sheet_name = "TempSheet"

try:
    response = api.delete_worksheet(file_name, sheet_name)
    print(f"상태: {response.status}")
except ApiException as e:
    print(f"오류: {e}")
```

**오류 처리**  

- 요청 전에 인증 토큰이 유효한지 확인하세요.  
- 응답 상태 코드를 확인하고, `400`, `401`, `404`, `500`에 대해 적절히 처리하세요.  
- 네트워크 또는 SDK 예외를 캡처하기 위해 try-catch 블록(또는 해당 구문)을 사용하세요.

**관련 작업**  

- [워크시트 추가](/ko/worksheets/add/) – 기존 워크북에 새 워크시트를 생성합니다.  
- [워크시트 복사](/ko/worksheets/copy/) – 기존 워크시트를 복제합니다.  
- [워크시트 이름 변경](/ko/worksheets/rename/) – 워크시트 이름을 변경합니다.  
- [워크시트 이동](/ko/worksheets/move/) – 워크북 내에서 워크시트 순서를 재정렬합니다.  
---