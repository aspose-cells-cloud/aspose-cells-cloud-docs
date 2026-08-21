---
title: "OLE 개체 내보내기 – Aspose.Cells Cloud API"
second_title: "문서"
linktitle: "OLE 개체"
type: docs
url: /export-excel-ole-object/
aliases: [/export/excel-ole-object/]
keywords: "Aspose.Cells, OLE 개체, 내보내기, Excel, 클라우드 API, PDF, PNG, DOCX, PPTX"
description: "Aspose.Cells Cloud API를 사용하여 Excel 워크북에서 OLE 개체를 내보냅니다. 요청 형식, 매개변수, 샘플 cURL 및 오류 처리 방법을 확인하세요."
weight: 20
ArticleTitle: "OLE 개체 내보내기 – Aspose.Cells Cloud API"
---

## **REST API**

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 강화되어 있으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.


### 요청 매개변수

| 매개변수          | 위치       | 유형   | 필수 여부 | 설명                                                                 |
| ----------------- | ---------- | ------ | --------- | -------------------------------------------------------------------- |
| `file`            | Form‑data  | 파일   | 예        | OLE 개체를 포함하는 Excel 워크북 (`.xlsx`, `.xls` 등)             |
| `outputFormat`    | Query      | 문자열 | 예        | 내보낼 개체의 대상 형식 (`pdf`, `png`, `jpeg`, `docx`, `pptx`)      |
| `objectType`      | Query      | 문자열 | 예        | 고정값 `oleobject`                                                  |


### 응답

요청이 성공하면 내보낸 파일 목록이 포함된 JSON 객체가 반환됩니다:

```json
{
  "Files": [
    {
      "Filename": "OLESlide.ppt",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "OLEDoc.docx",
      "FileSize": 382,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

**HTTP 상태 코드**

| 코드 | 의미                       | 설명                                                  |
|------|----------------------------|-------------------------------------------------------|
| 200  | OK                         | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함 |
| 400  | Bad Request                | 누락되거나 잘못된 매개변수 (예: 지원되지 않는 파일 형식) |
| 401  | Unauthorized               | 잘못되거나 누락된 JWT 토큰                            |
| 413  | Payload Too Large          | 업로드한 파일이 크기 제한 초과                        |
| 500  | Internal Server Error      | 예기치 않은 서버 오류                                 |

## SDK를 사용하여 PostExport API 사용 방법

### PostExport API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/LightCells/PostExport)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 요청을 수행할 수 있도록 합니다.

**cURL** 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예제는 cURL을 사용하여 클라우드 API에 요청하는 방법을 보여줍니다.

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=oleobject&format=pdf" \
  -H "Authorization: Bearer $ACCESS_TOKEN" \
  -F "file=@MyWorkbook.xlsx" \
  -F "outputFormat=pdf"
```

### OLE 개체란?

**OLE (Object Linking and Embedding, 개체 연결 및 포함)** 개체는 Word 문서, PowerPoint 슬라이드, 이미지 또는 기타 파일과 같은 외부 콘텐츠를 Excel 워크북 내부에 포함하는 방식입니다. 내보낼 때 포함된 콘텐츠가 추출되어 요청한 출력 형식으로 저장됩니다.

### 엔드포인트 개요

`POST https://api.aspose.cloud/v3.0/cells/export?objectType=oleobject&format={outputFormat}`

- `objectType` – 반드시 `oleobject`로 설정해야 합니다.
- `format` – 원하는 출력 형식 (예: `pdf`, `png`, `jpeg`, `docx`, `pptx`)

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 가장 빠르게 향상시킬 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}
---