---
title: "Excel을 JSON으로 변환"
second_title: "문서"
linktitle: "Excel을 JSON으로 변환"
type: docs
url: /ko/convert-excel-file-to-json-file/
keywords: "Aspose.Cells, Excel을 JSON으로 변환, 클라우드 API, 스프레드시트 변환, REST API"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 스프레드시트를 JSON 파일로 변환하는 방법을 알아보세요. cURL 예제, SDK 스니펫(C#, Java, Python), 필요한 매개변수, 인증, 응답 형식이 포함됩니다."
weight: 100
ArticleTitle: "Aspose.Cells Cloud API를 사용하여 Excel을 JSON으로 변환하기 – 빠른 가이드"
---


## REST API

이 REST API는 스프레드시트 파일을 JSON 형식의 파일로 변환합니다.  


```http
POST https://api.aspose.cloud/v3.0/cells/convert/json
```

### 보안 및 인증

Aspose.Cells Cloud API는 안전하며, [JWT 토큰 기반 인증](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)이 필요합니다.

### 요청

**쿼리 매개변수**

| 매개변수 이름           | 유형   | 설명                                                           |
| ----------------------- | ------ | --------------------------------------------------------------------- |
| `password`              | string | Excel 파일을 열기 위해 필요한 비밀번호 (선택 사항).                  |
| `storageName`           | string | 파일이 위치한 스토리지 이름 (선택 사항).             |
| `checkExcelRestriction` | bool   | 셀을 수정할 때 Excel 관련 제한을 적용할지 여부 (선택 사항). |

**요청 본문 매개변수**

| 매개변수 이름 | 유형 | 설명                                                                                       |
| -------------- | ---- | ------------------------------------------------------------------------------------------------- |
| `datafile`     | file | 업로드할 Excel 파일. `multipart/form-data` 요청의 첫 번째 파트로 전송되어야 합니다. |

#### 예제 cURL 호출

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/json" \
     -H "Authorization: Bearer $ACCESS_TOKEN" \
     -H "accept: application/json" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@myWorkbook.xlsx"
```

### 응답

서비스는 **FileInfo** 객체를 반환합니다. 주요 필드는 다음과 같습니다:

| 필드          | 유형    | 설명                                                                  |
| ------------- | ------- | ---------------------------------------------------------------------------- |
| `Filename`    | string  | 생성된 JSON 파일 이름 (예: `myWorkbook.json`).                   |
| `FileSize`    | integer | 생성된 파일의 크기(바이트 단위).                                         |
| `FileContent` | string  | JSON 파일의 Base64 인코딩 콘텐츠. 실제 JSON을 가져오려면 이를 디코딩하세요. |

**예제 응답**

```json
{
  "Filename": "myWorkbook.json",
  "FileSize": 8423,
  "FileContent": "eyJmb3JtYXR0ZWRfZGF0YSI6IH ... (base64 문자열) ..."
}
```

#### 오류 처리

요청이 실패하면 API는 다음과 같은 구조의 오류 객체를 반환합니다:

| 필드      | 유형   | 설명                              |
| --------- | ------ | ---------------------------------------- |
| `Code`    | string | 기계가 읽을 수 있는 오류 식별자.       |
| `Message` | string | 사람이 읽을 수 있는 오류 설명. |

일반적인 HTTP 상태 코드:

- **400** – 잘못된 요청 (예: 파일 누락, 매개변수 오류).
- **401** – 인증되지 않음 (잘못되거나 누락된 액세스 토큰).
- **500** – 내부 서버 오류.

**HTTP 상태 코드**

| 코드 | 의미                         | 설명                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | 성공 (OK)                   | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함. |
| 400  | 잘못된 요청 (Bad Request)   | 누락되거나 잘못된 매개변수 (예: 지원되지 않는 파일 형식). |
| 401  | 인증되지 않음 (Unauthorized) | 잘못되거나 누락된 JWT 토큰. |
| 413  | 페이로드가 너무 큼 (Payload Too Large) | 업로드된 파일이 크기 제한을 초과함. |
| 500  | 내부 서버 오류 (Internal Server Error) | 예기치 않은 서버 오류. |
## SDK를 사용하여 PostConvertWorkbookToJson API 사용 방법

### PostConvertWorkbookToJson API 사양


<a href="https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToJson" rel="noopener noreferrer" title="Aspose.Cells OpenAPI 사양 – 워크북을 JSON으로 변환">OpenAPI 사양</a>은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

**cURL** 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API에 호출을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/json" \
     -H "Authorization: Bearer $ACCESS_TOKEN" \
     -H "accept: application/json" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@myWorkbook.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "myWorkbook.json",
  "FileSize": 8423,
  "FileContent": "eyJmb3JtYXR0ZWRfZGF0YSI6IH... (base64 문자열)"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer" title="GitHub의 Aspose.Cells Cloud SDK">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 호출을 수행하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToJson.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToJson.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToJson.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToJson.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToJson.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToJson.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToJson.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToJson.go" >}}

{{< /tab >}}

{{< /tabs >}}

## 유사한 기능을 구현하는 다른 API

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – 추가 설정을 사용하여 Excel 파일을 HTML 파일로 저장하고 결과를 지정된 스토리지에 저장합니다.
- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – 추가 설정을 사용하여 Excel 파일을 HTML 파일로 변환하고 응답에 결과를 반환합니다.
- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Excel 파일을 검색합니다. 쿼리 매개변수와 함께 사용하여 HTML 형식으로 파일을 가져올 수 있습니다.
---