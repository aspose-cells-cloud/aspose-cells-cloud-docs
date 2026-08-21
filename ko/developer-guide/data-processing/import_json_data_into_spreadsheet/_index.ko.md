---
title: "JSON 데이터를 스프레드시트로 가져오기"
ArticleTitle: "JSON 데이터를 스프레드시트로 가져오기 – Aspose.Cells Cloud API"
second_title: "문서"
linktype: "docs"
url: "/cells/import/data/json"
aliases: []
keywords: "JSON 가져오기, Aspose.Cells, 스프레드시트, API"
description: "로컬 스프레드시트에 JSON 데이터 파일을 가져옵니다."
weight: 1
---

## Aspose.Cells Cloud 웹 서비스의 JSON 데이터를 스프레드시트로 가져오기

JSON 데이터 파일을 로컬 스프레드시트로 가져옵니다. 이 메서드는 JSON을 파싱하고, 데이터를 스프레드시트의 셀 구조에 매핑한 뒤, 파일을 로컬에 저장합니다. 지원되는 스프레드시트 형식은 .xlsx 및 .ods입니다.

### 웹 API 엔드포인트

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data/json
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 보장되며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름 | 유형   | 경로/쿼리 문자열/HTTP 본문 | 설명 |
|---------------|--------|----------------------------|------|
| datafile      | 파일   | FormData                   | 데이터 파일을 업로드합니다. |
| Spreadsheet   | 파일   | FormData                   | 스프레드시트 파일을 업로드합니다. |
| worksheet     | 문자열 | 쿼리                       | JSON 데이터를 가져올 워크시트를 지정합니다. |
| startcell     | 문자열 | 쿼리                       | 데이터 가져오기 시작 위치 |
| insert        | 논리값 | 쿼리                       | 삽입 동작을 제어합니다. true: 데이터 삽입; false: 기존 데이터 덮어쓰기. (기본값: true) |
| outPath       | 문자열 | 쿼리                       | (선택사항) 워크북이 저장될 폴더 경로입니다. 기본값은 null입니다. |
| outStorageName| 문자열 | 쿼리                       | 출력 파일 저장소 이름 |
| fontsLocation | 문자열 | 쿼리                       | 사용자 정의 글꼴 사용 |
| region        | 문자열 | 쿼리                       | 스프레드시트 지역/언어 설정(예: `en-US`, `fr-FR`). 숫자 서식, 날짜 파싱 및 지역별 동작에 영향을 줍니다. |
| password      | 문자열 | 쿼리                       | 스프레드시트 파일을 열기 위한 비밀번호 |

### 요청 본문 매개변수

| 매개변수 이름 | 유형 | 설명 |
| -------------- | ---- | ----------- |
| [TBD] | [TBD] | [TBD] |

### **응답**

```json
{
  "file": "이진 스트림"
}
```

**응답 상태 코드**

| 코드 | 의미 | 설명 |
|------|------|------|
| 200 | 성공 | 파일이 성공적으로 생성되어 반환되었습니다. |
| 400 | 잘못된 요청 | 잘못된 URL입니다. |
| 401 | 인증 실패 | 인증에 실패했거나 자격 증명이 제공되지 않았습니다. |
| 404 | 찾을 수 없음 | 소스 파일에 접근할 수 없습니다. |
| 413 | 요청 본문이 너무 큼 | [TBD] |
| 500 | 내부 서버 오류 | 스프레드시트에서 데이터를 가져오는 도중 예외가 발생했습니다. |

## SDK를 사용하여 JSON 데이터를 스프레드시트로 가져오기

### JSON 데이터를 스프레드시트로 가져오기 사양

[JSON 데이터를 스프레드시트로 가져오기 API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/ImportJSONDataIntoSpreadsheet)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose Cells Cloud 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API에 요청을 보내는 방법을 보여줍니다.

{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}
{< tab tabNum="1" >}
```bash
# 보안 연결을 위해 HTTPS 사용
curl -v "https://api.aspose.cloud/v4.0/cells/import/data/json?worksheet=Sheet1&startcell=A1&insert=true&outPath=output%2F&outStorageName=MyStorage&fontsLocation=%2Ffonts&region=en-US&password=Secret" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "datafile=@data.json" \
  -F "Spreadsheet=@workbook.xlsx"
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "file": "이진 스트림"
}
```
{< /tab >}
{< /tabs >}

### Aspose Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 가장 빠르게 향상시킬 수 있습니다. SDK는 하위 수준의 세부 사항을 추상화하여 프로젝트 작업에 집중할 수 있게 해줍니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose Cells Cloud 웹 서비스를 호출하는 방법을 보여줍니다:
 `[TBD]`
---