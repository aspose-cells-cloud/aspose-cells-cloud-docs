---
title: "고급 Excel 파일 변환"
second_title: "문서"
linktitle: "고급 변환"
type: docs
url: /ko/advanced-convert-excel/
keywords: "Aspose.Cells, Excel 변환, 클라우드 API, SDK"
description: "Aspose.Cells Cloud REST API는 Excel 워크시트를 다양한 형식으로 변환하고, 페이지 설정, 저장 옵션, 인쇄 설정을 세밀하게 제어할 수 있는 강력한 기능을 제공합니다. Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby, Swift용 SDK가 준비되어 있어 여러 플랫폼에서 원활하게 통합할 수 있습니다."
weight: 50
ArticleTitle: "고급 Excel 파일 변환 – Aspose.Cells Cloud API 가이드"
---

## Excel 변환을 위한 고급 클라우드 API

고급 변환 연산을 사용하면 Excel 워크북을 다양한 출력 형식(PDF, HTML, CSV 등)으로 변환하면서 페이지 설정, 저장 옵션, 인쇄 설정을 세밀하게 제어할 수 있습니다.

**사전 요구 사항 / 인증**  
이 엔드포인트를 사용하려면 Aspose.Cells Cloud에서 액세스 토큰을 획득하여 `Authorization` 헤더에 베어러 토큰으로 포함해야 합니다.

**API 참조**  
- **메서드:** `PUT`  
- **엔드포인트:** `/cells/convert`  
- **매개변수:**  
  - `format` (문자열, 필수) – 원하는 출력 형식 (예: `pdf`, `html`).  
  - `outPath` (문자열, 선택적) – 변환된 파일이 저장될 클라우드 저장소의 경로.  
  - `options` (객체, 선택적) – `pageSetup`, `saveOptions`, `printSettings` 등 고급 변환 옵션을 포함하는 JSON 객체.  
- **요청 본문 예시:**  
  ```json
  {
    "format": "pdf",
    "outPath": "output/converted.pdf",
    "options": {
      "pageSetup": {
        "orientation": "Landscape",
        "paperSize": "A4"
      },
      "saveOptions": {
        "compress": true
      },
      "printSettings": {
        "printHeadings": false
      }
    }
  }
  ```  
- **응답:**  
  - `200 OK` – 변환이 성공적으로 완료됨; 응답에는 변환된 파일 스트림 또는 저장된 파일에 대한 참조가 포함됨.  
  - `400 Bad Request` – 잘못된 매개변수 또는 형식이 잘못된 요청 본문.  
  - `401 Unauthorized` – 인증 실패 또는 토큰 누락.  
  - `500 Internal Server Error` – 변환 중 서버 측 오류 발생.  

**HTTP 상태 코드**

| 코드 | 의미                         | 설명                                              |
|------|------------------------------|---------------------------------------------------|
| 200  | OK (성공)                    | 필터가 성공적으로 적용됨; 응답에는 작업 세부 정보가 포함됨. |
| 400  | Bad Request (잘못된 요청)    | 누락되었거나 잘못된 매개변수 (예: 지원되지 않는 파일 형식). |
| 401  | Unauthorized (인증되지 않음) | 잘못되었거나 누락된 JWT 토큰. |
| 413  | Payload Too Large (ペイロードが大きすぎます) | 업로드된 파일이 크기 제한을 초과함. |
| 500  | Internal Server Error (서버 내부 오류) | 예기치 않은 서버 오류 발생. |

**참고 사항**  
* 일부 출력 형식은 특정 제한 사항이 있습니다(예: HTML 변환은 매크로를 보존하지 않음). 자세한 내용은 형식별 문서를 확인하십시오.

### 여러 데이터 소스에서 스프레드시트 파일을 로드할 수 있는 기능

### 페이지 설정 및 저장 옵션 설정

## 클라우드 SDK 패밀리

SDK를 사용하면 저수준 세부 사항을 처리함으로써 개발 속도를 높이고 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 저장소</a>를 확인하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 호출을 수행하는 방법을 보여줍니다:

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

<script type="application/ld+json">
{
  "@context":"https://schema.org",
  "@type":"WebAPI",
  "name":"Aspose.Cells Cloud 고급 변환",
  "description":"Excel 워크북을 PDF/HTML/CSV로 고급 옵션과 함께 변환합니다.",
  "url":"https://api.aspose.cloud/v3.0/cells/convert",
  "documentation":"https://docs.aspose.cloud/cells/ko/advanced-convert-excel/",
  "endpointDescription":"PUT /cells/convert",
  "input":{
    "@type":"PropertyValueSpecification",
    "valueRequired":true,
    "valueName":"format",
    "description":"원하는 출력 형식(pdf, html, csv, …)"
  },
  "target":{
    "@type":"EntryPoint",
    "urlTemplate":"https://api.aspose.cloud/v3.0/cells/convert?format={format}",
    "httpMethod":"PUT"
  }
}
</script>
---