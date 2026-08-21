---
title: "Aspose.Cells Cloud API – CellsObjectOperate 작업 사용하기 (REST)"
second_title: "문서"
type: docs
url: /tasks/cells-object-operate/
aliases: [/working-with-cellsobjectoperate-task/]
description: "Aspose.Cells Cloud API에서 CellsObjectOperate 작업을 사용하는 방법을 배워보세요. 매개변수 참조, 요청/응답 예제, 워크시트, 차트, 피벗 테이블 작업 시 적용할 수 있는 모범 사례 팁을 제공합니다."
weight: 20
ArticleTitle: "Aspose.Cells Cloud API – CellsObjectOperate 작업 사용하기 (REST)"
keywords:
  - "Aspose CellsObjectOperate"
  - "CellsObjectOperate 작업"
  - "Aspose.Cells Cloud API"
  - "Excel REST API"
  - "차트 작업"
  - "피벗 테이블 API"
  - "페이지 나눔선 API"
---

**개요**  
**CellsObjectOperate** 작업을 사용하면 워크북, 워크시트, 차트, 피벗 테이블, 도형, 페이지 나눔선 등 Excel 개체에 대해 단일 REST 호출로 생성(Create), 읽기(Read), 업데이트(Update), 삭제(Delete) (CRUD) 작업을 수행할 수 있습니다. `OperateObjectType`으로 개체 유형을 지정하고, 해당하는 매개변수 블록(예: 차트 관련 작업 시 `ChartOperateParameter`)을 제공합니다.

---

**OperateObject**

| 매개변수 이름           | 유형   | 설명 |
| ----------------------- | ------ | ----------- |
| OperateObjectType       | string | 작업을 수행할 Excel 개체 유형입니다. 허용 값: `Workbook`, `Worksheet`, `PageSetup`, `Cells`, `Chart`, `Shape`, `ListObject`, `PivotTable`, `WorkbookSettings`, `PageBreak`. |
| OperateObjectPosition   | object | 대상 개체의 위치를 식별하는 컨테이너입니다(예: 워크북 이름, 워크시트 이름, 차트 인덱스). 대부분의 작업에서 필요합니다. |

**OperateObjectPosition**

| 매개변수 이름  | 유형   | 설명 |
| -------------- | ------ | ----------- |
| Workbook       | object | 대상 개체를 포함하는 워크북입니다. `FileName`(클라우드 저장소) 또는 `FileContent`(Base64 인코딩) 중 하나를 반드시 포함해야 합니다. |
| SheetName      | string | 작업을 적용할 워크시트의 이름입니다. 워크시트 수준 개체(차트, 도형 등)에 필요합니다. |
| ChartIndex     | integer| 워크시트 내 차트의 0부터 시작하는 인덱스입니다. (`OperateObjectType`이 `Chart`인 경우 사용) |
| ShapeIndex     | integer| 워크시트 내 도형의 0부터 시작하는 인덱스입니다. (`OperateObjectType`이 `Shape`인 경우 사용) |
| CellName       | string | A1 스타일의 셀 참조(예: `A1`)입니다. 셀 수준 작업에 사용됩니다. |
| ListObjectIndex| integer| 목록 개체의 0부터 시작하는 인덱스입니다. (`OperateObjectType`이 `ListObject`인 경우 사용) |

**ChartOperateParameter**

| 매개변수 이름         | 유형    | 설명 |
| --------------------- | ------- | ----------- |
| ChartIndex            | integer | 수정할 차트의 인덱스입니다. 기존 차트를 업데이트할 때 필요합니다. |
| ChartType             | string  | 생성할 차트 유형(예: `Bar`, `Line`, `Pie`)입니다. |
| UpperLeftRow          | integer | 차트 왼쪽 상단 코너의 행 번호(0부터 시작)입니다. |
| UpperLeftColumn       | integer | 차트 왼쪽 상단 코너의 열 번호(0부터 시작)입니다. |
| LowerRightRow         | integer | 차트 오른쪽 하단 코너의 행 번호입니다. |
| LowerRightColumn      | integer | 차트 오른쪽 하단 코너의 열 번호입니다. |
| Area                  | string  | 차트의 데이터 범위(예: `A1:B5`)입니다. |
| IsVertical            | string  | 차트 방향이 수직이면 `true`, 그렇지 않으면 `false`입니다. |
| CategoryData          | string  | 범주(X축) 레이블을 제공하는 범위입니다. |
| IsAutoGetSerialName   | string  | 시리즈 이름을 자동으로 생성하려면 `true`, 사용자 정의 이름을 사용하려면 `false`입니다. |
| Title                 | string  | 차트에 표시될 제목 텍스트입니다. |

**ListObjectOperateParameter**

| 매개변수 이름 | 유형   | 설명 |
| -------------- | ------ | ----------- |
| ListObject     | object | 목록(테이블) 작업을 위한 구성 개체입니다. `ShowHeader`, `ShowTotal`, `Style` 등의 속성을 포함합니다. |

**PageBreakOperateParameter**

| 매개변수 이름 | 유형    | 설명 |
| -------------- | ------- | ----------- |
| PageBreakType  | string  | 페이지 나눔선 유형(`Horizontal` 또는 `Vertical`)입니다. |
| Index          | integer | 삭제 또는 수정할 페이지 나눔선의 0부터 시작하는 인덱스입니다. |
| Row            | integer | 수평 페이지 나눔선을 배치할 행 번호입니다. |
| Column         | integer | 수직 페이지 나눔선을 배치할 열 번호입니다. |
| StartIndex     | integer | 범위 기반 페이지 나눔 작업의 시작 인덱스입니다. |
| EndIndex       | integer | 범위 기반 페이지 나눔 작업의 끝 인덱스입니다. |

**PageSetupOperateParameter**

| 매개변수 이름 | 유형   | 설명 |
| -------------- | ------ | ----------- |
| PageSetup      | object | 페이지 레이아웃 설정(여백, 방향, 용지 크기 등)입니다. |

**PivotTableOperateParameter**

| 매개변수 이름    | 유형        | 설명 |
| ---------------- | ----------- | ----------- |
| DestCellName     | string      | 피벗 테이블의 대상 범위 왼쪽 상단 셀(예: `C5`)입니다. |
| SourceData       | string      | 피벗 테이블의 원본 범위(예: `A1:D100`)입니다. |
| TableName        | string      | 생성된 피벗 테이블에 할당된 이름입니다. |
| UseSameSource    | string      | 기존 원본 범위를 재사용하려면 `true`, 새 범위를 생성하려면 `false`입니다. |
| PivotTableIndex  | integer     | 업데이트할 피벗 테이블의 인덱스입니다. (수정/삭제 작업 시 필요) |
| PivotFieldRows   | integer[]   | 행 영역에 표시될 필드 인덱스 컬렉션입니다. |
| PivotFieldColumns| integer[]   | 열 영역에 표시될 필드 인덱스 컬렉션입니다. |
| PivotFieldData   | integer[]   | 데이터 영역에 표시될 필드 인덱스 컬렉션입니다. |

**ShapeOperateParameter**

| 매개변수 이름 | 유형   | 설명 |
| -------------- | ------ | ----------- |
| Shape          | object | 도형의 정의(유형, 위치, 크기, 텍스트 등)입니다. |

**WorkbookSettingsOperateParameter**

| 매개변수 이름    | 유형   | 설명 |
| ---------------- | ------ | ----------- |
| WorkbookSettings | object | 전체 워크북에 영향을 주는 설정(예: 계산 모드, 정밀도)입니다. |

**WorksheetOperateParameter**

| 매개변수 이름 | 유형   | 설명 |
| -------------- | ------ | ----------- |
| Name           | string | 작업을 수행할 현재 워크시트의 이름입니다. |
| SheetType      | string | 시트 유형(`Worksheet`, `Chart` 등)입니다. |
| NewName        | string | 워크시트 이름을 변경할 때의 새 이름입니다. |
| MovingRequest  | object | 워크시트 이동을 위한 매개변수(예: `FromIndex`, `ToIndex`)입니다. |

## REST API

| API                | Type | 설명 | 리소스 링크 |
| ------------------ | ---- | ----------- | ------------- |
| /cells/task/runtask| POST | 작업 실행    | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

### 필수 조건
- **인증** – 유효한 `Authorization: Bearer <access_token>` 헤더를 포함해야 합니다.  
- **저장소** – 원본 워크북은 Aspose Cloud 저장소에 저장되어 있어야 하거나, 요청 본문에 Base64로 인코딩된 콘텐츠로 제공되어야 합니다.  
- **API 버전** – 본 문서는 Aspose.Cells Cloud API의 **v3.0**을 대상으로 합니다.

### 샘플 요청(cURL)

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "OperateObject": {
               "OperateObjectType": "Chart",
               "OperateObjectPosition": {
                   "Workbook": { "FileName": "Sample.xlsx" },
                   "SheetName": "Sheet1"
               }
           },
           "ChartOperateParameter": {
               "ChartType": "Bar",
               "UpperLeftRow": 5,
               "UpperLeftColumn": 2,
               "LowerRightRow": 15,
               "LowerRightColumn": 8,
               "Area": "A1:B5",
               "Title": "Sales Chart",
               "IsVertical": "true"
           }
         }'
```

요청 본문은 아래에 정의된 **CellsObjectOperateRequest** 스키마를 따릅니다:

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "title": "CellsObjectOperateRequest",
  "type": "object",
  "required": ["OperateObject"],
  "properties": {
    "OperateObject": {
      "type": "object",
      "required": ["OperateObjectType"],
      "properties": {
        "OperateObjectType": { "type": "string", "enum": ["Workbook","Worksheet","PageSetup","Cells","Chart","Shape","ListObject","PivotTable","WorkbookSettings","PageBreak"] },
        "OperateObjectPosition": { "$ref": "#/definitions/OperateObjectPosition" }
      }
    },
    "ChartOperateParameter": { "$ref": "#/definitions/ChartOperateParameter" },
    "ListObjectOperateParameter": { "$ref": "#/definitions/ListObjectOperateParameter" },
    "PageBreakOperateParameter": { "$ref": "#/definitions/PageBreakOperateParameter" },
    "PageSetupOperateParameter": { "$ref": "#/definitions/PageSetupOperateParameter" },
    "PivotTableOperateParameter": { "$ref": "#/definitions/PivotTableOperateParameter" },
    "ShapeOperateParameter": { "$ref": "#/definitions/ShapeOperateParameter" },
    "WorkbookSettingsOperateParameter": { "$ref": "#/definitions/WorkbookSettingsOperateParameter" },
    "WorksheetOperateParameter": { "$ref": "#/definitions/WorksheetOperateParameter" }
  },
  "definitions": {
    "OperateObjectPosition": {
      "type": "object",
      "properties": {
        "Workbook": { "type": "object" },
        "SheetName": { "type": "string" },
        "ChartIndex": { "type": "integer" },
        "ShapeIndex": { "type": "integer" },
        "CellName": { "type": "string" },
        "ListObjectIndex": { "type": "integer" }
      }
    },
    "ChartOperateParameter": {
      "type": "object",
      "properties": {
        "ChartIndex": { "type": "integer" },
        "ChartType": { "type": "string" },
        "UpperLeftRow": { "type": "integer" },
        "UpperLeftColumn": { "type": "integer" },
        "LowerRightRow": { "type": "integer" },
        "LowerRightColumn": { "type": "integer" },
        "Area": { "type": "string" },
        "IsVertical": { "type": "string", "enum": ["true","false"] },
        "CategoryData": { "type": "string" },
        "IsAutoGetSerialName": { "type": "string", "enum": ["true","false"] },
        "Title": { "type": "string" }
      }
    }
    /* 추가 정의는 간결함을 위해 생략 */
  }
}
```

### 샘플 응답 (성공 – 200)

```json
{
  "Code": 200,
  "Status": "OK",
  "TaskId": "d9f2c4a1-5b6e-4a9c-8f2a-7e3b9c0e5f1a",
  "Result": {
    "ChartId": 0,
    "Message": "차트가 성공적으로 생성되었습니다."
  }
}
```

응답에는 다음 필드가 포함됩니다:

| 필드     | 유형   | 설명 |
| ------- | ------ | ----------- |
| Code    | integer| 작업 엔진에서 반환된 HTTP 유사 상태 코드입니다. |
| Status  | string | 사람이 읽을 수 있는 상태(예: `OK`)입니다. |
| TaskId  | string | 비동기 작업의 식별자입니다. |
| Result  | object | 작업 고유 결과를 보유하는 객체입니다. |
| Result.ChartId | integer | 생성 또는 수정된 차트의 식별자입니다. |
| Result.Message | string | 결과를 설명하는 간단한 메시지입니다. |

### 오류 처리

| HTTP 상태 | 오류 코드 | 설명 | 권장 해결 방법 |
| ----------- | ---------- | ----------- | ---------------- |
| 400         | InvalidParameter | 하나 이상의 요청 매개변수가 누락되었거나 잘못된 형식입니다. | 필수 필드와 데이터 유형을 확인하세요. |
| 401         | Unauthorized | 잘못되었거나 누락된 인증 토큰입니다. | 액세스 토큰을 갱신하고 `Authorization` 헤더에 포함하세요. |
| 404         | NotFound | 지정된 워크북, 워크시트 또는 개체가 존재하지 않습니다. | `FileName`, `SheetName`, 개체 인덱스를 확인하세요. |
| 500         | ServerError | 서버에서 예기치 않은 오류가 발생했습니다. | 요청을 재시도하고, 문제가 지속되면 지원팀에 문의하세요. |

### 일반적인 사용 사례
- 워크시트에 새 차트를 추가합니다.  
- 워크시트 이름을 변경합니다(`OperateObjectType = "Worksheet"` 및 `WorksheetOperateParameter.NewName` 사용).  
- 페이지 나눔선을 삽입합니다(`OperateObjectType = "PageBreak"` 및 `PageBreakOperateParameter` 사용).  
- 피벗 테이블의 원본 데이터를 업데이트합니다(`OperateObjectType = "PivotTable"` 및 `PivotTableOperateParameter.SourceData` 사용).  
- 계산 모드 등 워크북 설정을 수정합니다(`OperateObjectType = "WorkbookSettings"` 사용).  

---  

*모든 설명은 공식 Aspose.Cells Cloud OpenAPI 사양에서 파생되었습니다.*