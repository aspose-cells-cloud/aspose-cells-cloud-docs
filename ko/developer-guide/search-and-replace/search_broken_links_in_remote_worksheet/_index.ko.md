---
title: "원격 워크시트에서 깨진 링크 검색"
ArticleTitle: "원격 워크시트에서 깨진 링크 검색 – Aspose.Cells Cloud API"
second_title: "문서"
linktype: "docs"
url: /cells/{name}/worksheets/{worksheet}/search/broken-links
aliases: []
keywords: "Aspose.Cells, 깨진 링크 검색, 원격 워크시트"
description: "원격 클라우드 스토리지에 저장된 스프레드시트의 워크시트에서 깨진 링크를 검색합니다."
weight: 100
---

## Aspose.Cells Cloud 웹 서비스의 원격 워크시트에서 깨진 링크 검색

이 메서드는 원격 클라우드 스토리지에 저장된 스프레드시트 파일의 워크시트 내에 있는 깨진 링크를 검색합니다. 이 메서드는 모든 시트와 셀을 스캔하여 더 이상 유효한 대상(예: 유효하지 않은 URL 또는 누락된 외부 참조)을 가리키지 않는 하이퍼링크를 식별합니다. 이 작업은 로컬 머신에 파일을 다운로드하지 않고 클라우드 환경 내에서 원격으로 수행됩니다.

### 웹 API 엔드포인트

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/broken-links
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 제공하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름 | 유형 | 경로/쿼리 문자열/HTTP 본문 | 설명 |
|----------------|------|-----------------------------|-------------|
| name | string | 경로 | 검색할 워크북 파일의 이름입니다. |
| worksheet | string | 경로 | 검색 대상 워크시트를 지정합니다. |
| folder | string | 쿼리 | 워크북이 저장된 폴더 경로입니다. (선택 사항) |
| storageName | string | 쿼리 | (선택 사항) 사용자 지정 클라우드 스토리지를 사용할 경우 스토리지 이름입니다. 생략 시 기본 스토리지를 사용합니다. |
| region | string | 쿼리 | 스프레드시트의 지역/언어 설정(예: `en-US`, `fr-FR`)입니다. 숫자 형식, 날짜 파싱 및 로케일별 동작에 영향을 줍니다. |
| password | string | 쿼리 | 스프레드시트 파일을 열기 위한 비밀번호입니다. |

### 요청 본문 매개변수

| 매개변수 이름 | 유형 | 설명 |
| -------------- | ---- | ----------- |
| — | — | 이 작업에는 요청 본문이 필요하지 않습니다. |

### **응답**

```json
{
  "Links": [
    {
      "SheetName": "Sheet1",
      "CellName": "A1",
      "Url": "http://invalid.example.com"
    }
  ],
  "Count": 1
}
```

**응답 상태 코드**

| 코드 | 의미 | 설명 |
|------|---------|-------------|
| 200 | OK | 깨진 링크 목록을 성공적으로 검색했습니다. |
| 400 | Bad Request | 요청 매개변수가 잘못되었거나 URL 형식이 잘못되었습니다. |
| 401 | Unauthorized | 인증에 실패했거나 자격 증명이 제공되지 않았습니다. |
| 404 | Not Found | 소스 파일에 접근할 수 없습니다. |
| 413 | Payload Too Large | 요청 엔티티가 너무 큽니다. |
| 500 | Internal Server Error | 데이터를 가져오는 도중 스프레드시트에 문제가 발생했습니다. |

## SDK를 사용하여 원격 워크시트에서 깨진 링크 검색하는 방법

### 원격 워크시트에서 깨진 링크 검색 사양

[원격 워크시트에서 깨진 링크 검색 API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchBrokenLinksInRemoteWorksheet)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예시는 cURL을 사용하여 클라우드 API로 요청을 수행하는 방법을 보여줍니다.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# 보안 연결을 위해 HTTPS 사용
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/broken-links?folder={folder}&storageName={storageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "Links": [
    {
      "SheetName": "Sheet1",
      "CellName": "A1",
      "Url": "http://invalid.example.com"
    }
  ],
  "Count": 1
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK 사용

SDK를 사용하면 개발 속도가 가장 빠릅니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 작업에 집중할 수 있도록 해줍니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예시는 다양한 SDK를 사용하여 Aspose Cells Cloud 웹 서비스를 호출하는 방법을 보여줍니다:
`[TBD]`
---