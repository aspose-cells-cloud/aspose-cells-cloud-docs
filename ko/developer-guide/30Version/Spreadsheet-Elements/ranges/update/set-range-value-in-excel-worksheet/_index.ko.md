---
title: "Excel 워크시트에서 범위 값 설정"
second_title: "문서"
linktitle: "값 설정"
type: docs
url: /ranges/update/values/
aliases: [/set-range-value-in-excel-worksheet/]
keywords: "Aspose.Cells, Excel API, 범위 값 설정, REST API, 클라우드 SDK, 워크시트 업데이트"
description: "Aspose.Cells Cloud REST API(v3.0)를 사용하여 Excel 워크북에서 셀 또는 범위의 값을 설정하는 방법을 알아보세요. 엔드포인트, 매개변수, cURL 예제, SDK 코드 예제 및 오류 처리가 포함됩니다."
weight: 72
ArticleTitle: "Excel 워크시트에서 범위 값 설정 – Aspose.Cells Cloud API"
---

이 REST API를 사용하여 지정된 범위에 값을 설정합니다. 적절한 경우, 값은 다른 데이터 유형으로 변환되며 셀의 숫자 서식이 재설정됩니다.

**사전 요구 사항**  
- 유효한 Aspose Cloud 계정  
- `Cells.ReadWrite` 범위를 포함하는 JWT 토큰  
- 워크북이 이미 대상 스토리지 위치에 업로드되어 있어야 함  

## PostWorksheetCellsRangeValue API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/value
```

요청 매개변수는 다음과 같습니다:

| 매개변수 이름 | 유형    | 위치 | 설명                                                |
|---------------|---------|------|-------------------------------------------------------|
| name          | string  | path | 워크북 이름                                           |
| sheetName     | string  | path | 워크시트 이름                                         |
| value         | string  | query| 입력 값                                               |
| range         | object  | body | 워크시트 내 범위 객체                                 |
| isConverted   | boolean | query| 입력 값을 변환할지 여부를 나타냅니다                  |
| setStyle      | boolean | query| 대상 셀에 스타일을 적용할지 여부를 나타냅니다         |
| folder        | string  | query| 워크북 폴더                                           |
| storageName   | string  | query| 스토리지 이름                                         |

**요청 본문에 전송할 수 있는 `range` 객체 예제:**

```json
{
  "range": {
    "FirstRow": 0,
    "FirstColumn": 0,
    "RowCount": 1,
    "ColumnCount": 1
  }
}
```

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeValue)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API를 호출하는 방법을 보여줍니다. **`Authorization` 헤더에 유효한 JWT 토큰을 포함해야 합니다.**

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/value?value=25&isConverted=false&setStyle=false" \
  -X POST \
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

**응답 스키마**

| 필드     | 유형    | 설명                                              |
|---------|---------|---------------------------------------------------|
| Code    | integer | 작업의 HTTP 상태 코드                            |
| Status  | string  | 결과에 대한 간단한 설명 (예: "OK")               |
| Message | string  | 요청 실패 시 상세 오류 메시지 (선택 사항)        |
| Result  | object  | 성공적인 호출 시 반환되는 추가 데이터 (선택 사항)|

**가능한 HTTP 상태 코드**

- **200 OK** – 범위 값이 성공적으로 설정됨  
- **400 Bad Request** – 잘못된 매개변수 또는 잘못된 형식의 요청 본문  
- **401 Unauthorized** – 누락되었거나 유효하지 않은 JWT 토큰  
- **403 Forbidden** – 요청된 작업에 대한 충분한 권한 없음  
- **404 Not Found** – 지정된 워크북, 워크시트 또는 범위가 존재하지 않음  
- **500 Internal Server Error** – 예기치 않은 서버 오류  

*400 Bad Request의 예시 오류 응답:*

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "필수 필드가 누락된 'range' 객체입니다."
}
```

## 클라우드 SDK Family

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-SetRangeValueWorksheet-1.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-SetRangeValueWorksheet-1.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-PostSetCellRangeValue-.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-set_cell_range_value-.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-SetRangeValueWorksheet-1.js" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SetRangeValueInExcelWorksheet.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-SetRangeValueWorksheet-1.pl" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "7dc9243752ac8a0e5d9c0f211a029cd9" >}}
{{< /tab >}}

{{< /tabs >}}