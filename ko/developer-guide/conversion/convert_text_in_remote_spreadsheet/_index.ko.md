---
title: "원격 스프레드시트 내 텍스트 변환"
ArticleTitle: "원격 스프레드시트 내 텍스트 변환 – Aspose.Cells Cloud"
second_title: "문서"
linktitle: "원격 스프레드시트 내 텍스트 변환"
type: docs
url: /ko/cells/{name}/worksheets/{worksheet}/range/{range}/content/convert/text
aliases: []
keywords: "Aspose.Cells, 텍스트 변환, API"
description: "지정된 범위의 워크시트 내 텍스트를 변환합니다. 여기에는 숫자 변환, 문자 치환, 줄바꿈 처리, 악센트 문자 정규화가 포함됩니다."
weight: 1000
---

## Aspose.Cells Cloud 웹 서비스의 원격 스프레드시트 내 텍스트 변환 기능

이 기능은 텍스트로 저장된 숫자를 올바른 숫자 형식으로 변환하고, 원하지 않는 문자 및 줄바꿈을 원하는 문자로 대체하며, 악센트가 포함된 문자를 해당 악센트 없는 동등한 문자로 변환합니다.

### 웹 API 엔드포인트

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/convert/text
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 확보되었으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 파라미터

| 파라미터 이름   | 유형   | 경로/쿼리 문자열/HTTP 본문 | 설명 |
|------------------|--------|-----------------------------|-------------|
| name             | string | Path | (필수) 조회할 워크북 파일 이름 |
| worksheet        | string | Path | 스프레드시트 워크시트 지정 |
| range            | string | Path | 스프레드시트 워크시트 범위 지정 |
| convertTextType  | string | Query | 텍스트 유형 변환을 지정합니다. (필수) |
| sourceCharacters | string | Query | 원본 문자를 지정합니다. (선택 사항) |
| targetCharacters | string | Query | 대상 문자를 지정합니다. (선택 사항) |
| folder           | string | Query | (선택 사항) 워크북이 저장된 폴더 경로입니다. 기본값은 null입니다. |
| storageName      | string | Query | (선택 사항) 사용자 지정 클라우드 스토리지를 사용할 경우 스토리지 이름입니다. 생략 시 기본 스토리지를 사용합니다. |
| region           | string | Query | 스프레드시트 지역/언어 설정(예: `en-US`, `fr-FR`). 숫자 형식, 날짜 파싱 및 로케일별 동작에 영향을 줍니다. (선택 사항) |
| password         | string | Query | 스프레드시트 파일을 열기 위한 비밀번호입니다. (선택 사항) |

### 요청 본문 파라미터

| 파라미터 이름 | 유형 | 설명 |
| -------------- | ---- | ----------- |
| - | - | - |

### **응답**

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "텍스트 변환이 성공적으로 완료되었습니다.",
  "Data": {
    // 여기에 업데이트된 셀 수 등 변환 결과 세부 정보를 추가할 수 있습니다.
  }
}
```

**응답 상태 코드**

| 코드 | 의미 | 설명 |
|------|---------|-------------|
| 200 | OK | 텍스트 변환 작업이 성공적으로 완료되었습니다. |
| 400 | Bad Request | 요청이 잘못된 형식이거나 필수 파라미터가 누락되었습니다. |
| 401 | Unauthorized | 인증에 실패했거나 JWT 토큰이 누락되었거나 유효하지 않습니다. |
| 413 | Payload Too Large | 요청 본문 크기가 허용된 최대 크기를 초과했습니다. |
| 500 | Internal Server Error | 서버에서 예기치 않은 오류가 발생했습니다. |

## SDK를 사용한 원격 스프레드시트 내 텍스트 변환 사용 방법

### 원격 스프레드시트 내 텍스트 변환 사양

[원격 스프레드시트 내 텍스트 변환 API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{TextProcessingController}/{ConvertTextInRemoteSpreadsheet})은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 요청을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose Cells Cloud 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용해 클라우드 API에 요청을 보내는 방법을 보여줍니다.

{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}

{< tab tabNum="1" >}

```bash
# 보안 연결을 위해 HTTPS 사용
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/convert/text?convertTextType={convertTextType}&sourceCharacters={sourceCharacters}&targetCharacters={targetCharacters}&folder={folder}&storageName={storageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "텍스트 변환이 성공적으로 완료되었습니다.",
  "Data": {
    "UpdatedCellsCount": 124,
    "Details": "숫자가 변환되었고, 문자가 대체되었으며, 줄바꿈이 정규화되었습니다."
  }
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 가장 빠르게 향상시킬 수 있습니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 작업에 집중할 수 있도록 해줍니다. Aspose.Cells Cloud SDK 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용해 Aspose Cells Cloud 웹 서비스를 호출하는 방법을 보여줍니다:
 `[TBD]`
---