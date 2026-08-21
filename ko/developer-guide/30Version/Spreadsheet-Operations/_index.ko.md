---
title: "스프레드시트 작업"
second_title: "문서"
type: docs
url: /ko/spreadsheet-operations/
keywords: "Aspose Cells Cloud, Excel API, 스프레드시트 작업, 자동 맞춤, 배치 처리, 파일 보호, 변환, 가져오기 및 내보내기, 텍스트 처리"
description: "Aspose.Cells Cloud REST API를 사용하여 자동 맞춤, 배치 변환, 보호, 병합, 검색 및 바꾸기와 같은 스프레드시트 작업을 수행하는 방법을 알아보세요. 간결한 사용 참고 사항과 코드 샘플 안내를 제공합니다."
weight: 100
ArticleTitle: "스프레드시트 작업 – Aspose.Cells Cloud API 가이드"
---

스프레드시트 작업은 **Aspose.Cells Cloud**(v3.0)를 사용하여 Excel 워크북에서 수행할 수 있는 가장 흔한 작업들을 간략히 안내합니다. 열 너비 자동 조정, 파일 일괄 처리, 시트 보호 또는 텍스트 조작이 필요하든, REST API는 Python, C#, Java 등 다양한 언어에서 사용 가능한 전용 엔드포인트를 제공합니다. 아래 목록은 각 작업에 대한 자세한 문서 링크와 빠르게 시작할 수 있도록 간략한 사용 참고 사항을 포함하고 있습니다.

**사전 요구 사항**: 이러한 엔드포인트를 호출하려면 유효한 Aspose.Cells Cloud API 키가 필요하며, `Authorization` 헤더(`Bearer <access-token>`)를 포함해야 합니다. 예제는 API 버전 v3.0을 기준으로 합니다.

- **[자동 맞춤 옵션](/cells/auto-fitter-options/)** – 열 너비와 행 높이를 자동으로 조정합니다. `POST /cells/{file}/worksheets/{sheet}/autoFitColumns`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/autoFitColumns
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "autoFitOptions": {
      "autoFitType": "All",
      "autoFitMergedCells": true
    }
  }
  ```
- **[Excel 파일 배치 처리: 변환, 잠금, 보호, 분할 및 잠금 해제](/cells/batch/)** – 요청당 최대 100개 파일에 대해 일괄 작업(변환, 잠금, 보호, 분할, 잠금 해제)을 수행합니다. `POST /cells/batch`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/batch
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "tasks": [
      { "file": "Book1.xlsx", "action": "convert", "format": "pdf" },
      { "file": "Book2.xlsx", "action": "protect", "password": "Secret123" }
    ]
  }
  ```
- **[Excel 파일 압축 및 복구](/cells/compress-and-repair-excel-files/)** – 파일 크기를 줄이고 구조적 문제를 해결합니다. `POST /cells/{file}/compressAndRepair`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Report.xlsx/compressAndRepair
  Authorization: Bearer {access-token}
  ```
- **[Excel 파일을 다른 형식으로 변환 또는 다른 방식으로 저장](/cells/conversion-and-save-as/)** – Excel을 PDF, CSV, HTML 등으로 변환하거나 출력 형식을 변경합니다. `GET /cells/{file}/saveAs`  
  ```http
  GET https://api.aspose.cloud/v3.0/cells/Financials.xlsx/saveAs?format=pdf
  Authorization: Bearer {access-token}
  ```
- **[워크북 변환 옵션](/cells/convert-workbook-options/)** – 페이지 크기, 렌더링 옵션, 암호화 보호 등 세부 변환 설정을 조정합니다. `POST /cells/{file}/convert`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Presentation.xlsx/convert
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "format": "pdf",
    "options": {
      "pageSetup": { "orientation": "landscape" },
      "pdfSaveOptions": { "compressImages": true }
    }
  }
  ```
- **[Excel 파일 생성 또는 보고서 작성](/cells/creating-files-and-reports/)** – 완전히 새로운 워크북을 생성하거나 템플릿을 기반으로 생성합니다. `PUT /cells/{newFile}`  
  ```http
  PUT https://api.aspose.cloud/v3.0/cells/NewReport.xlsx
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "templateFile": "Template.xlsx",
    "dataSource": { "name": "Q1 매출", "value": 12345 }
  }
  ```
- **[Excel 파일로 데이터 가져오기 및 Excel 파일에서 데이터 내보내기](/cells/data-import-and-export/)** – CSV, JSON 또는 데이터베이스에서 데이터를 로드하고 워크시트 데이터를 내보냅니다. `POST /cells/{file}/importData`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Orders.xlsx/importData
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "importOptions": {
      "source": "json",
      "jsonData": [{ "OrderId": 1, "Amount": 250.0 }]
    }
  }
  ```
- **[Excel 파일 암호화, 복호화 및 디지털 서명](/cells/protect/)** – 암호 보호, 암호화 또는 디지털 서명을 적용합니다. `POST /cells/{file}/encrypt`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Sensitive.xlsx/encrypt
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "password": "StrongPass!23",
    "encryptionType": "Standard"
  }
  ```
- **[파일 정보](/cells/file-info/)** – 크기, 형식, 생성일 등의 메타데이터를 조회합니다. `GET /cells/{file}/info`  
  ```http
  GET https://api.aspose.cloud/v3.0/cells/Archive.xlsx/info
  Authorization: Bearer {access-token}
  ```
- **[Excel 파일 병합 및 분할](/cells/merge-and-split/)** – 여러 워크북을 하나로 합치거나 워크북을 별도 파일로 분할합니다. `POST /cells/merge` / `POST /cells/split`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/merge
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "files": ["Q1.xlsx", "Q2.xlsx"],
    "outputFile": "FullYear.xlsx"
  }
  ```
- **[Excel 파일 내 텍스트 콘텐츠 검색 및 바꾸기](/cells/search-and-replace/)** – 워크시트 전체에서 문자열을 찾아 바꿉니다. `POST /cells/{file}/searchReplace`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Report.xlsx/searchReplace
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "text": "초안",
    "newText": "최종",
    "options": { "matchCase": false }
  }
  ```
- **[Excel 텍스트 처리: 텍스트 추가, 문자 제거, 텍스트 자르기, 단어 대문자 변경 등](/cells/text-processing/)** – 셀 값에 대해 고급 텍스트 조작을 수행합니다. `POST /cells/{file}/textProcessing`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Notes.xlsx/textProcessing
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "operations": [
      { "type": "trim", "range": "A1:A10" },
      { "type": "toUpper", "range": "B1:B5" }
    ]
  }
  ```
- **[Excel 파일에 워터마크 삽입 또는 배경 설정](/cells/watermark-and-background/)** – 이미지 또는 텍스트 워터마크를 추가하고 워크시트 배경을 설정합니다. `POST /cells/{file}/watermark`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Presentation.xlsx/watermark
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "type": "text",
    "text": "기밀",
    "fontSize": 36,
    "color": "FF0000"
  }
  ```
- **[Excel 파일 작업: 수식 계산, 자동 맞춤, 개체 지우기 등](/cells/workbook/)** – 수식 계산, 개체 지우기, 자동 맞춤 등 일반적인 워크북 작업을 수행합니다. `POST /cells/{file}/workbookOperations`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Analytics.xlsx/workbookOperations
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "operations": [
      { "type": "calculateFormula" },
      { "type": "clearObjects", "objectType": "charts" }
    ]
  }
  ```