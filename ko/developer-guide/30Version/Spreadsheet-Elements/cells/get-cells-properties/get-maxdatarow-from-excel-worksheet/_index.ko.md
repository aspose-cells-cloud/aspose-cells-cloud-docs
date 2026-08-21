---
title: "엑셀 워크시트에서 MaxDataRow 가져오기"
type: docs
url: /ko/get-maxdatarow-from-excel-worksheet/
weight: 50
keywords: "엑셀, Aspose.Cells Cloud, REST API, MaxDataRow 가져오기, 워크시트"
description: "Aspose.Cells Cloud REST API를 사용하여 엑셀 워크북의 지정된 워크시트에서 데이터가 포함된 마지막 행의 인덱스를 검색합니다."
ArticleTitle: "Aspose.Cells Cloud API – 엑셀 워크시트에서 MaxDataRow 가져오기"
---

이 REST API는 `cellOrMethodName` 매개변수를 `maxdatarow`로 설정할 경우, 엑셀 파일 내에서 최대 데이터 행 인덱스를 반환합니다.

- **cURL 예제**

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/maxdatarow" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

*참고: 요청은 **HTTPS**를 통해 전송되어야 하며, 유효한 OAuth2 베어러 토큰을 포함해야 합니다.*

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MaxDataRow": 57
}
```

**가능한 HTTP 상태 코드**

| 코드 | 설명 |
|------|-------------|
| 200 | 성공 – 최대 데이터 행 인덱스를 반환합니다. |
| 401 | 인증되지 않음 – 잘못되었거나 누락된 인증 토큰입니다. |
| 403 | 접근 거부 – 워크북에 접근할 수 있는 권한이 부족합니다. |
| 404 | 찾을 수 없음 – 지정된 워크북 또는 워크시트가 존재하지 않습니다. |
| 500 | 내부 서버 오류 – 예기치 않은 서버 조건입니다. |

{{< /tab >}}

{{< /tabs >}}


- **Aspose.Cells Cloud SDK 사용하기**

SDK를 사용하는 것이 개발 속도를 높이는 가장 효율적인 방법입니다. SDK는 저수준 세부 사항을 처리해주므로, 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인해 주세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMaxDataRowWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMaxDataRowWorksheet-get-max-data-row.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMaxDataRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_max_data_row.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMaxDataRowFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMaxDataRowWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMaxDataRowWorksheet-get-max-data-row.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMaxDataRowWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "7b834250a25feb5b8a30500cf62cf7a9" >}}

{{< /tab >}}

{{< /tabs >}}

**참고 자료**

- <a href="https://docs.aspose.cloud/cells/get-maxrow-from-excel-worksheet/" target="_blank" rel="noopener noreferrer">엑셀 워크시트에서 MaxRow 가져오기</a>  
- <a href="https://docs.aspose.cloud/cells/get-maxcolumn-from-excel-worksheet/" target="_blank" rel="noopener noreferrer">엑셀 워크시트에서 MaxColumn 가져오기</a>  
- <a href="https://docs.aspose.cloud/cells/get-mindatarow-from-excel-worksheet/" target="_blank" rel="noopener noreferrer">엑셀 워크시트에서 MinDataRow 가져오기</a>

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebAPI",
  "name": "Aspose.Cells Cloud Get MaxDataRow",
  "description": "지정된 워크시트에서 데이터가 포함된 마지막 행의 인덱스를 반환합니다.",
  "url": "https://api.aspose.com/v3.0/cells/{fileName}/worksheets/{sheetName}/cells/maxdatarow",
  "method": "GET",
  "documentation": "https://docs.aspose.cloud/cells/get-maxdatarow-from-excel-worksheet/",
  "input": [
    {
      "name": "fileName",
      "valueRequired": true,
      "description": "엑셀 워크북의 이름입니다."
    },
    {
      "name": "sheetName",
      "valueRequired": true,
      "description": "워크시트의 이름입니다."
    }
  ],
  "output": {
    "@type": "DataType",
    "name": "MaxDataRow",
    "description": "데이터가 포함된 마지막 행의 0부터 시작하는 인덱스입니다."
  }
}
</script>

*최종 업데이트: 2026-07-30*