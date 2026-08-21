---
title: "엑셀 워크시트에서 피벗 테이블 가져오기"
second_title: "문서"
linktitle: 가져오기
type: docs
url: /pivot-tables/get/
aliases: [/get-worksheet-pivot-table-information-by-index/]
keywords: "Aspose.Cells, 피벗 테이블, 엑셀, REST API, 워크시트 피벗 테이블 가져오기"
description: "Aspose.Cells Cloud REST API를 사용하여 엑셀 워크시트에서 피벗 테이블을 검색합니다. 요청 구문, 매개변수, 인증, 응답 스키마, 오류 처리 및 SDK 예제를 포함합니다."
weight: 10
ArticleTitle: "엑셀 워크시트에서 피벗 테이블 가져오기"
---

이 REST API는 인덱스를 기준으로 워크시트의 **피벗 테이블** 정보를 검색합니다.

### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivottableIndex}
```

### 요청 매개변수

| 매개변수 이름        | 유형      | 위치   | 설명                                                 |
| ------------------- | --------- | ------ | ---------------------------------------------------- |
| **name**            | string    | path   | 엑셀 파일 이름.                                     |
| **sheetName**       | string    | path   | 피벗 테이블이 포함된 워크시트 이름.                 |
| **pivottableIndex** | integer   | path   | 워크시트 내 피벗 테이블의 0부터 시작하는 인덱스.     |
| **folder**          | string    | query  | 문서가 저장된 폴더.                                 |
| **storageName**     | string    | query  | Aspose Cloud 스토리지 이름.                         |

**cURL** 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "PivotFilters": [
    {
      "AutoFilter": {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "FilterColumns": [
          {
            "FieldIndex": 0,
            "FilterType": "string",
            "MultipleFilters": {
              "MatchBlank": true,
              "MultipleFilterList": [{}]
            },
            "ColorFilter": {
              "FilterByFillColor": "string",
              "Pattern": "string",
              "Color": {
                "Color": {
                  "A": 0,
                  "R": 0,
                  "G": 0,
                  "B": 0
                },
                "ColorIndex": 0,
                "IsShapeColor": true,
                "ThemeColor": {
                  "ColorType": "string",
                  "Tint": 0
                },
                "Type": "string"
              },
              "ForegroundColorColor": {
                "Color": {
                  "A": 0,
                  "R": 0,
                  "G": 0,
                  "B": 0
                },
                "ColorIndex": 0,
                "IsShapeColor": true,
                "ThemeColor": {
                  "ColorType": "string",
                  "Tint": 0
                },
                "Type": "string"
              },
              "BackgroundColor": {
                "Color": {
                  "A": 0,
                  "R": 0,
                  "G": 0,
                  "B": 0
                },
                "ColorIndex": 0,
                "IsShapeColor": true,
                "ThemeColor": {
                  "ColorType": "string",
                  "Tint": 0
                },
                "Type": "string"
              }
            },
            "CustomFilters": [
              {
                "FilterOperatorType": "string"
              }
            ],
            "DynamicFilter": {
              "DynamicFilterType": "string"
            },
            "IconFilter": {
              "IconId": 0,
              "IconSetType": "string"
            },
            "Top10Filter": {
              "Criteria": "string",
              "IsPercent": true,
              "IsTop": true,
              "Items": 0
            },
            "VisibleDropdown": "string"
          }
        ],
        "Range": "string",
        "Sorter": {
          "CaseSensitive": true,
          "HasHeaders": true,
          "KeyList": [
            {
              "Key": 0,
              "SortOrder": "string",
              "CustomList": "string"
            }
          ],
          "SortLeftToRight": true
        }
      },
      "EvaluationOrder": 0,
      "FieldIndex": 0,
      "FilterType": "string",
      "MeasureFldIndex": 0,
      "MemberPropertyFieldIndex": 0,
      "Name": "string",
      "Value1": "string",
      "Value2": "string"
    }
  ]
}
```

**응답 스키마**

| 필드             | 유형    | 설명                                           |
|----------------|---------|------------------------------------------------|
| Status         | string  | 작업 상태 텍스트(예: “OK”)                      |
| PivotFilters   | array   | 피벗 필터 정의 컬렉션.                         |
| └─ AutoFilter  | object  | 피벗에 적용된 자동 필터링 세부 정보.             |
|    └─ link     | object  | 필터에 대한 하이퍼링크 정보.                     |
|    └─ FilterColumns | array | 개별 열 필터 설정.                        |
|    └─ Range    | string  | 필터가 적용되는 셀 범위.                         |
|    └─ Sorter   | object  | 필터링된 데이터에 대한 정렬 구성.                |
| (추가 중첩 필드는 위 샘플 JSON과 동일한 구조를 따릅니다) |

{{< /tab >}}

{{< /tabs >}}

### 오류 처리

API는 표준 HTTP 상태 코드를 따릅니다. 일반적인 응답은 다음과 같습니다:

| 상태 코드 | 의미                                                              | 예시 JSON (오류)                                  |
| --------- | ----------------------------------------------------------------- | ------------------------------------------------- |
| 200       | 성공 – 피벗 테이블 반환됨                                         | —                                                 |
| 401       | 인증되지 않음 – 잘못되거나 누락된 토큰                            | `{"code":401,"message":"Invalid access token."}`  |
| 404       | 없음 – 파일, 워크시트 또는 피벗 테이블 인덱스가 존재하지 않음     | `{"code":404,"message":"Pivot table not found."}` |
| 500       | 서버 오류 – 예기치 않은 조건                                       | `{"code":500,"message":"Internal server error."}` |

**참고:** API는 최대 150MB까지의 엑셀 파일을 지원하며, 엑셀 2007~2021 형식과 호환됩니다. 워크시트 이름은 대소문자를 구분합니다.

## 클라우드 SDK 패밀리

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Objective C" tabName8="Android" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-GetWorksheetPivotTableByIndex-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-GetWorksheetPivotInfoByIndex-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetWorksheetPivotTablesInformationByIndex.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-GetWorksheetPivotTableByIndex-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Examples-Android-pivottables-GetPivotTableIndexWorksheet-get-pivottable-index-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-GetWorksheetPivotTableByIndex-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3ff21d138764aa6b6fd51fbaab8cdb95" >}}

{{< /tab >}}

{{< /tabs >}}