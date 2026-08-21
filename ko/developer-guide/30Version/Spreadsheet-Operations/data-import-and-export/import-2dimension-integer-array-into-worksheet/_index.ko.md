---
title: "2차원 정수 배열을 Excel 워크시트로 가져오기"
second_title: "문서"
linktype: "Import 2차원 정수 배열"
type: docs
url: /import-a-2d-integer-array-into-excel-worksheet/
aliases:
  [
    "/import-2dimension-integer-array-into-excel-worksheet/",
    "/import-2dimension-integer-array-into-worksheet/",
    "/import-data/2dimension-integer-array/",
    "/import/2dimension-integer-array/",
  ]
keywords: "Aspose.Cells Cloud, 2차원 정수 배열 가져오기, Excel 워크시트, REST API, SDK, Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby, Swift"
description: "Aspose.Cells Cloud REST API는 Excel 워크시트로 2차원 정수 배열을 가져올 수 있도록 지원합니다. Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby, Swift용 SDK를 제공합니다."
weight: 20
---

이 REST API는 **2차원 정수 배열을 Excel 워크시트로 가져옵니다**.

요청은 멀티파트 콘텐츠가 포함된 HTTP 요청입니다(참조: [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) 또는 [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). 멀티파트 콘텐츠의 첫 번째 파트에는 `Import2DimensionIntegerArrayOption` 데이터가 포함되고, 두 번째 파트에는 데이터 파일이 포함됩니다.

주요 매개변수는 다음 표에 설명되어 있습니다:

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **Import2DimensionIntegerArrayOption**

| 매개변수 이름          | 타입         | 설명                                                                                                                                                                  |
| ---------------------- | ------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| FirstRow              | int          | 데이터를 배치할 첫 번째 행의 1부터 시작하는 인덱스입니다.                                                                                                             |
| FirstColumn           | int          | 데이터를 배치할 첫 번째 열의 1부터 시작하는 인덱스입니다.                                                                                                             |
| Data                  | Integer[,]   | 가져올 값을 포함하는 2차원 정수 배열입니다.                                                                                                                            |
| DestinationWorksheet  | string       | 대상 워크시트의 이름입니다.                                                                                                                                           |
| IsInsert              | string       | 데이터를 삽입할지(`"true"`, 기존 셀을 이동), 기존 셀을 덮어쓸지(`"false"`)를 지정합니다.                                                                              |
| ImportDataType        | string       | 데이터 형식을 지정합니다. 지원되는 값: `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`. |
| Source                | FileSource   | `BatchData` 매개변수가 `null`일 때 데이터 파일의 위치를 나타냅니다.                                                                                                  |

### **예제**

```json
{
  "Data": [
    [1, 2],
    [3, 4]
  ],
  "DestinationWorksheet": "Sheet2",
  "FirstRow": 4,
  "FirstColumn": 1,
  "ImportDataType": "TwoDimensionIntArray"
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

| 코드 | 의미                     | 설명                                                                 |
|------|--------------------------|----------------------------------------------------------------------|
| 200  | OK                       | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보가 포함됨.            |
| 400  | Bad Request              | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식).             |
| 401  | Unauthorized             | 잘못되거나 누락된 JWT 토큰.                                          |
| 413  | Payload Too Large        | 업로드된 파일이 크기 제한을 초과함.                                  |
| 500  | Internal Server Error    | 예기치 않은 서버 오류.                                                |

## SDK를 사용하여 PostImportData API 사용하는 방법

### PostImportData API 사양

[OpenAPI 사양](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData)은 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의합니다.

### Aspose.Cells Cloud SDK 사용

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}