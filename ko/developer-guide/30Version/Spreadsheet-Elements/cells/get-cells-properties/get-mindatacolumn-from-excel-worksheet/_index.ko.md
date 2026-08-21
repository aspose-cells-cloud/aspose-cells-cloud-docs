---
title: "MinDataColumn 가져오기 – Aspose.Cells Cloud API 참조 (v3.0)"
type: docs
url: /ko/get-mindatacolumn-from-excel-worksheet/
weight: 110
keywords: "Aspose.Cells Cloud, MinDataColumn, Excel 워크시트, REST API, API 참조, v3.0, 데이터 열, 클라우드 API"
description: "Aspose.Cells Cloud REST API(v3.0)를 사용하여 Excel 워크시트에서 데이터가 포함된 가장 왼쪽 열을 검색합니다. 인증 세부 정보, 요청 구문, JSON 응답 예시, 오류 코드, SDK 스니펫이 포함됩니다."
ArticleTitle: "MinDataColumn 가져오기 – Aspose.Cells Cloud API 참조 (v3.0)"
---

**`mindatacolumn`** 엔드포인트는 지정된 워크시트에서 데이터가 있는 가장 왼쪽 열의 0부터 시작하는 인덱스를 반환합니다.  
즉, 이 엔드포인트는 실제로 데이터를 포함하고 있는 첫 번째 열이 어느 열인지 알려줍니다.

> **정의** – `mindatacolumn`: 워크시트에서 데이터가 있는 첫 번째 열의 인덱스(0부터 시작).

**사전 조건**  
- 유효한 OAuth2 액세스 토큰이 필요합니다.  
- Excel 파일은 Aspose Cloud 저장소에 업로드되어 있어야 합니다.

**요청 매개변수**

| 매개변수              | 유형     | 필수 여부 | 설명                                           |
|-----------------------|----------|-----------|------------------------------------------------|
| `fileName`            | string   | 예        | 클라우드 저장소에 저장된 Excel 파일의 이름.     |
| `sheetName`           | string   | 예        | 열 인덱스를 가져올 워크시트의 이름.             |
| `Authorization` (헤더) | string   | 예        | OAuth2 인증을 위한 베어러 토큰.                |

- **cURL 예시**

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/mindatacolumn" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/mindatacolumn" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MinDataColumn": 2
}
```

{{< /tab >}}

{{< /tabs >}}

**HTTP 상태 코드**

| 코드 | 의미               | 설명                                                    |
|------|--------------------|---------------------------------------------------------|
| 200  | OK (성공)          | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함.     |
| 400  | Bad Request (잘못된 요청) | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형)가 포함됨. |
| 401  | Unauthorized (인증되지 않음) | 잘못되거나 누락된 JWT 토큰.                             |
| 413  | Payload Too Large (ペイロードが大きすぎます) | 업로드된 파일이 크기 제한을 초과함.                    |
| 500  | Internal Server Error (내부 서버 오류) | 예기치 않은 서버 오류 발생.                           |
---

- Aspose.Cells Cloud SDK 사용하기

SDK를 사용하면 개발 속도를 최대한 높일 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 로직에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하십시오.

다음 코드 예시는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinDataColumnWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinDataColumnWorksheet-get-min-data-column.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinDataColumn.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_data_column.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinDataColumnFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinDataColumnWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinDataColumnWorksheet-get-min-data-column.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinDataColumnWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "48105eac1e6a64ad3ae4f269c32f3a88" >}}

{{< /tab >}}

{{< /tabs >}}
---