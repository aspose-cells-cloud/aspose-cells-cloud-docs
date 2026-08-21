---
title: "엑셀 워크시트에서 최대 행 번호(MaxRow) 가져오기"
type: docs
url: /get-maxrow-from-excel-worksheet/
weight: 40
ArticleTitle: "엑셀 워크시트에서 최대 행 번호 검색 – Aspose.Cells Cloud API"
keywords: "Aspose.Cells, 엑셀, MaxRow, REST API, 클라우드 SDK, 스프레드시트, 워크시트, GetMaxRow"
description: "Aspose.Cells Cloud REST API를 사용하여 엑셀 파일 내 워크시트의 최대 행 번호를 검색하는 방법을 알아보세요. 요청 구문, 응답 스키마, SDK 예제 및 사용 참고 사항이 포함되어 있습니다."
---

이 REST API는 `cellOrMethodName` 매개변수를 `maxrow`로 설정하면 엑셀 워크시트의 **최대 행 번호**를 반환합니다.

- **cURL 예제**

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/maxrow" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MaxRow": 1048576
}
```

{{< /tab >}}

{{< /tabs >}}

- **Aspose.Cells Cloud SDK 사용하기**

SDK를 사용하면 개발 속도를 가장 효율적으로 높일 수 있습니다. SDK는 저수준 세부 사항을 처리하므로, 프로젝트의 로직에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMaxRowWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMaxRowWorksheet-get-max-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMaxRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_max_row.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMaxRowFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMaxRowWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMaxRowWorksheet-get-max-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMaxRowWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "afcfd72b172e9c3e2d283a9ac059c8c7" >}}

{{< /tab >}}

{{< /tabs >}}

**API 참조**

| 항목 | 세부 정보 |
|------|---------|
| **메서드** | `GET` |
| **엔드포인트** | `/cells/{fileName}/worksheets/{sheetName}/cells/maxrow` |
| **경로 매개변수** | `fileName` – 엑셀 파일 이름 (필수) <br> `sheetName` – 워크시트 이름 (필수) |
| **쿼리 매개변수** | `folder` – 저장소 내 폴더 경로 (선택 사항) <br> `storageName` – 저장소 이름 (선택 사항) |
| **성공 응답** | `200 OK` <br> ```json { "MaxRow": 정수 } ``` |
| **오류 응답** | `400 Bad Request` – 잘못된 매개변수 <br> `401 Unauthorized` – 인증 실패 <br> `404 Not Found` – 파일 또는 워크시트를 찾을 수 없음 |

**사전 요구 사항**

- 유효한 Aspose Cloud 인증 토큰
- 대상 워크북은 Aspose Cloud 저장소에 업로드되었거나 공개 URL을 통해 접근 가능해야 함

**참고 사항**

- 이 작업은 API 버전 **v3.0** 이상에서 사용 가능합니다.  
- 반환되는 `MaxRow` 값은 사용된 가장 높은 행 인덱스(1부터 시작)를 나타냅니다. 빈 워크시트의 경우 일반적으로 `1`이 반환됩니다.  

다음 SDK 예제는 다양한 프로그래밍 언어에서 이 작업을 호출하는 방법을 보여줍니다.  
---