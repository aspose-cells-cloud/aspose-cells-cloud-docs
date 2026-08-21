---
title: "Excel을 PDF로 변환 – Aspose.Cells Cloud API"
ArticleTitle: "Excel을 PDF로 변환 – Aspose.Cells Cloud API"
second_title: "문서"
linktitle: "Excel을 PDF로 변환"
type: docs
url: /convert-excel-file-to-pdf-file/
aliases: [/convert-excel-file-to-pdf-in-cloud/, /convert/excel-to-pdf/]
keywords: "Aspose, Cells, Excel, PDF, 변환, 클라우드 API"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크북을 PDF로 변환하는 방법을 알아보세요. cURL, SDK 샘플(C#, Java, Python) 및 인증 가이드가 포함됩니다."
weight: 80
---

이 REST API는 스프레드시트 파일을 PDF 형식 파일로 변환합니다. **필수 조건:** 유효한 JWT 액세스 토큰을 획득하고, 소스 Excel 파일이 지원되는 저장소에 저장되어 있으며, 변환 엔드포인트를 호출할 수 있는 적절한 권한이 있어야 합니다.

## PostConvertWorkbookToPDF API

```http
POST https://api.aspose.cloud/v3.0/cells/convert/pdf
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 우수하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **쿼리 매개변수**

| 매개변수 이름           | 유형     | 설명                                                                 |
| :-------------------- | :----- | :------------------------------------------------------------------ |
| password              | string | Excel 파일을 열기 위한 비밀번호.                                                |
| storageName           | string | 파일이 위치한 저장소 이름.                                                       |
| checkExcelRestriction | bool   | 셀 관련 개체를 수정할 때 Excel 파일 제한 사항을 적용할지 여부.                               |

생략할 경우 `checkExcelRestriction`은 기본값 `false`로 설정됩니다.

### **요청 본문 매개변수**

| 매개변수 이름 | 유형   | 설명                                                      |
| :----------- | :----- | :------------------------------------------------------- |
| datafile     | file   | 멀티파트 콘텐츠의 첫 번째 파트로 저장된 데이터 파일.                             |

### **응답**

[FileInfo](/cells/file-info/)

응답은 파일 메타데이터를 포함하는 JSON 객체를 반환합니다. 생성된 PDF 파일 자체는 제공된 `FileContent`(base64 인코딩) 또는 `FileInfo` 링크를 통해 다운로드할 수 있습니다. API는 **FileInfo** 유형의 JSON 객체를 반환합니다:

- **FileInfo** – 생성된 **PDF** 파일의 이름, 크기 및 base64 인코딩된 콘텐츠를 포함하는 객체.

```json
{
  "Filename": "example.pdf",
  "FileSize": 12345,
  "FileContent": "base64_encoded_string"
}
```

**HTTP 상태 코드**

| 코드 | 의미                     | 설명                                              |
|------|-------------------------|---------------------------------------------------|
| 200  | OK                      | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보가 포함됨. |
| 400  | Bad Request             | 누락되었거나 잘못된 매개변수(예: 지원되지 않는 파일 유형).   |
| 401  | Unauthorized            | 잘못되었거나 누락된 JWT 토큰.                           |
| 413  | Payload Too Large       | 업로드된 파일이 크기 제한을 초과함.                       |
| 500  | Internal Server Error   | 예기치 않은 서버 오류.                               |

## SDK를 사용하여 PostConvertWorkbookToPDF API 사용하는 방법

### PostConvertWorkbookToPDF API 사양

[OpenAPI 사양](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPDF)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 요청을 수행할 수 있도록 합니다.

**요청 헤더**

| 헤더          | 유형     | 설명                                                |
| :------------ | :------ | :------------------------------------------------- |
| Authorization | string  | JWT 인증을 통해 획득한 베어러 토큰.                   |
| Content-Type  | string  | 파일 업로드 시 `multipart/form-data`여야 함.         |
| Accept        | string  | 응답 메타데이터 수신 시 `application/json`.         |

**cURL** 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. `Authorization` 헤더에 액세스 토큰을 포함시킨 후 아래 요청을 실행하세요.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/pdf" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <access_token>" \
     -F "datafile=@sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "xxxxxx.pdf",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}


### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 저수준 세부 사항을 처리함으로써 개발을 간소화할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 호출을 수행하는 방법을 보여줍니다:
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPDF.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPDF.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPDF.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPDF.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPDF.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToPDF.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPDF.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPDF.go" >}}

{{< /tab >}}

{{< /tabs >}}

## 이 기능을 구현하는 다른 API

| **API**        | **유형** | **설명**                                                  | **Swagger 링크**                                                                            |
| :------------- | :------- | :-------------------------------------------------------- | :------------------------------------------------------------------------------------------ |
| /cells/convert | PUT      | 요청 콘텐츠의 워크북을 지정된 형식으로 변환합니다.                  | [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) |

[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) API를 사용하면 MS Excel 파일을 PDF로 저장하고 추가 설정을 적용한 후 결과를 저장소에 저장할 수 있습니다.

이 REST API는 Excel 파일을 PDF로 변환합니다.

[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) API를 사용하면 MS Excel 파일을 PDF로 변환하고 추가 설정을 적용한 후 결과를 응답으로 반환할 수 있습니다.

[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook) API를 사용하면 MS Excel 파일을 PDF로 변환하고 추가 설정을 적용한 후 결과를 응답으로 반환할 수 있습니다.

이 [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook), [GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook), [PostDocumentSaveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) API는 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 요청을 수행할 수 있도록 합니다.

추가 변환 옵션은 [저장 옵션](/cells/save-options/) 페이지를 참조하세요.