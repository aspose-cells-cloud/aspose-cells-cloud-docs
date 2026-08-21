---
title: "엑셀을 마크다운으로 변환"
second_title: "문서"
linktitle: "엑셀 → 마크다운"
type: docs
url: /convert-excel-file-to-markdown-file/
keywords: "엑셀, 마크다운, 변환, Aspose.Cells Cloud, REST API, 엑셀을 마크다운으로 변환, aspose cells markdown api, 엑셀 마크다운 내보내기"
description: "Aspose.Cells Cloud REST API를 사용하여 엑셀 워크시트를 마크다운으로 변환 – cURL 예제, SDK 스니펫, 필요 파라미터 및 인증 세부 정보 포함."
weight: 100
ArticleTitle: "엑셀을 마크다운으로 변환 – Aspose.Cells Cloud API 문서"
---

이 REST API는 스프레드시트 파일을 마크다운 형식 파일로 변환합니다.

## 보안 및 인증
Aspose.Cells Cloud API는 보안이 강화되어 있으며, [JWT 토큰 기반 인증](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)이 필요합니다.

## REST API

```http
POST https://api.aspose.cloud/v3.0/cells/convert/markdown
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 강화되어 있으며, [JWT 토큰 기반 인증](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)이 필요합니다.

### 쿼리 파라미터


| 파라미터 이름          | 타입   | 위치   | 설명                                                                                           |
| --------------------- | ------ | ------ | ---------------------------------------------------------------------------------------------- |
| password              | string | query  | 엑셀 파일을 열기 위해 필요한 비밀번호.                                                         |
| storageName           | string | query  | 파일이 위치한 스토리지 이름.                                                                   |
| checkExcelRestriction | bool   | query  | 셀 또는 관련 개체를 수정할 때 엑셀 고유 제한을 적용할지 여부를 나타냅니다.                       |
| datafile              | file   | body   | multipart 콘텐츠의 첫 번째 파트로 업로드할 엑셀 파일.                                          |

### 응답

API는 **FileInfo** 타입의 JSON 객체를 반환합니다:

- **FileInfo** – 생성된 마크다운 파일의 이름, 크기, base64 인코딩 콘텐츠를 포함하는 객체입니다.

```json
{
  "Filename": "example.md",
  "FileSize": 12345,
  "FileContent": "base64_encoded_string"
}
```

### 오류 응답

| HTTP 코드 | 설명                                                         | 예시 JSON 본문                                  |
| --------- | ------------------------------------------------------------ | ----------------------------------------------- |
| 401       | 인증되지 않음 – 토큰 누락 또는 유효하지 않은 토큰.            | `{"error":"Invalid access token."}`             |
| 400       | 잘못된 요청 – 필수 파라미터 누락 또는 잘못된 파일 형식.       | `{"error":"The 'datafile' field is required."}` |
| 500       | 내부 서버 오류 – 예상치 못한 서버 문제.                       | `{"error":"An unexpected error occurred."}`     |



## SDK를 사용하여 PostConvertWorkbookToMarkdown API 사용하는 방법

### PostConvertWorkbookToMarkdown API 사양

[OpenAPI 사양](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToMarkdown)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

**cURL** 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예제는 cURL을 사용하여 Cloud API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```shell
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/markdown" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <access_token>" \
     -F "File=@your_excel_file.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.md",
  "FileSize": 12345,
  "FileContent": "base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용

SDK를 사용하는 것이 가장 빠른 개발 방법입니다. SDK는 저수준 세부 사항을 처리하므로 비즈니스 로직에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToMarkdown.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToMarkdown.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToMarkdown.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToMarkdown.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToMarkdown.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToMarkdown.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToMarkdown.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToMarkdown.go" >}}

{{< /tab >}}

{{< /tabs >}}

## 이 기능을 구현한 기타 API

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – 추가 설정과 함께 엑셀 파일을 HTML로 저장하고 결과를 저장합니다.
- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – 추가 옵션과 함께 엑셀 파일을 HTML로 변환하고 응답으로 결과를 반환합니다.
- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – 엑셀 파일을 검색하고 선택적 설정과 함께 HTML로 변환할 수 있습니다.
---