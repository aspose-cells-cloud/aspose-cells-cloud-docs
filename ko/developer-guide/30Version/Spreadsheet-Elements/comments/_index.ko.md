---
title: "Excel 주석 작업하기"
second_title: "문서"
linktype: "주석"
type: docs
url: /ko/comments/
aliases: [  /ko/working-with-comments/ ]
keywords: "Aspose.Cells Cloud, Excel 주석 API, 스프레드시트 주석, REST API"
description: "Aspose.Cells Cloud REST API v3.0을 사용하여 Excel 주석을 추가, 조회, 업데이트 및 삭제하는 방법을 코드 예제, 필수 조건, 오류 처리와 함께 알아보세요."
weight: 100
ArticleTitle: "Excel 주석 작업하기 – Aspose.Cells Cloud API 가이드"
---

엑셀 워크북을 작성할 때 사용자는 여러 가지 이유로 주석을 추가할 수 있습니다. 가장 흔한 용도는 다른 사용자와 파일을 공유할 때 셀의 수식을 설명하는 것입니다. 주석은 리마인더로 사용하거나 협업자에게 메모를 남기거나 다른 워크북과의 상호 참조 수단으로도 활용할 수 있습니다. 주석을 추가한 후에는 엑셀에서 사용자가 선호하는 스타일에 맞춰 주석 상자의 크기와 모양을 조정하거나 서식을 지정할 수 있습니다. 주석 관리를 숙련하면 이 기능을 최대한 활용할 수 있습니다.

**필수 조건**

- 활성화된 Aspose.Cells Cloud 계정  
- OAuth 2.0을 통해 획득한 유효한 **액세스 토큰**  
- API 버전 **v3.0** (이 가이드에서 사용하는 엔드포인트는 이 버전에 속합니다)  
- 선택 사항: 요청 생성을 간소화하기 위한 선호 언어에 대한 Aspose.Cells SDK

**버전**

아래 예제는 **Aspose.Cells Cloud REST API v3.0**을 대상으로 합니다. 향후 API 릴리스에서는 추가 매개변수가 도입되거나 응답 구조가 변경될 수 있으므로 최신 세부 정보는 항상 최신 API 참조 문서를 확인해야 합니다.

**주석 추가하기**

주석을 추가하려면 다음 엔드포인트로 **POST** 요청을 보냅니다:

```
POST https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments
Authorization: Bearer {access_token}
Content-Type: application/json
```

**경로 매개변수**

| 매개변수  | 유형   | 필수 여부 | 설명                                        |
|-----------|--------|-----------|---------------------------------------------|
| `file`    | string | 예        | 워크북 파일 이름 (확장자 포함)               |
| `sheet`   | string | 예        | 주석을 추가할 워크시트 이름                  |

**요청 본문 스키마**

| 필드       | 유형   | 필수 여부 | 설명                                        |
|------------|--------|-----------|---------------------------------------------|
| `CellName` | string | 예        | 셀의 A1 스타일 주소 (예: **B2**)             |
| `Comment`  | string | 예        | 저장할 주석 텍스트                           |
| `Author`   | string | 아니요    | 주석 작성자 이름                             |

**요청 본문 예시**

```json
{
  "CellName": "B2",
  "Comment": "검토 필요",
  "Author": "John Doe"
}
```

**성공 응답 예시** (`200 OK`)

```json
{
  "Code": 200,
  "Status": "OK",
  "Comment": {
    "CellName": "B2",
    "Author": "John Doe",
    "HtmlComment": "검토 필요",
    "Note": "검토 필요"
  }
}
```

**일반 오류 코드**

| 코드 | 의미                                      |
|------|-------------------------------------------|
| 400  | 잘못된 셀 주소 또는 요청 본문               |
| 401  | 인증되지 않음 – 누락/잘못된 토큰            |
| 404  | 워크북 또는 워크시트를 찾을 수 없음         |

**주석 조회하기**

워크시트에서 모든 주석을 조회합니다:

```
GET https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments
Authorization: Bearer {access_token}
```

**경로 매개변수**

| 매개변수  | 유형   | 필수 여부 | 설명                      |
|-----------|--------|-----------|---------------------------|
| `file`    | string | 예        | 워크북 파일 이름           |
| `sheet`   | string | 예        | 워크시트 이름              |

**응답 예시**

```json
{
  "Code": 200,
  "Status": "OK",
  "Comments": [
    {
      "CellName": "A1",
      "Author": "Alice",
      "HtmlComment": "초기 값",
      "Note": "초기 값"
    },
    {
      "CellName": "B2",
      "Author": "John Doe",
      "HtmlComment": "검토 필요",
      "Note": "검토 필요"
    }
  ]
}
```

**주석 업데이트하기**

기존 주석을 수정하려면 **PUT** 요청을 보냅니다. 주석은 워크시트 주석 컬렉션 내 **인덱스**(0부터 시작)로 식별됩니다.

```
PUT https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments/{commentIndex}
Authorization: Bearer {access_token}
Content-Type: application/json
```

**경로 매개변수**

| 매개변수       | 유형   | 필수 여부 | 설명                             |
|----------------|--------|-----------|----------------------------------|
| `file`         | string | 예        | 워크북 파일 이름                  |
| `sheet`        | string | 예        | 워크시트 이름                     |
| `commentIndex` | int    | 예        | 업데이트할 주석의 0부터 시작하는 인덱스 |

**요청 본문 스키마**

| 필드      | 유형   | 필수 여부 | 설명                       |
|-----------|--------|-----------|----------------------------|
| `Comment` | string | 예        | 새 주석 텍스트              |
| `Author`  | string | 아니요    | 업데이트된 작성자 이름 (선택 사항) |

**요청 본문 예시**

```json
{
  "Comment": "업데이트된 메모 텍스트",
  "Author": "John Doe"
}
```

응답은 **주석 추가하기** 섹션의 응답과 동일한 구조를 따릅니다.

**주석 삭제하기**

인덱스를 사용하여 단일 주석을 삭제합니다:

```
DELETE https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments/{commentIndex}
Authorization: Bearer {access_token}
```

**경로 매개변수**

| 매개변수       | 유형   | 필수 여부 | 설명                             |
|----------------|--------|-----------|----------------------------------|
| `file`         | string | 예        | 워크북 파일 이름                  |
| `sheet`        | string | 예        | 워크시트 이름                     |
| `commentIndex` | int    | 예        | 삭제할 주석의 0부터 시작하는 인덱스 |

성공적인 삭제 시 응답:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**모든 주석 삭제하기**

워크시트에서 모든 주석을 지우려면 다음을 수행합니다:

```
DELETE https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments
Authorization: Bearer {access_token}
```

**경로 매개변수**

| 매개변수  | 유형   | 필수 여부 | 설명                      |
|-----------|--------|-----------|---------------------------|
| `file`    | string | 예        | 워크북 파일 이름           |
| `sheet`   | string | 예        | 워크시트 이름              |

**오류 처리 가이드라인**

- **404 Not Found** – 워크북 ID, 워크시트 이름 및 주석 인덱스가 올바른지 확인합니다.  
- **400 Bad Request** – JSON 구문 및 필수 필드(`CellName`, `Comment`)를 확인합니다.  
- **429 Too Many Requests** – 지수 백오프를 구현하고 `Retry-After` 헤더를 준수합니다.

**요약**

- Excel 주석은 [셀에 메모를 추가하거나 수식을 설명하는 데](/cells/comments/add/) 사용됩니다.  
- Excel은 사용자가 워크시트에서 주석을 [편집](/cells/comments/update/), [삭제](/cells/comments/delete/), [표시](/cells/comments/get/) 또는 [숨김](/cells/comments/update/)할 수 있는 유연성을 제공합니다.  
- 사용자는 주석 상자의 [크기 조정](/cells/comments/update/) 및 [이동](/cells/comments/update/)도 할 수 있습니다.  

다른 스프레드시트 요소 작업에 대한 자세한 내용은 [셀 작업 가이드](/cells/working-with-cells/)를 참조하세요.