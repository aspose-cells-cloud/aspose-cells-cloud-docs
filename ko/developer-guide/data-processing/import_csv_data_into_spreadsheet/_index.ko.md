---
title: "CSV 데이터를 스프레드시트로 가져오기"
ArticleTitle: "CSV 데이터를 스프레드시트로 가져오기 – Aspose.Cells Cloud API"
second_title: "문서"
linktitle: "CSV 데이터를 스프레드시트로 가져오기"
type: docs
url: /ko/cells/import/data/csv
aliases: []
keywords: "Aspose.Cells, CSV 가져오기, 스프레드시트, API"
description: "Aspose.Cells Cloud API를 사용하여 로컬 스프레드시트에 CSV 데이터 파일을 가져옵니다."
weight: 100
---

## Aspose.Cells Cloud 웹 서비스의 CSV 데이터를 스프레드시트로 가져오기

CSV 데이터 파일을 로컬 스프레드시트로 가져옵니다. 이 메서드는 CSV를 파싱하여 스프레드시트의 셀 구조에 데이터를 매핑한 후 파일을 로컬에 저장합니다. 지원되는 스프레드시트 형식은 .xlsx 및 .ods입니다.

### 웹 API 엔드포인트

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data/csv
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 보장되며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름         | 유형    | 경로/쿼리 문자열/HTTP 본문 | 설명                                                                                                                          |
|-----------------------|---------|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| datafile              | 파일    | FormData                    | 데이터 파일을 업로드합니다.                                                                                                                    |
| Spreadsheet           | 파일    | FormData                    | 스프레드시트 파일을 업로드합니다.                                                                                                             |
| worksheet             | 문자열  | 쿼리                        | CSV 데이터를 가져올 워크시트를 지정합니다. (필수)                                                                              |
| startcell             | 문자열  | 쿼리                        | 데이터 가져오기 시작 위치입니다. (필수)                                                                                       |
| insert                | 논리형  | 쿼리                        | 삽입 동작을 제어합니다. true: 데이터 삽입; false: 기존 데이터 덮어쓰기. 기본값: true (선택 사항)                     |
| convertNumericData    | 논리형  | 쿼리                        | 텍스트 파일의 문자열을 숫자 데이터로 변환할지 여부입니다. 기본값: true (선택 사항)                                            |
| splitter              | 문자열  | 쿼리                        | CSV 필드를 분할하는 구분자입니다. 기본값: "," (선택 사항)                                                                         |
| outPath               | 문자열  | 쿼리                        | (선택 사항) 워크북이 저장될 폴더 경로입니다. 기본값은 null입니다 (선택 사항).                                            |
| outStorageName        | 문자열  | 쿼리                        | 출력 파일 저장소 이름입니다. (선택 사항)                                                                                                |
| fontsLocation         | 문자열  | 쿼리                        | 사용자 정의 폰트를 사용합니다. (선택 사항)                                                                                                         |
| region                | 문자열  | 쿼리                        | 스프레드시트 지역/언어 설정(예: `en-US`, `fr-FR`). 숫자 서식, 날짜 파싱 및 로케일별 동작에 영향을 줍니다. (선택 사항) |
| password              | 문자열  | 쿼리                        | 스프레드시트 파일을 열기 위한 암호입니다. (선택 사항)                                                                              |

### 요청 본문 매개변수

| 매개변수 이름 | 유형 | 설명 |
| ------------ | ---- | ----------- |
| [TBD] | [TBD] | [TBD] |

### **응답**

```json
{
  "file": "<결과 스프레드시트의 바이너리 스트림>"
}
```

**응답 상태 코드**

| 코드 | 의미 | 설명 |
|------|------|-------------|
| 200 | 성공 | CSV 데이터가 성공적으로 가져와지고 결과 스프레드시트 파일이 반환됩니다. |
| 400 | 잘못된 요청 | 잘못된 요청 매개변수 또는 잘못된 형식의 URL입니다. |
| 401 | 인증 실패 | 인증에 실패했거나 자격 증명이 제공되지 않았습니다. |
| 404 | 없음 | 소스 파일에 접근할 수 없습니다. |
| 413 | 페이로드가 너무 큼 | 업로드된 파일이 허용된 크기 제한을 초과했습니다. |
| 500 | 내부 서버 오류 | 스프레드시트에서 데이터를 가져오는 도중 오류가 발생했습니다. |

## SDK를 사용하여 CSV 데이터를 스프레드시트로 가져오기

### CSV 데이터를 스프레드시트로 가져오기 사양

[CSV 데이터를 스프레드시트로 가져오기 API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/ImportCSVDataIntoSpreadsheet)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예제는 cURL을 사용하여 Cloud API에 요청을 보내는 방법을 보여줍니다.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# 안전한 연결을 위해 HTTPS 사용
curl -v "https://api.aspose.cloud/v4.0/cells/import/data/csv?worksheet=Sheet1&startcell=A1&insert=true&convertNumericData=true&splitter=,&outPath=outputFolder&outStorageName=MyStorage&fontsLocation=/custom/fonts&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F "datafile=@sample.csv" \
  -F "Spreadsheet=@workbook.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<결과 스프레드시트의 바이너리 스트림>"
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK 사용

SDK를 사용하는 것이 개발 속도를 높이는 가장 빠른 방법입니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 작업에 집중할 수 있도록 합니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose Cells Cloud 웹 서비스를 호출하는 방법을 보여줍니다:
 `[TBD]`
---