---
title: "Excel 워크시트의 범위 데이터 정렬"
second_title: "Document"
linktitle: "정렬"
type: docs
url: /ko/worksheets/sort-data/
aliases: [  /ko/sort-worksheet-data/ ]
keywords: "Aspose.Cells Cloud, Excel 정렬 API, 워크시트 범위 정렬, REST API, dataSorter"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트의 특정 범위를 정렬합니다. 엔드포인트, 필수 매개변수, 인증 단계, 오류 처리 및 SDK 예제 포함."
weight: 20
---

REST API는 Excel 워크시트 내 지정된 범위의 데이터를 정렬합니다.

## REST API

```shell
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/sort
```

### 요청 매개변수

| 매개변수 이름 | 유형   | 위치 | 필수 | 설명                                                       |
| -------------- | ------ | -------- | -------- | ----------------------------------------------------------------- |
| name           | string | path     | Yes      | 워크북 이름.                                                |
| sheetName      | string | path     | Yes      | 워크시트 이름.                                               |
| cellArea       | string | query    | Yes      | 정렬할 셀 범위(예: `A5:A10`).                     |
| dataSorter     | object | body     | Yes      | 정렬 설정을 정의하는 JSON 객체(아래 스키마 참조). |
| folder         | string | query    | No       | 워크북이 위치한 폴더.                            |
| storageName    | string | query    | No       | 워크북이 위치한 스토리지 이름.            |

**`dataSorter` 객체 스키마** – 본문에는 다음 속성을 포함하는 JSON 객체가 포함되어야 합니다:

- `CaseSensitive` _(boolean, 필수)_ – 정렬 시 대/소문자를 구분할지 여부를 지정합니다.
- `HasHeaders` _(boolean, 필수)_ – 범위에 헤더 행이 포함되어 있는지 여부를 나타냅니다.
- `KeyList` _(array, 필수)_ – 정렬 키의 컬렉션입니다. 각 키 객체는 다음을 포함합니다:
  - `Key` _(integer)_ – 0부터 시작하는 열 인덱스.
  - `SortOrder` _(string)_ – `"ascending"` 또는 `"descending"`.
- `SortLeftToRight` _(boolean, 필수)_ – `true`인 경우, 좌에서 우로 정렬하고, 그렇지 않으면 위에서 아래로 정렬합니다.
- _(선택 사항)_ `CaseOrder`, `SortLeftToRight` 등은 OpenAPI 사양에 따라 추가로 제공될 수 있습니다.

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetRangeSort)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예제는 cURL을 사용해 클라우드 API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```shell
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/sort?cellArea=A5:A10" \
  -X POST \
  -d '{"CaseSensitive":false,"HasHeaders":false,"KeyList":[{"Key":0,"SortOrder":"descending"}],"SortLeftToRight":false}' \
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

**오류 처리** – API는 표준 HTTP 오류 코드를 반환할 수 있습니다. 일반적인 응답은 다음과 같습니다:

| HTTP 상태 코드 | 코드 | 메시지                                           |
| ----------- | ---- | ------------------------------------------------- |
| 400         | 400  | 잘못된 요청 – 누락되거나 잘못된 매개변수.      |
| 401         | 401  | 인증되지 않음 – 잘못되거나 누락된 JWT 토큰.       |
| 404         | 404  | 찾을 수 없음 – 워크북 또는 워크시트가 존재하지 않음. |
| 500         | 500  | 내부 서버 오류.                            |

오류 발생 시 응답 본문은 `{ "Code": <status>, "Message": "<description>", "Status": "Error" }` 형식을 따릅니다.

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 개발 속도를 극대화하는 가장 빠른 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPostWorksheetRangeSort.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-SortWorksheetData-sort-worksheet-data.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PostWorksheetRangeSort-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-sort_worksheet_range-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SortWorkSheetData.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-SortWorksheetData-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-SortWorksheetData-sort-worksheet-data.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-SortWorksheetData-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "48dd9dae5e2188a64e2284bb12b9201b" >}}

{{< /tab >}}

{{< /tabs >}}

---