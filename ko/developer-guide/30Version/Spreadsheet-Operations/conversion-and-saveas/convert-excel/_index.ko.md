---
title: "엑셀 파일을 다양한 형식으로 변환"
ArticleTitle: "엑셀 파일을 다양한 형식으로 변환"
second_title: "문서"
linktype: "변환 엑셀"
type: docs
url: /ko/convert-an-excel-file-to-different-formats/
aliases:
  [
    "/convert-excel-workbook-to-different-file-formats/",
    "/convert/excel-to-different-formats/",
  ]
keywords: "Aspose.Cells Cloud, 엑셀 변환, 파일 형식 변환, REST API, SDK, CSV, PDF, HTML, JSON, Markdown"
description: "Aspose.Cells Cloud REST API를 사용하여 엑셀 워크북을 CSV, PDF, HTML, JSON, Markdown 등 다양한 형식으로 변환합니다."
weight: 10
---

이 엔드포인트를 호출하기 전에 유효한 JWT 토큰을 획득했는지 확인하고, 소스 워크북이 지원되는 저장소 위치(예: Aspose Cloud Storage)에 저장되어 있는지 확인하세요. 토큰은 `Authorization` 헤더에 포함해야 하며, 필요에 따라 `storageName` 쿼리 파라미터를 지정해야 합니다.

이 REST API는 엑셀 파일을 다양한 출력 형식으로 변환합니다.

## PutConvertWorkBook API

```http
PUT https://api.aspose.cloud/v3.0/cells/convert
```

이 요청은 HTTP **PUT** 방식이며, 멀티파트 콘텐츠를 포함합니다(참고: [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) 또는 [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).  
멀티파트 본문의 첫 번째 파트에는 **데이터 파일**이 포함되고, 두 번째 파트에는 **저장 옵션**이 포함됩니다.

### 보안 및 인증

Aspose.Cells Cloud API는 보안이 강화되어 있으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 쿼리 파라미터

| 파라미터 이름           | 유형   | 설명                                                                                                                          |
| ----------------------- | ------ | ----------------------------------------------------------------------------------------------------------------------------- |
| `format`                | string | 대상 파일 형식(예: CSV, XLS, HTML, PDF, XML, TXT, TIFF, PNG, JPG, GIF, EMF, BMP, MD, Numbers, WMF, SVG 등).                     |
| `password`              | string | 소스 엑셀 파일을 열기 위해 필요한 비밀번호.                                                                                   |
| `outPath`               | string | 단일 출력 파일의 전체 경로(파일 이름 및 확장자 포함) 또는 여러 파일이 생성될 경우 폴더 경로.                                   |
| `storageName`           | string | 소스 파일이 위치한 저장소 이름.                                                                                               |
| `checkExcelRestriction` | bool   | **true**인 경우, 셀 또는 관련 개체를 수정하기 전에 엑셀 제약 조건을 검증합니다.                                                 |
| `streamFormat`          | string | 입력 파일 스트림의 형식.                                                                                                      |
| `region`                | string | 워크북에 적용할 지역 설정.                                                                                                    |
| `pageWideFitOnPerSheet` | bool   | PDF로 변환할 때 각 워크시트의 너비에 맞게 페이지 너비를 조정합니다.                                                          |
| `pageTallFitOnPerSheet` | bool   | PDF로 변환할 때 각 워크시트의 높이에 맞게 페이지 높이를 조정합니다.                                                          |
| `sheetName`             | string | 변환할 워크시트의 이름.                                                                                                       |
| `pageIndex`             | string | 변환할 페이지의 인덱스(`sheetName`이 필요함).                                                                                 |
| `onePagePerSheet`       | bool   | **true**인 경우, 각 워크시트당 하나의 PDF 페이지를 생성합니다.                                                                |
| `AutoRowsFit`           | bool   | 워크북 내 모든 행을 자동으로 맞춥니다.                                                                                        |
| `AutoColumnsFit`        | bool   | 워크북 내 열 너비를 자동으로 맞춥니다.                                                                                        |

### 요청 본문 파라미터

| 파라미터 이름 | 유형      | 설명                                                       |
| ------------- | --------- | ---------------------------------------------------------- |
| `datafile`    | data file | 멀티파트 본문의 첫 번째 파트에 포함된 엑셀 파일.           |
| `SaveOptions` | object    | 멀티파트 본문의 두 번째 파트에 포함된 저장 옵션.           |

### 응답

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```

**HTTP 상태 코드**

| 코드 | 의미                   | 설명                                                           |
|------|------------------------|----------------------------------------------------------------|
| 200  | OK (성공)              | 필터가 성공적으로 적용되었으며, 응답에 작업 세부 정보가 포함됨. |
| 400  | Bad Request (잘못된 요청) | 누락되거나 잘못된 파라미터(예: 지원되지 않는 파일 형식).      |
| 401  | Unauthorized (인증되지 않음) | 유효하지 않거나 누락된 JWT 토큰.                              |
| 413  | Payload Too Large (페이로드가 너무 큼) | 업로드된 파일이 크기 제한을 초과함.                           |
| 500  | Internal Server Error (내부 서버 오류) | 예기치 않은 서버 오류.                                         |

## SDK를 사용한 PutConvertWorkBook API 사용 방법

### PutConvertWorkBook API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)은 웹 브라우저에서 직접 REST 상호 작용을 가능하게 하는 공개 인터페이스를 정의합니다.

### cURL 예제

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/convert?format=html" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 저수준 세부 사항을 처리하므로 개발 속도가 빨라지고 비즈니스 로직에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "ExamplePutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "ExamplePutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "ExamplePutConvertWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ExamplePutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "ExamplePutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "ExamplePutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
---