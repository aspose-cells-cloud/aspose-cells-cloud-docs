---
title: "Excel을 PNG로 변환"
second_title: "문서"
linktitle: "Excel을 PNG로 변환"
type: docs
url: /ko/koconvert-excel-file-to-png-file/
keywords: "Excel을 PNG로 변환, Aspose.Cells Cloud, REST API, 스프레드시트 변환, PNG 형식"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 스프레드시트를 PNG 이미지로 변환합니다. 여러 SDK를 지원하며 다양한 프로그래밍 언어에 대한 자세한 예제를 제공합니다."
weight: 90
---

이 REST API는 스프레드시트 파일을 PNG 형식으로 변환합니다.

## REST API 사양

```
POST https://api.aspose.cloud/v3.0/cells/convert/png
```

### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **쿼리 매개변수**

| 매개변수 이름         | 유형   | 설명                                                                 |
| --------------------- | ------ | -------------------------------------------------------------------- |
| password              | string | Excel 파일을 열기 위해 필요한 비밀번호입니다.                         |
| storageName           | string | 파일이 위치한 저장소 이름입니다.                                      |
| checkExcelRestriction | bool   | 셀 또는 관련 개체를 수정할 때 Excel 파일 제한 사항을 확인할지 여부입니다. |

### **요청 본문 매개변수**

| 매개변수 이름 | 유형      | 설명                                                     |
| -------------- | --------- | -------------------------------------------------------- |
| datafile       | data file | 멀티파트 요청의 첫 번째 파트에 포함된 스프레드시트 파일입니다. |

### **응답**

API는 생성된 PNG 파일 정보를 담은 **FileInfo** 객체를 반환합니다.

| 필드            | 유형   | 설명                                      |
| --------------- | ------ | ----------------------------------------- |
| **Filename**    | string | PNG 파일 이름 (예: `example.png`)        |
| **FileSize**    | int    | 파일 크기(바이트 단위)                    |
| **FileContent** | string | PNG 파일의 Base64 인코딩 콘텐츠            |

[FileInfo](/cells/file-info/)


**HTTP 상태 코드**

| 코드 | 의미                        | 설명                                               |
|------|-----------------------------|----------------------------------------------------|
| 200  | OK                          | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함 |
| 400  | Bad Request                 | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식) |
| 401  | Unauthorized                | 잘못되거나 누락된 JWT 토큰                            |
| 413  | Payload Too Large           | 업로드된 파일이 크기 제한을 초과함                    |
| 500  | Internal Server Error       | 예기치 않은 서버 오류                                 |

## SDK를 사용한 PostConvertWorkbookToPNG API 사용 방법

### PostConvertWorkbookToPNG API 사양

[OpenAPI 사양](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPNG)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

**cURL** 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/png" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d {"File":{}}
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "xxxxxx.png",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPNG.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPNG.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPNG.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPNG.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPNG.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToPNG.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPNG.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPNG.go" >}}

{{< /tab >}}

{{< /tabs >}}

## 유사한 기능을 구현한 다른 API

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – Excel 파일을 CSV(또는 기타 형식)로 저장하며 추가 설정을 적용하고 결과를 저장합니다.
- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – Excel 파일을 CSV(또는 기타 형식)로 변환하며 선택적 매개변수를 사용하고 결과를 응답으로 반환합니다.
- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Excel 파일을 조회하며, 필요 시 실시간으로 CSV(또는 기타 형식)로 변환합니다.

---