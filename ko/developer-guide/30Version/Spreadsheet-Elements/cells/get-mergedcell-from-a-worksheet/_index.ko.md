---
title: "Excel 워크시트에서 병합 셀 가져오기 – Aspose.Cells Cloud API"
type: docs
url: /ko/get-mergedcell-from-a-worksheet/
weight: 60
keywords: "Aspose.Cells Cloud, 병합 셀, Excel 워크시트, REST API, Aspose.Cells SDK, Excel 병합 셀"
description: "Aspose.Cells Cloud API(v3.0)를 사용하여 Excel 워크시트에서 병합 셀 범위를 가져오는 방법을 알아보세요. 인증 절차, 전체 cURL 요청, 응답 스키마, 오류 처리, C#, Java, Python 등 다양한 언어의 SDK 예제를 포함합니다."
---

이 REST API는 Excel 워크시트의 **병합 셀**에 대한 정보를 반환합니다.

> **참고** – API 객체 이름은 **MergedCell**(단수형)입니다. 본문에서는 병합 셀이라는 *개념*(복수형)을 다룹니다.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/mergedCells
```

## 보안 및 인증

Aspose.Cells Cloud API는 [JWT 토큰 기반 인증](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)이 필요하며, 안전하게 설계되었습니다.

### 요청 매개변수

| 매개변수 이름 | 유형   | 위치 | 설명                             |
|--------------|--------|------|----------------------------------|
| **name**     | string | path | Excel 파일 이름.                 |
| **sheetName**| string | path | 워크시트 이름.                   |
| **folder**   | string | query| 문서가 포함된 폴더.              |
| **storageName**| string | query| 사용할 스토리지 이름.           |

## **응답**

MergedCellsResponse를 반환합니다.

```json
{
  "Status":"OK",
  "Code":200,
  "MergedCells":{
    "Count": 0,
    "MergedCellList":[
      {
        "Link":{
          "Href":"",
          "Rel":"",
          "Type":"",
          "Title":""
        }
      }
    ]
  }
}
```

**HTTP 상태 코드**

| 코드 | 의미                        | 설명                                             |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK                          | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함. |
| 400 | 잘못된 요청                    | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형). |
| 401 | 인증되지 않음                  | 잘못되거나 누락된 JWT 토큰. |
| 413 | 페이로드가 너무 큼              | 업로드된 파일이 크기 제한을 초과함. |
| 500 | 내부 서버 오류                 | 예기치 않은 서버 오류. |

## SDK를 사용하여 GetWorksheetMergedCells API 사용하는 방법

### GetWorksheetMergedCells API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetMergedCells)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예제는 cURL을 사용하여 Cloud API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/mergedCells" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MergedCells": {
    "Count": 1,
    "MergedCells": [
      {
      "link": {
            "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/cells/mergedcells/0",
            "Rel": "self"
          }
      }
    ]    
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}


### Aspose.Cells Cloud SDK 사용

SDK를 사용하는 것이 API에 가장 빠르게 개발할 수 있는 방법입니다. SDK가 저수준 세부 사항을 처리하므로 비즈니스 로직에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetMergedCells.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetMergedCells.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetMergedCells.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetMergedCells.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetMergedCells.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetMergedCells.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetMergedCells.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetMergedCells.go" >}}

{{< /tab >}}

{{< /tabs >}}