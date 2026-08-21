---
title: "명명된 범위를 기반으로 셀 데이터 가져오기"
second_title: "Document"
linktitle: "Values"
type: docs
url: /ranges/get/values/
aliases: [/get-cells-data-based-on-named-range/]
keywords: "Aspose.Cells, 클라우드, REST API, 엑셀, 명명된 범위, 셀 값, 워크시트"
description: "Aspose.Cells Cloud REST API를 사용하여 엑셀 워크시트의 명명된 범위에서 셀 값을 검색합니다. 이 서비스는 다양한 SDK(C#, Java, PHP, Ruby, Node.js, Python, Perl, Go)를 통해 제공되며, 다양한 개발 플랫폼에서 사용할 수 있습니다."
weight: 20
ArticleTitle: "명명된 범위를 기반으로 셀 데이터 가져오기 – Aspose.Cells Cloud API"
---

**사전 요구 사항**

- 적절한 범위(scope)가 부여된 유효한 JWT 액세스 토큰.
- 워크북이 Aspose Cloud 스토리지(또는 지정된 폴더)에 업로드되어 있어야 합니다.
- 기본 스토리지가 아닌 스토리지를 사용할 경우, 대상 스토리지 이름을 제공해야 합니다.

이 REST API는 명명된 범위 또는 행-열 인덱스로 식별되는 범위 내의 셀 목록을 반환합니다.

이 작업을 통해 개발자는 엑셀 워크시트 내 특정 명명된 범위에 속한 셀의 값을 프로그래밍 방식으로 검색할 수 있습니다. `namedRange` 식별자 또는 명시적인 행 및 열 인덱스를 제공하면, API는 주소, 행, 열, 값, 데이터 유형, 서식 정보를 포함한 세부 셀 목록을 반환합니다. 이 응답은 데이터 기반 애플리케이션 구동, 보고서 생성, 서버 측 추가 계산에 활용할 수 있습니다. Aspose.Cells Cloud 서비스는 다양한 프로그래밍 언어를 지원하는 SDK를 통해 제공되므로, 개발 플랫폼에 관계없이 원활하게 통합할 수 있습니다. HTTPS를 사용하여 데이터 전송을 보안으로 보장하며, API는 RESTful 원칙을 따르며 성공 및 오류 상황에 표준 HTTP 상태 코드를 반환합니다.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/value
```

### **요청 파라미터**

| 파라미터 이름 | 유형    | 위치  | 설명                                                                                      |
| ------------- | ------- | ----- | ----------------------------------------------------------------------------------------- |
| name          | string  | path  | 워크북 파일 이름.                                                                         |
| sheetName     | string  | path  | 워크북 내 워크시트 이름.                                                                  |
| namedRange    | string  | query | 검색할 명명된 범위(예: `A1:B2` 또는 `range_name1`).                                         |
| firstRow      | integer | query | 범위의 첫 번째 행 인덱스(0부터 시작). `namedRange`가 제공되지 않을 경우 사용됩니다.          |
| firstColumn   | integer | query | 범위의 첫 번째 열 인덱스(0부터 시작). `namedRange`가 제공되지 않을 경우 사용됩니다.          |
| rowCount      | integer | query | 범위에 포함할 행 수.                                                                      |
| columnCount   | integer | query | 범위에 포함할 열 수.                                                                      |
| folder        | string  | query | 워크북이 위치한 폴더.                                                                     |
| storageName   | string  | query | 워크북이 위치한 클라우드 스토리지 이름.                                                    |

[OpenAPI 사양서](https://apireference.aspose.cloud/cells/#/Ranges/GetWorksheetCellsRangeValue)는 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스를 쉽게 호출할 수 있습니다. 아래 예시는 명명된 범위에서 셀 값을 요청하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/value?namerange=data" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "CellsList": [
    {
      "Name": "B10",
      "Row": 9,
      "Column": 1,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "C10",
      "Row": 9,
      "Column": 2,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "D10",
      "Row": 9,
      "Column": 3,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "E10",
      "Row": 9,
      "Column": 4,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "F10",
      "Row": 9,
      "Column": 5,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "G10",
      "Row": 9,
      "Column": 6,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "H10",
      "Row": 9,
      "Column": 7,
      "Value": "a8",
      "Type": "IsString",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\">a8</Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    }
  ],
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**보안 참고 사항:** API를 호출할 때 항상 HTTPS를 사용해야 합니다. 이 서비스는 평문 HTTP를 지원하지 않으며, HTTPS를 사용해야 요청이 암호화되고 보안 모범 사례를 준수합니다.

**HTTP 상태 코드**

| 코드 | 의미                   | 설명                                          |
|------|------------------------|-----------------------------------------------|
| 200  | OK                     | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함. |
| 400  | Bad Request            | 누락되거나 잘못된 파라미터(예: 지원되지 않는 파일 유형). |
| 401  | Unauthorized           | 잘못되거나 누락된 JWT 토큰.                     |
| 413  | Payload Too Large      | 업로드된 파일이 크기 제한을 초과함.             |
| 500  | Internal Server Error  | 예기치 않은 서버 오류.                          |

**예시 오류 응답 (400 Bad Request)**

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "파라미터 'namedRange'가 누락되었거나 잘못되었습니다."
}
```

> **팁:** API는 `firstRow` 및 `firstColumn`에 대해 0부터 시작하는 인덱스를 사용합니다. 예를 들어, 워크시트의 첫 번째 행은 `0`입니다.

## 클라우드 SDK 패밀리

SDK를 사용하면 개발 속도를 가장 효율적으로 높일 수 있습니다. SDK는 저수준 세부 사항을 추상화하여 비즈니스 로직에 집중할 수 있도록 해줍니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하십시오.

다음 코드 예시는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCellsRangeValue.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCellsRangeValue.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCellsRangeValue.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCellsRangeValue.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCellsRangeValue.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCellsRangeValue.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCellsRangeValue.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCellsRangeValue.go" >}}

{{< /tab >}}

{{< /tabs >}}