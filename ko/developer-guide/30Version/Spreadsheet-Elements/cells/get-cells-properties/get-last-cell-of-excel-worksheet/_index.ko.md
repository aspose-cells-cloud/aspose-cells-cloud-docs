---
title: "Excel 워크시트의 마지막 셀 가져오기 – Aspose.Cells Cloud API(v4.0)"
type: docs
url: /ko/get-last-cell-of-excel-worksheet/
weight: 30
keywords: "Aspose.Cells, Excel API, 마지막 셀 가져오기, 스프레드시트, 클라우드"
description: "Aspose.Cells Cloud REST API v4.0을 사용하여 Excel 워크시트의 끝 셀 주소를 검색합니다. 요청 세부 정보, cURL 예제, JSON 응답 및 SDK 샘플을 포함합니다."
ArticleTitle: "Excel 워크시트의 끝 셀 가져오기 – Aspose.Cells Cloud API v4.0"
---

이 REST API는 `cellOrMethodName` 매개변수를 `endcell`로 설정하면 Excel 워크시트의 **endcell**(끝 셀)을 반환합니다.

**개요**  
**마지막 셀 가져오기** 작업은 지정된 워크시트에서 마지막으로 사용된 셀의 주소를 반환합니다. 워크북 전체를 스캔하지 않고 시트의 유효 데이터 범위를 파악하는 데 유용합니다.

- **cURL 예제.**

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/endcell" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Cell": {
    "Name": "F341",
    "Row": 340,
    "Column": 5,
    "Value": "<More Info>",
    "Type": "IsString",
    "Formula": "=HYPERLINK(SUBSTITUTE(HelpURLTemplate,\"xxxxxxxxxx\",[Help Topic]),\"<More Info>\")",
    "IsFormula": false,
    "IsMerged": false,
    "IsArrayHeader": false,
    "IsInArray": false,
    "IsErrorValue": false,
    "IsInTable": false,
    "IsStyleSet": false,
    "HtmlString": "<Font Style=\"TEXT-DECORATION: underline;FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\">&lt;More Info&gt;</Font>",
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### 매개변수
| 매개변수               | 유형     | 필수 여부 | 설명 |
|-----------------------|---------|----------|------|
| `fileName`            | string  | 예       | 클라우드에 저장된 Excel 파일 이름. |
| `worksheetName`       | string  | 예       | 마지막 셀을 가져올 워크시트 이름. |
| `cellOrMethodName`    | string  | 예       | 이 작업을 호출하려면 **`endcell`**로 설정해야 합니다. |
| `folder` *(선택 사항)* | string  | 아니요   | 워크북이 위치한 클라우드 폴더 경로. |
| `storageName` *(선택 사항)*| string | 아니요 | 스토리지 이름. 생략 시 기본 스토리지가 사용됩니다. |

**HTTP 상태 코드**

| 코드 | 의미                         | 설명                                         |
|------|------------------------------|----------------------------------------------|
| 200  | OK                           | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함. |
| 400  | Bad Request                  | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식). |
| 401  | Unauthorized                 | 잘못되거나 누락된 JWT 토큰. |
| 413  | Payload Too Large            | 업로드된 파일이 크기 제한을 초과함. |
| 500  | Internal Server Error        | 예기치 않은 서버 오류. |

- **Aspose.Cells Cloud SDK 사용**

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 정보를 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetLastCellWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetEndCellWorksheet-get-last-cell-excel-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetLastCell.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_last_cell.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetLastCellOfExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetLastCellWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetEndCellWorksheet-get-last-cell-excel-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

_곧 제공 예정._

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetLastCellWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3cf3e145c223fd6f6f3d9f6377092db5" >}}

{{< /tab >}}

{{< /tabs >}}

셀 탐색과 관련된 추가 작업은 **[첫 번째 셀 가져오기](/get-first-cell-of-excel-worksheet/)** 및 **[최대 행 가져오기](/get-max-row-of-worksheet/)** 주제를 참조하세요.