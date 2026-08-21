---
title: "이중 배열을 Excel 워크시트로 가져오기"
second_title: "문서"
linktitle: "이중 배열 가져오기"
type: docs
url: /import-double-array-into-excel-worksheet/
aliases:
  - /import-double-array-into-worksheet/
  - /import-data/double-array/
  - /import/double-array/
keywords: "Aspose.Cells, 이중 배열 가져오기, Excel API, 클라우드 SDK"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트로 이중 배열을 가져오는 방법을 알아보세요. 인증, 요청 형식, 매개변수, 샘플 XML/JSON, 응답 세부 정보를 포함합니다."
weight: 20
ArticleTitle: "이중 배열을 Excel 워크시트로 가져오기 – Aspose.Cells Cloud 가이드"
---

이 REST API는 **이중 배열 데이터**를 Excel 워크시트로 가져옵니다.

> **사전 조건:** 이 API를 호출하기 전에 유효한 JWT 토큰이 필요합니다. 자세한 내용은 인증 가이드를 참조하세요.

multipart 콘텐츠(참조: [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) 또는 [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html))를 포함하는 HTTP 요청을 보냅니다.  
multipart 본문의 첫 번째 부분에는 **ImportDoubleArrayOption** 데이터가 포함되고, 두 번째 부분에는 데이터 파일이 포함됩니다.

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 위해 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

#### **ImportDoubleArrayOption**

| 매개변수 이름         | 유형         | 설명                                                                                             |
| -------------------- | ------------ | ------------------------------------------------------------------------------------------------ |
| FirstRow             | int          | 데이터를 배치할 첫 번째 행의 0부터 시작하는 인덱스                                               |
| FirstColumn          | int          | 데이터를 배치할 첫 번째 열의 0부터 시작하는 인덱스                                               |
| IsVertical           | boolean      | `true` / `false` – 배열을 수직(`true`)으로 삽입할지 수평(`false`)으로 삽입할지 결정합니다.        |
| Data                 | Double[]     | 가져올 이중 값 배열                                                                              |
| DestinationWorksheet | string       | 대상 워크시트의 이름                                                                            |
| IsInsert             | boolean      | `true` / `false` – `true`이면 데이터를 삽입하고, `false`이면 기존 셀을 덮어씁니다.               |
| ImportDataType       | string       | 가져오는 데이터 유형(예: `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`)     |
| Source               | FileSource   | `BatchData` 매개변수가 null일 때 데이터 파일 위치를 지정합니다.                                 |

#### 예시(XML)

```xml
<ImportDoubleArrayOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>DoubleArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Data>1.99,1.9,2.0</Data>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_double_xml.txt</FilePath>
    </Source>
</ImportDoubleArrayOption>
```

#### 예시(JSON)

```json
{
  "Data": [1.99, 1.9, 2.0],
  "DestinationWorksheet": "Sheet1",
  "FirstRow": 0,
  "FirstColumn": 0,
  "IsVertical": false,
  "IsInsert": true,
  "ImportDataType": "DoubleArray"
}
```

### 응답

성공적인 요청은 다음과 유사한 JSON 페이로드를 포함하는 **HTTP 200** 상태 코드를 반환합니다:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

가능한 상태 코드:

| 코드 | 의미                                 |
| ---- | ----------------------------------- |
| 200  | 가져오기 성공                         |
| 400  | 잘못된 요청 – 누락되거나 유효하지 않은 데이터 |
| 401  | 인증 실패 – 유효하지 않거나 누락된 토큰    |
| 500  | 내부 서버 오류                       |

### 오류 처리

오류 발생 시 API는 오류 코드와 설명 메시지를 포함하는 JSON 객체를 반환합니다. 인증되지 않은 요청의 예시:

```json
{
  "Code": 401,
  "Status": "Error"
}
```

관련 가져오기 작업에 대한 자세한 정보는 “2차원 이중 배열 가져오기” 및 “정수 배열 가져오기” 문서 페이지를 참조하세요.

## SDK를 사용하여 PostImportData API 사용 방법

### PostImportData API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 개발 속도가 최적화됩니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-Double.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}