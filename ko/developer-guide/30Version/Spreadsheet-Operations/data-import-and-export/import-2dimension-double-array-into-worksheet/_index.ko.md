---
title: "2차원 double 배열을 Excel 워크시트로 가져오기"
second_title: "문서"
linktype: "2차원 double 배열 가져오기"
type: docs
url: /import-a-2d-double-array-into-excel-worksheet/
aliases:
  [
    "/import-2dimension-double-array-into-excel-worksheet/",
    "/import-2dimension-double-array-into-worksheet/",
    "/import-data/2dimension-double-array/",
    "/import/2dimension-double-array/",
  ]
keywords: "2차원 double 배열 가져오기, Excel, Aspose Cells Cloud, REST API, 스프레드시트, 데이터 가져오기"
description: "Aspose.Cells Cloud REST API를 사용하여 2차원 double 배열을 Excel 워크시트로 가져오는 방법을 알아보세요. 요청 형식, 매개변수 및 SDK 코드 예제가 포함됩니다."
weight: 20
---

이 REST API는 **2차원 double 배열**을 Excel 워크시트로 가져옵니다.

요청은 멀티파트 콘텐츠를 포함하는 HTTP `POST` 요청입니다([RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) 또는 [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html) 참조). 멀티파트 본문의 첫 번째 파트에는 **Import2DimensionDoubleArrayOption** 데이터가 포함되고, 두 번째 파트에는 소스 데이터 파일이 포함됩니다.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

중요 매개변수는 다음 표에 설명되어 있습니다:

### Import2DimensionDoubleArrayOption

| 매개변수 이름           | 유형         | 설명                                                                                                             |
| ------------------------ | ------------ | ----------------------------------------------------------------------------------------------------------------------- |
| **FirstRow**             | `int`        | 가져오기가 시작되는 행 인덱스(1부터 시작).                                                                            |
| **FirstColumn**          | `int`        | 가져오기가 시작되는 열 인덱스(1부터 시작).                                                                         |
| **Data**                 | `Double[,]`  | 가져올 double 값의 2차원 배열.                                                                  |
| **DestinationWorksheet** | `string`     | 데이터를 수신할 워크시트의 이름.                                                                       |
| **IsInsert**             | `string`     | 행을 삽입하려면 `"true"`, 기존 셀을 덮어쓰려면 `"false"`입니다.                                                         |
| **ImportDataType**       | `string`     | 가져오는 데이터 유형(예: `IntArray`, `DoubleArray`, `TwoDimensionDoubleArray`, `BatchData`, `csvData` 등). |
| **Source**               | `FileSource` | `BatchData` 매개변수가 null일 때 데이터 파일 위치를 나타냅니다.                                                |

**예시**

```json
{
  "Data": [
    [1.0, 2.9, 3.1],
    [2.0, 2.1, 3.1]
  ],
  "DestinationWorksheet": "Sheet2",
  "FirstRow": 4,
  "FirstColumn": 1,
  "importDataType": "TwoDimensionDoubleArray"
}
```

### 응답

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP 상태 코드**

| 코드 | 의미                     | 설명                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | 성공 (OK)                          | 필터가 성공적으로 적용되었으며, 응답에 작업 세부 정보가 포함됩니다. |
| 400  | 잘못된 요청 (Bad Request)                 | 누락되었거나 잘못된 매개변수(예: 지원되지 않는 파일 형식). |
| 401  | 인증되지 않음 (Unauthorized)                | 잘못되었거나 누락된 JWT 토큰. |
| 413  | 페이로드가 너무 큼 (Payload Too Large)           | 업로드된 파일이 크기 제한을 초과했습니다. |
| 500  | 내부 서버 오류 (Internal Server Error)       | 예기치 않은 서버 오류. |
## SDK를 사용하여 PostImportData API 사용하는 방법

### PostImportData API 사양

[OpenAPI 사양](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData)은 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 하는 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의합니다.

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 가장 빠르게 이 기능을 통합할 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 비즈니스 로직에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2Double.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}