---
title: "차트를 PDF로 변환"
ArticleTitle: "Aspose.Cells Cloud API를 사용하여 차트를 PDF로 변환"
second_title: "문서"
linktype: "docs"
url: /cells/convert/chart/pdf
aliases: []
keywords: "차트를 PDF로 변환, Aspose.Cells, PDF, 차트 변환"
description: "로컬 드라이브에 있는 스프레드시트의 차트를 PDF로 변환합니다."
weight: 100
---

## Aspose.Cells Cloud 웹 서비스의 차트를 PDF로 변환 기능

이 메서드는 로컬 파일 업로드를 통해 제공된 스프레드시트 파일에서 차트를 읽어 PDF 형식으로 변환한 뒤 변환 결과를 반환합니다. 이 기능은 모두 클라우드 서버에서 실행되므로 중간 저장소가 필요 없습니다. 소스 파일 경로와 대상 형식은 정확해야 하며, 소스 파일을 읽기 위한 적절한 권한이 필요합니다. 파일 누락, 접근 문제 또는 변환 실패와 같은 오류는 적절한 HTTP 오류 응답을 반환합니다.

### 웹 API 엔드포인트

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/chart/pdf
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 완비되어 있으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름   | 유형   | 경로/쿼리 문자열/HTTP 본문 | 설명 |
|------------------|--------|-----------------------------|-------------|
| Spreadsheet      | 파일   | FormData                    | 스프레드시트 파일 업로드 |
| worksheet        | 문자열 | 쿼리                        | 스프레드시트 워크시트 이름 |
| chartIndex       | 정수   | 쿼리                        | 워크시트의 차트 인덱스 |
| outPath          | 문자열 | 쿼리                        | (선택 사항) 워크북이 저장될 폴더 경로. 기본값은 null입니다. |
| outStorageName   | 문자열 | 쿼리                        | 출력 파일 저장소 이름 |
| fontsLocation    | 문자열 | 쿼리                        | 사용자 정의 글꼴 사용 |
| region           | 문자열 | 쿼리                        | 스프레드시트 지역/언어 설정(예: `en-US`, `fr-FR`). 숫자 서식, 날짜 파싱 및 로케일 관련 동작에 영향을 미칩니다. |
| password         | 문자열 | 쿼리                        | 스프레드시트 파일 열기 비밀번호 |

### 요청 본문 매개변수

| 매개변수 이름 | 유형 | 설명 |
| -------------- | ---- | ----------- |
| Spreadsheet    | 파일 | 스프레드시트 파일 업로드 |

### **응답**

```json
{
  "ResponseFile": "이진 PDF 파일 스트림"
}
```

**응답 상태 코드**

| 코드 | 의미 | 설명 |
|------|------|------|
| 200 | 성공 | 차트가 성공적으로 PDF로 변환되었으며, 이진 PDF 파일이 반환됨 |
| 400 | 잘못된 요청 | 잘못된 요청 매개변수 또는 잘못된 형식의 URL |
| 401 | 인증 실패 | 인증 실패 또는 자격 증명 미제공 |
| 404 | 찾을 수 없음 | 소스 파일에 접근할 수 없음 |
| 413 | 요청 페이로드가 너무 큼 | 업로드된 파일이 허용된 크기 제한을 초과함 |
| 500 | 내부 서버 오류 | 변환 처리 중 오류 발생 |

## SDK를 사용하여 차트를 PDF로 변환하는 방법

### 차트를 PDF로 변환 사양

[차트를 PDF로 변환 API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertChartToPdf)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예시는 cURL을 사용하여 클라우드 API에 요청하는 방법을 보여줍니다.

{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}
{< tab tabNum="1" >}
```bash
# 보안 연결을 위해 HTTPS 사용
curl -v "https://api.aspose.cloud/v4.0/cells/convert/chart/pdf?worksheet={worksheet}&chartIndex={chartIndex}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/pdf" \
  -H "Authorization: Bearer <jwt 토큰>" \
  -F "Spreadsheet=@sample.xlsx"
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "ResponseFile": "이진 PDF 파일 스트림"
}
```
{< /tab >}
{< /tabs >}

### Aspose Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 가장 빠르게 향상시킬 수 있습니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 작업에 집중할 수 있도록 해줍니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하십시오.

다음 코드 예시는 다양한 SDK를 사용하여 Aspose Cells Cloud 웹 서비스를 호출하는 방법을 보여줍니다:
`[TBD]`
---