---
title: "Excel을 TIFF로 변환"
second_title: "문서"
linketitle: "Excel을 TIFF로 변환"
type: docs
url: /ko/convert-excel-file-to-tiff-file/
aliases: [  /ko/convert-excel-file-to-tiff-in-cloud/ , /ko/convert/excel-to-tiff/ ]
keywords: "Aspose.Cells Cloud, Excel을 TIFF로 변환, REST API, cURL, SDK, .NET, Java, Python, 이미지 내보내기"
description: "Aspose.Cells Cloud API를 사용하여 Excel 워크북을 고품질 TIFF 이미지로 변환하는 방법을 알아보세요. 자세한 cURL 명령어, SDK 예제(C#, Java, Python 등), 인증 단계, 오류 처리를 포함합니다."
weight: 90
---

**Aspose.Cells Cloud**의 **Convert**, **SaveAs**, **Export** 엔드포인트를 사용하면 Excel 워크북을 TIFF 이미지로 변환할 수 있습니다.  
이 엔드포인트는 직접 **cURL**로 호출하거나 지원되는 SDK 중 하나를 통해 호출할 수 있습니다.

## REST API

| **API**                | **메서드** | **용도**                                                                                      | **Swagger 링크**                                                                            |
| ---------------------- | ---------- | --------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| `/cells/convert`       | PUT        | 요청 본문에 제공된 워크북을 지정된 형식(TIFF)으로 변환합니다.                                 | [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) |
| `/cells/{name}`        | GET        | 이름이 지정된 워크북을 다른 형식(TIFF)으로 내보내고 결과를 응답으로 반환합니다.               | [GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)               |
| `/cells/{name}/saveAs` | POST       | 워크북을 선택한 형식(TIFF)으로 저장하고 결과를 클라우드 저장소에 저장합니다.                   | [PostDocumentSaveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)   |

이러한 엔드포인트는 공개적으로 접근 가능하며, 웹 브라우저 또는 어떤 HTTP 클라이언트에서도 직접 호출할 수 있습니다.

### cURL 예제

{{< tabs tabTotal="3" tabID="11" tabName11="convert" tabName12="saveas" tabName13="export">}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/convert?format=tiff" \
     -X PUT \
     -d '{"File":{"Name":"book1.xlsx","Data":"<base64‑내용>"},"SaveFormat":"tiff"}' \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <jwt 토큰>"
```

{{< /tab >}}
{{< tab tabNum="12" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx/saveas?newfilename=book1.tiff" \
     -X POST \
     -d '{"SaveFormat":"tiff","ImageFormat":"tiff"}' \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <jwt 토큰>"
```

{{< /tab >}}
{{< tab tabNum="13" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=tiff" \
     -X GET \
     -H "Authorization: Bearer <jwt 토큰>"
```

{{< /tab >}}
{{< /tabs >}}

> **참고:**
>
> - **Convert** 요청 본문에는 파일(또는 저장된 파일에 대한 참조)과 원하는 `SaveFormat`이 포함되어야 합니다.
> - **Export** 요청은 요청 본문이 필요 없으며, 형식은 쿼리 문자열(`format=tiff`)을 통해 제공됩니다.

## 오류 처리

| **상태 코드** | **의미**         | **일반적인 원인**                     |
| ------------- | ---------------- | ------------------------------------- |
| 200           | 성공             | TIFF 이미지가 반환됩니다(바이너리 스트림). |
| 400           | 잘못된 요청      | 매개변수 누락 또는 잘못된 형식.        |
| 401           | 인증되지 않음    | 잘못되었거나 누락된 JWT 토큰.          |
| 404           | 찾을 수 없음     | 지정된 워크북이 존재하지 않습니다.      |
| 500           | 내부 서버 오류   | 예기치 않은 서버 측 조건.             |

오류가 발생하면 API는 `Code`, `Message`, 그리고 선택적으로 `Description`을 포함하는 JSON 페이로드를 반환합니다.

## 클라우드 SDK 패밀리

SDK를 사용하면 개발 속도가 가장 빠릅니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbookToTiff.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbookToTiff.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbookToTiff.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbookToTiff.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbookToTiff.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbookToTiff.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbookToTiff.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbookToTiff.go" >}}

{{< /tab >}}

{{< /tabs >}}