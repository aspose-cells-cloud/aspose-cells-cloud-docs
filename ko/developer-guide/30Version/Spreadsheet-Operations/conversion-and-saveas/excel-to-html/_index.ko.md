---
title: Excel을 HTML로 변환
description: Aspose.Cells Cloud API v3.0을 사용하여 Excel 워크북을 HTML 파일로 변환합니다.
api_version: v3.0
base_url: https://api.aspose.cloud/v3.0
---

# Excel을 HTML로 변환

Aspose.Cells Cloud은 Excel 워크북(XLS, XLSX, CSV 등)을 HTML 문서로 변환하는 강력한 REST 엔드포인트를 제공합니다. 이 작업은 생성된 HTML 파일(파일 이름, 크기, Base64 인코딩 콘텐츠)을 포함하는 **FileInfo** 객체를 반환합니다.

---

## 사전 요구 사항

| 요구 사항 | 충족 방법 |
|-----------|-----------|
| **Aspose Cloud 계정** | [aspose.cloud](https://www.aspose.cloud)에서 가입하세요. |
| **JWT 액세스 토큰** | OAuth 2.0 `POST /connect/token` 엔드포인트를 통해 베어러 토큰을 획득하세요. |
| **스토리지(선택 사항)** | API가 특정 스토리지에서 파일을 읽거나 쓰기를 원할 경우, 먼저 스토리지를 생성하세요(예: Amazon S3, Azure Blob, 또는 Aspose Cloud 스토리지). |
| **cURL / SDK** | multipart/form-data를 지원하는 HTTP 클라이언트(cURL, Postman 또는 Aspose.Cells SDK 중 하나). |

---

## 인증

Aspose.Cells Cloud 요청은 모두 **JWT 토큰 기반 인증**이 필요합니다.

```http
Authorization: Bearer <access-token>
```

토큰은 모든 요청의 `Authorization` 헤더에 포함되어야 합니다.

---

## 엔드포인트

```
POST https://api.aspose.cloud/v3.0/cells/convert/html
```

> **참고** – 요청은 `multipart/form-data`로 전송되어야 합니다. Excel 파일은 multipart 본문의 첫 번째 파트로 제공되어야 합니다.

---

### 보안 및 인증

Aspose.Cells Cloud API는 보안이 확보되었으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>을 요구합니다.

## 요청 파라미터

### 쿼리 파라미터

| 이름                     | 유형    | 필수 여부 | 기본값 | 설명 |
|--------------------------|---------|-----------|--------|------|
| `password`               | string  | 아니요    | –      | 보호된 워크북을 열기 위한 비밀번호. |
| `storageName`            | string  | 아니요    | –      | 원본 파일이 위치한 스토리지 이름. |
| `checkExcelRestriction` | boolean | 아니요    | `true` | `true`일 경우, 서비스는 Excel 특정 제한 사항(예: 보호된 시트)을 검증합니다. |
| `region`                 | string  | 아니요    | –      | 워크북의 지역 설정(예: `en-US`). |
| `FontsLocation`          | string  | 아니요    | –      | 렌더링에 필요한 사용자 정의 글꼴이 포함된 폴더의 URL 또는 경로. |

### 폼 데이터(Multipart)

| 이름 | 유형 | 필수 여부 | 설명 |
|------|------|-----------|------|
| **File** | file | **예** | 변환할 Excel 워크북. multipart 요청의 첫 번째 파트로 제공되어야 합니다. |

---

## 요청 예시(cURL)

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/html?checkExcelRestriction=true" \
     -H "accept: multipart/form-data" \
     -H "Authorization: Bearer <access-token>" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@/path/to/your_workbook.xlsx"
```

---

## 성공적인 응답

**상태 코드:** `200 OK`

| 필드         | 유형   | 설명 |
|--------------|--------|------|
| `Filename`   | string | 생성된 HTML 파일의 이름(예: `example.html`). |
| `FileSize`   | int    | HTML 파일의 크기(바이트 단위). |
| `FileContent`| string | Base64 인코딩된 HTML 콘텐츠. |

```json
{
  "Filename": "example.html",
  "FileSize": 12345,
  "FileContent": "base64_encoded_string"
}
```

응답 스키마는 **FileInfo** 모델에 의해 정의됩니다: [/cells/file-info](/cells/file-info/).

---

## 오류 응답

| 코드 | 의미 | 예제 페이로드 |
|------|------|---------------|
| `400` | 잘못된 요청 – 누락 또는 잘못된 파라미터 | ```json { "Code": "BadRequest", "Message": "The 'File' part is required." } ``` |
| `401` | 인증되지 않음 – 잘못되거나 누락된 JWT 토큰 | ```json { "Code": "InvalidToken", "Message": "Access token is missing or expired." } ``` |
| `404` | 찾을 수 없음 – 지정된 스토리지에서 원본 파일을 찾을 수 없음 | ```json { "Code": "FileNotFound", "Message": "File 'my.xlsx' does not exist in storage 'MyStorage'." } ``` |
| `413` | 페이로드가 너무 큼 – 업로드된 파일이 허용된 크기를 초과함 | ```json { "Code": "RequestEntityTooLarge", "Message": "Uploaded file exceeds the 100 MB limit." } ``` |
| `429` | 요청이 너무 많음 – 속도 제한 초과 | ```json { "Code": "TooManyRequests", "Message": "Rate limit of 60 calls per minute exceeded." } ``` |
| `500` | 내부 서버 오류 – 예상치 못한 서버 조건 | ```json { "Code": "InternalError", "Message": "An unexpected error occurred. Please try again later." } ``` |

---

## 속도 제한

| 제한 | 설명 |
|------|------|
| **계정당 분당 60개 요청**(기본값) | 이 제한을 초과할 경우 `429 Too Many Requests`가 반환됩니다. 클라이언트 로직을 조정하거나 Aspose Cloud 포털을 통해 더 높은 할당량을 요청하세요. |

---

## SDK 지원

Aspose는 이 엔드포인트를 래핑하는 여러 언어에 대한 1급 SDK를 제공합니다. 아래 예시는 공식 SDK를 사용하여 동일한 변환을 수행하는 방법을 보여줍니다.

| 언어 | 예시 |
|------|------|
| C#   | <details><summary>예시 보기</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar apiInstance = new ConversionApi();\nvar file = File.ReadAllBytes("your.xlsx");\nvar result = apiInstance.PostConvertWorkbookToHtml(file, password: null, checkExcelRestriction: true);\nConsole.WriteLine(result.Filename);\n```</details> |
| Java | <details><summary>예시 보기</summary>```java\nConversionApi api = new ConversionApi();\nFile file = new File("your.xlsx");\nFileInfo info = api.postConvertWorkbookToHtml(file, null, true);\nSystem.out.println(info.getFilename());\n```</details> |
| Python | <details><summary>예시 보기</summary>```python\nfrom asposecellscloud import ConversionApi\napi = ConversionApi()\nwith open('your.xlsx', 'rb') as f:\n    file_info = api.post_convert_workbook_to_html(file=f.read())\nprint(file_info.filename)\n```</details> |
| Node.js | <details><summary>예시 보기</summary>```javascript\nconst { ConversionApi } = require('asposecellscloud');\nconst api = new ConversionApi();\nconst fs = require('fs');\napi.postConvertWorkbookToHtml({ File: fs.createReadStream('your.xlsx') })\n   .then(info => console.log(info.Filename));\n```</details> |
| Go   | <details><summary>예시 보기</summary>```go\nimport (\n    "asposecellscloud"\n    "os"\n)\nfunc main() {\n    api := asposecellscloud.NewConversionApi()\n    f, _ := os.Open("your.xlsx")\n    info, _ := api.PostConvertWorkbookToHtml(f, nil, true)\n    fmt.Println(info.Filename)\n}\n```</details> |
| PHP  | <details><summary>예시 보기</summary>```php\nuse Aspose\Cells\ConversionApi;\n$api = new ConversionApi();\n$file = fopen('your.xlsx', 'r');\n$info = $api->postConvertWorkbookToHtml($file);\necho $info->getFilename();\n```</details> |
| Ruby | <details><summary>예시 보기</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::ConversionApi.new\nfile = File.open('your.xlsx')\ninfo = api.post_convert_workbook_to_html(file: file)\nputs info.filename\n```</details> |
| Perl | <details><summary>예시 보기</summary>```perl\nuse Aspose::Cells::ConversionApi;\nmy $api = Aspose::Cells::ConversionApi->new();\nopen my $fh, '<', 'your.xlsx' or die $!;\nmy $info = $api->post_convert_workbook_to_html(file => $fh);\nprint $info->{Filename};\n```</details> |

지원되는 전체 SDK 목록 및 설치 지침은 **Aspose.Cells Cloud SDKs** 저장소를 참조하세요: <https://github.com/aspose-cells-cloud>.

---

## 관련 엔드포인트

| 엔드포인트 | 설명 |
|------------|------|
| `POST /cells/{name}/saveAs` | 기존 Excel 파일을 HTML(또는 다른 형식)로 저장하여 스토리지에 직접 저장합니다. |
| `PUT /cells/convert` | 추가 변환 옵션을 지정하여 워크북을 HTML로 변환하며, 결과는 응답 본문에 반환됩니다. |
| `GET /cells/{name}` | 저장된 HTML(또는 다른 형식) 워크북을 쿼리 파라미터를 사용하여 검색합니다. |

---

## 자주 묻는 질문

**Q:** *Excel을 HTML로 변환하는 API를 호출할 때 인증은 어떻게 하나요?*  
**A:** OAuth 2.0 `/connect/token` 엔드포인트에서 획득한 `Authorization: Bearer <access-token>` 헤더를 포함하세요.

**Q:** *`FileInfo` 응답에는 어떤 내용이 포함되나요?*  
**A:** `Filename`(문자열), `FileSize`(정수, 바이트), `FileContent`(Base64 인코딩된 HTML 콘텐츠)의 세 가지 필드가 포함됩니다.

**Q:** *어떤 오류 코드를 만날 수 있나요?*  
**A:** `400`(잘못된 요청), `401`(인증되지 않음), `404`(파일을 찾을 수 없음), `413`(페이로드가 너무 큼), `429`(요청이 너무 많음), `500`(내부 서버 오류). 각각 `Code`와 `Message` 필드를 포함하는 JSON 페이로드를 반환합니다.

**Q:** *사용자 정의 글꼴 위치를 지정할 수 있나요?*  
**A:** 예. `FontsLocation` 쿼리 파라미터를 사용하여 필요한 글꼴이 포함된 폴더 또는 URL을 지정할 수 있습니다.

**Q:** *이 작업에는 속도 제한이 있나요?*  
**A:** 기본 제한은 **계정당 분당 60회 호출**입니다. 초과 시 `429 Too Many Requests`가 반환됩니다.

---

## JSON-LD 범위 표시(구조화된 데이터)

이 블록을 추가하면 검색 결과에 리치 스니펫 범위 표시를 활성화하여 SEO를 향상시킬 수 있습니다.

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "itemListElement": [
    { "@type": "ListItem", "position": 1, "name": "Home", "item": "https://docs.aspose.cloud/" },
    { "@type": "ListItem", "position": 2, "name": "Developer Center", "item": "https://docs.aspose.cloud/cells/" },
    { "@type": "ListItem", "position": 3, "name": "Conversion", "item": "https://docs.aspose.cloud/cells/conversion/" },
    { "@type": "ListItem", "position": 4, "name": "Excel to HTML", "item": "https://docs.aspose.cloud/cells/convert-excel-file-to-html-file/" }
  ]
}
</script>
```

---

## 변경 로그

| 버전 | 날짜 | 변경 사항 |
|------|------|-----------|
| **v3.0** | 2024-10-01 | `PostConvertWorkbookToHtml`의 초기 공개 릴리스. |
| **v3.1** | 2025-04-15 | `region` 및 `FontsLocation` 쿼리 파라미터 추가; 오류 페이로드 형식 업데이트. |
| **v3.2** | 2026-03-20 | 속도 제한 문서 및 샘플 오류 응답 추가. |

---

추가 도움이 필요하면 Aspose 지원팀에 문의하거나 공식 API 참조를 방문하세요: <https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToHtml>  
---