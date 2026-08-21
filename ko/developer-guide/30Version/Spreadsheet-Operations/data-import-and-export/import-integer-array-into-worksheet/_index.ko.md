---
title: "정수 배열을 Excel 워크시트로 가져오기"
linktitle: "정수 배열 가져오기"
type: docs
url: /import-integer-array-into-excel-worksheet/
aliases:
  - /import-integer-array-into-excel-worksheet/
  - /import-integer-array-into-worksheet/
  - /import-data/integer-array/
  - /import/integer-array/
keywords: "Aspose.Cells Cloud, Excel, 정수 배열 가져오기, REST API, SDK, C#, PHP, Ruby, Java, Python"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트에 정수 배열을 가져오는 방법을 알아보세요. 요청 구문, 매개변수, 여러 SDK에 대한 샘플 코드 및 응답 세부 정보가 포함되어 있습니다."
weight: 30
ArticleTitle: "정수 배열을 Excel 워크시트로 가져오기 – Aspose.Cells Cloud API"
---

이 REST API는 정수 배열을 Excel 워크시트로 가져옵니다.

요청은 멀티파트 콘텐츠를 포함하는 HTTP **POST**여야 합니다(참조: [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) 또는 [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). 멀티파트 본문의 첫 번째 파트는 **ImportIntegerArrayOption** JSON 페이로드를 포함하고, 두 번째 파트는 소스 데이터 파일(예: CSV 또는 바이너리 Excel 파일)을 포함합니다.

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

두 엔드포인트는 동일한 멀티파트 페이로드를 수락합니다. 첫 번째 엔드포인트는 일반 가져오기 작업을 수행하며, 두 번째 엔드포인트는 `{name}`으로 식별되는 특정 워크북을 대상으로 합니다.

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **요청 매개변수**

### ImportIntegerArrayOption

| 매개변수 이름            | 유형       | 설명                                                                                                                                                                                    |
| ------------------------ | ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **FirstRow**             | int        | 데이터를 배치할 첫 번째 행의 0부터 시작하는 인덱스입니다.                                                                                                                               |
| **FirstColumn**          | int        | 데이터를 배치할 첫 번째 열의 0부터 시작하는 인덱스입니다.                                                                                                                            |
| **IsVertical**           | boolean    | `true`이면 수직(열 방향)으로 배열을 삽입하고, `false`이면 수평(행 방향)으로 삽입합니다.                                                                                       |
| **Data**                 | Integer[]  | 가져올 정수 배열입니다.                                                                                                                                                              |
| **DestinationWorksheet** | string     | 데이터를 수신할 워크시트의 이름입니다.                                                                                                                                              |
| **IsInsert**             | boolean    | `true`이면 데이터를 쓰기 전에 행/열을 삽입하고, `false`이면 기존 셀을 덮어씁니다.                                                                                                    |
| **ImportDataType**       | string     | 가져오는 데이터 유형입니다. 유효한 값: `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`. |
| **Source**               | FileSource | **BatchData** 매개변수가 `null`일 때 데이터 파일의 위치를 나타냅니다.                                                                                                            |

#### 예제 요청 본문

```json
{
  "Data": [1, 2, 4],
  "DestinationWorksheet": "Sheet1",
  "FirstRow": 1,
  "FirstColumn": 2,
  "IsVertical": true,
  "IsInsert": true,
  "ImportDataType": "IntArray"
}
```

### 응답

성공적인 요청은 다음과 유사한 JSON 페이로드와 함께 **HTTP 200**을 반환합니다:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

가능한 상태 코드:

| 코드 | 의미                                     |
| ---- | --------------------------------------- |
| 200  | 가져오기 성공                             |
| 400  | 잘못된 요청 – 누락되거나 유효하지 않은 데이터 |
| 401  | 인증되지 않음 – 잘못되거나 누락된 토큰       |
| 500  | 내부 서버 오류                           |

## SDK를 사용하여 PostImportData API 사용 방법

### PostImportData API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

### Aspose.Cells Cloud SDK 사용

SDK를 사용하는 것이 이 기능을 통합하는 가장 빠른 방법입니다. SDK는 저수준 세부 사항을 추상화하여 비즈니스 로직에 집중할 수 있게 해줍니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}
---