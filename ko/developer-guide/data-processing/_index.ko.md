---
title: "Aspose.Cells Cloud – 스프레드시트 데이터 병합, 분할 및 가져오기"
second_title: "문서"
ArticleTitle: "스프레드시트 데이터 처리 – 병합, 분할 및 가져오기"
linktype: "데이터 처리"
type: docs
url: /ko/data-processing/
keywords: "Aspose.Cells Cloud, 스프레드시트 데이터 처리, Excel 병합, Excel 분할, CSV 가져오기, JSON 가져오기, API"
description: "Aspose.Cells Cloud REST API를 사용해 CSV/JSON 데이터를 가져오고, 원격 Excel 워크북을 병합하며, 대규모 스프레드시트를 분할하는 자세한 가이드. 요청/응답 예제 포함."
weight: 30
---

**Aspose.Cells Cloud** – 클라우드에서 Excel 파일을 프로그래밍 방식으로 조작할 수 있도록 해주는 RESTful 서비스입니다. 다양한 형식의 데이터 가져오기, 워크북 병합, 대규모 스프레드시트 분할을 지원합니다.

**Aspose.Cells Cloud API의 데이터 처리(Data Processing)** 섹션을 사용하면 스프레드시트 데이터를 프로그래밍 방식으로 가져오고, 병합하며, 분할할 수 있습니다. 아래 엔드포인트를 사용해 CSV/JSON 데이터 가져오기, 워크북 병합, 대용량 파일을 관리 가능한 조각으로 분할 작업을 수행하세요.

## 데이터 가져오기 및 관리

- **[CSV, JSON, XML 데이터를 Excel 파일로 가져오기](https://docs.aspose.cloud/cells/import-data-into-spreadsheet/)**  

가져오기 작업은 CSV, JSON 또는 XML 페이로드를 받아 대상 워크북에 새 워크시트를 생성하거나 기존 워크시트를 업데이트합니다.

**엔드포인트 상세 정보**

| HTTP 메서드 | 엔드포인트 | 요청 본문 | 성공 응답 |
|-------------|----------|--------------|------------------|
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/import` | `application/json` 또는 `text/csv` (형식에 따라 다름) | `200 OK` 및 업데이트된 워크북 메타데이터를 포함한 JSON 응답 |
| GET | `https://api.aspose.cloud/v3.0/cells/{fileName}?format=excel` | *없음* | 처리된 워크북 파일 반환 |

**cURL 요청 예시 (CSV 가져오기)**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/import" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: text/csv" \
     --data-binary @data.csv
```

**JSON 응답 예시**

```json
{
  "Code": 200,
  "Status": "OK",
  "Workbook": {
    "FileName": "MyWorkbook.xlsx",
    "Worksheets": 3
  }
}
```

> **필수 조건**: OAuth2 액세스 토큰이 필요합니다. 소스 파일은 Aspose Cloud 저장소에 있어야 하거나 멀티파트 업로드를 통해 제공되어야 합니다.

## 파일 병합 작업

- **[원격 Excel 파일을 지정된 워크북에 병합](https://docs.aspose.cloud/cells/merge-remote-spreadsheet/)**
- **[여러 Excel 파일을 단일 워크북으로 병합](https://docs.aspose.cloud/cells/merge-spreadsheets/)**
- **[원격 폴더 내 일치하는 Excel 파일 병합](https://docs.aspose.cloud/cells/merge-spreadsheets-in-remote-folder/)**  

병합은 두 개 이상의 워크북을 단일 대상 워크북으로 결합합니다. API는 명시적 파일 목록과 저장소 폴더 내 패턴 기반 병합을 모두 지원합니다.

**엔드포인트 상세 정보**

| HTTP 메서드 | 엔드포인트 | 매개변수 | 성공 응답 |
|-------------|----------|------------|------------------|
| POST | `https://api.aspose.cloud/v3.0/cells/merge` | `files`(파일 이름 배열), `target`(선택적 대상 워크북 이름) | `200 OK` 및 병합된 워크북 정보를 포함한 JSON 응답 |
| POST | `https://api.aspose.cloud/v3.0/cells/merge/remote` | `sourceFolder`, `pattern`, `target` | `200 OK` 및 병합된 워크북 메타데이터 |

**cURL 요청 예시 (명시적 목록 병합)**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/merge" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "files": ["Book1.xlsx", "Book2.xlsx"],
           "target": "Combined.xlsx"
         }'
```

**JSON 응답 예시**

```json
{
  "Code": 200,
  "Status": "OK",
  "MergedWorkbook": {
    "FileName": "Combined.xlsx",
    "Worksheets": 10
  }
}
```

> **필수 조건**: 모든 소스 워크북은 동일한 클라우드 저장소 위치에 저장되어야 하며, 요청자에게 읽기/쓰기 권한이 있어야 합니다.

## 파일 분할 작업

- **[워크시트 기준으로 Excel 파일을 여러 파일로 분할](https://docs.aspose.cloud/cells/split-remote-spreadsheet/)**
- **[사용자 정의 규칙에 따라 Excel 파일 분할](https://docs.aspose.cloud/cells/split-spreadsheet/)**  

분할은 개별 워크시트 또는 행/열 그룹을 별도의 워크북 파일로 추출합니다.

**엔드포인트 상세 정보**

| HTTP 메서드 | 엔드포인트 | 매개변수 | 성공 응답 |
|-------------|----------|------------|------------------|
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/split` | `splitBy`(예: `worksheet`), `outputFolder` | `200 OK` 및 생성된 파일 URL 목록 |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/split/custom` | 사용자 정의 규칙 JSON(페이지 크기, 행 범위 등) | `200 OK` 및 분할된 파일 상세 정보 |

**cURL 요청 예시 (워크시트 기준 분할)**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/BigReport.xlsx/split" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "splitBy": "worksheet",
           "outputFolder": "Splits/"
         }'
```

**JSON 응답 예시**

```json
{
  "Code": 200,
  "Status": "OK",
  "Splits": [
    {"FileName": "BigReport_Sheet1.xlsx", "Url": "https://storage.aspose.cloud/..."},
    {"FileName": "BigReport_Sheet2.xlsx", "Url": "https://storage.aspose.cloud/..."}
  ]
}
```

> **필수 조건**: 소스 워크북은 Aspose Cloud 저장소에서 접근 가능해야 하며, 요청자는 대상 폴더에 쓰기 권한이 있어야 합니다.