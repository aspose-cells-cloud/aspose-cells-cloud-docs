---
title: "Excel 워크시트에 대량 데이터 가져오기"
second_title: "문서"
linktitle: "대량 데이터 가져오기"
type: docs
url: /import-batch-data-into-excel/
aliases:
  - /import-batch-data-into-worksheet/
  - /import-data/batch-data/
  - /import/batch-data/
keywords: "Aspose.Cells, 클라우드 API, 대량 데이터 가져오기, Excel, CSV, JSON, XML, 배열"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트에 대량 데이터(CSV, JSON, XML, 배열)를 가져오는 방법을 알아보세요. 인증, 요청/응답 예제, SDK 스니펫, 오류 처리가 포함됩니다."
weight: 19
ArticleTitle: "Excel 워크시트에 대량 데이터 가져오기 – Aspose.Cells Cloud 문서"
---

이 REST API는 **대량 데이터**를 Excel 워크시트에 가져옵니다. 멀티파트 요청을 받아 첫 번째 파트에는 **ImportBatchDataOption** 객체가 포함되고 두 번째 파트에는 실제 데이터 파일(CSV, JSON, XML 등)이 전달됩니다.

이 작업은 멀티파트 콘텐츠를 사용하는 HTTP 요청을 사용합니다(참고: [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) 또는 [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).  

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 위해 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### ImportBatchDataOption

| 매개변수 이름             | 유형              | 설명                                                                                                                                                                |
| ------------------------- | ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **BatchData**             | `List<CellValue>` | 직접 쓸 셀 값의 컬렉션.                                                                                                                                             |
| **DestinationWorksheet**  | `string`          | 데이터를 가져올 워크시트의 이름.                                                                                                                                     |
| **IsInsert**              | `bool`            | `true`인 경우 데이터를 삽입하고 기존 셀을 밀어내고, `false`인 경우 기존 셀을 덮어씁니다.                                                                            |
| **ImportDataType**        | `string`          | 가져올 데이터의 형식. 허용되는 값: `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`. |
| **Source**                | `FileSource`      | **BatchData**가 `null`일 때 데이터 파일의 위치를 지정합니다.                                                                                                       |

### CellValue

| 매개변수 이름   | 유형     | 설명                                          |
| --------------- | -------- | --------------------------------------------- |
| **rowIndex**    | `int`    | 대상 셀의 0부터 시작하는 행 인덱스.           |
| **columnIndex** | `int`    | 대상 셀의 0부터 시작하는 열 인덱스.           |
| **type**        | `string` | 값의 데이터 유형(예: `int`, `double`, `string`). |
| **value**       | `string` | 셀에 쓸 실제 값.                              |
| **style**       | `Style`  | 셀의 선택적 서식 정보.                        |

### FileSource

| 매개변수 이름       | 유형     | 설명                                                             |
| ------------------- | -------- | ---------------------------------------------------------------- |
| **FileSourceType**  | `string` | 파일의 소스: `InMemoryFiles`, `CloudFileSystem`, `RequestFiles`. |
| **FilePath**        | `string` | 선택한 소스 내에서의 파일 경로 또는 식별자.                      |

### 예제(XML)

```xml
<ImportBatchDataOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>IntArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_int_xml.txt</FilePath>
    </Source>
</ImportBatchDataOption>
```

### 응답

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP 상태 코드**

| 코드 | 의미                    | 설명                                                                 |
|------|-------------------------|----------------------------------------------------------------------|
| 200  | OK                      | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보가 포함됨.           |
| 400  | Bad Request             | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식).             |
| 401  | Unauthorized            | 잘못되거나 누락된 JWT 토큰.                                          |
| 413  | Payload Too Large       | 업로드된 파일이 크기 제한을 초과함.                                  |
| 500  | Internal Server Error   | 예기치 않은 서버 오류.                                               |

## SDK를 사용하여 PostImportData API 사용하기

### PostImportData API 사양

[OpenAPI 사양](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData)은 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 하는 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의합니다.

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 이 기능을 통합하는 가장 빠른 방법입니다. SDK는 저수준 세부 정보를 처리하므로 비즈니스 로직에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportBatchData.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}