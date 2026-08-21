---
title: "Excel 워크시트에서 MinRow 가져오기 – Aspose.Cells Cloud API 참조"
type: docs
url: /ko/get-minrow-from-excel-worksheet/
weight: 80
keywords: "Aspose.Cells, GetMinRow, Excel 워크시트, REST API, 최소 행 인덱스, 클라우드 SDK"
description: "Aspose.Cells Cloud REST API(v3.0)를 사용하여 워크시트의 최소 행 인덱스를 검색하는 방법을 알아보세요. 인증이 포함된 전체 cURL 요청, 응답 스키마, 여러 언어의 SDK 예제가 포함되어 있습니다."
ArticleTitle: "Excel 워크시트에서 MinRow 가져오기 – Aspose.Cells Cloud API 참조"
---

이 REST API는 `cellOrMethodName` 매개변수가 `minrow`로 설정된 경우 Excel 워크시트 내 최소 행 인덱스를 반환합니다. 이 엔드포인트는 주어진 워크시트에서 비어 있지 않은 첫 번째 행(0부터 시작하는 인덱스)을 확인하는 데 사용할 수 있습니다.

- **cURL 예제:**

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/minrow" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "MinRow": 0
}
```

{{< /tab >}}

{{< /tabs >}}

**요청**

```
GET https://api.aspose.com/v3.0/cells/{fileName}/worksheets/{sheetName}/cells/minrow
```

| 속성               | 유형   | 필수 여부 | 설명                                                  |
|--------------------|--------|-----------|-------------------------------------------------------|
| `fileName`         | string | 예        | 워크북 이름(예: `myWorkbook.xlsx`).                   |
| `sheetName`        | string | 예        | 대상 워크시트(예: `Sheet1`).                          |
| `cellOrMethodName` | string | 예        | 고정값 `minrow`.                                      |
| `folder`           | string | 아니요    | 클라우드 스토리지 폴더 경로.                          |
| `storageName`      | string | 아니요    | 기본값이 아닌 스토리지를 사용하는 경우 스토리지 이름. |

**응답**

서비스는 `MinRow` 속성을 포함하는 JSON 객체를 반환하며, 이는 비어 있지 않은 첫 번째 행의 인덱스(0부터 시작)를 나타냅니다.

| HTTP 상태 코드 | 의미                                         |
|----------------|----------------------------------------------|
| 200            | 성공 – `MinRow`를 포함하는 JSON 페이로드.   |
| 401            | 인증 실패 – 잘못되었거나 누락된 토큰.        |
| 404            | 워크북 또는 워크시트를 찾을 수 없음.         |
| 500            | 내부 서버 오류.                              |

`MinRow` 값은 시트 내 데이터의 시작 지점을 빠르게 확인해야 할 때 유용합니다.

- **Aspose.Cells Cloud SDK 사용**

SDK를 사용하는 것이 개발 속도를 높이는 가장 빠른 방법입니다. SDK는 저수준 세부 사항을 처리해주므로, 프로젝트 자체에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinRowWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinRowWorksheet-get-min-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_row.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinRowFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinRowWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinRowWorksheet-get-min-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinRowWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "d9497c39cde5cecb6709ff5feb2ab2b8" >}}

{{< /tab >}}

{{< /tabs >}}