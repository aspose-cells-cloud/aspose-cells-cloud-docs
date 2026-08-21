---
title: "Excel 워크시트에 여러 행 추가"
ArticleTitle: "Aspose.Cells Cloud API를 사용하여 Excel 워크시트에 여러 행 추가"
second_title: "문서"
linktype: "docs"
url: /ko/rows/add/rows/
keywords: "Aspose.Cells Cloud, 행 삽입, Excel 워크시트, REST API, SDK, 여러 행 추가"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트에 여러 행을 삽입하는 방법을 배워보세요. 이 가이드는 엔드포인트, 요청 매개변수, 샘플 cURL 명령 및 SDK 사용 예제를 다룹니다."
weight: 20
---

이 REST API는 Excel 워크시트에 여러 개의 새 행을 추가합니다.

## PutInsertWorksheetRows API

```http
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows
```

### **보안 및 인증**

Aspose.Cells Cloud API는 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>을 요구합니다.

### **요청 매개변수**

| 매개변수 이름     | 유형      | 위치   | 설명                                                                   |
| ---------------- | --------- | ------ | ---------------------------------------------------------------------- |
| name             | string    | path   | 워크북 이름.                                                            |
| sheetName        | string    | path   | 워크시트 이름.                                                          |
| startrow         | integer   | query  | 삽입할 첫 번째 행의 인덱스 (**0부터 시작**).                            |
| totalRows        | integer   | query  | 삽입할 행 수.                                                            |
| updateReference  | boolean   | query  | 삽입 후 셀 참조를 업데이트할지 여부 (`true` 또는 `false`).              |
| folder           | string    | query  | 문서가 포함된 폴더.                                                     |
| storageName      | string    | query  | 스토리지 이름.                                                          |

**사전 조건**  
이 작업을 호출하기 전에 지정된 스토리지(또는 폴더)에 워크북이 이미 존재해야 합니다.

**인증**  
API는 유효한 JWT 토큰을 요구합니다. 아래 cURL 예제에 표시된 대로 `Authorization` 헤더에 토큰을 포함하세요.

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Cells/PutInsertWorksheetRows)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=11&updateReference=true" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **참고:** 이 `PUT` 작업은 요청 본문을 필요로 하지 않습니다. 클라이언트 라이브러리가 요청 페이로드를 강제하는 경우 빈 JSON 객체(`{}`)를 전송할 수 있습니다.

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*가능한 응답 코드*  

- **200 OK** – 행이 성공적으로 삽입되었습니다.  
- **400 Bad Request** – 잘못된 매개변수(예: 음수 행 인덱스).  
- **401 Unauthorized** – JWT 토큰 누락 또는 유효하지 않은 토큰.  
- **404 Not Found** – 지정된 워크북 또는 워크시트가 존재하지 않음.  
- **500 Internal Server Error** – 예기치 않은 서버 오류.

{{< /tab >}}

{{< /tabs >}}

행에 대한 추가 작업은 관련 페이지인 **행 삭제**, **행 조회**, **행 복사**를 참조하세요.

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 개발을 가장 빠르게 진행할 수 있는 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutInsertWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutInsertWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutInsertWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutInsertWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PutInsertWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutInsertWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutInsertWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutInsertWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}