---
title: "Aspose.Cells Cloud API – 셀 범위 병합"
second_title: "문서"
linktitle: "병합"
type: docs
url: /ko/ranges/merge/
aliases: [  /ko/combines-a-range-of-cells-into-a-single-cell/ ]
keywords: "Aspose.Cells, 셀 병합, Excel API, REST, 클라우드 SDK"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트의 셀 범위를 단일 셀로 병합합니다. C#, Java, Python 등 다양한 언어에 대한 요청 형식, 매개변수 및 SDK 예제를 확인하세요."
weight: 20
---

이 REST API는 Excel 워크시트에서 셀 범위를 단일 셀로 병합합니다.

**개요** – 범위 병합은 선택한 셀을 하나의 셀로 결합하며, 상단 왼쪽 셀의 값을 보존하고 나머지 셀 값은 버립니다. 여러 열 또는 행에 걸친 헤더를 만들거나 워크시트 레이아웃을 간소화해야 할 때 이 작업을 사용하세요.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/merge
```

### **요청 매개변수**

| 매개변수 이름   | 유형   | 위치   | 설명                                           |
| --------------- | ------ | ------ | ---------------------------------------------- |
| **name**        | string | path   | 워크북 이름.                                   |
| **sheetName**   | string | path   | 워크시트 이름.                                 |
| **range**       | object | body   | 병합할 셀을 지정하는 Range 객체.               |
| **folder**      | string | query  | 워크북이 저장된 폴더.                          |
| **storageName** | string | query  | 스토리지 이름.                                 |

#### 요청 본문 스키마

**Range** 객체는 다음 필드를 반드시 포함해야 합니다(기타 필드는 선택 사항입니다):

| 속성            | 유형    | 필수 여부 | 설명                                              |
| --------------- | ------- | --------- | ------------------------------------------------- |
| **FirstRow**    | integer | Yes       | 범위 내 첫 번째 행의 0 기반 인덱스.               |
| **FirstColumn** | integer | Yes       | 범위 내 첫 번째 열의 0 기반 인덱스.               |
| **RowCount**    | integer | Yes       | 범위에 포함할 행 수.                              |
| **ColumnCount** | integer | Yes       | 범위에 포함할 열 수.                              |
| **Name**        | string  | No        | 범위의 선택적 이름.                               |
| **RefersTo**    | string  | No        | 범위가 참조하는 수식.                             |
| **Worksheet**   | string  | No        | 워크시트 이름(경로 매개변수와 다른 경우).         |
| **RowHeight**   | number  | No        | 범위 내 행의 높이(픽셀 단위).                     |
| **ColumnWidth** | number  | No        | 범위 내 열의 너비(픽셀 단위).                     |

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/merge" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "FirstRow": 9,
        "FirstColumn": 0,
        "RowCount": 1,
        "ColumnCount": 7
      }'
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

#### 응답 세부 정보

| HTTP 상태 코드                | 설명                                              | 샘플 JSON                                              |
| ----------------------------- | ------------------------------------------------- | ------------------------------------------------------ |
| **200 OK**                    | 범위가 성공적으로 병합되었습니다.                 | `{ "Code": 200, "Status": "OK" }`                      |
| **400 Bad Request**           | 잘못된 범위 매개변수(예: 범위를 벗어난 인덱스).    | `{ "Code": 400, "Message": "Invalid range." }`         |
| **401 Unauthorized**          | 누락되거나 잘못된 JWT 토큰.                       | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404 Not Found**             | 워크북 또는 워크시트를 찾을 수 없습니다.         | `{ "Code": 404, "Message": "Resource not found." }`    |
| **500 Internal Server Error** | 예기치 않은 서버 오류.                            | `{ "Code": 500, "Message": "Internal server error." }` |

## 클라우드 SDK Family

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeMerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeMerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeMerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeMerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeMerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeMerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeMerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeMerge.go" >}}

{{< /tab >}}

{{< /tabs >}}