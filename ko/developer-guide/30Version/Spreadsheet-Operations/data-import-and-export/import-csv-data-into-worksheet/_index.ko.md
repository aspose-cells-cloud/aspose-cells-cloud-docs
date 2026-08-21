---
title: "CSV 데이터를 Excel 워크시트로 가져오기"
second_title: "문서"
linktitle: "CSV 데이터 가져오기"
type: docs
url: /ko/import-CSV-data-into-excel/
aliases:
  - /import-CSV-data-into-worksheet/
  - /import-data/csv-data/
  - /import/csv-data/
keywords: "CSV 데이터 가져오기, Excel, Aspose.Cells Cloud, REST API, 스프레드시트, CSV 가져오기"
description: "Aspose.Cells Cloud REST API는 CSV 데이터를 Excel 워크시트로 가져올 수 있도록 지원합니다. 지원되는 SDK는 Android, .NET, Go, Java, Node.js, Perl, PHP, Python, Ruby, Swift 등입니다."
weight: 19
---

이 REST API는 **CSV 데이터를 Excel 워크시트로 가져옵니다**.

요청은 multipart 콘텐츠가 포함된 HTTP 요청입니다(참고: [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) 또는 [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). multipart 콘텐츠의 첫 번째 파트는 `ImportCSVDataOption` 데이터를 포함하고, 두 번째 파트는 CSV 파일을 포함합니다.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 위해 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

중요한 매개변수는 아래 표에 설명되어 있습니다.

### ImportCSVDataOption

| 매개변수 이름       | 유형                       | 설명                                                                    |
| ------------------ | -------------------------- | ----------------------------------------------------------------------- |
| SeparatorString    | string                     | CSV 파일에서 필드를 구분하는 데 사용되는 문자(예: `,` 또는 `;`).       |
| ConvertNumericData | string (`true`/`false`)    | 숫자형 문자열을 숫자 값으로 변환할지 여부를 나타냅니다.               |
| FirstRow           | int                        | 데이터를 배치할 첫 번째 행의 1부터 시작하는 인덱스입니다.              |
| FirstColumn        | int                        | 데이터를 배치할 첫 번째 열의 1부터 시작하는 인덱스입니다.              |
| SourceFile         | string                     | 가져올 소스 CSV 파일의 이름입니다.                                      |
| CustomParsers      | List\<CustomParserConfig\> | 특정 열에 적용할 사용자 정의 파서 설정의 컬렉션입니다.                 |

### CustomParserConfig

| 매개변수 이름  | 유형   | 설명                                                            |
| -------------- | ------ | --------------------------------------------------------------- |
| ColumnIndex    | int    | 사용자 정의 파서가 적용되는 열의 0부터 시작하는 인덱스입니다.    |
| ParseMethod    | string | 열의 파싱 방법(예: `ToString`, `ToDate`, `ToNumber`)입니다.     |
| CustomStyle    | string | 파싱된 셀에 적용되는 사용자 정의 스타일(예: 숫자 서식)입니다.     |

**예제**

```xml
<ImportCSVDataOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>true</IsInsert>
    <ImportDataType>CSVData</ImportDataType>
    <SeparatorString>;</SeparatorString>
    <ConvertNumericData>true</ConvertNumericData>
    <FirstRow>1</FirstRow>
    <FirstColumn>2</FirstColumn>
    <SourceFile>TestImportDataCSV.CSV</SourceFile>
    <CustomParsers>
        <CustomParserConfig>
            <ColumnIndex>0</ColumnIndex>
            <ParseMethod>ToString</ParseMethod>
            <CustomStyle>#</CustomStyle>
        </CustomParserConfig>
    </CustomParsers>
</ImportCSVDataOption>
```
### 응답

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP 상태 코드**

| 코드 | 의미                    | 설명                                                     |
|------|-------------------------|----------------------------------------------------------|
| 200  | OK                      | 필터가 성공적으로 적용되었으며, 응답에 작업 세부 정보가 포함됩니다. |
| 400  | Bad Request             | 누락되었거나 잘못된 매개변수(예: 지원되지 않는 파일 형식)입니다.  |
| 401  | Unauthorized            | 잘못되었거나 누락된 JWT 토큰입니다.                         |
| 413  | Payload Too Large       | 업로드된 파일이 크기 제한을 초과했습니다.                    |
| 500  | Internal Server Error   | 예기치 않은 서버 오류입니다.                                |

## SDK를 사용하여 PostImportData API 사용하는 방법

### PostImportData API 사양

[OpenAPI 사양](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData)은 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의합니다.

### Aspose.Cells Cloud SDK 사용

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 추상화하여 비즈니스 로직에 집중할 수 있도록 해줍니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

아래 코드 예제는 PHP SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="1" tabID="1" tabName1="PHP" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportCSVData.php" >}}
{{< /tab >}}
{{< /tabs >}}