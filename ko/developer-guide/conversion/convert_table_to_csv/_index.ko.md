---
title: "테이블을 CSV로 변환"
ArticleTitle: "테이블을 CSV로 변환 – Aspose.Cells Cloud API"
second_title: "문서"
linktitle: "테이블을 CSV로 변환"
type: docs
url: /cells/convert/table/csv
aliases: []
keywords: "테이블 CSV 변환, Aspose.Cells, 클라우드 API"
description: "로컬 드라이브에 있는 스프레드시트의 테이블을 CSV 파일로 변환합니다."
weight: 1
---

## Aspose.Cells Cloud 웹 서비스의 테이블을 CSV로 변환

이 메서드는 로컬 파일 시스템에서 스프레드시트 파일을 읽어 지정된 테이블을 CSV 파일로 변환한 후 변환 결과를 반환합니다. 이 기능은 클라우드 서버에서 완전히 실행되므로 클라우드 스토리지로 중간 업로드가 필요하지 않습니다. 소스 파일 경로와 대상 형식을 올바르게 지정해야 하며, 소스 파일을 읽기 위한 적절한 권한이 필요합니다. 파일 누락, 경로 접근 불가능 또는 변환 실패와 같은 오류는 적절한 예외를 발생시킵니다.

### 웹 API 엔드포인트

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/csv
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 위해 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름     | 유형   | 경로/쿼리 문자열/HTTP 본문 | 설명 |
|------------------|--------|-----------------------------|-------------|
| Spreadsheet      | 파일   | FormData                    | 스프레드시트 파일 업로드 |
| worksheet        | 문자열 | 쿼리                        | 스프레드시트 워크시트 이름 |
| tableName        | 문자열 | 쿼리                        | 테이블 이름 |
| outPath          | 문자열 | 쿼리                        | (선택 사항) 워크북이 저장될 폴더 경로. 기본값은 null입니다. |
| outStorageName   | 문자열 | 쿼리                        | 출력 파일 스토리지 이름 |
| fontsLocation    | 문자열 | 쿼리                        | 사용자 지정 폰트 사용 |
| AutoRowsFit      | 부울   | 쿼리                        | (선택 사항) 워크시트의 모든 행을 자동 조정 |
| AutoColumnsFit   | 부울   | 쿼리                        | (선택 사항) 워크시트의 모든 열을 자동 조정 |
| region           | 문자열 | 쿼리                        | 스프레드시트 지역/언어 설정(예: `en-US`, `fr-FR`). 숫자 서식, 날짜 파싱 및 로케일 관련 동작에 영향을 줍니다. |
| password         | 문자열 | 쿼리                        | 스프레드시트 파일을 열기 위한 비밀번호 |

### 요청 본문 매개변수

| 매개변수 이름 | 유형 | 설명 |
| -------------- | ---- | ----------- |
| *없음* | *없음* | *요청 본문이 필요하지 않습니다. 파일은 multipart/form-data로 전송됩니다.* |

### **응답**

```json
{
  "file": "생성된 CSV 파일의 이진 스트림"
}
```

**응답 상태 코드**

| 코드 | 의미 | 설명 |
|------|------|-------------|
| 200 | 성공 | 테이블이 성공적으로 변환되어 CSV 파일이 반환됩니다. |
| 400 | 잘못된 요청 | 잘못된 요청 매개변수 또는 잘못된 형식의 URL |
| 401 | 인증되지 않음 | 인증 실패 또는 자격 증명이 제공되지 않음 |
| 404 | 존재하지 않음 | 소스 파일에 접근할 수 없거나 파일이 존재하지 않음 |
| 413 | 페이로드가 너무 큼 | 업로드된 파일이 허용된 크기 제한을 초과함 |
| 500 | 내부 서버 오류 | 변환 중 스프레드시트에 문제가 발생함 |

## SDK를 사용하여 테이블을 CSV로 변환하는 방법

### 테이블을 CSV로 변환 스펙

[테이블을 CSV로 변환 API 스펙](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToCsv)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API로 요청을 보내는 방법을 보여줍니다.

{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}

{< tab tabNum="1" >}

```bash
# 안전한 연결을 위해 HTTPS 사용
curl -v "https://api.aspose.cloud/v4.0/cells/convert/table/csv?worksheet={worksheet}&tableName={tableName}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&AutoRowsFit={AutoRowsFit}&AutoColumnsFit={AutoColumnsFit}&region={region}&password={password}" \
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
  "file": "생성된 CSV 파일의 이진 스트림"
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK 사용

SDK를 사용하면 개발 속도가 가장 빨라집니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 작업에 집중할 수 있게 해줍니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells Cloud 웹 서비스를 호출하는 방법을 보여줍니다:
`[TBD]`
---