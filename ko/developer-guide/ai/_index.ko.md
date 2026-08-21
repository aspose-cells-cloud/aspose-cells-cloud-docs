---
title: "Aspose.Cells Cloud AI – 작업 분해, 스프레드시트 및 텍스트 번역"
second_title: "문서"
ArticleTitle: "AI 역량 강화하기: 엑셀 번역, 작업 분해 등 배우기"
linktype: "AI"
type: docs
url: /ai/
keywords: "Aspose.Cells, Cloud AI, 엑셀 번역, 작업 분해, REST API"
description: "Aspose.Cells Cloud AI를 활용해 작업을 분해하고 엑셀 워크북 및 텍스트 파일을 번역해 보세요. REST 엔드포인트, 샘플 코드, 모범 사례를 포함합니다."
weight: 20
---

Aspose.Cells Cloud AI는 엑셀 및 텍스트 데이터 처리를 간편하게 도와주는 세 가지 강력한 AI 기반 서비스를 제공합니다: **사용자 작업 분해**, **스프레드시트 번역**, **텍스트 파일 번역**. 이 API를 통해 개발자는 복잡한 사용자 목표를 실행 가능한 단계로 프로그래밍 방식으로 분해하고, 전체 워크북이나 일반 텍스트 파일을 번역한 뒤, 이를 사용자 애플리케이션에 통합할 수 있습니다. 아래 엔드포인트를 사용해 빠르게 시작하고, 각 서비스에 제공된 상세 요청/응답 사양을 참고하세요.

- **[사용자 작업 분해](https://docs.aspose.cloud/cells/decompose-user-task/)** – Aspose.Cells Cloud AI를 사용해 사용자 목표를 순차적 행동 계획으로 변환합니다.  
  - **요청 메서드:** `POST`  
  - **엔드포인트 URL:** `https://api.aspose.cloud/v4.0/cells/ai/decompose-task`  
  - **헤더:** `Authorization: Bearer <access_token>`, `Content-Type: application/json`  
  - **요청 본문(JSON):**  
    ```json
    {
      "task": "차트와 피벗 테이블이 포함된 분기별 매출 보고서 생성"
    }
    ```  
  - **응답:** 작업 목록이 포함된 스프레드시트 파일을 다운로드 가능한 파일로 반환합니다.  
  - **상태 코드:** `200 OK`, `400 Bad Request`, `401 Unauthorized`, `500 Internal Server Error`  
  - **사전 조건:** **CellsAI** 범위(scope)가 포함된 유효한 액세스 토큰  
  - **응답 예시(JSON 스니펫):**  
    ```json
    {
      "fileId": "12345abcde",
      "downloadUrl": "https://api.aspose.cloud/v4.0/cells/ai/files/12345abcde"
    }
    ```  
  - **참고:** 생성된 워크북에는 순서가 정리된 단계가 포함된 **TaskList**라는 워크시트가 포함됩니다. 요청 제한: 1분당 100회

- **[스프레드시트 번역](https://docs.aspose.cloud/cells/translate-spreadsheet/)** – Aspose.Cells Cloud AI를 사용해 전체 스프레드시트를 번역합니다.  
  - **요청 메서드:** `POST`  
  - **엔드포인트 URL:** `https://api.aspose.cloud/v4.0/cells/ai/translate-spreadsheet`  
  - **헤더:** `Authorization: Bearer <access_token>`, `Content-Type: multipart/form-data`  
  - **요청 파라미터:**  
    - `file` – 번역할 엑셀 파일(바이너리)  
    - `targetLanguage` – ISO 언어 코드(예: `fr`, `de`)  
  - **응답:** 번역된 워크북을 다운로드 가능한 파일로 반환합니다.  
  - **상태 코드:** `200 OK`, `400 Bad Request`, `401 Unauthorized`, `415 Unsupported Media Type`, `500 Internal Server Error`  
  - **사전 조건:** **CellsAI** 범위가 포함된 액세스 토큰 및 충분한 저장소 할당량  
  - **응답 예시(JSON 스니펫):**  
    ```json
    {
      "translatedFileId": "f9d8c7b6",
      "downloadUrl": "https://api.aspose.cloud/v4.0/cells/ai/files/f9d8c7b6"
    }
    ```  
  - **참고:** 모든 셀 값, 주석 및 시트 이름이 번역됩니다. 요청 제한: 1분당 100회

- **[텍스트 파일 번역](https://docs.aspose.cloud/cells/translate-text-file/)** – Aspose.Cells Cloud AI를 사용해 전체 텍스트 파일을 번역합니다.  
  - **요청 메서드:** `POST`  
  - **엔드포인트 URL:** `https://api.aspose.cloud/v4.0/cells/ai/translate-text`  
  - **헤더:** `Authorization: Bearer <access_token>`, `Content-Type: multipart/form-data`  
  - **요청 파라미터:**  
    - `file` – 번역할 텍스트 파일(바이너리)  
    - `targetLanguage` – ISO 언어 코드(예: `es`, `ja`)  
  - **응답:** 번역된 텍스트 파일을 반환합니다.  
  - **상태 코드:** `200 OK`, `400 Bad Request`, `401 Unauthorized`, `415 Unsupported Media Type`, `500 Internal Server Error`  
  - **사전 조건:** **CellsAI** 범위가 포함된 유효한 액세스 토큰  
  - **응답 예시(JSON 스니펫):**  
    ```json
    {
      "translatedFileId": "a1b2c3d4",
      "downloadUrl": "https://api.aspose.cloud/v4.0/cells/ai/files/a1b2c3d4"
    }
    ```  
  - **참고:** 최대 5MB 크기의 UTF-8 인코딩 일반 텍스트 파일을 지원합니다. 요청 제한: 1분당 100회