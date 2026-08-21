---
title: "워크시트에서 셀 서식 가져오기 – Aspose.Cells Cloud API"
type: docs
url: /ko/get-cell-style-from-a-worksheet/
weight: 10
keywords: "Aspose.Cells, Excel, REST API, 셀 서식, 스프레드시트, 클라우드 SDK, API 문서"
description: "Aspose.Cells Cloud REST API v3를 사용하여 Excel 워크시트의 특정 셀 서식을 가져오는 방법을 알아보세요. cURL 예제, 응답 스키마, 상태 코드, SDK 스니펫이 포함됩니다."
ArticleTitle: "Aspose.Cells Cloud API를 사용하여 워크시트에서 셀 서식 가져오기 – 상세 가이드"
---

이 REST API를 사용하여 Excel 워크시트의 셀 **서식**을 가져올 수 있습니다.

## GetWorksheetCellStyle API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/style
```

### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 파라미터


| 파라미터 이름 | 타입   | 위치 | 설명                              |
| ------------- | ------ | ---- | --------------------------------- |
| name          | string | path | Excel 문서의 이름입니다.          |
| sheetName     | string | path | 워크시트의 이름입니다.            |
| cellName      | string | path | 셀의 주소입니다(예: A1).           |
| folder        | string | query | 파일이 포함된 폴더입니다.         |
| storageName   | string | query | 사용할 스토리지의 이름입니다.     |


### **응답**

```json
{
  "Style": {
    "Font": {
      "Color": { "A": 255, "R": 5, "G": 99, "B": 193 },
      "DoubleSize": 11,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Calibri",
      "Size": 11,
      "Underline": "Single"
    },
    "Name": null,
    "CultureCustom": "General",
    "Custom": "",
    "BackgroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "ForegroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "IsFormulaHidden": false,
    "IsDateTime": false,
    "IsTextWrapped": false,
    "IsGradient": false,
    "IsLocked": true,
    "IsPercent": false,
    "ShrinkToFit": false,
    "IndentLevel": 0,
    "Number": 0,
    "RotationAngle": 0,
    "Pattern": "None",
    "TextDirection": "Context",
    "VerticalAlignment": "Bottom",
    "HorizontalAlignment": "General",
    "BorderCollection": [
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "BottomBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalDown"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalUp"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Horizontal"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "LeftBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "RightBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "TopBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Vertical"
      }
    ],
    "BackgroundThemeColor": null,
    "ForegroundThemeColor": null,
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/cells/a1/style",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

**HTTP 상태 코드**

| 코드 | 의미                        | 설명                                             |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함. |
| 400  | Bad Request                 | 누락되거나 잘못된 파라미터(예: 지원되지 않는 파일 형식). |
| 401  | Unauthorized                | 잘못되거나 누락된 JWT 토큰. |
| 413  | Payload Too Large           | 업로드된 파일이 크기 제한을 초과함. |
| 500  | Internal Server Error       | 예기치 않은 서버 오류. |

**오류 응답**  
이 엔드포인트의 일반적인 오류 응답 본문은 표준 Aspose.Cells 오류 형식을 따릅니다. 예를 들어, 400 Bad Request는 다음과 같은 응답을 반환합니다:

```json
{
  "Code": 400,
  "Message": "Invalid parameter 'cellName'.",
  "Description": "The cell name provided is not in a valid A1 format."
}
```

동일하게, 401 Unauthorized는 다음과 같은 응답을 반환합니다:

```json
{
  "Code": 401,
  "Message": "Authentication failed.",
  "Description": "The JWT token is missing or invalid."
}
```

## SDK를 사용하여 GetWorksheetCellStyle API 사용하기

### GetWorksheetCellStyle API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCellStyle)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/a1/style" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Style": {
    "Font": {
      "Color": { "A": 255, "R": 5, "G": 99, "B": 193 },
      "DoubleSize": 11,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Calibri",
      "Size": 11,
      "Underline": "Single"
    },
    "Name": null,
    "CultureCustom": "General",
    "Custom": "",
    "BackgroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "ForegroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "IsFormulaHidden": false,
    "IsDateTime": false,
    "IsTextWrapped": false,
    "IsGradient": false,
    "IsLocked": true,
    "IsPercent": false,
    "ShrinkToFit": false,
    "IndentLevel": 0,
    "Number": 0,
    "RotationAngle": 0,
    "Pattern": "None",
    "TextDirection": "Context",
    "VerticalAlignment": "Bottom",
    "HorizontalAlignment": "General",
    "BorderCollection": [
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "BottomBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalDown"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalUp"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Horizontal"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "LeftBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "RightBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "TopBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Vertical"
      }
    ],
    "BackgroundThemeColor": null,
    "ForegroundThemeColor": null,
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/cells/a1/style",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## 응답 스키마

| 필드                      | 타입    | 설명                                                                 |
| ------------------------ | ------- | ------------------------------------------------------------------- |
| **Style**                | object  | 셀의 모든 서식 관련 속성이 포함된 컨테이너입니다.                    |
| Style.Font               | object  | 글꼴 설정(이름, 크기, 색상, 스타일 플래그)입니다.                    |
| Style.Font.Color         | object  | 글꼴의 RGBA 색상 값입니다.                                           |
| Style.Font.IsBold        | boolean | 글꼴이 굵게 설정되어 있으면 `true`입니다.                            |
| Style.Font.IsItalic      | boolean | 글꼴이 이텔릭(기울임)이면 `true`입니다.                              |
| Style.Font.IsStrikeout   | boolean | 글꼴에 취소선이 적용되어 있으면 `true`입니다.                        |
| Style.Font.IsSubscript   | boolean | 글꼴이 아래 첨자이면 `true`입니다.                                   |
| Style.Font.IsSuperscript | boolean | 글꼴이 위 첨자이면 `true`입니다.                                     |
| Style.Font.Name          | string  | 글꼴 패밀리 이름(예: **Calibri**)입니다.                             |
| Style.Font.Size          | number  | 글꼴 크기(포인트 단위)입니다.                                        |
| Style.Font.Underline     | string  | 밑줄 스타일(예: **Single**)입니다.                                   |
| Style.IsLocked           | boolean | 셀이 편집으로부터 보호되는지 여부를 나타냅니다.                      |
| Style.IsTextWrapped      | boolean | 텍스트 줄 바꿈이 활성화되어 있으면 `true`입니다.                      |
| Style.IsGradient         | boolean | 그라데이션 채우기가 적용되어 있으면 `true`입니다.                     |
| Style.Pattern            | string  | 채우기 패턴 이름(예: **None**)입니다.                                |
| Style.BorderCollection   | array   | 선 스타일, 색상 및 테두리 유형을 정의하는 테두리 객체의 목록입니다.   |
| Style.BackgroundColor    | object  | 셀 배경의 RGBA 값입니다.                                             |
| Style.ForegroundColor    | object  | 셀 전경의 RGBA 값입니다.                                             |
| …                        | …       | _(다른 필드는 API 참조에서 정의한 것과 동일한 패턴을 따릅니다.)_    |

### Aspose.Cells Cloud SDK 사용하기

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCellStyle.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCellStyle.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCellStyle.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCellStyle.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCellStyle.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCellStyle.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCellStyle.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCellStyle.go" >}}

{{< /tab >}}

{{< /tabs >}}

**참고 자료**  
- [셀 서식 설정](https://apireference.aspose.cloud/cells/#/Cells/SetWorksheetCellStyle)  
- [셀 값 가져오기](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell)