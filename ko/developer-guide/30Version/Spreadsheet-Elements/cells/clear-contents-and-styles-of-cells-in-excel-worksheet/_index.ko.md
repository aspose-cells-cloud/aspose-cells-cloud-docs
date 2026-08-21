---
title: "Excel 워크시트에서 셀의 콘텐츠 및 스타일 지우기"
type: docs
url: /clear-contents-and-styles-of-cells-in-excel-worksheet/
weight: 50
keywords:
  - Aspose.Cells
  - Excel API
  - 셀 콘텐츠 지우기
  - 셀 스타일 지우기
  - 클라우드 스프레드시트
  - REST API
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트에서 셀의 콘텐츠 및 스타일을 지우는 방법을 학습하고, cURL 예제 및 SDK 코드 스니펫을 제공합니다."
ArticleTitle: "Excel 워크시트에서 셀의 콘텐츠 및 스타일 지우기 – Aspose.Cells Cloud API"
---

**Clear Contents and Styles**(콘텐츠 및 스타일 지우기) 엔드포인트를 사용하기 전에 다음 사항을 확인하십시오.

* Aspose.Cells Cloud 인증 흐름에서 얻은 유효한 **JWT 토큰**이 있어야 합니다.  
* 워크북이 선택한 저장 위치에 업로드되어 있거나(`folder` 매개변수를 통해) 접근 가능해야 합니다.  
* 언어별 클라이언트 라이브러리 중 하나를 사용하려는 경우 필요한 SDK 버전이 설치되어 있어야 합니다.

이 REST API는 Excel 파일의 셀 콘텐츠를 지웁니다.

## PostClearContents API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/clearcontents
```

### **보안 및 인증**

Aspose.Cells Cloud API는 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>을 요구하는 보안 API입니다.

### **응답**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP 상태 코드**

| 코드 | 의미                 | 설명                                                  |
|------|----------------------|-------------------------------------------------------|
| 200  | OK(성공)            | 필터가 성공적으로 적용되었으며, 응답에 작업 세부 정보가 포함됩니다. |
| 400  | Bad Request(잘못된 요청) | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식)가 있습니다. |
| 401  | Unauthorized(인증되지 않음) | 유효하지 않거나 누락된 JWT 토큰입니다. |
| 413  | Payload Too Large(ペイロード가 너무 큼) | 업로드된 파일이 크기 제한을 초과합니다. |
| 500  | Internal Server Error(내부 서버 오류) | 예기치 않은 서버 오류가 발생했습니다. |

## SDK를 사용하여 PostClearContents API 사용하는 방법

### PostClearContents API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Cells/PostClearContents)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API에 호출을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/clearcontents?range=A2:C11" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용하기

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 처리해주므로, 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 호출을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostClearContents.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostClearContents.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostClearContents.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostClearContents.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostClearContents.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostClearContents.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostClearContents.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostClearContents.go" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Excel 워크시트에서 셀의 콘텐츠 및 스타일 지우기",
  "description": "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트에서 셀의 콘텐츠 및 스타일을 지우는 방법입니다.",
  "url": "https://docs.aspose.cloud/cells/clear-contents-and-styles-of-cells-in-excel-worksheet/",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2023-07-08",
  "publisher": {
    "@type": "Organization",
    "name": "Aspose",
    "logo": {
      "@type": "ImageObject",
      "url": "https://docs.aspose.cloud/cells/images/Aspose-image-for-open-graph.jpg",
      "caption": "Aspose.Cells Cloud – 셀 콘텐츠 및 스타일 지우기"
    }
  },
  "keywords": "Aspose.Cells, Excel API, 셀 콘텐츠 지우기, 셀 스타일 지우기, REST API, 클라우드 스프레드시트"
}
</script>