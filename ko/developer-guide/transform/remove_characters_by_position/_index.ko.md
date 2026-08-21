---
title: "위치 기준 문자 제거"
ArticleTitle: "위치 기준 문자 제거 – Aspose.Cells Cloud API"
second_title: "문서"
linktitle: "위치 기준 문자 제거"
type: docs
url: /ko/cells/content/remove/characters-by-position
aliases: []
keywords: "Aspose.Cells, 문자 제거, API"
description: "스preadsheet에서 셀의 위치 기준으로 문자를 삭제합니다."
weight: 100
---

## Aspose.Cells Cloud 웹 서비스의 위치 기준 문자 제거 기능

대상 범위 내 모든 셀에서 지정된 위치(앞에서부터/뒤에서부터 N개, 특정 하위 문자열 앞/뒤, 또는 두 구분자 사이)의 문자를 삭제하며, 수식, 서식 및 데이터 유효성 검사를 그대로 보존합니다.

### 웹 API 엔드포인트

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/characters-by-position
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 우수하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 파라미터

| 파라미터 이름              | 타입    | 경로/쿼리 문자열/HTTP 본문 | 설명                                                                                                          |
|---------------------------|---------|-----------------------------|----------------------------------------------------------------------------------------------------------------------|
| Spreadsheet               | File    | FormData                    | 스프레드시트 파일 업로드.                                                                                            |
| theFirstNCharacters       | Integer | Query                       | 선택된 셀에서 앞에서부터 n개의 문자를 제거하도록 지정. 선택 사항.                                               |
| theLastNCharacters        | Integer | Query                       | 선택된 셀에서 뒤에서부터 n개의 문자를 제거하도록 지정. 선택 사항.                                                |
| allCharactersBeforeText   | String  | Query                       | 지정된 하위 문자열 앞에 위치한 텍스트를 삭제. 선택 사항.                                                          |
| allCharactersAfterText    | String  | Query                       | 지정된 하위 문자열 뒤에 위치한 텍스트를 삭제. 선택 사항.                                                           |
| caseSensitive             | Boolean | Query                       | `Substring` 모드 및 `CustomChars` 사용 시 대/소문자 구분 여부에 영향. 선택 사항.                                                   |
| worksheet                 | String  | Query                       | 스프레드시트의 워크시트를 지정. 선택 사항.                                                                      |
| range                     | String  | Query                       | 스프레드시트의 워크시트 범위를 지정 (예: `A1:B10`). 선택 사항.                                               |
| outPath                   | String  | Query                       | (선택 사항) 워크북이 저장될 폴더 경로. 기본값은 null입니다. 선택 사항.                                 |
| outStorageName            | String  | Query                       | 출력 파일 스토리지 이름. 선택 사항.                                                                                  |
| region                    | String  | Query                       | 스프레드시트 지역/언어 설정 (예: `en-US`, `fr-FR`). 선택 사항.                                             |
| password                  | String  | Query                       | 스프레드시트 파일을 열기 위한 비밀번호. 선택 사항.                                                                 |

### 요청 본문 파라미터

| 파라미터 이름 | 타입 | 설명 |
| -------------- | ---- | ----------- |
| Spreadsheet    | File | 스프레드시트 파일 업로드. |

### **응답**

```json
{
  "status": "OK",
  "message": "문자가 성공적으로 제거되었습니다.",
  "downloadUrl": "https://api.aspose.cloud/v4.0/storage/file/sample_output.xlsx"
}
```

**응답 상태 코드**

| 코드 | 의미 | 설명 |
|------|------|-------------|
| 200 | OK | 작업이 성공적으로 완료되었으며, 처리된 파일이 반환됩니다. |
| 400 | Bad Request | 요청이 잘못 구성되었거나 유효하지 않은 파라미터가 포함되어 있습니다. |
| 401 | Unauthorized | 인증에 실패했거나 JWT 토큰이 누락되었거나 유효하지 않습니다. |
| 413 | Payload Too Large | 업로드된 파일이 허용된 크기 제한을 초과했습니다. |
| 500 | Internal Server Error | 서버 측에서 예기치 않은 오류가 발생했습니다. |

## SDK를 사용하여 위치 기준 문자 제거 기능 사용하는 방법

### 위치 기준 문자 제거 사양

[위치 기준 문자 제거 API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveCharactersByPosition)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells Cloud 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예시는 cURL을 사용하여 Cloud API에 요청을 보내는 방법을 보여줍니다.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# 안전한 연결을 위해 HTTPS 사용
curl -v "https://api.aspose.cloud/v4.0/cells/content/remove/characters-by-position?theFirstNCharacters=5&worksheet=Sheet1&range=A1%3AB10" \
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
  "status": "OK",
  "message": "문자가 성공적으로 제거되었습니다.",
  "downloadUrl": "https://api.aspose.cloud/v4.0/storage/file/sample_output.xlsx"
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK 사용

SDK를 사용하는 것이 개발 속도를 가장 빠르게 향상시키는 방법입니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 작업에 집중할 수 있도록 해줍니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose Cells Cloud 웹 서비스를 호출하는 방법을 보여줍니다:
`[TBD]`
---