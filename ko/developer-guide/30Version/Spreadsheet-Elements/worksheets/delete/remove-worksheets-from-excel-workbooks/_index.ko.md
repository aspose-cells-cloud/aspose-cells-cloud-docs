---
title: "워크시트 삭제"
second_title: "문서"
linktype: "워크시트 하나"
type: docs
url: /ko/worksheets/delete-worksheet/
aliases: [  /ko/remove-worksheets-from-excel-workbooks/ ]
keywords: "Aspose.Cells Cloud, 워크시트 삭제, Excel, 스프레드시트, REST API"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크북에서 워크시트를 삭제합니다. C#, Java, PHP, Ruby, Node.js, Python, Perl, Go 및 cURL용 SDK를 지원합니다."
weight: 20
ArticleTitle: "워크시트 삭제 – Aspose.Cells Cloud API"
---

이 REST API는 워크시트를 삭제합니다.  
사전 조건: 이 API를 호출하려면 **Authorization** 헤더에 유효한 JWT 인증 토큰을 제공해야 하며, 워크북이 위치한 저장소 위치에 접근 권한이 있어야 합니다.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

*참고: 이 API는 현재 안정적인 버전인 **v3.0**을 사용합니다. 향후 버전 변경 사항은 릴리스 노트에서 공지됩니다.*

### **요청 매개변수**

| 매개변수 이름 | 유형   | 위치 | 설명              |
| ------------- | ------ | ---- | ----------------- |
| name          | string | path | 문서 이름.        |
| sheetName     | string | path | 워크시트 이름.    |
| folder        | string | query| 문서가 위치한 폴더.|
| storageName   | string | query| 저장소 이름.      |

가능한 HTTP 응답 코드:

| 상태 코드 | 설명                                 |
| --------- | ------------------------------------ |
| 200 OK    | 워크시트가 성공적으로 삭제되었습니다. |
| 400 Bad Request | 잘못된 요청 매개변수입니다.         |
| 401 Unauthorized | 인증에 실패했거나 토큰이 누락되었습니다. |
| 404 Not Found | 지정된 워크북 또는 워크시트가 존재하지 않습니다. |
| 500 Internal Server Error | 예기치 않은 서버 오류입니다. |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheet)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API로 요청하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet3" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

*모든 요청은 HTTPS를 통해 이루어져야 하며, API는 비 TLS 연결을 지원하지 않습니다.*

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

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스로 요청을 수행하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}