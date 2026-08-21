---
title: "엑셀 파일을 다른 형식으로 변환하거나 다른 방식으로 저장하기"
second_title: "문서"
linktitle: "변환 및 다른 이름으로 저장"
type: docs
url: /ko/conversion-and-save-as/
aliases: [  /ko/convert-excel/ , /ko/convert/ ]
keywords: "Aspose.Cells, 엑셀 변환 API, 엑셀을 PDF로 변환, 엑셀을 CSV로 변환, 엑셀을 JSON으로 변환, 클라우드 스프레드시트 변환"
description: "Aspose.Cells Cloud REST API를 사용하여 엑셀 워크북을 PDF, CSV, JSON, HTML 등 15개 이상의 다양한 형식으로 변환하는 방법을 알아보세요. 엔드포인트 세부 정보, 샘플 cURL 명령어, Java, .NET, Python 등 SDK 코드 스니펫이 포함되어 있습니다."
weight: 30
ArticleTitle: "Aspose.Cells Cloud로 엑셀 파일을 PDF, CSV, JSON 등으로 변환하기"
---

기존에 [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/) 등 특정 형식으로 엑셀 파일을 생성했다면, 특정 기능을 활용하기 위해 파일을 다른 형식으로 변환하는 것이 유용할 수 있습니다. 예를 들어, 엑셀 파일을 [PDF](https://docs.fileformat.com/pdf/)로 변환하면 내용이 무단 수정으로부터 보호되며, 읽기와 공유가 용이해집니다.

**사전 요구 사항**  
변환 API를 호출하기 전에 Aspose Cloud에서 OAuth 2.0 액세스 토큰을 획득하고, 워크북이 Aspose Cloud 스토리지에 저장되어 있는지(또는 PUT 변환 엔드포인트 요청 본문에 포함되어 있는지) 확인하십시오.

문서 변환은 복잡한 과정입니다. 변환 과정의 복잡성에는 여러 요인이 영향을 미치며, 변환 시 이러한 요소를 고려해야 합니다. 엑셀 형식 간 정확하고 전문 수준의 변환을 제공하는 것이 Aspose.Cells Cloud의 주요 기능 중 하나입니다.

이 서비스는 모든 문서 형식 변환에 원활하게 작동합니다. 다음 형식으로 문서를 가져오기 및 내보내기가 가능합니다:

**지원되는 형식**  
- 가져오기/내보내기: [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/)
- 내보내기 전용: [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/)

### 변환 API

| API                         | 설명                                                                                     |
| :-------------------------- | :-------------------------------------------------------------------------------------- |
| `GET /cells/{name}`         | 클라우드 스토리지에서 엑셀 워크북을 가져와 요청된 형식으로 변환합니다.                   |
| `PUT /cells/convert`        | 요청 본문에 제공된 엑셀 워크북을 지정된 출력 형식으로 변환합니다.                        |
| `POST /cells/{name}/saveAs` | 기존 엑셀 워크북을 다른 형식으로 직접 클라우드 스토리지에 저장합니다.                     |

**API 세부 정보**

- **GET /cells/{name}**  
  - **경로 매개변수:** `name` – 워크북 파일 이름(필수).  
  - **쿼리 매개변수:** `format` – 대상 형식(예: pdf, csv, json); `storage` – 클라우드 스토리지 이름(선택 사항); `folder` – 스토리지 내 폴더 경로(선택 사항).  
  - **응답:** 변환된 워크북의 파일 스트림; `Content‑Type`은 대상 형식과 일치합니다.  
  - **상태 코드:** 200 OK, 400 Bad Request, 401 Unauthorized, 404 Not Found, 500 Internal Server Error.  

- **PUT /cells/convert**  
  - **요청 본문:** 변환할 소스 워크북 파일(`file`)과 원하는 출력 형식을 지정하는 필수 필드 `format`을 포함하는 multipart/form‑data.  
  - **응답:** 변환된 파일의 이진 스트림.  
  - **상태 코드:** 200 OK, 400 Bad Request, 401 Unauthorized, 500 Internal Server Error.  

- **POST /cells/{name}/saveAs**  
  - **경로 매개변수:** `name` – 기존 워크북 이름.  
  - **쿼리 매개변수:** `format` – 대상 형식; `outPath` – 클라우드 스토리지 내 저장 경로(선택 사항); `storage` – 스토리지 이름(선택 사항).  
  - **응답:** 작업 결과 및 저장된 파일 경로를 포함하는 JSON 객체. 예시 응답:  

    ```json
    {
      "status": "OK",
      "code": 200,
      "message": "File saved successfully.",
      "path": "Converted/MyWorkbook.pdf"
    }
    ```  

  - **상태 코드:** 200 OK, 400 Bad Request, 401 Unauthorized, 404 Not Found, 500 Internal Server Error.  

**PDF로 변환하는 샘플 cURL**

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx?format=pdf" \
  -H "Authorization: Bearer {access_token}" \
  -o MyWorkbook.pdf
```

**Java SDK 코드 스니펫 (GET /cells/{name})**

```java
CellsApi apiInstance = new CellsApi();
String name = "MyWorkbook.xlsx";
String format = "pdf";
File result = apiInstance.cellsGetWorkbook(name, format, null, null);
result.renameTo(new File("MyWorkbook.pdf"));
```

**.NET SDK 코드 스니펫 (PUT /cells/convert)**

```csharp
var api = new CellsApi();
var file = File.ReadAllBytes("MyWorkbook.xlsx");
var format = "pdf";
var result = api.ConvertWorkbook(new MemoryStream(file), format);
File.WriteAllBytes("MyWorkbook.pdf", result);
```

**Python SDK 코드 스니펫 (POST /cells/{name}/saveAs)**

```python
import asposecellscloud
api = asposecellscloud.CellsApi()
api.post_save_as(name="MyWorkbook.xlsx", format="pdf", out_path="Converted/MyWorkbook.pdf")
```

다음 문서에서는 각 API를 자세히 설명하고 추가적인 cURL 및 SDK 예제를 제공합니다:

- [엑셀 파일을 다른 형식으로 변환하기](/cells/convert-an-excel-file-to-different-formats)
- [엑셀 파일을 다른 형식으로 저장하기](/cells/save-an-excel-file-as-other-formats-files)
- [엑셀 파일을 CSV 파일로 변환하기](/cells/convert-excel-file-to-csv-file)
- [엑셀 파일을 DOCX 파일로 변환하기](/cells/convert-excel-file-to-docx-file)
- [엑셀 파일을 HTML 파일로 변환하기](/cells/convert-excel-file-to-html-file)
- [엑셀 파일을 JSON 파일로 변환하기](/cells/convert-excel-file-to-json-file)
- [엑셀 파일을 Markdown 파일로 변환하기](/cells/convert-excel-file-to-markdown-file)
- [엑셀 파일을 PDF 파일로 변환하기](/cells/convert-excel-file-to-pdf-file)
- [엑셀 파일을 PNG 파일로 변환하기](/cells/convert-excel-file-to-png-file)
- [엑셀 파일을 PPTX 파일로 변환하기](/cells/convert-excel-file-to-pptx-file)
- [엑셀 파일을 SQL 파일로 변환하기](/cells/convert-excel-file-to-sql-file)
- [엑셀 파일을 TIFF 파일로 변환하기](/cells/convert-excel-file-to-tiff-file)
---