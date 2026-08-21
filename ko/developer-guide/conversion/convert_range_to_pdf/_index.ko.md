---
title: "ConvertRangeToPdf"
ArticleTitle: "범위를 PDF로 변환 – Aspose.Cells Cloud API"
second_title: "문서"
linktype: "docs"
url: /cells/convert/range/pdf
aliases: []
keywords: "Aspose.Cells, 범위를 PDF로 변환, API"
description: "Aspose.Cells Cloud를 사용하여 스프레드시트의 지정된 범위를 PDF로 변환합니다."
weight: 1
---

## Aspose.Cells Cloud 웹 서비스의 ConvertRangeToPdf

로컬 드라이브에 있는 스프레드시트의 범위를 PDF 파일로 변환합니다.

### 웹 API 엔드포인트

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/pdf
```

### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 파라미터

| 파라미터 이름   | 유형   | 경로/쿼리 문자열/HTTP 본문 | 설명                                                                                                                                    |
|------------------|--------|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | 파일   | FormData                    | 업로드할 스프레드시트 파일.                                                                                                                       |
| worksheet        | 문자열 | 쿼리                        | 스프레드시트의 워크시트 이름.                                                                                                                |
| range            | 문자열 | 쿼리                        | 셀 영역. 예: A1:C10                                                                                                                         |
| outPath          | 문자열 | 쿼리                        | (선택 사항) 워크북이 저장될 폴더 경로. 기본값은 null입니다.                                                                 |
| outStorageName   | 문자열 | 쿼리                        | 출력 파일의 저장소 이름.                                                                                                                      |
| fontsLocation    | 문자열 | 쿼리                        | 사용자 정의 글꼴 사용.                                                                                                                              |
| AutoRowsFit      | 불리언 | 쿼리                        | (선택 사항) 워크시트의 모든 행을 자동으로 맞춥니다.                                                                                                   |
| AutoColumnsFit   | 불리언 | 쿼리                        | (선택 사항) 워크시트의 모든 열을 자동으로 맞춥니다.                                                                                                |
| region           | 문자열 | 쿼리                        | 스프레드시트 지역/언어 설정(예: `en-US`, `fr-FR`). 숫자 서식, 날짜 파싱 및 지역별 동작에 영향을 줍니다.       |
| password         | 문자열 | 쿼리                        | 스프레드시트 파일을 열기 위한 비밀번호.                                                                                                     |

### 요청 본문 파라미터

| 파라미터 이름 | 유형 | 설명 |
|----------------|------|-------------|
| Spreadsheet    | 파일 | 업로드할 스프레드시트 파일. |

### **응답**

```json
{
  "file": "<이진 PDF 콘텐츠>"
}
```

**응답 상태 코드**

| 코드 | 의미 | 설명 |
|------|---------|-------------|
| 200 | OK | 변환 성공; 생성된 PDF 파일 스트림을 반환합니다. |
| 400 | Bad Request | 잘못된 URL입니다. |
| 401 | Unauthorized | 인증에 실패했거나 자격 증명이 제공되지 않았습니다. |
| 413 | Payload Too Large | 업로드된 파일이 허용된 크기 제한을 초과했습니다. |
| 500 | Internal Server Error | 스프레드시트에서 변환 데이터를 가져오는 동안 문제가 발생했습니다. |

## ConvertRangeToPdf를 SDK와 함께 사용하는 방법

### ConvertRangeToPdf 스펙

[ConvertRangeToPdf API 스펙](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToPdf)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose Cells Cloud 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예시는 cURL을 사용하여 Cloud API에 요청을 보내는 방법을 보여줍니다.

{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}

{< tab tabNum="1" >}

```bash
# 보안 연결을 위해 HTTPS 사용
curl -v "https://api.aspose.cloud/v4.0/cells/convert/range/pdf?worksheet=Sheet1&range=A1:C10" \
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

SDK를 사용하면 개발 속도가 가장 빠르게 향상됩니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 작업에 집중할 수 있도록 해줍니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose Cells Cloud 웹 서비스를 호출하는 방법을 보여줍니다:

```csharp
// C#용 SDK 예제 코드
var apiInstance = new ConversionApi();
var file = File.OpenRead("sample.xlsx");
var result = apiInstance.ConvertRangeToPdf(file, "Sheet1", "A1:C10", outPath: null, outStorageName: null, fontsLocation: null, autoRowsFit: null, autoColumnsFit: null, region: null, password: null);
File.WriteAllBytes("output.pdf", result);
```

```java
// Java용 SDK 예제 코드
ConversionApi api = new ConversionApi();
File file = new File("sample.xlsx");
byte[] result = api.convertRangeToPdf(file, "Sheet1", "A1:C10", null, null, null, null, null, null, null);
Files.write(Paths.get("output.pdf"), result);
```

```python
# Python용 SDK 예제 코드
api_instance = conversion_api.ConversionApi()
with open("sample.xlsx", "rb") as f:
    result = api_instance.convert_range_to_pdf(f, worksheet="Sheet1", range="A1:C10")
    with open("output.pdf", "wb") as out_file:
        out_file.write(result)
```

```javascript
// JavaScript/Node.js용 SDK 예제 코드
const fs = require('fs');
const { ConversionApi } = require('asposecellscloud');
const apiInstance = new ConversionApi();

let file = fs.createReadStream('sample.xlsx');
apiInstance.convertRangeToPdf(file, { worksheet: 'Sheet1', range: 'A1:C10' })
    .then((result) => {
        fs.writeFileSync('output.pdf', result);
    })
    .catch((error) => console.error(error));
```

`[TBD]`
---