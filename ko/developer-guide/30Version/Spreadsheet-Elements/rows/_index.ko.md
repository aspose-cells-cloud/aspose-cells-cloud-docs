---
title: "Excel 행 작업 – Aspose.Cells Cloud API"
ArticleTitle: "Excel 행 작업 – Aspose.Cells Cloud API"
second_title: "문서"
linktitle: "행"
type: docs
url: /ko/rows/
aliases: [  /ko/working-with-rows/ ]
keywords: "Aspose.Cells, Excel 행, REST API, 스프레드시트 조작"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 파일의 행을 조작합니다. Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby, Swift를 지원합니다."
weight: 100
---

## Excel 파일에서 행 작업하기

**최종 업데이트: 2026년 7월**

- [Excel 워크시트에서 행 정보를 얻는 방법.](/cells/rows/get/row/)
- [Excel 워크시트에 빈 행을 추가하는 방법.](/cells/rows/add/row/)
- [Excel 워크시트에서 행을 복사하는 방법.](/cells/rows/copy/)
- [Excel 워크시트에서 행을 숨기는 방법.](/cells/rows/hide/)
- [Excel 워크시트에서 행을 다시 보이게 하는 방법.](/cells/rows/unhide/)
- [Excel 워크시트에서 행을 그룹화하는 방법.](/cells/rows/group/)
- [Excel 워크시트에서 행 그룹을 해제하는 방법.](/cells/rows/ungroup/)
- [워크시트에서 행을 삭제하는 방법](/cells/rows/delete/)

일반적인 행 작업을 위한 빠른 API 참조:

| 작업   | HTTP 메서드 | 엔드포인트                                                               | 주요 파라미터                         |
|-------|-----------|------------------------------------------------------------------------|--------------------------------------|
| [행 정보 조회](https://docs.aspose.cloud/cells/rows/get/row/)     | GET         | `/cells/{fileName}/worksheets/{sheetName}/rows/{rowIndex}`            | `fileName`, `sheetName`, `rowIndex`    |
| [행 추가](https://docs.aspose.cloud/cells/rows/add/row/)     | POST        | `/cells/{fileName}/worksheets/{sheetName}/rows`                       | `rowIndex`, `height`                   |
| [행 복사](https://docs.aspose.cloud/cells/rows/copy/)      | POST        | `/cells/{fileName}/worksheets/{sheetName}/rows/copy`                  | `sourceIndex`, `destinationIndex`, `rowCount` |
| [행 삭제](https://docs.aspose.cloud/cells/rows/delete/)   | DELETE      | `/cells/{fileName}/worksheets/{sheetName}/rows/{rowIndex}`            | `fileName`, `sheetName`, `rowIndex`    |
| [행 숨기기](https://docs.aspose.cloud/cells/rows/hide/)      | POST        | `/cells/{fileName}/worksheets/{sheetName}/rows/hide`                  | `startIndex`, `endIndex`               |
| [행 보이기](https://docs.aspose.cloud/cells/rows/unhide/)  | POST        | `/cells/{fileName}/worksheets/{sheetName}/rows/unhide`                | `startIndex`, `endIndex`               |
| [행 그룹화](https://docs.aspose.cloud/cells/rows/group/)    | POST        | `/cells/{fileName}/worksheets/{sheetName}/rows/group`                 | `startIndex`, `endIndex`               |
| [행 그룹 해제](https://docs.aspose.cloud/cells/rows/ungroup/)| POST        | `/cells/{fileName}/worksheets/{sheetName}/rows/ungroup`               | `startIndex`, `endIndex`               |

**요청 / 응답 세부 정보**

- **행 정보 조회**  
  *요청*: 본문 불필요.  
  *응답 (200)*:  
  ```json
  {
    "RowIndex": 5,
    "Height": 15.0,
    "IsHidden": false,
    "Style": { ... }
  }
  ```  
  *오류*: 400 Bad Request(잘못된 인덱스), 404 Not Found(파일 또는 시트 없음).

- **행 추가**  
  *요청 본문(JSON)*:  
  ```json
  {
    "RowIndex": 10,
    "Height": 20.0
  }
  ```  
  *응답 (201)*:  
  ```json
  { "Code": "Success", "Status": "Row added", "RowIndex": 10 }
  ```  
  *오류*: 400 Bad Request(누락되거나 잘못된 파라미터), 401 Unauthorized.

- **행 복사**  
  *요청 본문(JSON)*:  
  ```json
  {
    "SourceIndex": 2,
    "DestinationIndex": 8,
    "RowCount": 3
  }
  ```  
  *응답 (200)*:  
  ```json
  { "Code": "Success", "Status": "Rows copied" }
  ```  
  *오류*: 400 Bad Request, 404 Not Found.

- **행 삭제**  
  *요청*: 본문 불필요.  
  *응답 (200)*:  
  ```json
  { "Code": "Success", "Status": "Row deleted", "RowIndex": 7 }
  ```  
  *오류*: 400 Bad Request, 404 Not Found.

- **행 숨기기**  
  *요청 본문(JSON)*:  
  ```json
  { "StartIndex": 3, "EndIndex": 5 }
  ```  
  *응답 (200)*: `{ "Code": "Success", "Status": "Rows hidden" }`  
  *오류*: 400 Bad Request.

- **행 보이기** – *행 숨기기*와 동일한 요청 본문; 응답은 동일하며 상태는 “Rows unhidden”입니다.

- **행 그룹화** – *행 숨기기*와 동일한 요청 본문; 응답 상태는 “Rows grouped”입니다.

- **행 그룹 해제** – *행 숨기기*와 동일한 요청 본문; 응답 상태는 “Rows ungrouped”입니다.

모든 작업은 유효한 OAuth 2.0/JWT 액세스 토큰과 적절한 SDK 버전이 필요합니다.