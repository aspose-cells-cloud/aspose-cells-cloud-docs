---
title: "Excel을 Docx로 변환"
second_title: "문서"
linktitle: "Excel을 Docx로 변환"
type: docs
url: /koconvert-excel-file-to-docx-file/
keywords: "Excel을 Docx로 변환, Aspose.Cells Cloud, REST API, 스프레드시트 변환, 문서 생성"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 스프레드시트를 DOCX 문서로 변환합니다. 다양한 SDK 및 프로그래밍 언어를 지원하여 원활한 통합이 가능합니다."
weight: 90
---

이 REST API는 스프레드시트 파일을 DOCX 형식 파일로 변환합니다.

## REST API

```http
POST https://api.aspose.cloud/v3.0/cells/convert/docx
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 갖춰져 있으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.



**쿼리 매개변수**

| 매개변수 이름         | 유형   | 설명                                                                                     |
| --------------------- | ------ | ---------------------------------------------------------------------------------------- |
| password              | string | Excel 파일을 열기 위해 필요한 비밀번호.                                                   |
| storageName           | string | 파일이 위치한 스토리지의 이름.                                                              |
| checkExcelRestriction | bool   | 사용자가 셀 관련 개체를 수정할 때 Excel 파일의 제한 사항을 확인할지 여부를 나타냅니다.          |

**요청 본문 매개변수**

| 매개변수 이름 | 유형      | 설명                                                    |
| -------------- | --------- | ------------------------------------------------------- |
| datafile       | data file | 멀티파트 요청 본문의 첫 번째 파트에 저장된 데이터 파일. |

**응답**

API는 생성된 Word 파일 정보를 담은 **FileInfo** 객체를 반환합니다.

| 필드            | 유형   | 설명                                         |
| --------------- | ------ | -------------------------------------------- |
| **Filename**    | string | Word 파일 이름(예: `example.docx`).          |
| **FileSize**    | int    | 파일 크기(바이트 단위).                      |
| **FileContent** | string | Base64로 인코딩된 Word 파일 콘텐츠.          |


[FileInfo](/cells/file-info/)

**HTTP 상태 코드**

| 코드 | 의미                        | 설명                                                |
|------|-----------------------------|-----------------------------------------------------|
| 200  | OK                          | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함. |
| 400  | Bad Request                 | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식). |
| 401  | Unauthorized                | 잘못되거나 누락된 JWT 토큰.                           |
| 413  | Payload Too Large           | 업로드된 파일이 크기 제한을 초과함.                   |
| 500  | Internal Server Error       | 예기치 않은 서버 오류.                                |
## SDK를 사용하여 PostConvertWorkbookToDocx API 사용하는 방법

### PostConvertWorkbookToDocx API 사양

[OpenAPI 사양](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToDocx)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

**cURL** 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API에 요청하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/docx" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d '{"File":{}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.docx",
  "FileSize": 12345,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리해주므로, 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToDocx.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToDocx.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToDocx.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToDocx.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToDocx.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToDocx.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToDocx.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToDocx.go" >}}

{{< /tab >}}

{{< /tabs >}}

## 이 기능을 구현한 기타 API

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – 추가 설정을 사용하여 Excel 파일을 DOCX 파일로 저장하고, 결과를 지정된 스토리지에 저장합니다.

- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – 선택적 설정을 사용하여 Excel 파일을 DOCX 파일로 변환하고, 결과를 응답으로 반환합니다.

- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Excel 워크북을 가져와 선택적 매개변수를 사용하여 DOCX 파일로 변환합니다.

---