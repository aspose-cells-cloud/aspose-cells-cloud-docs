---
title: "범위에서 셀 병합 해제"
second_title: "문서"
linktitle: "병합 해제"
type: docs
url: /ko/ranges/unmerge/
aliases: [  /ko/unmerge-merged-cells-of-the-range/ ]
keywords: "Aspose.Cells Cloud, 셀 병합 해제, Excel API, 워크시트 범위, REST API"
description: "Aspose.Cells Cloud API를 사용하여 특정 워크시트 범위 내 병합된 셀을 해제하는 방법을 알아보세요. 엔드포인트, 매개변수, 샘플 cURL 및 C#, Java, Python 등 다양한 언어의 SDK 코드 스니펫이 포함됩니다."
weight: 20
---  

이 REST API는 Excel 워크시트의 지정된 범위 내 병합된 셀을 해제합니다.

## REST API  

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/unmerge
```  

요청 파라미터는 다음과 같습니다:

| 파라미터 이름 | 타입   | 위치 | 필수 여부 | 설명                                   |
|---------------|--------|------|-----------|----------------------------------------|
| name          | string | path | Yes       | 워크북 이름.                           |
| sheetName     | string | path | Yes       | 워크시트 이름.                         |
| range         | object | body | Yes       | 해제할 셀을 정의하는 범위 객체입니다.     |
| folder        | string | query| No        | 워크북이 포함된 폴더입니다.             |
| storageName   | string | query| No        | 스토리지 이름.                          |

[OpenAPI 사양서](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeUnmerge)는 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용해 클라우드 API로 요청하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청(Request)" tabName2="응답(Response)" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/unmerge" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
    "ColumnCount": 7,
    "ColumnWidth": 19,
    "FirstColumn": 0,
    "FirstRow": 9,
    "Name": "string",
    "RefersTo": "string",
    "RowCount": 1,
    "RowHeight": 15,
    "Worksheet": "Sheet1"
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

## 클라우드 SDK 패밀리  

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리하므로, 여러분은 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeUnMerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeUnMerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeUnMerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeUnMerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeUnMerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeUnMerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeUnMerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeUnMerge.go" >}}

{{< /tab >}}

{{< /tabs >}}