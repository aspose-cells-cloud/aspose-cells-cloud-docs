---
title: "ConvertWorksheetToPdf"
ArticleTitle: "워크시트를 PDF로 변환 – Aspose.Cells Cloud API"
second_title: "문서"
linktitle: "ConvertWorksheetToPdf"
type: docs
url: /ko/cells/convert/worksheet/pdf
aliases: []
keywords: "Aspose.Cells, 워크시트를 PDF로 변환, API"
description: "Aspose.Cells Cloud를 사용하여 스프레드시트 파일의 워크시트를 PDF로 변환합니다."
weight: 10
---

## Aspose.Cells Cloud 웹 서비스의 ConvertWorksheetToPdf

이 메서드는 로컬 파일 시스템에서 스프레드시트 파일을 읽어 워크시트를 PDF 파일로 변환한 후 변환된 결과를 반환합니다. 소스 파일 경로와 대상 형식을 올바르게 지정해야 합니다. 소스 파일을 읽고, 필요한 경우 변환된 파일을 쓸 수 있는 적절한 권한이 설정되어 있는지 확인하십시오. 변환 프로세스는 클라우드 서버 내에서 완전히 수행되므로 클라우드 스토리지 사용이나 외부 다운로드가 필요 없습니다.

주요 기능으로는 클라우드 네이티브 변환, 클라우드 리소스 부하 감소, 간소화된 워크플로우가 있습니다.

### 웹 API 엔드포인트

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 확보되어 있으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 파라미터

| 파라미터 이름   | 유형    | 경로/쿼리 스트링/HTTP 본문 | 설명                                                                                                                            |
|------------------|---------|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | 파일    | FormData                    | 스프레드시트 파일 업로드.                                                                                                               |
| worksheet        | 문자열  | 쿼리                        | 스프레드시트의 워크시트 이름.                                                                                                         |
| outPath          | 문자열  | 쿼리                        | (선택 사항) 워크북이 저장될 폴더 경로. 기본값은 null입니다.                                                          |
| outStorageName   | 문자열  | 쿼리                        | 출력 파일 스토리지 이름.                                                                                                              |
| fontsLocation    | 문자열  | 쿼리                        | 사용자 정의 폰트 사용.                                                                                                                      |
| AutoRowsFit      | 불리언  | 쿼리                        | (선택 사항) 워크시트의 모든 행을 자동 조정.                                                                                           |
| AutoColumnsFit   | 불리언  | 쿼리                        | (선택 사항) 워크시트의 모든 열을 자동 조정.                                                                                        |
| region           | 문자열  | 쿼리                        | 스프레드시트 지역/언어 설정(예: `en-US`, `fr-FR`). 숫자 서식, 날짜 파싱 및 로케일 관련 동작에 영향을 미칩니다. |
| password         | 문자열  | 쿼리                        | 스프레드시트 파일을 열기 위한 비밀번호.                                                                                             |

### 요청 본문 파라미터

| 파라미터 이름 | 유형 | 설명 |
| -------------- | ---- | ----------- |
| [TBD]          |      |             |

### **응답**

```json
{
  "file": "<생성된 PDF의 바이너리 스트림>"
}
```

**응답 상태 코드**

| 코드 | 의미 | 설명 |
|------|---------|-------------|
| 200 | 성공 | 워크시트가 성공적으로 PDF로 변환되어 파일 스트림으로 반환됨. |
| 400 | 잘못된 요청 | 잘못된 요청 파라미터 또는 잘못된 형식의 URL. |
| 401 | 인증 실패 | 인증에 실패했거나 자격 증명이 제공되지 않음. |
| 404 | 찾을 수 없음 | 소스 파일에 접근할 수 없음. |
| 413 | 페이로드 너무 큼 | 업로드된 파일이 허용된 크기 제한을 초과함. |
| 500 | 내부 서버 오류 | 변환 중 스프레드시트에 문제가 발생함. |

## SDK를 사용하여 ConvertWorksheetToPdf 사용 방법

### ConvertWorksheetToPdf 사양

[ConvertWorksheetToPdf API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#Conversion/ConvertWorksheetToPdf)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API에 요청을 보내는 방법을 보여줍니다.

{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}

{< tab tabNum="1" >}

```bash
# 안전한 연결을 위해 HTTPS 사용
curl -v "https://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf?worksheet=Sheet1&outPath=output%2Ffolder&outStorageName=MyStorage&fontsLocation=%2Fcustom%2Ffonts&AutoRowsFit=true&AutoColumnsFit=true&region=en-US&password=SecretPwd" \
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
  "file": "<생성된 PDF의 바이너리 스트림>"
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 가장 빠르게 향상시킬 수 있습니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 작업에 집중할 수 있도록 도와줍니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose Cells Cloud 웹 서비스를 호출하는 방법을 보여줍니다:
`[TBD]`
---