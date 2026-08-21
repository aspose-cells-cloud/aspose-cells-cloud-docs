---
title: "스프레드시트의 모든 텍스트 항목 검색"
ArticleTitle: "스프레드시트의 모든 텍스트 항목 검색 – Aspose.Cells Cloud API"
second_title: "문서"
linktype: "docs"
url: /ko/cells/search/content/all-textitems
aliases: []
keywords: "Aspose.Cells, 검색, 텍스트 항목, API"
description: "Aspose.Cells Cloud API를 사용하여 스프레드시트 파일 내의 모든 텍스트 항목을 검색합니다."
weight: 100
---

## Aspose.Cells Cloud 웹 서비스의 스프레드시트 모든 텍스트 항목 검색

이 메서드는 로컬 스프레드시트 파일 내의 모든 텍스트 항목을 검색합니다. 워크시트의 모든 시트와 셀을 대상으로 검색을 수행하며, 검색어의 출현 위치를 식별합니다. 이 작업은 클라우드 측에서 실행되므로 클라우드 스토리지가 필요 없습니다. 소스 파일을 읽을 수 있는 적절한 권한이 있는지 확인하십시오. 소스 파일에 접근할 수 없거나 검색 과정 중 오류(예: 지원되지 않는 파일 형식)가 발생하면 적절한 예외가 발생합니다. 구현 세부 사항에 따라 이 메서드는 일치하는 항목의 위치(예: 시트 이름, 셀 좌표)를 반환할 수 있습니다.

### 웹 API 엔드포인트

```http
PUT https://api.aspose.cloud/v4.0/cells/search/content/all-textitems
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 보장되며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 파라미터

| 파라미터 이름 | 유형 | 경로/쿼리 문자열/HTTP 본문 | 설명 |
|----------------|------|-----------------------------|-------------|
| Spreadsheet | 파일 | FormData | 스프레드시트 파일 업로드 |
| region | 문자열 | 쿼리 | 스프레드시트 지역/언어 설정(예: `en-US`, `fr-FR`). 숫자 서식, 날짜 파싱 및 지역별 동작에 영향을 미칩니다. |
| password | 문자열 | 쿼리 | 스프레드시트 파일을 열기 위한 비밀번호 |

### 요청 본문 파라미터

| 파라미터 이름 | 유형 | 설명 |
| -------------- | ---- | ----------- |
| [TBD] | [TBD] | [TBD] |

### **응답**

```json
{
  "SearchResults": [
    {
      "SheetName": "Sheet1",
      "CellName": "A1",
      "Text": "Sample text"
    }
    // ... 추가 항목
  ],
  "TotalCount": 42
}
```

**응답 상태 코드**

| 코드 | 의미 | 설명 |
|------|------|------|
| 200 | OK | 요청이 성공적이며 응답에 검색된 모든 텍스트 항목이 포함됩니다. |
| 400 | Bad Request | 잘못된 URL 또는 형식이 맞지 않는 요청 파라미터 |
| 401 | Unauthorized | 인증에 실패했거나 자격 증명이 제공되지 않았습니다. |
| 404 | Not Found | 소스 파일에 접근할 수 없습니다. |
| 413 | Payload Too Large | 업로드한 파일이 허용된 크기 제한을 초과했습니다. |
| 500 | Internal Server Error | 스프레드시트에서 데이터를 가져오는 과정에서 예상치 못한 문제가 발생했습니다. |

## SDK를 사용하여 스프레드시트 모든 텍스트 항목 검색 사용하기

### 스프레드시트 모든 텍스트 항목 검색 사양

[스프레드시트 모든 텍스트 항목 검색 API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{SearchController}/{SearchSpreadsheetAllTextItems})은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API에 요청을 보내는 방법을 보여줍니다.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# 보안 연결을 위해 HTTPS 사용
curl -v "https://api.aspose.cloud/v4.0/cells/search/content/all-textitems?region=en-US&password=myPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "SearchResults": [
    {
      "SheetName": "Sheet1",
      "CellName": "A1",
      "Text": "Sample text"
    }
    // ... 추가 항목
  ],
  "TotalCount": 42
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK 사용하기

SDK를 사용하는 것이 개발 속도를 가장 빠르게 향상시키는 방법입니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 작업에 집중할 수 있도록 해줍니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 참조하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose Cells Cloud 웹 서비스를 호출하는 방법을 보여줍니다:
 `[TBD]`
---