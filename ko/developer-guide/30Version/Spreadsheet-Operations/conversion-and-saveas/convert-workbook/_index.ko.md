---
title: "엑셀 파일을 다양한 형식으로 변환하기"
second_title: "문서"
linktitle: "스프레드시트 변환"
type: docs
url: /convert-a-spread-file-to-different-formats/
keywords: "Excel 변환, 스프레드시트 변환, Aspose.Cells Cloud, REST API, PDF, CSV, JSON, Markdown, 파일 형식 변환"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크북을 PDF, CSV, JSON, Markdown 등 다양한 형식으로 변환합니다. 이 API는 C#, Java, Python 등 여러 프로그래밍 언어에 대한 여러 SDK를 지원합니다."
weight: 10
ArticleTitle: "엑셀 파일을 다양한 형식으로 변환하기 – Aspose.Cells Cloud API 가이드"
---

이 REST API는 엑셀 파일을 다른 형식으로 변환합니다. 다양한 출력 형식을 지원하며, 변환 전에 페이지 설정 및 저장 옵션을 설정할 수 있습니다.

## PostConvertWorkBook API

```http
POST https://api.aspose.cloud/v3.0/cells/convert
```

이 API를 사용하기 전에 유효한 JWT 토큰이 있고, 사용 중인 프로그래밍 언어에 맞는 Aspose.Cells Cloud SDK를 설치했는지 확인하세요.

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 보장되며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

## SDK를 사용하여 PostConvertWorkBook API 사용하기

### PostConvertWorkBook API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Workbook/PostConvertWorkBook)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

**cURL** 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예시는 cURL을 사용하여 클라우드 API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청(Request)" tabName12="응답(Response)" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d {}
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "filename",
  "FileSize": 12345,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용하기

SDK를 사용하는 것이 개발을 진행하는 가장 빠른 방법입니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 개발에 집중할 수 있도록 해줍니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 여러 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}