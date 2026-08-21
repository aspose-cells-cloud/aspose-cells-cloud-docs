---
title: "Aspose.Cells Cloud API – Excel 워크시트의 MaxDataColumn 가져오기(v3.0)"
type: docs
url: /ko/get-maxdatacolumn-from-excel-worksheet/
weight: 70
keywords: "Aspose.Cells Cloud, MaxDataColumn 가져오기, Excel 워크시트, REST API, v3.0, SDK"
description: "지정된 워크시트에서 데이터가 포함된 최대 열 인덱스를 Aspose.Cells Cloud REST API(v3.0)를 사용해 검색합니다. 요청 세부 정보, 샘플 응답 및 SDK 예제가 포함되어 있습니다."
ArticleTitle: "Aspose.Cells Cloud API – Excel 워크시트의 MaxDataColumn 가져오기(v3.0)"
---

이 REST API는 `cellOrMethodName` 매개변수를 `maxdatacolumn`으로 설정할 때 Excel 워크시트의 최대 데이터 열 인덱스를 반환합니다.

## **cURL 예제**

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/maxdatacolumn" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MaxDataColumn": 12
}
```

{{< /tab >}}

{{< /tabs >}}

**요청 세부 정보**  
- **HTTP 메서드:** `GET`  
- **엔드포인트 패턴:** `https://api.aspose.com/v3.0/cells/{fileName}/worksheets/{sheetName}/cells/maxdatacolumn`  
- **경로 매개변수:**  
  - `fileName` – Excel 파일 이름(예: `myWorkbook.xlsx`).  
  - `sheetName` – 워크시트 이름(예: `Sheet1`).  
- **헤더:**  
  - `Authorization: Bearer <access_token>` (필수)  
  - `Accept: application/json` (권장)  

**매개변수**

| 매개변수 | 위치 | 유형   | 필수 여부 | 설명 |
|----------|------|--------|-----------|------|
| `fileName` | 경로 | string | 예       | 클라우드 스토리지에 저장된 Excel 파일 이름입니다. |
| `sheetName` | 경로 | string | 예       | 최대 데이터 열을 가져올 워크시트입니다. |
| `cellOrMethodName` | 경로 | string | 예 | 이 작업을 호출하려면 반드시 `maxdatacolumn`으로 설정해야 합니다. |

**응답**

| 상태 코드 | 설명                                   | 예제 페이로드 |
|-----------|----------------------------------------|---------------|
| 200       | 성공 – 최대 데이터 열 인덱스를 반환합니다. | `{ "MaxDataColumn": 12 }` |
| 401       | 인증되지 않음 – 잘못되거나 누락된 액세스 토큰입니다. | `{ "error": "Invalid authentication." }` |
| 404       | 찾을 수 없음 – 파일 또는 워크시트가 존재하지 않습니다. | `{ "error": "Resource not found." }` |
| 500       | 내부 서버 오류 – 예기치 않은 조건입니다. | `{ "error": "Server error." }` |

**오류 처리**  
요청이 실패한 경우, HTTP 상태 코드와 응답 본문의 `error` 메시지를 확인하십시오. 액세스 토큰이 유효하고, 지정된 파일과 워크시트가 Aspose Cloud 스토리지에 존재하는지 확인하십시오.

- **Aspose.Cells Cloud SDK 사용하기**

SDK를 사용하는 것이 개발 속도를 최대한 높이는 가장 효율적인 방법입니다. SDK는 저수준 세부 사항을 처리해주므로, 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하십시오.

다음 코드 예제는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMaxDataColumnWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMaxDataColumnWorksheet-get-max-data-column.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMaxDataColumn.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_max_data_column.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMaxDataColumnFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMaxDataColumnWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMaxDataColumnWorksheet-get-max-data-column.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMaxDataColumnWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "126f68818f671a2f6087ee334726c454" >}}

{{< /tab >}}

{{< /tabs >}}