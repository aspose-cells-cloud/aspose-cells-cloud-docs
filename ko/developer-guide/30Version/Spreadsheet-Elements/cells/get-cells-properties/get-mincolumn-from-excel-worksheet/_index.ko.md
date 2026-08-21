---
title: "Excel 워크시트에서 최소 열(MinColumn) 가져오기"
type: docs
url: /get-mincolumn-from-excel-worksheet/ko/
weight: 100
keywords: Excel, Aspose.Cells Cloud, REST API, MinColumn 가져오기, 워크시트, SDK, 클라우드 API
description: Aspose.Cells Cloud REST API를 통해 Excel 파일의 워크시트에서 데이터가 포함된 최소 열 인덱스를 검색합니다.
ArticleTitle: "Excel 워크시트에서 최소 열(MinColumn) 가져오기 - Aspose.Cells Cloud API"
---

이 REST API는 `cellOrMethodName` 매개변수를 `mincolumn`으로 설정하면 Excel 워크시트에서 데이터가 포함된 최소 열 인덱스를 반환합니다.

- **cURL 예제**

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/mincolumn" \
     -H "Authorization: Bearer <YOUR_ACCESS_TOKEN>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MinColumn": 2
}
```

{{< /tab >}}

{{< /tabs >}}

**요청 세부 정보**

| 매개변수 | 유형 | 필수 여부 | 설명 |
|----------|------|-----------|------|
| `cellOrMethodName` | string | 예 | 작업을 나타내기 위한 고정 값 `mincolumn`. |
| `folder` | string | 아니요 | 워크북이 포함된 폴더 경로(루트가 아닐 경우). |
| `storageName` | string | 아니요 | 사용할 Aspose Cloud 스토리지 이름. |

**응답 세부 정보**

API는 단일 속성을 가진 JSON 객체를 반환합니다:

```json
{
  "MinColumn": integer   // 데이터가 포함된 가장 왼쪽 열의 0부터 시작하는 인덱스.
}
```

일반적인 HTTP 상태 코드:

- **200 OK** – 요청 성공, `MinColumn` 값 반환.  
- **401 Unauthorized** – 인증 토큰 누락 또는 유효하지 않음.  
- **404 Not Found** – 지정된 워크북, 워크시트 또는 셀 범위가 존재하지 않음.  
- **500 Internal Server Error** – 예기치 않은 서버 오류.

- **Aspose.Cells Cloud SDK 사용**

SDK를 사용하는 것이 개발에 가장 효율적인 방법입니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 로직에 집중할 수 있도록 도와줍니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinColumnWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinColumnWorksheet-get-min-column-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinColumn.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_column.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinColumnFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinColumnWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinColumnWorksheet-get-min-column-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinColumnWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "108bf3803d41abd988a29cdbd39aee44" >}}

{{< /tab >}}

{{< /tabs >}}
---