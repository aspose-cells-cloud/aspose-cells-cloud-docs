---
title: "Excel 워크시트에 행 추가하는 방법"
second_title: "Document"
linktitle: "Add"
type: docs
url: /rows/add/
keywords: "Aspose.Cells, 행 추가, Excel API, REST, C#, Java, Python, Node.js"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트에 단일 또는 여러 행을 추가하는 단계별 가이드. C#, Java, Python 및 Node.js 코드 예제 제공."
weight: 20
ArticleTitle: "Aspose.Cells Cloud API로 Excel 워크시트에 행 추가 – 단계별 가이드"
---

## Excel 워크시트에 행 추가하는 방법

이 문서에서는 Aspose.Cells Cloud REST API를 사용하여 기존 워크시트에 빈 행 하나 또는 여러 개를 삽입하는 방법을 설명합니다. 진행하기 전에 유효한 API 키와 적절한 SDK가 설치되어 있는지 확인하세요.

**사전 요구 사항**  
- [ ] 활성 구독이 있는 Aspose.Cells Cloud 계정  
- [ ] Aspose Cloud 대시보드에서 생성된 API 키/액세스 토큰  
- [ ] 설치 및 설정된 지원 SDK 중 하나(C#, Java, Python, Node.js)  

**API 참조**  
- **HTTP 메서드:** `POST`  
- **엔드포인트:** `https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/rows`  
- **필수 경로 매개변수:**  
  - `fileName` – 클라우드에 저장된 Excel 파일 이름  
  - `sheetName` – 행을 추가할 워크시트 이름  
- **쿼리 매개변수:**  
  - `startrow` – 삽입을 시작할 행의 0부터 시작하는 인덱스  
  - `totalRows` – 삽입할 행 수  
  - `folder` – (선택 사항) 파일이 위치한 클라우드 폴더 경로  
  - `storage` – (선택 사항) 기본이 아닌 저장소를 사용할 경우 저장소 이름  
- **요청 본문(JSON 예시):**  

  ```json
  {
    "startrow": 5,
    "totalRows": 3
  }
  ```

  **cURL 예시**

  ```bash
  curl -X POST "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/rows?startrow=5&totalRows=3&folder=MyFolder&storage=MyStorage" \
      -H "Authorization: Bearer {access_token}" \
      -H "Content-Type: application/json" \
      -d '{"startrow":5,"totalRows":3}'
  ```

- **성공 응답(HTTP 200):** 업데이트된 워크시트 정보(새로운 행 수 포함)를 반환합니다.  

  ```json
  {
    "Code": 200,
    "Status": "OK",
    "Worksheet": {
      "Name": "Sheet1",
      "RowsCount": 30
    }
  }
  ```

- **오류 응답 예시(HTTP 400):**  

  ```json
  {
    "Code": 400,
    "Status": "Bad Request",
    "Message": "startrow 매개변수가 유효하지 않습니다. 음이 아닌 정수여야 합니다."
  }
  ```

- **상태 코드:**  

  | 코드 | 의미                                      |
  |------|-------------------------------------------|
  | 200  | 행 추가 성공                              |
  | 400  | 잘못된 매개변수 또는 잘못된 형식의 JSON   |
  | 401  | 인증 실패                                 |
  | 404  | 파일 또는 워크시트를 찾을 수 없음         |
  | 500  | 서버 오류                                 |

아래는 행 추가에 대한 자세한 예제로 연결되는 빠른 링크입니다:

- [Excel 워크시트에 빈 행 추가하는 방법](/cells/rows/add/row/)
- [Excel 워크시트에 여러 행 추가하는 방법](/cells/rows/add/rows/)
---