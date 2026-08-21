---
title: "문자열 배열을 엑셀 워크시트로 가져오기 – Aspose.Cells Cloud"
second_title: "문서"
linktitle: "문자열 배열 가져오기"
type: docs
url: /import-string-array-into-excel-worksheet/
aliases:
  - /import-string-array-into-worksheet/
  - /import-data/string-array/
  - /import/string-array/
keywords: "Aspose.Cells Cloud, 문자열 배열 가져오기, 엑셀 REST API, 멀티파트 업로드, 워크시트 데이터 가져오기, 클라우드 SDK"
description: "Aspose.Cells Cloud REST API(v3.0)를 사용하여 엑셀 워크시트에 문자열 배열을 가져오는 방법을 알아보세요. 요청 형식, 매개변수 및 SDK 예제가 포함됩니다."
weight: 40
ArticleTitle: "문자열 배열을 엑셀 워크시트로 가져오기 – Aspose.Cells Cloud"
---

문자열 배열을 엑셀 워크시트로 가져오는 작업은 목록 기반 데이터로 스프레드시트를 채울 때 흔히 이루어지는 작업입니다. 이 작업은 구성 값 로드, 외부 소스에서 데이터 전송, 미리 정의된 문자열 컬렉션으로 워크시트를 초기화하는 등의 시나리오에 유용합니다.

**필수 조건:**  
- Aspose.Cells Cloud 인증 흐름을 통해 얻은 유효한 JWT 토큰.  
- Aspose Cloud 스토리지에 존재하는 기존 워크북(또는 이를 생성할 수 있는 능력).  
- `ImportStringArrayOption` 모델을 지원하는 적절한 SDK 버전.

이 REST API는 문자열 배열 데이터를 엑셀 워크시트로 가져옵니다.

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **요청 매개변수**

요청은 multipart HTTP 콘텐츠를 사용합니다(참고: [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) 또는 [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).  
multipart 본문의 첫 번째 부분은 **ImportStringArrayOption** 페이로드를 포함하며, 두 번째 부분은 원본 데이터 파일을 포함합니다.

중요 매개변수는 다음 표에 설명되어 있습니다:

<caption>ImportStringArrayOption 매개변수</caption>
### **ImportStringArrayOption**

| 매개변수 이름          | 유형         | 설명                                                                                                                                                                         |
| ---------------------- | ------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| FirstRow               | int          | 데이터가 배치될 시작 행 인덱스(1부터 시작).                                                                                                                                   |
| FirstColumn            | int          | 데이터가 배치될 시작 열 인덱스(1부터 시작).                                                                                                                                   |
| IsVertical             | boolean      | `true`이면 데이터를 수직으로 삽입하고, `false`이면 수평으로 삽입합니다.                                                                                                       |
| Data                   | String[]     | 가져올 문자열 배열.                                                                                                                                                           |
| DestinationWorksheet   | string       | 데이터를 수신할 워크시트 이름.                                                                                                                                               |
| IsInsert               | boolean      | `true`이면 기존 셀을 이동시키며 행/열을 삽입하고, `false`이면 기존 셀을 덮어씁니다.                                                                                          |
| ImportDataType         | string       | 가져올 데이터 유형(예: `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`).      |
| Source                 | FileSource   | **BatchData**가 null일 때 데이터 파일이 위치한 곳을 설명합니다(예: `CloudFileSystem`, `LocalFile`). `BatchData`가 제공되지 않을 경우 필수입니다.                            |

### 예제

```xml
<ImportStringArrayOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>StringArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_string_xml.txt</FilePath>
    </Source>
</ImportStringArrayOption>
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
| ---- | ---------------------------------------- |
| 200  | 가져오기 성공                             |
| 400  | 잘못된 요청 – 누락되거나 유효하지 않은 데이터 |
| 401  | 인증되지 않음 – 유효하지 않거나 누락된 토큰   |
| 500  | 내부 서버 오류                            |


## SDK를 사용하여 PostImportData API 사용하기

### PostImportData API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

### Aspose.Cells Cloud SDK 사용하기

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-String.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}