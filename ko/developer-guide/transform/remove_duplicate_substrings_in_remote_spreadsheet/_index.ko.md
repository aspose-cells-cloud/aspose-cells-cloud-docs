---
title: "원격 스프레드시트에서 중복 부분 문자열 제거"
ArticleTitle: "원격 스프레드시트에서 중복 부분 문자열 제거 – Aspose.Cells Cloud API"
second_title: "문서"
linktitle: "원격 스프레드시트에서 중복 부분 문자열 제거"
type: docs
url: /cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/duplicate-substrings
aliases: []
keywords: "Aspose.Cells, 중복 부분 문자열 제거, API"
description: "워크북 내 지정된 범위의 셀에 포함된 반복되는 부분 문자열을 찾아 제거하는 API입니다."
weight: 1
---

## Aspose.Cells Cloud 웹 서비스의 원격 스프레드시트에서 중복 부분 문자열 제거 기능

사용자 정의 또는 사전 설정된 구분 기호를 사용해 선택한 범위 내 모든 셀에서 반복되는 부분 문자열을 찾아 제거하며, 수식, 서식, 데이터 유효성 검사를 유지합니다.

**중복 감지 방식**  
1. 선택한 구분 기호를 기준으로 각 셀 값을 부분 문자열로 분할합니다.  
2. 도구는 **동일한 셀 내**에서 부분 문자열을 비교하며, 중복된 값 중 **첫 번째 발생 항목만** 유지합니다.  
3. 정리된 부분 문자열을 동일한 구분 기호로 다시 결합하여 셀에 다시 저장합니다.  

**구분 기호 옵션**  
- 사전 설정 목록: 쉼표, 세미콜론, 공백, 탭, 줄 바꿈  
- `Custom`(사용자 정의) – 임의의 문자(여러 문자는 하나의 복합 구분 기호로 처리) 입력 가능  
- `TreatConsecutiveDelimitersAsOne` – 인접한 구분 기호들을 하나의 구분자로 통합  

문자열 타입 셀만 처리되며, 숫자, 논리값, 수식은 분할 전에 문자열로 변환됩니다(수식은 제거됨). 정리된 셀 수와 업데이트된 워크북 스트림을 반환합니다.

### 웹 API 엔드포인트

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/duplicate-substrings
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 위해 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 파라미터

| 파라미터 이름 | 타입 | 경로/쿼리 문자열/HTTP 본문 | 설명 |
|---------------|------|---------------------------|------|
| name | string | Path | (필수) 가져올 워크북 파일의 이름 |
| worksheet | string | Path | 스프레드시트의 워크시트 지정 |
| range | string | Path | 스프레드시트의 워크시트 범위 지정 |
| delimiters | string | Query | 셀 값을 분할하는 데 사용할 구분 기호(예: 쉼표, 세미콜론, 공백, 탭, 줄 바꿈). 필수 항목 |
| treatConsecutiveDelimitersAsOne | boolean | Query | 인접한 구분 기호들을 하나의 구분자로 통합. 기본값: true. 선택 사항 |
| caseSensitive | boolean | Query | 중복 감지 시 대소문자를 구분하여 비교. 선택 사항 |
| folder | string | Query | (선택 사항) 워크북이 저장된 폴더 경로. 기본값: null |
| storageName | string | Query | (선택 사항) 사용자 정의 클라우드 스토리지를 사용할 경우 스토리지 이름 |
| region | string | Query | 스프레드시트 지역/언어 설정(예: `en-US`, `fr-FR`). 선택 사항 |
| password | string | Query | 스프레드시트 파일을 열기 위한 비밀번호. 선택 사항 |

### 요청 본문 파라미터

| 파라미터 이름 | 타입 | 설명 |
| -------------- | ---- | ----------- |
| - | - | 이 작업은 요청 본문이 필요 없습니다. |

### **응답**

```json
{
  "code": 200,
  "status": "OK",
  "cellsCount": 123,
  "file": "base64-인코딩된 워크북 스트림"
}
```

**응답 상태 코드**

| 코드 | 의미 | 설명 |
|------|------|------|
| 200 | OK | 작업 성공; 정리된 셀 수와 업데이트된 워크북 스트림 반환 |
| 400 | Bad Request | 요청 파라미터 중 하나 이상이 누락되었거나 유효하지 않음 |
| 401 | Unauthorized | 인증 실패 또는 JWT 토큰 누락/유효하지 않음 |
| 413 | Payload Too Large | 요청이 허용된 크기 제한을 초과함 |
| 500 | Internal Server Error | 서버에서 예기치 않은 오류 발생 |

## SDK를 사용하여 원격 스프레드시트에서 중복 부분 문자열 제거 기능 사용하기

### 원격 스프레드시트에서 중복 부분 문자열 제거 API 사양

[원격 스프레드시트에서 중복 부분 문자열 제거 API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveDuplicateSubstringsInRemoteSpreadsheet)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 요청을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용해 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예시는 cURL을 사용해 Cloud API에 요청을 보내는 방법을 보여줍니다.

{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}
{< tab tabNum="1" >}
```bash
# 보안 연결을 위해 HTTPS 사용
curl -v "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/range/A1:C10/content/remove/duplicate-substrings?delimiters=comma%2Csemicolon&treatConsecutiveDelimitersAsOne=true&caseSensitive=false" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "code": 200,
  "status": "OK",
  "cellsCount": 123,
  "file": "base64-인코딩된 워크북 스트림"
}
```
{< /tab >}
{< /tabs >}

### Aspose Cells Cloud SDK 사용하기

SDK를 사용하면 개발 속도를 가장 빠르게 향상시킬 수 있습니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 작업에 집중할 수 있도록 도와줍니다. Aspose.Cells Cloud SDK 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예시는 다양한 SDK를 사용해 Aspose Cells Cloud 웹 서비스를 호출하는 방법을 보여줍니다:
`[TBD]`
---