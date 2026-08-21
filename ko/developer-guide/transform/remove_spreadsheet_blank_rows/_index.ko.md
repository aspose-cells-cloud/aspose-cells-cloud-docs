---
title: "스프레드시트 빈 행 제거"
ArticleTitle: "스프레드시트 빈 행 제거 – Aspose.Cells Cloud API"
second_title: "문서"
linktype: "docs"
url: "/cells/remove/blank-rows"
aliases: []
keywords: "Aspose.Cells, 빈 행 제거, 스프레드시트, API"
description: "스프레드시트 파일에서 모든 빈 행을 삭제합니다."
weight: 100
---

## Aspose.Cells Cloud 웹 서비스의 스프레드시트 빈 행 제거 기능

이 메서드는 데이터나 개체가 전혀 포함되어 있지 않은 완전히 비어 있는 행을 스프레드시트에서 제거합니다. 모든 시트를 스캔하여 모든 셀이 비어 있는 행을 식별합니다. 이 작업은 스프레드시트에서 직접 수행되며, 내용이 전혀 없는 행만 삭제되도록 보장합니다. 이를 통해 스프레드시트를 정리하고 불필요한 빈 행을 제거하여 데이터를 더 체계적으로 정리하고 관리하기 쉽게 만듭니다. 사용자는 삭제된 행이 복구될 수 없으므로 이 작업을 수행하기 전에 스프레드시트를 백업해 두어야 합니다.

### 웹 API 엔드포인트

```http
PUT https://api.aspose.cloud/v4.0/cells/remove/blank-rows
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 보장되며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 파라미터

| 파라미터 이름 | 타입   | 경로/쿼리 스트링/HTTP 본문 | 설명 |
|---------------|--------|----------------------------|------|
| Spreadsheet   | File   | FormData                   | 스프레드시트 파일 업로드. |
| outPath       | String | Query                      | (선택사항) 워크북이 저장될 폴더 경로. 기본값은 null입니다. |
| outStorageName| String | Query                      | 출력 파일의 저장소 이름. |
| region        | String | Query                      | 스프레드시트 지역/언어 설정(예: `en-US`, `fr-FR`). 숫자 형식, 날짜 파싱 및 로케일 관련 동작에 영향을 미칩니다. |
| password      | String | Query                      | 스프레드시트 파일을 열기 위한 비밀번호. |

### 요청 본문 파라미터

| 파라미터 이름 | 타입 | 설명 |
|---------------|------|------|
| Spreadsheet   | File | 스프레드시트 파일 업로드. |

### **응답**

```json
{
  "ResponseFile": "이진 파일 스트림"
}
```

**응답 상태 코드**

| 코드 | 의미 | 설명 |
|------|------|------|
| 200 | OK | 빈 행이 제거된 처리된 스프레드시트 파일이 반환됩니다. |
| 400 | Bad Request | 잘못된 URL 또는 요청 파라미터입니다. |
| 401 | Unauthorized | 인증에 실패했거나 자격 증명이 제공되지 않았습니다. |
| 404 | Not Found | 원본 파일에 접근할 수 없습니다. |
| 413 | Payload Too Large | 요청 페이로드가 허용된 크기를 초과했습니다. |
| 500 | Internal Server Error | 스프레드시트에서 데이터를 가져오는 과정에서 문제가 발생했습니다. |

## SDK를 사용하여 스프레드시트 빈 행 제거하는 방법

### 스프레드시트 빈 행 제거 사양

[스프레드시트 빈 행 제거 API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Transform/RemoveSpreadsheetBlankRows)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예시는 cURL을 사용하여 Cloud API에 요청을 보내는 방법을 보여줍니다.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}
{< tab tabNum="1" >}
```bash
# 보안 연결을 위해 HTTPS 사용
curl -v "https://api.aspose.cloud/v4.0/cells/remove/blank-rows?outPath=outputFolder&outStorageName=MyStorage&region=en-US&password=12345" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@sample.xlsx'
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "ResponseFile": "이진 파일 스트림"
}
```
{< /tab >}
{< /tabs >}

### Aspose Cells Cloud SDK 사용

SDK를 사용하는 것이 개발 속도를 가장 빠르게 향상시킬 수 있는 방법입니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 작업에 집중할 수 있도록 합니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예시는 다양한 SDK를 사용하여 Aspose Cells Cloud 웹 서비스를 호출하는 방법을 보여줍니다:
`[TBD]`
---