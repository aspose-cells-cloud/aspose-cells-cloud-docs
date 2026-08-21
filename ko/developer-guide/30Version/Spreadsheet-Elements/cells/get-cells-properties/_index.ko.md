---
title: "셀 속성 가져오기"
type: docs
url: /get-cells-properties/
weight: 130
keywords: "Aspose Cells Cloud, REST API, Excel, 워크시트, 셀 속성, 셀 속성 가져오기"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트에서 특정 셀 또는 미리 정의된 셀 메서드의 속성을 가져오는 방법을 알아보세요."
---

이 REST API는 Excel 파일에서 특정 셀을 가져오는 방법을 보여줍니다.

## REST API

```bash
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellOrMethodName}
```

## 보안 및 인증

Aspose.Cells Cloud API는 [JWT 토큰 기반 인증](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)이 필요합니다.

### 요청 매개변수

| 매개변수 이름        | 유형   | 위치 | 설명                                                                                                                                                                                                 |
| -------------------- | ------ | ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**             | string | path | Excel 문서 이름입니다.                                                                                                                                                                              |
| **sheetName**        | string | path | 셀이 포함된 워크시트 이름입니다.                                                                                                                                                                    |
| **cellOrMethodName** | string | path | 셀 이름 또는 미리 정의된 메서드 이름(예: `firstcell`, `endcell`, `maxrow`, `maxdatarow`, `maxcolumn`, `maxdatacolumn`, `minrow`, `mindatarow`, `mincolumn`, `mindatacolumn`)입니다. |
| **folder**           | string | query | 문서가 저장된 폴더입니다.                                                                                                                                                                           |
| **storageName**      | string | query | 스토리지 서비스 이름입니다.                                                                                                                                                                         |

## **응답**

CellResponse를 반환합니다.

- **응답 필드 개요**

| 필드             | 유형    | 설명                                                 |
| --------------- | ------- | ---------------------------------------------------- |
| `Name`          | string  | 셀의 주소(예: `F341`).                               |
| `Row`           | integer | 0부터 시작하는 행 인덱스입니다.                      |
| `Column`        | integer | 0부터 시작하는 열 인덱스입니다.                      |
| `Value`         | string  | 셀에 표시된 값입니다.                                |
| `Type`          | string  | 셀의 데이터 유형(예: `IsString`).                   |
| `Formula`       | string  | 셀에 수식이 포함된 경우 수식 텍스트입니다.          |
| `IsFormula`     | bool    | 셀에 수식이 포함되어 있는지 여부를 나타냅니다.      |
| `IsMerged`      | bool    | 셀이 병합된 범위에 속하는지 여부를 나타냅니다.       |
| `IsArrayHeader` | bool    | 셀이 배열 헤더인지 여부를 나타냅니다.                |
| `IsInArray`     | bool    | 셀이 배열에 속하는지 여부를 나타냅니다.              |
| `IsErrorValue`  | bool    | 셀에 오류 값이 포함되어 있는지 여부를 나타냅니다.    |
| `IsInTable`     | bool    | 셀이 테이블 내부에 있는지 여부를 나타냅니다.         |
| `IsStyleSet`    | bool    | 셀에 스타일이 적용되어 있는지 여부를 나타냅니다.     |
| `HtmlString`    | string  | 셀 값의 HTML 인코딩 표현입니다.                      |
| `Style.link`    | object  | 스타일 리소스로의 하이퍼링크입니다.                  |


```json
{
  "Status":"OK",
  "Code":200,
  "Cell":{
    "Name":"A1",
    "Row": 0,
    "Column":0,
    "Value": "Hello Aspose.Cells",
    "Type":"String",
    "Formula" : "",
    ...
  }
}
```

**HTTP 상태 코드**

| 코드 | 의미                        | 설명                                                           |
|------|-----------------------------|----------------------------------------------------------------|
| 200  | OK                          | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함.          |
| 400  | Bad Request                 | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형).        |
| 401  | Unauthorized                | 잘못되거나 누락된 JWT 토큰.                                     |
| 413  | Payload Too Large           | 업로드된 파일이 크기 제한을 초과함.                             |
| 500  | Internal Server Error       | 예기치 않은 서버 오류.                                          |

## SDK를 사용하여 GetWorksheetCell API 사용하는 방법

### GetWorksheetCell API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API에 요청을 보내는 방법을 보여줍니다.
{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3?client_id=YOUR_CLIENT_ID&client_secret=YOUR_CLIENT_SECRET" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Cell": {
    "Name": "A3",
    "Row": 2,
    "Column": 0,
    "Value": "Statistical",
    "Type": "IsString",
    "IsFormula": false,
    "IsMerged": false,
    "IsArrayHeader": false,
    "IsInArray": false,
    "IsErrorValue": false,
    "IsInTable": false,
    "IsStyleSet": false,
    "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\">Statistical</Font>",
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    },
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 가장 효율적으로 높일 수 있습니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 작업에 집중할 수 있게 해줍니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다.

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

### 특정 셀을 가져오는 방법

- [워크시트에서 셀 데이터 가져오기](/cells/get-cell-data-from-a-worksheet/)
- [Excel 워크시트에서 첫 번째 셀 가져오기](/cells/get-first-cell-from-excel-worksheet/)
- [Excel 워크시트에서 마지막 셀 가져오기](/cells/get-last-cell-of-excel-worksheet/)
- [Excel 워크시트에서 MaxRow 가져오기](/cells/get-maxrow-from-excel-worksheet/)
- [Excel 워크시트에서 MaxDataRow 가져오기](/cells/get-maxdatarow-from-excel-worksheet/)
- [Excel 워크시트에서 MaxColumn 가져오기](/cells/get-maxcolumn-from-excel-worksheet/)
- [Excel 워크시트에서 MaxDataColumn 가져오기](/cells/get-maxdatacolumn-from-excel-worksheet/)
- [Excel 워크시트에서 MinRow 가져오기](/cells/get-minrow-from-excel-worksheet/)
- [Excel 워크시트에서 MinDataRow 가져오기](/cells/get-mindatarow-from-excel-worksheet/)
- [Excel 워크시트에서 MinColumn 가져오기](/cells/get-mincolumn-from-excel-worksheet/)
- [Excel 워크시트에서 MinDataColumn 가져오기](/cells/get-mindatacolumn-from-excel-worksheet/)