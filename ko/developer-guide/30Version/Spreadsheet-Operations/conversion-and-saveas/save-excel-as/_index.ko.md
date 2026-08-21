---
title: "Excel 워크북 저장 – Aspose.Cells Cloud API"
second_title: "문서"
linktitle: "다른 형식으로 저장"
type: docs
url: /ko/save-an-excel-file-as-other-formats-files/
aliases:
  - /convert-excel-workbook-to-different-file-formats/
  - /saveas-other-formats/
keywords: "Aspose Cells, Excel, 다른 형식으로 저장, PDF, CSV, JSON, Markdown, REST API"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크북을 PDF, CSV, JSON, Markdown 및 기타 형식으로 저장합니다."
weight: 30
---

이 REST API는 Excel 파일을 다양한 형식으로 **저장**할 수 있도록 합니다.  
이 엔드포인트를 호출하기 전에 유효한 OAuth 2.0 액세스 토큰을 확보했고, 소스 워크북이 Aspose Cloud 스토리지에 저장되어 있는지 확인해야 합니다.

**필수 조건**  
1. JWT 액세스 토큰을 발급받아 모든 요청의 `Authorization: Bearer <token>` 헤더에 포함시킵니다.  
2. 소스 워크북을 Aspose Cloud 스토리지에 업로드하거나(또는 이미 존재하는지 확인)합니다.  
3. 워크북이 위치한 스토리지 이름과 폴더 경로를 알고 있어야 합니다.

## PostWorkbookSaveAs API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/saveAs
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 위해 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>을 요구합니다.

### **경로 매개변수**

| 매개변수 이름 | 유형   | 설명                           |
| -------------- | ------ | ----------------------------- |
| name           | string | Excel 파일의 이름입니다.        |

### **쿼리 매개변수**

| 매개변수 이름          | 유형   | 설명                                                                                       |
| --------------------- | ------ | ----------------------------------------------------------------------------------------- |
| newfilename           | string | 저장된 문서의 새 파일 이름입니다.                                                            |
| isAutoFitRows         | string | `true`인 경우 워크북의 모든 행을 자동으로 조정합니다. 기본값은 `false`입니다.                 |
| isAutoFitColumns      | string | `true`인 경우 워크북의 열 너비를 자동으로 조정합니다. 기본값은 `false`입니다.                |
| folder                | string | 원본 워크북이 위치한 폴더입니다.                                                             |
| storageName           | string | 소스 파일이 위치한 스토리지의 이름입니다.                                                    |
| outStorageName        | string | 출력 파일이 저장될 스토리지의 이름입니다.                                                     |
| checkExcelRestriction | bool   | 셀 또는 관련 개체를 수정할 때 Excel 제한 사항을 적용할지 여부를 지정합니다.                    |
| region                | string | 워크북에 적용되는 지역 설정입니다.                                                            |
| pageWideFitOnPerSheet | bool   | 변환 시 각 워크시트의 페이지 너비를 조정합니다.                                               |
| pageTallFitOnPerSheet | bool   | 변환 시 각 워크시트의 페이지 높이를 조정합니다.                                               |
| sheetName             | string | 변환할 워크시트의 이름입니다.                                                                 |
| pageIndex             | string | 지정된 워크시트 내에서 변환할 페이지 인덱스입니다(`sheetName`이 필요합니다).                     |
| onePagePerSheet       | bool   | PDF로 변환 시 각 워크시트당 한 페이지를 생성합니다.                                            |

### **요청 본문 매개변수**

| 매개변수 이름 | 유형   | 설명                                                    |
| -------------- | ------ | ------------------------------------------------------ |
| SaveOptions    | Object | 멀티파트 요청의 두 번째 부분에 제공된 저장 옵션입니다.     |

**요청 본문 예시(멀티파트 요청의 JSON 부분)**

```json
{
  "SaveOptions": {
    "SaveFormat": "pdf",
    "CompressionLevel": 9
  }
}
```

### 응답

API는 `SaveResponse` 개체를 반환합니다.

```json
{
  "Status": "OK",
  "Code": 200,
  "SaveResult": {
    "Documents": [
      {
        "Name": "sample.pdf",
        "Size": 10240,
        "Folder": "output",
        "Storage": "MyStorage"
      }
    ]
  }
}
```

**HTTP 상태 코드**

| 코드 | 의미                         | 설명                                             |
|------|-----------------------------|-------------------------------------------------|
| 200  | OK                          | 필터가 성공적으로 적용되었으며, 응답에 작업 세부 정보가 포함되어 있습니다. |
| 400  | Bad Request                 | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식)가 있습니다. |
| 401  | Unauthorized                | 유효하지 않거나 누락된 JWT 토큰입니다.              |
| 413  | Payload Too Large           | 업로드된 파일이 크기 제한을 초과합니다.               |
| 500  | Internal Server Error       | 예기치 않은 서버 오류가 발생했습니다.                 |

## SDK를 사용한 PostWorkbookSaveAs API 사용 방법

### PostWorkbookSaveAs API 사양

[OpenAPI 사양](https://reference.aspose.cloud/cells/#/Conversion/PostWorkbookSaveAs)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

**cURL**을 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예시는 cURL을 사용하여 Cloud API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/sampleBook.xlsx/SaveAs?newfilename=sample.pdf&isAutoFitRows=true&isAutoFitColumns=true" \
  -H "accept: multipart/form-data" \
  -H "Authorization: Bearer <your_jwt_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "SaveResult": {
    "Documents": [
      {
        "Name": "sample.pdf",
        "Size": 10240,
        "Folder": "output",
        "Storage": "MyStorage"
      }
    ]
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 크게 향상시킬 수 있습니다. SDK는 저수준 세부 사항을 처리해주므로, 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예시는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookSaveAs.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookSaveAs.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookSaveAs.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookSaveAs.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookSaveAs.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookSaveAs.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookSaveAs.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbookSaveAs.go" >}}

{{< /tab >}}

{{< /tabs >}}

기타 변환 시나리오는 [Excel을 PDF로 변환](/convert-excel-to-pdf/) 및 [Excel을 CSV로 내보내기](/export-excel-to-csv/) 가이드를 참조하세요.