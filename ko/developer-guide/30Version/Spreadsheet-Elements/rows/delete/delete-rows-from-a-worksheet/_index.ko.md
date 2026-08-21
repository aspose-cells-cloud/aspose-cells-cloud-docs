---
title: "Excel 워크시트에서 여러 행 삭제"
second_title: "문서"
linktitle: "행"
type: docs
url: /rows/delete/rows/
keywords: "Aspose.Cells Cloud, 행 삭제, 여러 행 삭제, Excel 워크시트, REST API, SDK"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트에서 하나 이상의 행을 삭제하는 방법을 알아보세요. 엔드포인트 세부 정보, 매개변수, cURL 예제 및 다양한 언어에 대한 SDK 코드 예제가 포함되어 있습니다."
weight: 80
ArticleTitle: "Aspose.Cells Cloud API를 사용하여 Excel 워크시트에서 여러 행 삭제"
---

이 REST API는 Excel 워크시트에서 **여러 행을 삭제**합니다.

**필수 조건:** 이 엔드포인트를 호출하려면 Aspose Cloud 인증을 통해 획득한 유효한 JWT 액세스 토큰과 워크북에 대한 적절한 저장소 권한이 있어야 합니다.

## DeleteWorksheetRows API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows
```

### **보안 및 인증**

Aspose.Cells Cloud API는 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요하며, 보안이 강화되어 있습니다.

### **요청 매개변수**

| 매개변수 이름   | 유형    | 경로 / 쿼리 문자열 / HTTP 본문 | 설명                                                                 |
| --------------- | ------- | ------------------------------- | -------------------------------------------------------------------- |
| name            | string  | path                            | 워크북 이름.                                                         |
| sheetName       | string  | path                            | 워크시트 이름.                                                       |
| startrow        | integer | query                           | 삭제할 첫 번째 행의 0부터 시작하는 인덱스(예: `0` = 첫 번째 행).     |
| totalRows       | integer | query                           | 삭제할 행 수.                                                        |
| updateReference | boolean | query                           | 삭제 후 참조를 업데이트할지 여부(`true`/`false`).                   |
| folder          | string  | query                           | 문서 폴더.                                                           |
| storageName     | string  | query                           | 저장소 이름.                                                         |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Cells/DeleteWorksheetRows)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API에 요청하는 방법을 보여줍니다. **모든 엔드포인트는 HTTPS를 사용해야 하며, HTTP는 더 이상 지원되지 않습니다.**

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=1&updateReference=true" \
-X DELETE \
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

**가능한 응답 코드**

| HTTP 상태 코드 | 설명                                     |
|-------------|------------------------------------------|
| 200         | 행이 성공적으로 삭제되었습니다.           |
| 400         | 잘못된 요청 – 잘못된 매개변수.            |
| 401         | 인증되지 않음 – 누락되거나 유효하지 않은 JWT 토큰. |
| 404         | 없음 – 워크북 또는 워크시트가 존재하지 않습니다.  |
| 500         | 내부 서버 오류 – 예기치 않은 조건.          |

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 요청을 보내는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}
---