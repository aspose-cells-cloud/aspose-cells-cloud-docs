---
title: "SearchAllTextItemsInRemoteSpreadsheet"
ArticleTitle: "SearchAllTextItemsInRemoteSpreadsheet – Aspose.Cells Cloud API"
second_title: "문서"
linktype: "docs"
url: /ko/cells/{name}/search/content/all-textitems
aliases: []
keywords: "검색, 텍스트 항목, Aspose.Cells"
description: "Aspose.Cells Cloud를 사용하여 원격 스프레드시트에서 모든 텍스트 항목을 검색합니다."
weight: 100
---

## Aspose.Cells Cloud 웹 서비스의 SearchAllTextItemsInRemoteSpreadsheet

이 메서드는 원격 스프레드시트 파일 내의 모든 텍스트 항목을 검색합니다. 워크북의 모든 시트와 셀을 검색하여 검색어의 출현 위치를 식별할 수 있습니다. 이 작업은 클라우드에서 수행되므로 로컬 저장소가 필요하지 않습니다. 원본 파일을 읽을 수 있는 권한이 있는지 확인하세요. 원본 파일에 접근할 수 없거나 검색 과정 중 오류(예: 지원되지 않는 파일 형식)가 발생하면 적절한 예외가 발생합니다. 구현 세부 사항에 따라 메서드는 일치하는 항목의 위치(예: 시트 이름, 셀 좌표)를 반환할 수 있습니다.

### 웹 API 엔드포인트

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/search/content/all-textitems
```

### **보안 및 인증**

Aspose.Cells Cloud API는 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>을 요구하는 보안 방식입니다.

### 요청 매개변수

| 매개변수 이름 | 유형   | 경로/쿼리 문자열/HTTP 본문 | 설명 |
|---------------|--------|----------------------------|------|
| name          | string | 경로                       | 워크북 파일의 이름입니다. |
| folder        | string | 쿼리                       | 워크북이 저장된 폴더 경로입니다. |
| storageName   | string | 쿼리                       | (선택 사항) 사용자 정의 클라우드 저장소를 사용하는 경우 저장소 이름입니다. 생략 시 기본 저장소를 사용합니다. |
| region        | string | 쿼리                       | 스프레드시트 지역/언어 설정(예: `en-US`, `fr-FR`)입니다. 숫자 포맷, 날짜 파싱 및 지역별 동작에 영향을 줍니다. |
| password      | string | 쿼리                       | 스프레드시트 파일을 열기 위한 비밀번호입니다. |

### 요청 본문 매개변수

| 매개변수 이름 | 유형 | 설명 |
| -------------- | ---- | ----------- |
| [TBD]          |      | [TBD] |

### **응답**

```json
{
  "TextItems": [
    {
      "SheetName": "string",
      "CellAddress": "string",
      "Text": "string"
    }
  ],
  "TotalCount": 0
}
```

**응답 상태 코드**

| 코드 | 의미 | 설명 |
|------|------|------|
| 200 | OK | 요청이 성공했으며 응답에 스프레드시트에서 찾은 모든 텍스트 항목이 포함되어 있습니다. |
| 400 | Bad Request | 잘못된 URL 또는 요청 매개변수입니다. |
| 401 | Unauthorized | 인증에 실패했거나 자격 증명이 제공되지 않았습니다. |
| 404 | Not Found | 원본 파일에 접근할 수 없습니다. |
| 413 | Payload Too Large | 요청 페이로드가 허용된 크기를 초과했습니다. |
| 500 | Internal Server Error | 스프레드시트에서 데이터를 가져오는 도중 오류가 발생했습니다. |

## SDK를 사용한 SearchAllTextItemsInRemoteSpreadsheet 사용 방법

### SearchAllTextItemsInRemoteSpreadsheet 사양

[SearchAllTextItemsInRemoteSpreadsheet API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchAllTextItemsInRemoteSpreadsheet)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 요청을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예제는 cURL을 사용하여 클라우드 API에 요청을 보내는 방법을 보여줍니다.

{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}

{< tab tabNum="1" >}

```bash
# 보안 연결을 위해 HTTPS 사용
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/search/content/all-textitems?folder={folder}&storageName={storageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "TextItems": [
    {
      "SheetName": "시트1",
      "CellAddress": "A1",
      "Text": "예제 텍스트"
    }
  ],
  "TotalCount": 1
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 가장 빠르게 향상시킬 수 있습니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 작업에 집중할 수 있게 해줍니다. Aspose.Cells Cloud SDK 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose Cells Cloud 웹 서비스를 호출하는 방법을 보여줍니다:
`[TBD]`
---