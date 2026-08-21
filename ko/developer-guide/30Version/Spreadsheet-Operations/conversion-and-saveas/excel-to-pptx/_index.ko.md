---
title: "Aspose.Cells Cloud API v3.0을 사용하여 Excel을 PPTX로 변환"
second_title: "문서"
linktitle: "Excel을 PPTX로 변환"
type: docs
url: /ko/convert-excel-file-to-pptx-file/
keywords: "Aspose, Cells, Excel, PPTX, 변환, REST API, 클라우드"
description: "Aspose.Cells Cloud REST API v3.0을 사용하여 Excel 워크북을 PPTX 프레젠테이션으로 변환하는 방법을 알아보세요. cURL 요청, SDK 코드 예제, 인증 및 오류 처리가 포함됩니다."
weight: 90
ArticleTitle: "Aspose.Cells Cloud API v3.0을 사용하여 Excel을 PPTX로 변환"
---

이 REST API는 스프레드시트 파일을 PPTX 형식으로 변환합니다.

## PostConvertWorkbookToPptx API

```http
POST https://api.aspose.cloud/v3.0/cells/convert/pptx
```

### **보안 및 인증**

Aspose.Cells Cloud API는 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 쿼리 파라미터

| 파라미터 이름           | 타입   | 설명                                                                                     |
| ----------------------- | ------ | ----------------------------------------------------------------------------------------- |
| `password`              | string | Excel 워크북을 열기 위해 필요한 비밀번호.                                                |
| `storageName`           | string | 원본 파일이 위치한 저장소 이름.                                                            |
| `checkExcelRestriction` | bool   | 셀 관련 개체를 수정할 때 Excel 파일 제한을 적용할지 여부를 나타냅니다.                    |

### 요청 본문 파라미터

| 파라미터 이름 | 타입      | 설명                                                                   |
| -------------- | --------- | ------------------------------------------------------------------------ |
| `datafile`     | data file | multipart 요청 본문의 첫 번째 파트에 포함된 Excel 파일.                   |

**예시 multipart 요청 본문(간소화됨):**

```
--boundary
Content-Disposition: form-data; name="File"; filename="input.xlsx"
Content-Type: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet

<input.xlsx의 바이너리 콘텐츠>
--boundary
Content-Disposition: form-data; name="password"

MyPwd
--boundary--
```

### 응답

API는 생성된 pptx 파일을 포함하는 **FileInfo** 객체를 반환합니다.

| 필드            | 타입   | 설명                                         |
| --------------- | ------ | --------------------------------------------- |
| **Filename**    | string | pptx 파일 이름 (예: `example.pptx`).         |
| **FileSize**    | int    | 파일 크기(바이트 단위).                       |
| **FileContent** | string | Base64로 인코딩된 pptx 파일 콘텐츠.          |

[FileInfo](/cells/file-info/)


**HTTP 상태 코드**

| 코드 | 의미                        | 설명                                               |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함. |
| 400  | Bad Request                 | 누락되거나 잘못된 파라미터(예: 지원되지 않는 파일 형식). |
| 401  | Unauthorized                | 잘못되거나 누락된 JWT 토큰. |
| 413  | Payload Too Large           | 업로드된 파일이 크기 제한을 초과함. |
| 500  | Internal Server Error       | 예기치 않은 서버 오류. |

*참고:* 이 엔드포인트는 일반적인 Excel 형식(`.xlsx`, `.xls`, `.xlsm`)을 지원합니다. 최대 파일 크기는 50MB로 제한됩니다. 적절한 파라미터가 제공되지 않으면 매크로나 보호된 시트가 포함된 워크북의 변환이 제한될 수 있습니다.

## SDK를 사용하여 PostConvertWorkbookToPptx API 사용 방법

### PostConvertWorkbookToPptx API 사양

<a href="https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPptx" rel="noopener noreferrer">OpenAPI 사양</a>은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

**cURL** 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 아래 예제는 cURL을 사용하여 클라우드 API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/pptx?storageName=MyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@/path/to/input.xlsx" \
     -F "password=MyPwd"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.pptx",
  "FileSize": 123456,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용

SDK를 사용하는 것이 가장 빠른 개발 방법입니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트에 집중할 수 있게 해줍니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud" rel="noopener noreferrer")를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPptx.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPptx.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPptx.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPptx.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPptx.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1c" "Example_PostConvertWorkbookToPptx.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPptx.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPptx.go" >}}

{{< /tab >}}

{{< /tabs >}}

## 이 기능을 구현한 다른 API

- **[POST /cells/convert/pdf](https://apireference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPdf)** – Excel 파일을 PDF로 변환합니다.
- **[POST /cells/convert/png](https://apireference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPng)** – Excel 파일을 PNG 이미지로 변환합니다.
- **[POST /cells/convert/svg](https://apireference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToSvg)** – Excel 파일을 SVG 형식으로 변환합니다.