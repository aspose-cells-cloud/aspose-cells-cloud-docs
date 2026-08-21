---
title: "Excel을 SQL로 변환"
second_title: "문서"
linktitle: "Excel을 SQL로 변환"
type: docs
url: /ko/convert-excel-file-to-sql-file/
keywords: "Aspose.Cells, Excel을 SQL로 변환, 클라우드 API, 스프레드시트 변환, REST"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 스프레드시트를 SQL 파일로 변환합니다. 다양한 SDK 및 프로그래밍 언어를 지원하여 애플리케이션에 원활하게 통합할 수 있습니다."
weight: 100
ArticleTitle: "Excel을 SQL로 변환 – Aspose.Cells Cloud API"
---

이 REST API는 스프레드시트 파일을 SQL 형식 파일로 변환합니다.

**필수 조건**  
이 엔드포인트를 사용하려면 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a> 가이드에 따라 생성된 유효한 JWT 토큰이 필요합니다. 이 API는 서비스 문서에 정의된 크기 제한 내의 Excel 파일을 지원하며, `password` 쿼리 매개변수를 제공하면 암호 보호가 된 워크북도 처리할 수 있습니다.

## PostConvertWorkbookToSQL API

```http
POST https://api.aspose.cloud/v3.0/cells/convert/sql
```

### **보안 및 인증**

Aspose.Cells Cloud API는 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>을 요구하며, 보안이 강화되어 있습니다.

### **쿼리 매개변수**

| 매개변수 이름         | 유형   | 설명                                                                 |
| --------------------- | ------ | ------------------------------------------------------------------- |
| password              | string | Excel 파일을 열 때 필요한 암호.                                      |
| storageName           | string | 파일이 저장된 저장소 이름.                                            |
| checkExcelRestriction | bool   | 셀 관련 개체를 수정할 때 Excel 파일 제한을 확인할지 여부.            |

### **요청 본문 매개변수**

| 매개변수 이름 | 유형      | 설명                                                             |
| -------------- | --------- | ---------------------------------------------------------------- |
| datafile       | data file | 변환할 스프레드시트 파일. 요청의 첫 번째 파트로 포함됩니다.      |

### 응답

API는 생성된 SQL 파일 정보를 담은 **FileInfo** 객체를 반환합니다.

| 필드            | 유형   | 설명                                      |
| --------------- | ------ | ----------------------------------------- |
| **Filename**    | string | SQL 파일 이름 (예: `example.sql`).       |
| **FileSize**    | int    | 파일 크기(바이트 단위).                   |
| **FileContent** | string | Base64 인코딩된 SQL 파일 내용.            |

[FileInfo](/cells/file-info/)

**HTTP 상태 코드**

| 코드 | 의미                         | 설명                                           |
|------|------------------------------|-----------------------------------------------|
| 200  | OK                           | 필터가 성공적으로 적용됨; 응답에 작업 세부정보 포함. |
| 400  | Bad Request                  | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형). |
| 401  | Unauthorized                 | 잘못되거나 누락된 JWT 토큰.                    |
| 413  | Payload Too Large            | 업로드된 파일이 크기 제한을 초과함.            |
| 500  | Internal Server Error        | 예기치 않은 서버 오류.                         |

## SDK를 사용하여 PostConvertWorkbookToSQL API 사용하는 방법

### PostConvertWorkbookToSQL API 사양

<a href="https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToSQL" rel="noopener noreferrer">OpenAPI 사양</a>은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하고, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

**cURL** 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예제는 cURL을 사용해 클라우드 API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/sql" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d '{"File":{}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.sql",
  "FileSize": 1024,
  "FileContent": "base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부사항을 처리해주므로, 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다.
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToSQL.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToSQL.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToSQL.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToSQL.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToSQL.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToSQL.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToSQL.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToSQL.go" >}}

{{< /tab >}}

{{< /tabs >}}

## 이 기능을 구현한 다른 API

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – 워크북을 다른 형식으로 저장하고 결과를 지정된 저장소에 저장합니다.

- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – 워크북을 다른 형식으로 변환하고, 선택적 설정을 적용한 후 결과를 응답으로 반환합니다.

- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – 선택적 변환 설정과 함께 워크북을 검색합니다.

**참고 사항**  
- 암호 보호가 된 Excel 파일을 변환할 때는 반드시 `password` 쿼리 매개변수를 제공해야 하며, 그렇지 않으면 400 오류로 변환이 실패합니다.  
- 서비스는 SQL 파일 내용을 Base64 형식으로 반환하므로, `.sql` 파일로 저장하기 전에 디코딩해야 합니다.  

**샘플 파일**  
API를 빠르게 테스트하려면 샘플 Excel 워크북을 [여기](https://example.com/sample.xlsx)에서, 미리 생성된 SQL 결과를 [여기](https://example.com/sample.sql)에서 다운로드하세요.
---