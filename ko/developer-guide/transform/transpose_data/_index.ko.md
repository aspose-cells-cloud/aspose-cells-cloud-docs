---
title: "TransposeData"
ArticleTitle: "TransposeData – Aspose.Cells Cloud API"
second_title: "문서"
linktype: "docs"
url: /ko/cells/transpose
aliases: [  /ko/cells/transpose ]
keywords: "TransposeData, Aspose.Cells, 클라우드 API, 스프레드시트, 전치"
description: "스프레드시트에서 행과 열을 전치합니다."
weight: 1000
---

## Aspose.Cells Cloud 웹 서비스의 TransposeData

스프레드시트에서 행과 열을 전치합니다.

### 웹 API 엔드포인트

```http
PUT https://api.aspose.cloud/v4.0/cells/transpose
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름   | 유형   | 경로/쿼리 문자열/HTTP 본문 | 설명                                                                                                                            |
|------------------|--------|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | 파일   | FormData                    | 업로드할 스프레드시트 파일.                                                                                                               |
| worksheet        | 문자열 | 쿼리                        | 워크시트 이름.                                                                                                                    |
| cellArea         | 문자열 | 쿼리                        | 지정된 데이터 범위.                                                                                                                |
| outPath          | 문자열 | 쿼리                        | (선택 사항) 워크북이 저장될 폴더 경로. 기본값은 null입니다.                                                          |
| outStorageName   | 문자열 | 쿼리                        | 출력 파일 저장소 이름.                                                                                                              |
| region           | 문자열 | 쿼리                        | 스프레드시트 지역/언어 설정(예: `en-US`, `fr-FR`). 숫자 서식, 날짜 파싱, 지역별 동작에 영향을 미칩니다. |
| password         | 문자열 | 쿼리                        | 스프레드시트 파일을 열기 위한 비밀번호.                                                                                             |

### 요청 본문 매개변수

| 매개변수 이름 | 유형 | 설명 |
| -------------- | ---- | ----------- |
| [TBD]          | [TBD]| [TBD]       |

### **응답**

```json
{
  "file": "전치된 스프레드시트의 이진 스트림"
}
```

**응답 상태 코드**

| 코드 | 의미 | 설명 |
|------|------|------|
| 200 | OK | 전치된 스프레드시트 파일이 반환됩니다. |
| 400 | Bad Request | 잘못된 입력 매개변수 또는 잘못된 형식의 요청입니다. |
| 401 | Unauthorized | 인증에 실패했거나 JWT 토큰이 누락되었거나 유효하지 않습니다. |
| 413 | Payload Too Large | 업로드된 파일이 허용된 크기 제한을 초과합니다. |
| 500 | Internal Server Error | 예기치 않은 서버 오류입니다. |

## SDK를 사용하여 TransposeData 사용 방법

### TransposeData 사양

[TransposeData API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{Transform}/{TransposeData})은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 요청을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose Cells Cloud 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API로 요청을 보내는 방법을 보여줍니다.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# 안전한 연결을 위해 HTTPS 사용
curl -v "https://api.aspose.cloud/v4.0/cells/transpose?worksheet=Sheet1&cellArea=A1:C10&outPath=output%2Ffolder&outStorageName=MyStorage&region=en-US&password=MyPassword" \
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
  "file": "전치된 스프레드시트의 이진 스트림"
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 가장 빠르게 향상시킬 수 있습니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 작업에 집중할 수 있게 해줍니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose Cells Cloud 웹 서비스를 호출하는 방법을 보여줍니다:
`[TBD]`
---