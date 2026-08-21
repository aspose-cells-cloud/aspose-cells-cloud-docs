---
title: "엑셀 워크시트에서 행 삭제 작업하기"
second_title: "Document"
linktitle: "삭제"
type: docs
url: /ko/rows/delete/
keywords: "Aspose.Cells, 행 삭제, Excel API, REST, 클라우드, 스프레드시트, 엑셀, SDK"
description: "Aspose.Cells Cloud REST API를 사용하여 엑셀 워크시트에서 단일 행 또는 여러 행을 삭제하는 방법을 배워보세요. Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby, Swift 등에 대한 코드 예제가 포함되어 있습니다."
weight: 20
ArticleTitle: "엑셀 워크시트에서 행 삭제 작업하기 – Aspose.Cells Cloud API 가이드"
---

## 사용 가능한 삭제 작업

다음 예제는 Aspose.Cells Cloud REST API를 사용하여 엑셀 워크시트에서 빈 행 하나 또는 여러 행을 삭제하는 방법을 설명합니다.

- [엑셀 워크시트에서 빈 행 삭제하는 방법](/cells/rows/delete/row/)
- [엑셀 워크시트에서 여러 행 삭제하는 방법](/cells/rows/delete/rows/)

**API 참조**

| 항목                | 세부 정보 |
|---------------------|---------------------------------------------------------------|
| **HTTP 메서드**     | DELETE |
| **엔드포인트**        | `/cells/{fileName}/worksheets/{sheetName}/rows` |
| **경로 매개변수**| `fileName` – 엑셀 파일 이름(필수)<br>`sheetName` – 워크시트 이름(필수) |
| **쿼리 매개변수**| `startrow` – 삭제할 첫 번째 행의 인덱스(필수)<br>`totalRows` – 삭제할 행 수(필수)<br>`storage` – 클라우드 스토리지 이름(선택 사항)<br>`folder` – 스토리지 내 폴더 경로(선택 사항) |
| **요청 본문**    | *없음* |
| **응답 예시**| ```json<br>{<br>  "Code": 200,<br>  "Status": "OK",<br>  "RowsDeleted": 1<br>}<br>``` |
| **가능한 상태 코드**| 200 OK – 행이 성공적으로 삭제됨<br>400 Bad Request – 유효하지 않은 매개변수<br>401 Unauthorized – 인증 실패<br>404 Not Found – 파일 또는 워크시트를 찾을 수 없음<br>500 Internal Server Error – 서버 측 문제 |

**참고 링크**

- [행 추가](/cells/rows/add/)
- [행 조회](/cells/rows/get/)
- [행 복사](/cells/rows/copy/)
- [행 숨기기](/cells/rows/hide/)
- [행 개요](/cells/rows/)