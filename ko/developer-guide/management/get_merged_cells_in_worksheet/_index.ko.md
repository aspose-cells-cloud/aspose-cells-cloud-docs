---
title: "워크시트에서 병합된 셀 가져오기"
ArticleTitle: "워크시트에서 병합된 셀 가져오기 – Aspose.Cells Cloud API"
second_title: "문서"
linktitle: "GetMergedCellsInWorksheet"
type: docs
url: /ko/cells/spreadsheet/mergedcells
aliases: []
keywords: "Aspose Cells, 병합된 셀, 워크시트, API"
description: "로컬 스프레드시트 워크시트에서 모든 병합된 셀 영역을 가져옵니다."
weight: 1000
---

## Aspose.Cells Cloud 웹 서비스의 워크시트에서 병합된 셀 가져오기

로컬 스프레드시트 워크시트에서 모든 병합된 셀 영역을 가져옵니다.

### 웹 API 엔드포인트

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/mergedcells
```

### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 파라미터

| 파라미터 이름 | 타입 | 경로/쿼리 스트링/HTTP 본문 | 설명 |
|----------------|------|-----------------------------|-------------|
| Spreadsheet | 파일 | FormData | 스프레드시트 파일 업로드. |
| worksheet | 문자열 | 쿼리 | 워크시트 이름. |
| region | 문자열 | 쿼리 | 스프레드시트 지역/언어 설정(예: `en-US`, `fr-FR`). 숫자 서식, 날짜 파싱 및 로케일별 동작에 영향을 미칩니다. |
| password | 문자열 | 쿼리 | 스프레드시트 파일을 열기 위한 비밀번호. |

### 요청 본문 파라미터

| 파라미터 이름 | 타입 | 설명 |
| -------------- | ---- | ----------- |
| 없음 | 없음 | 이 작업은 JSON 본문을 받지 않으며, 스프레드시트 파일은 `multipart/form-data`로 전송됩니다. |

### **응답**

```json
[
  {
    "Column": 1,
    "ColumnCount": 3,
    "Row": 5,
    "RowCount": 2
  },
  {
    "Column": 6,
    "ColumnCount": 2,
    "Row": 10,
    "RowCount": 4
  }
]
```

**응답 상태 코드**

| 코드 | 의미 | 설명 |
|------|------|-------------|
| 200 | 성공 | 병합된 셀 영역을 성공적으로 조회했습니다. |
| 400 | 잘못된 요청 | 하나 이상의 요청 파라미터가 유효하지 않거나 누락되었습니다. |
| 401 | 인증되지 않음 | 인증 실패 – 잘못되거나 누락된 JWT 토큰. |
| 413 | 페이로드가 너무 큼 | 업로드한 스프레드시트가 허용된 크기 제한을 초과했습니다. |
| 500 | 내부 서버 오류 | 서버에서 예기치 않은 오류가 발생했습니다. |

## SDK를 사용하여 워크시트에서 병합된 셀 가져오기

### 워크시트에서 병합된 셀 가져오기 사양

[워크시트에서 병합된 셀 가져오기 API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetMergedCellsInWorksheet)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API에 요청을 보내는 방법을 보여줍니다.

{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}

{< tab tabNum="1" >}

```bash
# 안전한 연결을 위해 HTTPS 사용
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/mergedcells?worksheet=Sheet1&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@example.xlsx'
```

{< /tab >}

{< tab tabNum="2" >}

```json
[
  {
    "Column": 1,
    "ColumnCount": 3,
    "Row": 5,
    "RowCount": 2
  },
  {
    "Column": 6,
    "ColumnCount": 2,
    "Row": 10,
    "RowCount": 4
  }
]
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 가장 빠르게 높일 수 있습니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 작업에 집중할 수 있도록 도와줍니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose Cells Cloud 웹 서비스를 호출하는 방법을 보여줍니다:
 `[TBD]`
---