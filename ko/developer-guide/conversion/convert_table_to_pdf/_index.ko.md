---
title: "테이블을 PDF로 변환"
ArticleTitle: "테이블을 PDF로 변환 – Aspose.Cells Cloud API"
second_title: "문서"
linktitle: "테이블을 PDF로 변환"
type: docs
url: /ko/cells/convert/table/pdf
aliases: []
keywords: "테이블 PDF 변환, Aspose.Cells, API"
description: "로컬 드라이브의 스프레드시트 테이블을 Aspose.Cells Cloud를 사용해 PDF 파일로 변환합니다."
weight: 1000
---

## Aspose.Cells Cloud 웹 서비스의 테이블을 PDF로 변환 기능

이 작업은 로컬 파일 시스템에서 스프레드시트 파일을 읽어 지정된 테이블을 PDF 문서로 변환한 후 변환된 결과를 반환합니다. 이 과정은 모두 클라우드 서버에서 완료되므로 클라우드 스토리지로의 중간 업로드가 필요 없습니다. 이 API는 출력 위치, 사용자 정의 글꼴, 행/열 자동 조정, 지역 설정, 암호로 보호된 워크북 등에 대한 선택적 매개변수를 지원합니다.

### 웹 API 엔드포인트

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/pdf
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 위해 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>을 요구합니다.

### 요청 매개변수

| 매개변수 이름   | 유형   | 경로/쿼리 문자열/HTTP 본문 | 설명                                                                                                                                                     |
|----------------|--------|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet    | 파일   | FormData                  | 업로드할 스프레드시트 파일.                                                                                                                              |
| worksheet      | 문자열 | 쿼리                      | 스프레드시트의 워크시트 이름.                                                                                                                            |
| tableName      | 문자열 | 쿼리                      | 테이블 이름.                                                                                                                                             |
| outPath        | 문자열 | 쿼리                      | (선택 사항) 워크북이 저장될 폴더 경로. 기본값은 null입니다.                                                                                             |
| outStorageName | 문자열 | 쿼리                      | 출력 파일의 스토리지 이름.                                                                                                                               |
| fontsLocation  | 문자열 | 쿼리                      | 사용자 정의 글꼴 사용.                                                                                                                                   |
| AutoRowsFit    | 불리언 | 쿼리                      | (선택 사항) 워크시트의 모든 행을 자동으로 조정합니다.                                                                                                    |
| AutoColumnsFit | 불리언 | 쿼리                      | (선택 사항) 워크시트의 모든 열을 자동으로 조정합니다.                                                                                                   |
| region         | 문자열 | 쿼리                      | 스프레드시트 지역/언어 설정(예: `en-US`, `fr-FR`). 숫자 서식, 날짜 파싱 및 로케일 관련 동작에 영향을 미칩니다.                                          |
| password       | 문자열 | 쿼리                      | 스프레드시트 파일을 열기 위한 암호.                                                                                                                      |

### 요청 본문 매개변수

| 매개변수 이름 | 유형 | 설명 |
|--------------|------|------|
| *없음* | *없음* | *JSON 본문이 필요하지 않습니다. 파일은 multipart/form-data를 통해 전송됩니다.* |

### **응답**

```json
{
  "file": "<이진 PDF 콘텐츠>"
}
```

**응답 상태 코드**

| 코드 | 의미 | 설명 |
|------|------|------|
| 200 | 성공 | 테이블이 성공적으로 PDF로 변환되었으며, 응답 본문에 PDF 파일 스트림이 포함됩니다. |
| 400 | 잘못된 요청 | 요청 매개변수가 유효하지 않거나 URL이 잘못되었습니다. |
| 401 | 인증 실패 | 인증에 실패했거나 자격 증명이 제공되지 않았습니다. |
| 404 | 존재하지 않음 | 원본 파일에 접근할 수 없거나 워크시트/테이블을 찾을 수 없습니다. |
| 413 | 페이로드가 너무 큼 | 업로드된 스프레드시트가 허용된 크기 제한을 초과했습니다. |
| 500 | 내부 서버 오류 | 스프레드시트를 PDF로 변환하는 중 오류가 발생했습니다. |

## SDK를 사용하여 테이블을 PDF로 변환하는 방법

### 테이블을 PDF로 변환 사양

[테이블을 PDF로 변환 API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToPdf)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 요청을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells Cloud 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예제는 cURL을 사용해 클라우드 API를 호출하는 방법을 보여줍니다.

{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}

{< tab tabNum="1" >}

```bash
# 보안 연결을 위해 HTTPS 사용
curl -v "https://api.aspose.cloud/v4.0/cells/convert/table/pdf?worksheet={worksheet}&tableName={tableName}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&AutoRowsFit={AutoRowsFit}&AutoColumnsFit={AutoColumnsFit}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/pdf" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<이진 PDF 콘텐츠>"
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 가장 빠르게 향상시킬 수 있습니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 작업에 집중할 수 있도록 도와줍니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 참조하십시오.

다음 코드 예제는 다양한 SDK를 사용해 Aspose.Cells Cloud 웹 서비스를 호출하는 방법을 보여줍니다:

```csharp
// C#용 SDK 예제 코드
var apiInstance = new ConversionApi();
var file = File.ReadAllBytes("sample.xlsx");
var response = apiInstance.ConvertTableToPdf(
    file,
    worksheet: "Sheet1",
    tableName: "Table1",
    outPath: null,
    outStorageName: null,
    fontsLocation: null,
    AutoRowsFit: null,
    AutoColumnsFit: null,
    region: null,
    password: null);
File.WriteAllBytes("output.pdf", response);
```

```java
// Java용 SDK 예제 코드
ConversionApi apiInstance = new ConversionApi();
byte[] file = Files.readAllBytes(Paths.get("sample.xlsx"));
byte[] result = apiInstance.convertTableToPdf(
    file,
    "Sheet1",
    "Table1",
    null,
    null,
    null,
    null,
    null,
    null,
    null);
Files.write(Paths.get("output.pdf"), result);
```

```python
# Python용 SDK 예제 코드
api_instance = conversion_api.ConversionApi()
with open("sample.xlsx", "rb") as f:
    file_bytes = f.read()
pdf_bytes = api_instance.convert_table_to_pdf(
    file=file_bytes,
    worksheet="Sheet1",
    table_name="Table1")
with open("output.pdf", "wb") as out_file:
    out_file.write(pdf_bytes)
```

`[TBD]`