---
title: "워크시트에서 셀 데이터 가져오기"
type: docs
url: /ko/get-cell-data-from-a-worksheet/
weight: 10
keywords: "Aspose.Cells Cloud, 셀 데이터 가져오기, Excel API, REST API, 셀 값, 워크시트 API, Aspose API 예제"
description: "Aspose.Cells Cloud REST API(v3.0)를 사용하여 Excel 워크시트에서 단일 셀의 값, 유형, 스타일을 검색합니다. cURL, SDK 예제, 매개변수 및 오류 처리를 포함합니다."
---

이 REST API는 **`cellOrMethodName`** 매개변수에 셀 이름(A1 스타일 주소, 예: `A3`)을 지정하면 Excel 워크시트에서 해당 셀을 검색합니다.

- **cURL 예제**

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```shell
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

**매개변수**

| 매개변수             | 유형     | 설명                                                      | 필수 여부 |
|----------------------|----------|-------------------------------------------------------------|---------|
| `cellOrMethodName`  | 문자열   | 첫 번째 셀을 검색하려면 `firstcell`로 설정해야 합니다.     | 예      |
| `fileName`          | 문자열   | 워크북 파일 이름(예: `myWorkbook.xlsx`)                     | 예      |
| `worksheet`         | 문자열   | 워크시트 이름(예: `Sheet1`)                                 | 예      |
| `Authorization`     | 헤더     | 인증용 Bearer 토큰                                           | 예      |

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Cell": {
    "Name": "A3",
    "Row": 2,
    "Column": 0,
    "Value": "Category",
    "Type": "IsString",
    "IsFormula": false,
    "IsMerged": false,
    "IsArrayHeader": false,
    "IsInArray": false,
    "IsErrorValue": false,
    "IsInTable": false,
    "IsStyleSet": false,
    "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #ffffff;\">Category</Font>",
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

- **Aspose.Cells Cloud SDK 사용**

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCell.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCell.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCell.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCell.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCell.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCell.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCell.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCell.go" >}}

{{< /tab >}}

{{< /tabs >}}