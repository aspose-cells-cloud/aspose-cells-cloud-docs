---
title: "Excel 워크시트에서 MinDataRow 가져오기"
type: docs
url: /ko/get-mindatarow-from-excel-worksheet/
weight: 90
keywords: "Aspose Cells, MinDataRow, Excel API, 클라우드 SDK"
description: "Aspose.Cells 클라우드 API v3.0을 사용하여 워크시트의 최소 데이터 행 인덱스를 검색합니다. 요청 패턴, 매개변수, 샘플 cURL, 응답 예시, 상태 코드 및 SDK 스니펫이 포함됩니다."
ArticleTitle: "Excel 워크시트에서 MinDataRow 가져오기 – Aspose.Cells 클라우드 API"
---

**Aspose.Cells Cloud API v3.0**의 **Get MinDataRow** 엔드포인트는 지정된 워크시트에서 데이터가 포함된 첫 번째 행의 인덱스를 반환합니다. 이 작업을 수행하려면 유효한 액세스 토큰(Bearer 인증)과 쿼리 매개변수 `cellOrMethodName`을 `mindatarow`로 설정해야 합니다.

**API 버전: 3.0**

### cURL 예제

요청은 HTTP GET 메서드를 사용합니다. `{fileName}`과 `{sheetName}` 플레이스홀더를 실제 워크북 및 워크시트 이름으로 대체하세요.

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/cells/mindatarow?cellOrMethodName=mindatarow" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

**요청 매개변수**

| 매개변수           | 위치 | 유형   | 필수 여부 | 설명                                              |
|--------------------|------|--------|-----------|---------------------------------------------------|
| `fileName`         | 경로 | string | 예        | Excel 워크북 이름(확장자 포함).                   |
| `sheetName`        | 경로 | string | 예        | 워크북 내 워크시트 이름.                           |
| `cellOrMethodName` | 쿼리 | string | 예        | 이 작업을 호출하려면 `mindatarow`로 설정해야 함.   |

**응답 예시**

```json
{
  "MinDataRow": 5
}
```

**HTTP 상태 코드**

| 코드 | 의미                      | 설명                                                |
|------|---------------------------|-----------------------------------------------------|
| 200  | OK                        | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함. |
| 400  | Bad Request               | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식). |
| 401  | Unauthorized              | 잘못되거나 누락된 JWT 토큰.                          |
| 413  | Payload Too Large         | 업로드된 파일이 크기 제한을 초과함.                  |
| 500  | Internal Server Error     | 예기치 않은 서버 오류.                               |

### SDK 예제

SDK를 사용하면 개발 속도가 가장 빠릅니다. SDK는 저수준 세부 정보를 처리하므로 프로젝트 로직에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinDataRowWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinDataRowWorksheet-get-min-data-row.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinDataRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_data_row.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinDataRowFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinDataRowWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinDataRowWorksheet-get-min-data-row.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinDataRowWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "85f2a886ba296b8abf640c0638b4eec1" >}}

{{< /tab >}}

{{< /tabs >}}

**참고 자료**

- [Get MaxDataRow](https://docs.aspose.cloud/cells/get-maxdatarow-from-excel-worksheet/)
- [Get MinColumn](https://docs.aspose.cloud/cells/get-mincolumn-from-excel-worksheet/)
- [Get MaxColumn](https://docs.aspose.cloud/cells/get-maxcolumn-from-excel-worksheet/)