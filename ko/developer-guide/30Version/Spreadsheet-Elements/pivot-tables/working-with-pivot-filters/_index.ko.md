---
title: "피벗 필터 사용하기"
second_title: "문서"
linktitle: 필터
type: docs
url: /ko/pivot-tables/add-filters/
aliases: [  /ko/working-with-pivot-filters/ ]
keywords: "Aspose.Cells, 피벗 테이블, 필터, REST API, 클라우드"
description: "Aspose.Cells Cloud REST API를 사용하여 피벗 테이블 필터를 추가, 조회 및 삭제하는 방법을 배워보세요. 요청 구문, 필요한 매개변수, cURL 예제, C# 및 Go용 SDK 스니펫이 포함됩니다."
weight: 50
ArticleTitle: "피벗 필터 사용하기 – Aspose.Cells Cloud 문서"
---

이 REST API는 지정된 인덱스에 있는 피벗 테이블에 **피벗 필터**를 추가합니다.

**사전 준비 사항**  
이 엔드포인트를 호출하기 전에 다음을 수행해야 합니다:

- 유효한 OAuth/JWT 액세스 토큰을 생성하고 `Authorization` 헤더에 포함합니다.  
- 대상 워크북이 액세스 가능한 클라우드 폴더에 저장되어 있는지 확인합니다(`folder` 및 선택적으로 `storageName`을 지정합니다).  
- Aspose.Cells Cloud API 버전 3.0 이상을 사용합니다.

## PutWorksheetPivotTableFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotFilters
```

### 보안 및 인증

Aspose.Cells Cloud API는 보안이며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름         | 유형     | 위치   | 설명                                                                                             |
| --------------------- | ------- | ------ | ------------------------------------------------------------------------------------------------ |
| **name**              | string  | path   | Excel 파일의 이름입니다.                                                                         |
| **sheetName**         | string  | path   | 피벗 테이블이 포함된 워크시트입니다.                                                             |
| **pivotTableIndex**   | integer | path   | 필터를 적용할 피벗 테이블의 0부터 시작하는 인덱스입니다.                                        |
| **filter**            | object  | body   | 필터 설정을 정의하는 JSON 객체입니다. 아래 **filter schema** 테이블을 참조하세요.              |
| **needReCalculate**   | boolean | query  | **true**인 경우 필터 추가 후 워크북을 다시 계산하도록 강제합니다. 기본값은 **false**입니다.    |
| **folder**            | string  | query  | 파일이 위치한 클라우드 저장소의 폴더입니다.                                                     |
| **storageName**       | string  | query  | 클라우드 저장소의 이름입니다.                                                                    |

**filter schema**

| 속성                         | 유형     | 설명                                                                                     |
| ---------------------------- | ------- | ---------------------------------------------------------------------------------------- |
| **AutoFilter**               | object  | 자동 필터 설정입니다. 사용하지 않는 경우 생략 가능합니다.                               |
| **EvaluationOrder**          | integer | 필터가 평가되는 순서입니다.                                                              |
| **FieldIndex**               | integer | 필터를 적용할 필드의 0부터 시작하는 인덱스입니다.                                        |
| **FilterType**               | string  | 필터 유형(예: `Value`, `Count`, `Label`)입니다.                                         |
| **MeasureFldIndex**          | integer | 측정값 필드의 인덱스입니다(해당되는 경우).                                               |
| **MemberPropertyFieldIndex** | integer | 멤버 속성 필드의 인덱스입니다(해당되는 경우).                                            |
| **Name**                     | string  | 필터의 선택적 이름입니다.                                                                |
| **Value1**                   | string  | 필터에서 사용하는 첫 번째 값입니다(예: 범위의 하한값).                                   |
| **Value2**                   | string  | 필터에서 사용하는 두 번째 값입니다(예: 범위의 상한값).                                   |
| **CustomFilters**            | array   | 사용자 정의 필터 객체 컬렉션입니다(각 객체는 `FilterOperatorType`, `Value1`, `Value2` 포함). |
| **DynamicFilter**            | object  | 동적 필터 설정입니다(예: Top10, Bottom10).                                               |
| **IconFilter**               | object  | 아이콘 기반 필터 설정입니다.                                                             |
| **Top10Filter**              | object  | Top10/Bottom10 필터 설정입니다.                                                          |
| **ColorFilter**              | object  | 색상 기반 필터 설정입니다.                                                               |
| **Visibledropdown**          | boolean | 필터 드롭다운이 표시되는지 여부를 나타냅니다.                                            |

> **참고:** 위에 나열된 모든 매개변수는 API 참조에서 명시적으로 선택 사항으로 표시되지 않는 한 모두 필수입니다.

### 응답 코드

| 코드 | 의미                                           |
| ---- | ---------------------------------------------- |
| 200  | 필터가 성공적으로 추가되었습니다.              |
| 400  | 잘못된 요청 — 유효하지 않은 매개변수입니다.     |
| 401  | 인증되지 않음 — 토큰이 누락되었거나 유효하지 않습니다. |
| 404  | 찾을 수 없음 — 워크북 또는 피벗 테이블이 없습니다. |
| 500  | 내부 서버 오류입니다.                           |

**모범 사례**  
- 필터 객체는 가능한 한 작게 유지하세요. 큰 필터 정의는 요청 지연을 증가시킬 수 있습니다.  
- 요청은 멱등성(idempotent)을 갖습니다 — 동일한 필터를 두 번 추가해도 중복되지 않습니다.  
- 계정당 분당 100개 요청으로 API 속도 제한을 준수하세요.  

*추가 참고 사항:*  
- 필터 정의의 최대 크기는 1MB입니다. 더 큰 페이로드는 400 오류로 거부됩니다.  
- `needReCalculate=true`를 사용할 경우, 대규모 워크북의 응답 시간이 길어질 수 있습니다.  

전체 OpenAPI 정의는 다음 링크에서 확인할 수 있습니다:  
[OpenAPI 명세서](https://apireference.aspose.cloud/cells/#/PivotTables/PutWorksheetPivotTableFilter)

### 예제 cURL 요청

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/pivottables/0/PivotFilters?needReCalculate=true" \
  -X PUT \
  -d '{
        "AutoFilter": {
          "link": { "Href": "https://example.com", "Rel": "self", "Title": "AutoFilter Link", "Type": "application/json" },
          "FilterColumns": [
            {
              "FieldIndex": 0,
              "FilterType": "Value",
              "MultipleFilters": {
                "MatchBlank": true,
                "MultipleFilterList": [ { "Value": "example" } ]
              },
              "ColorFilter": {
                "FilterByFillColor": "FF0000",
                "Pattern": "Solid",
                "Color": {
                  "Color": { "A": 255, "R": 255, "G": 0, "B": 0 },
                  "ColorIndex": 3,
                  "IsShapeColor": false,
                  "ThemeColor": { "ColorType": "Accent1", "Tint": 0 },
                  "Type": "Rgb"
                },
                "ForegroundColorColor": null,
                "BackgroundColor": null
              },
              "CustomFilters": [ { "FilterOperatorType": "Equals", "Value1": "Example" } ],
              "DynamicFilter": { "DynamicFilterType": "Top10" },
              "IconFilter": { "IconId": 1, "IconSetType": "3Arrows" },
              "Top10Filter": { "Criteria": "Top", "IsPercent": true, "IsTop": true, "Items": 10 },
              "Visibledropdown": "true"
            }
          ],
          "Range": "A1:D100",
          "Sorter": {
            "CaseSensitive": false,
            "HasHeaders": true,
            "KeyList": [ { "Key": 0, "SortOrder": "Ascending", "CustomList": null } ],
            "SortLeftToRight": false
          }
        },
        "EvaluationOrder": 0,
        "FieldIndex": 0,
        "FilterType": "Value",
        "MeasureFldIndex": 0,
        "MemberPropertyFieldIndex": 0,
        "Name": "MyFilter",
        "Value1": "10",
        "Value2": "20"
      }' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## 클라우드 SDK 패밀리

SDK를 사용하면 Aspose.Cells Cloud를 개발하는 데 가장 빠른 방법입니다. SDK는 저수준 세부 사항을 처리해주므로 비즈니스 로직에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using System;
using System.Threading.Tasks;
using Aspose.Cells.Cloud.Sdk.Api;
using Aspose.Cells.Cloud.Sdk.Model;

public class PivotFilterExample
{
    public static async Task AddPivotFilterAsync()
    {
        // API 클라이언트 초기화(자신의 자격 증명으로 바꾸세요)
        var config = new Configuration
        {
            ClientId = "YOUR_CLIENT_ID",
            ClientSecret = "YOUR_CLIENT_SECRET"
        };
        var apiInstance = new CellsApi(config);

        // 필터 객체 생성
        var filter = new PivotFilter
        {
            AutoFilter = null,
            EvaluationOrder = 0,
            FieldIndex = 1,
            FilterType = "Count"
        };

        // 요청 준비
        var request = new PutWorksheetPivotTableFilterRequest(
            name: "Book1.xlsx",
            sheetName: "PivotSheet",
            pivotTableIndex: 0,
            filter: filter,
            needReCalculate: true,
            folder: "Temp",
            storageName: null);

        // 요청 실행
        var response = await apiInstance.PutWorksheetPivotTableFilterAsync(request);
        Console.WriteLine($"상태: {response.Status}");
    }
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "2a2aa16c2d9fd7e46b1b19f5fea5842b" >}}

{{< /tab >}}

{{< /tabs >}}

피벗 테이블과 관련된 추가 작업은 **추가**, **삭제**, **지우기** 필터 문서를 참조하세요.