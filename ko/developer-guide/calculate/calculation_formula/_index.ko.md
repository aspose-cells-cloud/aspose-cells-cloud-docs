---
title: "수식 계산"
ArticleTitle: "수식 계산 – Aspose.Cells Cloud API"
second_title: "문서"
linktype: "docs"
url: /cells/calculate/formula
aliases: []
keywords: "Aspose Cells, 수식 계산, 스프레드시트, API"
description: "Aspose.Cells Cloud API를 사용하여 스프레드시트에서 수식을 계산합니다."
weight: 100
---

## Aspose.Cells Cloud 웹 서비스의 수식 계산 기능

업로드된 스프레드시트 파일의 지정된 워크시트에서 주어진 수식을 계산하고, 결과 스프레드시트를 파일 스트림 형태로 반환합니다. 이 작업은 **region** 매개변수를 통해 로케일별 처리를 지원하며, 암호로 보호된 파일도 열 수 있습니다.

### 웹 API 엔드포인트

```http
PUT https://api.aspose.cloud/v4.0/cells/calculate/formula
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 보장되며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름 | 유형   | 경로/쿼리 문자열/HTTP 본문 | 설명 |
|---------------|--------|----------------------------|------|
| Spreadsheet   | 파일   | FormData                   | 업로드할 스프레드시트 파일 |
| worksheet     | 문자열 | 쿼리                       | 수식이 포함된 워크시트 이름 |
| formula       | 문자열 | 쿼리                       | 계산할 수식 (예: `=SUM(A1:B2)`) |
| region        | 문자열 | 쿼리                       | 스프레드시트 지역/언어 설정 (예: `en-US`, `fr-FR`). 숫자 서식, 날짜 파싱, 로케일별 동작에 영향을 줍니다. |
| password      | 문자열 | 쿼리                       | 스프레드시트 파일을 열기 위한 암호 |

### 요청 본문 매개변수

| 매개변수 이름 | 유형 | 설명 |
| ------------- | ---- | ---- |
| [TBD] | [TBD] | [TBD] |

### **응답**

```json
{
  "File": "<결과 스프레드시트의 이진 스트림>"
}
```

**응답 상태 코드**

| 코드 | 의미 | 설명 |
|------|------|------|
| 200 | 성공 | 계산이 성공적으로 완료되었으며, 결과 스프레드시트 파일이 반환됩니다. |
| 400 | 잘못된 요청 | 하나 이상의 요청 매개변수가 누락되었거나 유효하지 않습니다. |
| 401 | 인증되지 않음 | 인증에 실패했거나 JWT 토큰이 누락되었거나 유효하지 않습니다. |
| 413 | 페이로드가 너무 큼 | 업로드된 파일이 허용된 최대 크기를 초과했습니다. |
| 500 | 내부 서버 오류 | 서버에서 예기치 않은 오류가 발생했습니다. |

## SDK를 사용하여 수식 계산 사용 방법

### 수식 계산 사양

[수식 계산 API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Calculate/CalculationFormula)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose Cells Cloud 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예시는 cURL을 사용하여 Cloud API에 요청을 보내는 방법을 보여줍니다.

{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}

{< tab tabNum="1" >}

```bash
# 보안 연결을 위해 HTTPS 사용
curl -v "https://api.aspose.cloud/v4.0/cells/calculate/formula?worksheet=Sheet1&formula=%3DSUM(A1%3AB2)&region=en-US&password=MyPassword" \
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
  "File": "<결과 스프레드시트의 이진 스트림>"
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 가장 빠르게 향상시킬 수 있습니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 작업에 집중할 수 있게 해줍니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose Cells Cloud 웹 서비스를 호출하는 방법을 보여줍니다:
 `[TBD]`
---