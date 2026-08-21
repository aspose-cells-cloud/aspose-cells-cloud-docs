---
title: "Excel 파일에 데이터 가져오기 및 Excel 파일에서 데이터 내보내기"
second_title: "문서"
linktitle: "데이터 가져오기 및 내보내기"
type: docs
url: /ko/data-import-and-export/
keywords: "Aspose.Cells Cloud, 데이터 가져오기, Excel 내보내기, API, CSV, JSON, 이미지, 배열"
description: "Aspose.Cells Cloud API(v3.0)를 사용하여 CSV, JSON, 배열 및 이미지에서 Excel 파일로 데이터를 가져오고 워크북, 차트 및 도형을 PDF, PNG 등 다양한 형식으로 내보내는 방법을 알아보세요."
weight: 25
---

Aspose.Cells Cloud API는 다양한 소스에서 데이터를 가져올 수 있으며, Excel 워크북, 차트 및 기타 개체를 **XLSX**, **CSV**, **PDF**, **HTML**, **PNG** 등 다양한 형식으로 내보낼 수 있습니다. 이를 통해 데이터 관리 및 공유를 간단하고 효율적으로 수행할 수 있습니다.

**API 버전:** **v3.0** – 최종 업데이트: **2024‑03‑15**

### 빠른 시작 가이드

1. **페이로드 준비** – 가져오기 또는 내보내기 옵션을 설명하는 JSON 본문(`ImportCSVDataOption`, `ExportOptions` 등)을 작성합니다.
2. **요청 전송** – `curl`, Postman 또는 SDK를 사용해 적절한 엔드포인트(`POST /cells/import` 또는 `POST /cells/export`)를 호출합니다.
3. **응답 처리** – 성공 시 처리된 파일(바이너리 또는 Base64 인코딩)을 수신합니다. 오류 발생 시 HTTP 상태 코드와 JSON 본문에 포함된 오류 메시지를 확인합니다.

#### 사전 요구 사항

- 활성화된 Aspose Cloud 계정 및 유효한 JWT 토큰
- 대상 워크북이 지정된 저장소 위치에 존재해야 합니다(저장소 기반 API 사용 시).
- 올바른 `Content-Type` 헤더(`multipart/form-data`는 파일 업로드용, `application/json`은 JSON 본문용).

## 다양한 데이터 소스에서 데이터를 가져오는 방법

Excel 파일로 데이터를 가져오는 과정에는 여러 고려 사항이 있습니다. 전문 수준의 품질로 다양한 형식과 유형의 데이터를 가져올 수 있는 기능은 Aspose.Cells Cloud의 주요 기능 중 하나입니다.

### 데이터 가져오기 API 정보

다음 API는 하나 이상의 Excel 파일에 데이터를 가져오기 위해 제공됩니다:

| API                                                                                                | 설명                                               |
| :------------------------------------------------------------------------------------------------- | :------------------------------------------------- |
| [POST /cells/import](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)              | 저장소를 사용하지 않고 Excel 파일에 데이터를 가져옵니다. |
| [POST /cells/{name}/importdata](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) | 클라우드에 저장된 Excel 파일에 데이터를 가져옵니다.    |

### 요청 매개변수

#### 저장소를 사용하지 않는 경우

| 매개변수 이름 | 유형    | 위치     | 설명                            |
| :------------ | :------ | :------- | :------------------------------ |
| file          | 파일    | formData | 업로드할 파일                   |
| ImportOption  | ImportOptions | body     | 가져올 형식(IntArray, DoubleArray, StringArray, TwoDimensionIntArray, TwoDimensionDoubleArray, TwoDimensionStringArray, BatchData, csvData, Picture 등) 지정 |

#### 저장소를 사용하는 경우

| 매개변수 이름 | 유형        | 위치   | 설명                   |
| :------------ | :---------- | :----- | :--------------------- |
| name          | string      | path   | Excel 파일 이름        |
| folder        | string      | query  | 저장소 내 폴더 경로    |
| storageName   | string      | query  | 저장소 이름            |
| importData    | ImportOptions | body   | 가져올 데이터 페이로드 |

#### 데이터 가져오기 옵션 매개변수

**중요 매개변수는 다음 표에 설명되어 있습니다:**

{{< tabs tabTotal="11" tabID="1" tabName1="ImportBatchDataOption"  tabName2="ImportCSVDataOption"   tabName3="ImportPictureOption" tabName4="Import2DimensionIntArrayOption" tabName5="Import2DimensionDoubleArrayOption" tabName6="Import2DimensionStringArrayOption" tabName7="ImportIntegerArrayOption" tabName8="ImportDoubleArrayOption" tabName9="ImportStringArrayOption" tabName10="CellValue" tabName11="FileSource" >}}

{{< tab tabNum="1" >}}

<table class="table">
  <thead>
    <tr><th>매개변수</th><th>유형</th><th>설명</th></tr>
  </thead>
  <tbody>
    <tr><td>BatchData</td><td>List&lt;CellValue&gt;</td><td>가져올 일괄 데이터</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>대상 워크시트 이름</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>데이터 삽입 여부(true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionStringBatchDataArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>BatchData가 null일 때 데이터 파일 위치</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="2" >}}

<table class="table">
  <thead>
    <tr><th>매개변수</th><th>유형</th><th>설명</th></tr>
  </thead>
  <tbody>
    <tr><td>ConvertNumericData</td><td>boolean</td><td>숫자 데이터 변환 여부(true/false)</td></tr>
    <tr><td>FirstRow</td><td>int</td><td>첫 번째 행 인덱스</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>첫 번째 열 인덱스</td></tr>
    <tr><td>SeparatorString</td><td>string</td><td>열 구분자</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>대상 워크시트 이름</td></tr>
    <tr><td>CustomParsers</td><td>List&lt;CustomParserConfig&gt;</td><td>사용자 정의 파서 설정</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>CSVData</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>BatchData가 null일 때 데이터 파일 위치</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="3" >}}

<table class="table">
  <thead>
    <tr><th>매개변수</th><th>유형</th><th>설명</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>첫 번째 행 인덱스</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>첫 번째 열 인덱스</td></tr>
    <tr><td>IsVertical</td><td>boolean</td><td>이미지를 수직으로 배치할지 여부(true/false)</td></tr>
    <tr><td>Data</td><td>string[]</td><td>이미지 데이터(Base64 문자열)</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>대상 워크시트 이름</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>데이터 삽입 여부(true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>Picture</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>BatchData가 null일 때 데이터 파일 위치</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="4" >}}

<table class="table">
  <thead>
    <tr><th>매개변수</th><th>유형</th><th>설명</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>첫 번째 행 인덱스</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>첫 번째 열 인덱스</td></tr>
    <tr><td>Data</td><td>int[,] </td><td>2차원 정수 배열</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>대상 워크시트 이름</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>데이터 삽입 여부(true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionIntArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>BatchData가 null일 때 데이터 파일 위치</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="5" >}}

<table class="table">
  <thead>
    <tr><th>매개변수</th><th>유형</th><th>설명</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>첫 번째 행 인덱스</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>첫 번째 열 인덱스</td></tr>
    <tr><td>Data</td><td>double[,] </td><td>2차원 실수(double) 배열</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>대상 워크시트 이름</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>데이터 삽입 여부(true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionDoubleArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>BatchData가 null일 때 데이터 파일 위치</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="6" >}}

<table class="table">
  <thead>
    <tr><th>매개변수</th><th>유형</th><th>설명</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>첫 번째 행 인덱스</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>첫 번째 열 인덱스</td></tr>
    <tr><td>Data</td><td>string[,] </td><td>2차원 문자열 배열</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>대상 워크시트 이름</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>데이터 삽입 여부(true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionStringArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>BatchData가 null일 때 데이터 파일 위치</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="7" >}}

<table class="table">
  <thead>
    <tr><th>매개변수</th><th>유형</th><th>설명</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>첫 번째 행 인덱스</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>첫 번째 열 인덱스</td></tr>
    <tr><td>IsVertical</td><td>boolean</td><td>배열을 수직으로 배치할지 여부(true/false)</td></tr>
    <tr><td>Data</td><td>int[] </td><td>1차원 정수 배열</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>대상 워크시트 이름</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>데이터 삽입 여부(true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>IntegerArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>BatchData가 null일 때 데이터 파일 위치</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="8" >}}

<table class="table">
  <thead>
    <tr><th>매개변수</th><th>유형</th><th>설명</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>첫 번째 행 인덱스</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>첫 번째 열 인덱스</td></tr>
    <tr><td>IsVertical</td><td>boolean</td><td>배열을 수직으로 배치할지 여부(true/false)</td></tr>
    <tr><td>Data</td><td>double[] </td><td>1차원 실수(double) 배열</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>대상 워크시트 이름</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>데이터 삽입 여부(true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>DoubleArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>BatchData가 null일 때 데이터 파일 위치</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="9" >}}

<table class="table">
  <thead>
    <tr><th>매개변수</th><th>유형</th><th>설명</th></tr>
  </thead>
  <tbody>
    <tr><td>UpperLeftRow</td><td>int</td><td>좌상단 행 인덱스</td></tr>
    <tr><td>UpperLeftColumn</td><td>int</td><td>좌상단 열 인덱스</td></tr>
    <tr><td>LowerRightRow</td><td>int</td><td>우하단 행 인덱스</td></tr>
    <tr><td>LowerRightColumn</td><td>int</td><td>우하단 열 인덱스</td></tr>
    <tr><td>Filename</td><td>string</td><td>소스 파일 이름</td></tr>
    <tr><td>Data</td><td>string</td><td>가져올 문자열 데이터</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>대상 워크시트 이름</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>데이터 삽입 여부(true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>StringArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>BatchData가 null일 때 데이터 파일 위치</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="10" >}}

<table class="table">
  <thead>
    <tr><th>매개변수</th><th>유형</th><th>설명</th></tr>
  </thead>
  <tbody>
    <tr><td>rowIndex</td><td>int</td><td>셀의 행 인덱스</td></tr>
    <tr><td>columnIndex</td><td>int</td><td>셀의 열 인덱스</td></tr>
    <tr><td>type</td><td>string</td><td>셀 값의 데이터 유형</td></tr>
    <tr><td>value</td><td>string</td><td>셀 값</td></tr>
    <tr><td>style</td><td>Style (object)</td><td>셀 스타일 정의</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="11" >}}

<table class="table">
  <thead>
    <tr><th>매개변수</th><th>유형</th><th>설명</th></tr>
  </thead>
  <tbody>
    <tr><td>FileSourceType</td><td>string</td><td>InMemoryFiles, CloudFileSystem, 또는 RequestFiles</td></tr>
    <tr><td>FilePath</td><td>string</td><td>소스 파일 경로</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< /tabs >}}

## Excel 개체를 다양한 파일 형식으로 내보내는 방법

원래 **XLS**, **XLSX**, **XLSB**, **CSV** 등의 형식으로 Excel 파일을 생성한 경우, 특정 기능을 활용하기 위해 다른 형식으로 변환하고자 할 수 있습니다. 예를 들어, **PDF**로 내보내면 콘텐츠가 무단 수정으로부터 보호되며, 읽기 및 공유가 용이해집니다.

Excel 개체를 내보내는 과정에는 여러 고려 사항이 있습니다. Aspose.Cells Cloud는 워크북, 차트, 도형 및 이미지를 다양한 형식으로 고품질로 내보낼 수 있습니다:

_내보내기 전용 형식_: PDF, OTS, XPS, DIF, PNG, JPEG, BMP, SVG, TIFF, EMF, NUMBERS, FODS  
_가져오기 및 내보내기 모두 가능_: XLS, XLSX, XLSB, CSV, TSV, XLSM, ODS, TXT.

요청은 [RFC 2046] 및 [RFC 1341]에서 정의된 대로 multipart 콘텐츠를 사용합니다. 첫 번째 부분은 데이터 파일을 포함하고, 두 번째 부분은 저장 옵션을 포함합니다.

### 내보내기 API 정보

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

#### 요청 매개변수

| 매개변수 이름 | 유형   | 위치     | 설명                                                                                     |
| :------------ | :----- | :------- | :--------------------------------------------------------------------------------------- |
| file          | file   | formData | 업로드할 파일                                                                            |
| objectType    | string | query    | 개체 유형(`workbook`, `worksheet`, `chart`, `shape`, `picture`, `listobject`, `oleobject`) |
| format        | string | query    | 원하는 출력 파일 형식([지원되는 파일 형식](/cells/supported-file-formats/) 참조)           |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/LightCells/PostExport)은 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의합니다.

cURL 명령줄 도구를 사용하여 API를 호출할 수 있습니다. 아래 예시는 요청 및 JSON 응답을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/export" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'file1=@example1.xlsx' \
  -F 'file2=@example2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "example1.pdf",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "example2.pdf",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}

#### 일반적인 HTTP 상태 코드

| 상태 코드 | 의미                                      | 권장 조치                                     |
| :-------- | :---------------------------------------- | :-------------------------------------------- |
| 200       | 성공 – 파일이 내보내졌습니다.             | 반환된 파일을 처리합니다.                     |
| 400       | 잘못된 요청 – 누락되거나 잘못된 매개변수. | 요청 페이로드 및 쿼리 문자열을 확인합니다.    |
| 401       | 인증 실패 – 유효하지 않거나 만료된 JWT 토큰. | 토큰을 갱신한 후 다시 시도합니다.             |
| 404       | 없음 – 지정된 워크북 또는 워크시트가 존재하지 않습니다. | 파일 이름 및 저장소 경로를 확인합니다.         |
| 500       | 내부 서버 오류 – 서버에서 예기치 않은 조건 발생. | 요청 ID와 함께 Aspose 지원팀에 문의합니다.     |

## 가져오기 및 내보내기 API 호출 방법

다음 문서는 각 API를 자세히 설명하며, cURL 및 SDK 예제가 포함되어 있습니다:

- [저장소를 사용하지 않고 Excel 파일에 데이터를 가져오는 방법](/cells/import/without-using-storage)
- [저장소를 사용하여 Excel 파일에 데이터를 가져오는 방법](/cells/import/with-using-storage)
- [Excel 워크시트에 일괄 데이터를 가져오는 방법](/cells/import-batch-data-into-excel-worksheet/)
- [Excel 워크시트에 CSV 데이터를 가져오는 방법](/cells/import-CSV-data-into-excel-worksheet/)
- [Excel 워크시트에 이미지를 가져오는 방법](/cells/import-picture-into-excel-worksheet/)
- [Excel 워크시트에 정수 배열을 가져오는 방법](/cells/import-integer-array-into-excel-worksheet/)
- [Excel 워크시트에 실수(double) 배열을 가져오는 방법](/cells/import-double-array-into-excel-worksheet/)
- [Excel 워크시트에 문자열 배열을 가져오는 방법](/cells/import-string-array-into-excel-worksheet/)
- [Excel 워크시트에 2차원 정수 배열을 가져오는 방법](/cells/import-a-2D-integer-array-into-excel-worksheet/)
- [Excel 워크시트에 2차원 실수(double) 배열을 가져오는 방법](/cells/import-a-2D-double-array-into-excel-worksheet/)
- [Excel 워크시트에 2차원 문자열 배열을 가져오는 방법](/cells/import-a-2D-string-array-into-excel-worksheet/)
- [Excel 차트를 다른 파일 형식으로 내보내는 방법](/cells/export-excel-chart-to-different-formats/)
- [Excel 목록 개체를 다른 파일 형식으로 내보내는 방법](/cells/export-excel-listobject-to-different-formats/)
- [Excel OLE 개체를 다른 파일 형식으로 내보내는 방법](/cells/export-excel-ole-object/)
- [Excel 이미지를 다른 파일 형식으로 내보내는 방법](/cells/export-excel-picture-to-different-formats/)
- [Excel 도형을 다른 파일 형식으로 내보내는 방법](/cells/export-excel-shape-to-different-formats/)
- [Excel 워크북을 다른 파일 형식으로 내보내는 방법](/cells/export-excel-to-different-formats/)
- [Excel 워크시트를 다른 파일 형식으로 내보내는 방법](/cells/export-excel-worksheet-to-different-formats/)