---
title: "Excel에서 워크시트 이름 바꾸기 – Aspose.Cells Cloud API"
second_title: "문서"
ArticleTitle: "Excel에서 워크시트 이름 바꾸는 방법 – 시트 이름 변경"
linktitle: "스프레드시트에서 워크시트 이름 바꾸기"
type: docs
url: /rename-worksheet-in-spreadsheet/
keywords: "워크시트 이름 변경, Aspose.Cells Cloud, Excel API, 스프레드시트, SDK, REST API"
description: "Aspose.Cells Cloud API를 사용해 Excel 워크시트 이름을 손쉽게 변경하세요. 필요한 매개변수를 확인하고, cURL 예제를 살펴보며 C#, Java, Python 등 다양한 언어의 SDK 코드를 얻으세요."
weight: 100
---

Aspose.Cells Cloud API를 사용해 프로그래밍 방식으로 Excel 워크북의 워크시트 이름을 변경하세요. 시트 이름을 바꾸고 탭 라벨을 동적으로 업데이트하며, RESTful API 호출을 통해 스프레드시트 정리를 자동화하세요. 문서 표준화 및 워크플로우 자동화에 유용합니다.

## 스프레드시트 API에서 워크시트 이름 바꾸기

### 웹 API

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet?sourceName={sourceName}&targetName={targetName}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}
```

**cURL 예제**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet?sourceName=Sheet1&targetName=Report_Q1" \
     -H "Authorization: Bearer {access_token}" \
     -F "spreadsheet=@myWorkbook.xlsx"
```

### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름       | 유형     | 위치     | 설명                                                                                                                                                                                                                                                                               |
| ------------------- | -------- | -------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Spreadsheet**     | 파일     | FormData | **필수**. 이름을 바꿀 워크시트가 포함된 Excel 워크북 파일(.xlsx, .xls 등).                                                                                                                                                                                                      |
| **sourceName**      | 문자열   | 쿼리     | **필수**. 이름을 바꾸려는 워크시트의 현재 이름.                                                                                                                                                                                                                                  |
| **targetName**      | 문자열   | 쿼리     | **필수**. 워크시트에 할당할 새 이름. Excel의 이름 지정 규칙(`:`, `\`, `?`, `*`, `[`, `]` 불가)을 준수하며 워크북 내에서 고유해야 합니다.                                                                                                                                           |
| **outPath**         | 문자열   | 쿼리     | **선택 사항**. 이름이 변경된 워크북을 저장할 클라우드 스토리지의 대상 폴더 경로. `null`이거나 생략 시, 서비스는 원본 워크북과 동일한 폴더(또는 기본 경로)에 파일을 저장합니다.                                                                                                         |
| **outStorageName**  | 문자열   | 쿼리     | **선택 사항**. 설정한 클라우드 스토리지 서비스의 이름 식별자(예: `ArchiveStorage`). 생략 시 기본 저장소가 사용됩니다.                                                                                                                                                               |
| **region**          | 문자열   | 쿼리     | **선택 사항**. 지역 설정(예: `ko-KR`)으로, 문자 인코딩이나 지역별 이름 지정 규칙에 영향을 줄 수 있습니다.                                                                                                                                                                          |
| **password**        | 문자열   | 쿼리     | **선택 사항**. 암호로 보호된 워크북을 열고 수정하는 데 필요한 복호화 암호. 파일이 암호화되지 않은 경우 생략 가능.                                                                                                                                                                |

**참고**: 워크시트 이름은 최대 31자로 제한되며, `:`, `\`, `?`, `*`, `[`, `]` 문자를 포함할 수 없습니다.

### 응답

성공적인 요청은 상태 정보와 이름이 변경된 파일의 링크를 포함하는 JSON 객체를 반환합니다.

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**HTTP 상태 코드**

| 코드 | 의미                    | 설명                                                          |
| ---- | ----------------------- | ------------------------------------------------------------- |
| 200  | OK(성공)                | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함.         |
| 400  | 잘못된 요청             | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식).       |
| 401  | 인증되지 않음           | 잘못되거나 누락된 JWT 토큰.                                    |
| 413  | 페이로드가 너무 큼      | 업로드한 파일이 크기 제한을 초과함.                            |
| 500  | 내부 서버 오류          | 예기치 않은 서버 오류.                                         |

## Rename Worksheet in Spreadsheet API를 어디에 사용해야 할까요?

- **보고서 생성 및 브랜드 표준화** – 고객 보고서를 자동으로 생성할 때, 일반적인 워크시트 이름(`Sheet1` 등)을 고객별 이름(`AcmeCorp_Q1_Summary` 등)으로 바꿔 전문적인 결과물을 제공합니다.
- **데이터 처리 파이프라인 표준화** – ETL 워크플로우에서 이름이 일관되지 않은 워크시트를 `Raw_Data` 또는 `Cleaned_Data`와 같은 표준 이름으로 바꿔 후속 분석 요구 사항을 충족합니다.
- **다국어 콘텐츠 제공** – 사용자의 언어 설정에 따라 워크시트 이름을 현지화(`数据` 또는 `Data` 등)한 후 파일을 제공해 맞춤형 사용자 경험을 제공합니다.

## 왜 Rename Worksheet in Spreadsheet API를 사용해야 할까요?

- **개발자 친화적** – 다양한 언어를 위한 SDK와 종합적인 문서를 제공해 사용자 정의 솔루션을 구축하는 것보다 통합이 간편합니다.
- **수동 작업 감소** – 워크시트 이름 변경을 자동화해 수동 작업을 줄입니다.
- **사용량 과금 모델** – API 호출만 과금되어 사전 라이선스 비용이 없습니다.
- **서버 유지보수 불필요** – 클라우드 서비스이므로 서버 호스팅, 유지보수 및 소프트웨어 업데이트가 필요 없습니다.
- **자동화 지원** – 워크플로우 내에서 문서 표준화를 자동화할 수 있습니다.

## SDK를 사용하여 Rename Worksheet in Spreadsheet API 활용하기

### OpenAPI 사양

<a href="https://reference.aspose.cloud/cells/#/ManagementController/RenameWorksheetInSpreadsheet" target="_blank" rel="noopener noreferrer">OpenAPI 사양</a>은 웹 브라우저에서 직접 REST 상호 작용을 가능하게 하는 공개적으로 액세스 가능한 프로그래밍 인터페이스를 상세히 설명합니다.

cURL 명령줄 도구를 사용해 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL로 Cloud API에 요청하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet?sheetName=Sheet1&destName=NewSheetName" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -F "Spreadsheet=@/path/to/input.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 인코딩됨)",
  "contentType": "MIME 유형",
  "fileDownloadName": "선택적 파일 이름"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 최대한 빠르게 할 수 있습니다. SDK는 기본 HTTP 세부 정보를 추상화하여 최소한의 코드로 워크시트 이름을 변경할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 GitHub 저장소를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RenameWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RenameWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RenameWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RenameWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RenameWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RenameWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RenameWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RenameWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}