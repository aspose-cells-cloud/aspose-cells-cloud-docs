---
title: "2차원 문자열 배열을 Excel 워크시트로 가져오기"
second_title: "문서"
linktitle: "2차원 문자열 배열 가져오기"
type: docs
url: /import-a-2D-string-array-into-excel-worksheet/
aliases:
  [
    "/import-2dimension-string-array-into-excel-worksheet/",
    "/import-2dimension-string-array-into-worksheet/",
    "/import-data/-2dimension-string-array/",
    "/import-data/2dimension-string-array/",
    "/import/2dimension-string-array/",
  ]
keywords: "Aspose.Cells Cloud, 2차원 문자열 배열 가져오기, Excel, REST API, SDK"
description: "Aspose.Cells Cloud REST API를 사용하여 2차원 문자열 배열을 Excel 워크시트로 가져오는 방법을 알아보세요. 요청 형식, 매개변수 세부 정보, C#, PHP, Ruby용 SDK 코드 예제가 포함되어 있습니다."
weight: 20
---

이 REST API는 **2차원 문자열 배열**을 Excel 워크시트로 가져옵니다.

이 요청은 multipart 콘텐츠를 포함하는 HTTP 요청입니다(참조: [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) 또는 [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). multipart 콘텐츠의 첫 번째 부분은 `Import2DimensionStringArrayOption` 데이터를 포함하고, 두 번째 부분은 데이터 파일을 포함합니다.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 적용되며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

주요 매개변수는 다음 표에 설명되어 있습니다:

### **Import2DimensionStringArrayOption**

| 매개변수 이름        | 유형                | 설명                                                                   |
| -------------------- | ------------------- | ----------------------------------------------------------------------------- |
| FirstRow             | int                 | 가져오기 작업이 시작되는 행의 0부터 시작하는 인덱스입니다.                          |
| FirstColumn          | int                 | 가져오기 작업이 시작되는 열의 0부터 시작하는 인덱스입니다.                       |
| Data                 | String[,]           | 가져올 문자열 값이 포함된 2차원 배열입니다.            |
| DestinationWorksheet | string              | 가져온 데이터를 수신할 워크시트 이름입니다.                    |
| IsInsert             | string (true/false) | **true**인 경우, 데이터가 삽입되고 기존 셀은 해당 위치로 이동됩니다. |
| ImportDataType       | string              | 데이터 유형을 지정합니다. 이 작업의 경우 `TwoDimensionStringArray`를 사용합니다.    |
| Source               | FileSource          | `BatchData` 매개변수가 null일 때 데이터 파일 위치를 나타냅니다.      |

### 예제 요청 본문

```json
{
  "Data": [
    ["1.0", "2.9"],
    ["2.0", "2.1"]
  ],
  "DestinationWorksheet": "Sheet2",
  "FirstRow": 1,
  "FirstColumn": 1,
  "ImportDataType": "TwoDimensionStringArray"
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

| 코드 | 의미                         | 설명                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보가 포함됨. |
| 400  | Bad Request                 | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식). |
| 401  | Unauthorized                | 잘못되거나 누락된 JWT 토큰. |
| 413  | Payload Too Large           | 업로드된 파일이 크기 제한을 초과함. |
| 500  | Internal Server Error       | 예기치 않은 서버 오류. |
## SDK를 사용하여 PostImportData API 사용하는 방법

### PostImportData API 사양

[OpenAPI 사양](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData)은 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의합니다.

### Aspose.Cells Cloud SDK 사용하기

SDK를 사용하면 이 기능을 통합하는 가장 빠른 방법입니다. SDK는 저수준 세부 정보를 추상화하여 비즈니스 로직에 집중할 수 있도록 도와줍니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2String.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}