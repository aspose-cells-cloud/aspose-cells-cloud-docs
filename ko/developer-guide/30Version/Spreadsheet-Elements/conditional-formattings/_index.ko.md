---
title: "Excel 조건부 서식 작업"
second_title: "문서"
linktitle: "조건부 서식"
type: docs
url: /conditional-formattings/
aliases: [/working-with-conditional-formatting/]
keywords: "Excel, 조건부 서식, Aspose.Cells Cloud, API"
description: "Aspose.Cells Cloud API는 엑셀에서 조건부 서식 규칙을 검색, 추가, 수정 및 삭제할 수 있는 엔드포인트를 제공하여 워크시트 데이터의 동적 시각적 분석을 가능하게 합니다."
weight: 100
ArticleTitle: "Excel 조건부 서식 작업 – API 가이드"
---

Excel의 조건부 서식 기능은 셀 값에 따라 특정 색상으로 셀을 강조 표시할 수 있도록 해줍니다.

조건부 서식을 사용하여 데이터를 시각적으로 탐색하고 분석하고, 중요한 문제를 감지하며, 패턴과 추세를 식별할 수 있습니다.

조건부 서식을 사용하면 흥미로운 셀이나 셀 범위를 쉽게 강조 표시하고, 비정상적인 값을 강조하며, 데이터 막대, 색상 척도, 데이터 변화에 따라 다른 아이콘 세트 등을 사용하여 데이터를 시각화할 수 있습니다.

조건부 서식은 지정한 조건에 따라 셀의 외관을 변경합니다. 조건이 참이면 셀 범위가 서식이 적용되고, 조건이 거짓이면 셀 범위는 변경되지 않습니다. 내장된 조건은 많으며, 필요에 따라 직접 조건을 만들 수도 있습니다(특정 수식을 사용하여 **TRUE** 또는 **FALSE**를 평가하도록 설정 가능).

Aspose.Cells Cloud API는 프로그래밍 방식으로 조건부 서식 규칙을 관리할 수 있는 일련의 엔드포인트를 제공합니다. 다음 작업을 사용할 수 있습니다:

- **워크시트의 조건부 서식 가져오기** – 워크시트에 적용된 모든 조건부 서식 규칙을 검색합니다.  
  - **메서드:** `GET`  
  - **엔드포인트:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings`  
  - **매개변수:** `fileName`(문자열, 필수), `sheetName`(문자열, 필수), 선택적 쿼리 매개변수(예: `folder`, `storageName`)  
  - **cURL 예시:**  
    ```bash
    curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings?folder=Docs&storageName=MyStorage" -H "Authorization: Bearer {access_token}"
    ```
- **조건부 서식 가져오기** – 지정된 식별자로 특정 조건부 서식 규칙을 반환합니다.  
  - **메서드:** `GET`  
  - **엔드포인트:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}`  
  - **매개변수:** `index`(정수, 필수)는 규칙의 위치를 식별합니다.  
  - **cURL 예시:**  
    ```bash
    curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0" -H "Authorization: Bearer {access_token}"
    ```
- **서식 조건용 셀 영역 추가** – 지정된 조건부 서식이 적용될 셀 범위를 추가합니다.  
  - **메서드:** `POST`  
  - **엔드포인트:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}/cellarea`  
  - **요청 본문(JSON):** `{ "FirstRow": 1, "FirstColumn": 1, "RowCount": 5, "ColumnCount": 3 }`  
  - **cURL 예시:**  
    ```bash
    curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0/cellarea" \
         -H "Authorization: Bearer {access_token}" \
         -H "Content-Type: application/json" \
         -d '{"FirstRow":1,"FirstColumn":1,"RowCount":5,"ColumnCount":3}'
    ```
- **서식 조건용 조건 추가** – 기존 서식 규칙에 새 조건(예: 값, 수식)을 정의합니다.  
  - **메서드:** `POST`  
  - **엔드포인트:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}/condition`  
  - **요청 본문(JSON):** `{ "Type": "CellValue", "Operator": "GreaterThan", "Formula1": "100" }`  
  - **cURL 예시:**  
    ```bash
    curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0/condition" \
         -H "Authorization: Bearer {access_token}" \
         -H "Content-Type: application/json" \
         -d '{"Type":"CellValue","Operator":"GreaterThan","Formula1":"100"}'
    ```
- **서식 조건 추가** – 유형 및 스타일을 포함한 완전한 조건부 서식 규칙을 생성합니다.  
  - **메서드:** `POST`  
  - **엔드포인트:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings`  
  - **요청 본문(JSON):**  
    ```json
    {
      "Priority": 0,
      "Type": "HighlightCells",
      "Style": { "ForegroundColor": "FFFF0000" },
      "Condition": { "Operator": "LessThan", "Formula1": "50" },
      "CellArea": { "FirstRow": 0, "FirstColumn": 0, "RowCount": 10, "ColumnCount": 5 }
    }
    ```  
  - **cURL 예시:**  
    ```bash
    curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings" \
         -H "Authorization: Bearer {access_token}" \
         -H "Content-Type: application/json" \
         -d @condition.json
    ```
- **모든 조건부 서식 지우기** – 대상 워크시트에서 모든 조건부 서식 규칙을 제거합니다.  
  - **메서드:** `DELETE`  
  - **엔드포인트:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings`  
  - **cURL 예시:**  
    ```bash
    curl -X DELETE "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings" -H "Authorization: Bearer {access_token}"
    ```
- **조건부 서식에서 셀 영역 제거** – 조건부 서식 규칙에서 이전에 정의한 셀 영역을 삭제합니다.  
  - **메서드:** `DELETE`  
  - **엔드포인트:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}/cellarea`  
  - **cURL 예시:**  
    ```bash
    curl -X DELETE "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0/cellarea" -H "Authorization: Bearer {access_token}"
    ```
- **조건부 서식 제거** – 워크시트에서 전체 조건부 서식 규칙을 삭제합니다.  
  - **메서드:** `DELETE`  
  - **엔드포인트:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}`  
  - **cURL 예시:**  
    ```bash
    curl -X DELETE "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0" -H "Authorization: Bearer {access_token}"
    ```

위 예시는 각 작업에 필요한 HTTP 메서드, URL 패턴, 주요 매개변수 및 요청 페이로드 샘플을 보여줍니다. 필요하다면 언어별 코드 스니펫을 위해 적절한 SDK(C#, Java, Python 등)를 사용할 수 있습니다.