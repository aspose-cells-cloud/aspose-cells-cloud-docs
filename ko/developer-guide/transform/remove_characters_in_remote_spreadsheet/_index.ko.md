---
title: "원격 스프레드시트에서 문자 제거"
ArticleTitle: "원격 스프레드시트에서 문자 제거 – Aspose.Cells Cloud API"
second_title: "문서"
linktype: "docs"
url: /ko/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/characters
aliases: []
keywords: "Aspose.Cells, 문자 제거, 텍스트 처리"
description: "원격 스프레드시트의 선택한 범위 내 모든 셀에서 사용자 정의 문자, 미리 정의된 기호 집합 또는 임의의 부분 문자열을 제거하면서 수식, 서식 및 데이터 유효성 검사를 보존합니다."
weight: 100
---

## Aspose.Cells Cloud 웹 서비스의 원격 스프레드시트에서 문자 제거 기능

원격 스프레드시트의 선택한 범위 내 모든 셀에서 사용자 정의 문자, 미리 정의된 기호 집합 또는 임의의 부분 문자열을 제거하면서 수식, 서식 및 데이터 유효성 검사를 보존합니다.

### 웹 API 엔드포인트

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/characters
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 확보되었으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 파라미터

| 파라미터 이름       | 유형    | 경로/쿼리 문자열/HTTP 본문 | 설명                                                                                                                                                                       |
|---------------------|---------|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name                | string  | 경로                        | (필수) 가져올 워크북 파일의 이름입니다.                                                                                                                         |
| worksheet           | string  | 경로                        | 스프레드시트의 워크시트를 지정합니다.                                                                                                                                              |
| range               | string  | 경로                        | 스프레드시트의 워크시트 범위를 지정합니다.                                                                                                                                       |
| removeTextMethod    | string  | 쿼리                        | 텍스트 제거 방법 유형을 지정합니다.                                                                                                                                          |
| characterSets       | string  | 쿼리                        | 문자 집합을 지정합니다.                                                                                                                                                       |
| removeCustomValue   | string  | 쿼리                        | 사용자 정의 값 제거를 지정합니다.                                                                                                                                                  |
| caseSensitive       | boolean | 쿼리                        | `Substring` 모드 및 `CustomChars`에 영향을 미치며, 활성화 시 대소문자를 구분합니다.                                                                                                                          |
| folder              | string  | 쿼리                        | (선택 사항) 워크북이 저장된 폴더 경로입니다. 기본값은 null입니다.                                                                                                    |
| storageName         | string  | 쿼리                        | (선택 사항) 사용자 정의 클라우드 스토리지를 사용할 경우 스토리지 이름입니다. 생략 시 기본 스토리지를 사용합니다.                                                                               |
| region              | string  | 쿼리                        | 스프레드시트 지역/언어 설정(예: `en-US`, `fr-FR`)입니다. 숫자 서식, 날짜 파싱 및 지역별 동작에 영향을 미칩니다.                                         |
| password            | string  | 쿼리                        | 스프레드시트 파일을 열기 위한 비밀번호입니다.                                                                                                                                         |

### 요청 본문 파라미터

| 파라미터 이름 | 유형 | 설명 |
| -------------- | ---- | ----------- |
| *없음* | *없음* | 이 작업은 요청 본문이 필요하지 않습니다. |

### **응답**

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "문자가 성공적으로 제거되었습니다.",
  "Data": {
    "RequestId": "string",
    "Workbook": {
      "Name": "string",
      "Path": "string"
    }
  }
}
```

**응답 상태 코드**

| 코드 | 의미 | 설명 |
|------|---------|-------------|
| 200 | OK | 문자가 성공적으로 제거되었으며 워크북이 업데이트되었습니다. |
| 400 | Bad Request | 하나 이상의 파라미터가 누락되었거나 유효하지 않습니다. |
| 401 | Unauthorized | 인증 실패 – JWT 토큰이 누락되었거나 유효하지 않습니다. |
| 413 | Payload Too Large | 요청 크기가 허용된 한도를 초과합니다. |
| 500 | Internal Server Error | 서버 측에서 예기치 않은 오류가 발생했습니다. |

## SDK를 사용하여 원격 스프레드시트에서 문자 제거하는 방법

### 원격 스프레드시트에서 문자 제거 사양

[원격 스프레드시트에서 문자 제거 API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{TextProcessingController}/RemoveCharactersInRemoteSpreadsheet)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API에 호출을 수행하는 방법을 보여줍니다.

{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}

{< tab tabNum="1" >}

```bash
# 안전한 연결을 위해 HTTPS 사용
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/characters?removeTextMethod={removeTextMethod}&characterSets={characterSets}&removeCustomValue={removeCustomValue}&caseSensitive={caseSensitive}&folder={folder}&storageName={storageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt 토큰>"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "문자가 성공적으로 제거되었습니다.",
  "Data": {
    "RequestId": "3f5e2c1a-9b7d-4a6e-8c2f-1d5e9b7a6c4f",
    "Workbook": {
      "Name": "Sample.xlsx",
      "Path": "/documents/Sample.xlsx"
    }
  }
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 가장 빠르게 향상시킬 수 있습니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 작업에 집중할 수 있도록 해줍니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose Cells Cloud 웹 서비스를 호출하는 방법을 보여줍니다:
`[TBD]`
---