---
title: "워크시트를 HTML 테이블로 변환"
ArticleTitle: "워크시트를 HTML 테이블로 변환 – Aspose.Cells Cloud API"
second_title: "문서"
linktype: "docs"
url: /cells/convert/worksheet/html-table
aliases: []
keywords: "Aspose.Cells, ConvertWorksheetToHtmlTable, HTML 테이블, API"
description: "로컬 드라이브의 스프레드시트 워크시트를 HTML 테이블 파일로 변환합니다(Aspose.Cells Cloud 사용)."
weight: 100
---

## Aspose.Cells Cloud 웹 서비스의 워크시트를 HTML 테이블로 변환

이 작업은 로컬 파일 시스템에서 스프레드시트 파일을 읽어 지정된 워크시트를 HTML 테이블로 변환한 후, 변환된 결과를 파일 스트림으로 반환합니다. 변환은 클라우드 서버에서 완전히 수행되므로 클라우드 스토리지로의 중간 업로드가 필요 없습니다. 로케일 설정 및 암호로 보호된 워크북도 지원합니다.

### 웹 API 엔드포인트

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/html-table
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 강화되어 있으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 파라미터

| 파라미터 이름 | 타입   | 경로/쿼리 스트링/HTTP 본문 | 설명 |
|---------------|--------|----------------------------|------|
| Spreadsheet   | 파일   | FormData                   | 스프레드시트 파일 업로드 |
| worksheet     | 문자열 | 쿼리                       | 스프레드시트의 워크시트 이름 (필수) |
| region        | 문자열 | 쿼리                       | 스프레드시트 지역/언어 설정(예: `en-US`, `fr-FR`). 숫자 서식, 날짜 파싱 및 로케일 관련 동작에 영향을 줍니다. |
| password      | 문자열 | 쿼리                       | 스프레드시트 파일을 열기 위한 암호 |

### 요청 본문 파라미터

| 파라미터 이름 | 타입 | 설명 |
| ------------- | ---- | ---- |
| *없음* | *없음* | *JSON 본문이 필요하지 않습니다. 파일은 multipart/form-data로 전송됩니다.* |

### **응답**

```json
{
  "File": "생성된 HTML 테이블의 바이너리 스트림"
}
```

**응답 상태 코드**

| 코드 | 의미 | 설명 |
|------|------|------|
| 200 | 성공 | 워크시트가 성공적으로 HTML 테이블로 변환되어 파일 스트림으로 반환되었습니다. |
| 400 | 잘못된 요청 | 잘못된 요청 URL이거나 필수 파라미터가 누락되었습니다. |
| 401 | 인증 실패 | 인증에 실패했거나 자격 증명이 제공되지 않았습니다. |
| 404 | 찾을 수 없음 | 원본 파일에 접근할 수 없습니다. |
| 500 | 내부 서버 오류 | 변환 데이터를 가져오는 동안 스프레드시트에 문제가 발생했습니다. |
| 413 | 페이로드가 너무 큼 | 업로드된 파일이 허용된 크기 제한을 초과했습니다. |

## SDK를 사용하여 워크시트를 HTML 테이블로 변환하는 방법

### 워크시트를 HTML 테이블로 변환 사양

[워크시트를 HTML 테이블로 변환 API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToHtmlTable)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API에 호출하는 방법을 보여줍니다.

{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}

{< tab tabNum="1" >}

```bash
# 보안 연결을 위해 HTTPS 사용
curl -v "https://api.aspose.cloud/v4.0/cells/convert/worksheet/html-table?worksheet={worksheet}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "File": "생성된 HTML 테이블의 바이너리 스트림"
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 최대한 빠르게 향상시킬 수 있습니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 작업에 집중할 수 있게 해줍니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells Cloud 웹 서비스를 호출하는 방법을 보여줍니다:
`[TBD]`
---