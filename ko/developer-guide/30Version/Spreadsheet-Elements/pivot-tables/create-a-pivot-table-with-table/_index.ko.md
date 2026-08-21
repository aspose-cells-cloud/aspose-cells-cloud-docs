---
title: "표를 피벗 테이블로 변환"
second_title: "문서"
linktitle: 변환
type: docs
url: /ko/pivot-tables/convert-table-to-pivottable/
aliases:
  [
    "/create-a-pivottable-with-table/",
    "/create-new-pivot-table-with-list-object-as-source-data/",
  ]
keywords: "피벗 테이블, 목록 객체, Aspose.Cells Cloud, REST API, 표를 피벗 테이블로 변환"
description: "Aspose.Cells Cloud REST API를 사용하여 목록 객체에서 피벗 테이블을 만드는 방법을 배웁니다. 요청 세부 정보, cURL 예제, SDK 참조를 포함합니다."
weight: 60
ArticleTitle: "표를 피벗 테이블로 변환 – Aspose.Cells Cloud 문서"
---

이 REST API는 목록 객체에서 **피벗 테이블**을 생성합니다.

피벗 테이블은 목록 객체의 데이터를 요약하여 워크시트 내에서 직접 대규모 데이터 세트를 분석하고 보고할 수 있도록 해줍니다.

**필수 조건:**  
- 인증을 위한 유효한 JWT 베어러 토큰  
- 워크북이 지정된 저장소 위치에 존재해야 함  
- 대상 워크시트에 요약하려는 목록 객체가 포함되어 있어야 함  

## PostWorksheetListObjectSummarizeWithPivotTable API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/SummarizeWithPivotTable
```

### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **요청 매개변수**

| 매개변수 이름   | 유형    | 위치 | 설명                                   |
| --------------- | ------- | ---- | -------------------------------------- |
| name            | string  | path | 워크북 파일 이름                       |
| sheetName       | string  | path | 목록 객체가 포함된 워크시트 이름       |
| listObjectIndex | integer | path | 워크시트 내 목록 객체의 인덱스         |
| destsheetName   | string  | query | 대상 워크시트 이름                    |
| request         | object  | body | 피벗 테이블을 정의하는 JSON 페이로드   |
| folder          | string  | query | 워크북이 위치한 폴더 경로             |
| storageName     | string  | query | 저장소 이름                           |

요청 본문은 아래에 정의된 JSON 스키마를 따라야 합니다:

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "type": "object",
  "properties": {
    "Name": { "type": "string", "description": "새 피벗 테이블의 이름." },
    "DestCellName": { "type": "string", "description": "피벗 테이블의 좌상단 셀 (예: \"C1\")." },
    "PivotFieldRows": {
      "type": "array",
      "items": { "type": "integer" },
      "description": "행에 배치할 필드의 0부터 시작하는 인덱스."
    },
    "PivotFieldColumns": {
      "type": "array",
      "items": { "type": "integer" },
      "description": "열에 배치할 필드의 0부터 시작하는 인덱스."
    },
    "PivotFieldData": {
      "type": "array",
      "items": { "type": "integer" },
      "description": "데이터 필드로 사용할 필드의 0부터 시작하는 인덱스."
    }
  },
  "required": ["Name", "DestCellName", "PivotFieldRows", "PivotFieldColumns", "PivotFieldData"]
}
```

<a href="https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObjectSummarizeWithPivotTable" rel="noopener noreferrer">OpenAPI 사양</a>은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

**cURL** 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API에 요청하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/TestCase.xlsx/worksheets/Sheet2/listobjects/0/SummarizeWithPivotTable?folder=CellsTests&destsheetName=Sheet4" \
-X POST \
-d '{"Name":"TestPivot","DestCellName":"C1","PivotFieldRows":[0,1],"PivotFieldColumns":[2],"PivotFieldData":[3,4]}' \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

*참고: 실제 운영 환경에서는 프로덕션 엔드포인트(`api.aspose.cloud`)를 사용하세요. QA 엔드포인트(`api-qa.aspose.cloud`)는 테스트 목적으로만 사용됩니다. 모든 프로덕션 호출은 HTTPS를 사용해야 합니다.*

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**HTTP 상태 코드**

| 코드 | 의미                         | 설명                                             |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함 |
| 400  | Bad Request                 | 누락되거나 잘못된 매개변수 (예: 지원되지 않는 파일 형식) |
| 401  | Unauthorized                | 잘못되거나 누락된 JWT 토큰                         |
| 413  | Payload Too Large           | 업로드된 파일이 크기 제한을 초과함                 |
| 500  | Internal Server Error       | 예기치 않은 서버 오류                              |

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 요청을 보내는 방법을 보여줍니다: