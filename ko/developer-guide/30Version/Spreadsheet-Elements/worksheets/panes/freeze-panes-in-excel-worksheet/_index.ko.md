---
title: "Excel 워크시트에서 창 고정"
second_title: "문서"
linktitle: "고정"
type: docs
url: /ko/worksheets/panes/freeze/
aliases: [  /ko/freeze-panes-in-excel-worksheet/ , /ko/worksheets/freeze-panes/ ]
keywords: "Aspose.Cells Cloud, 창 고정, Excel, REST API, 워크시트"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트에서 행 및 열을 고정하는 방법을 알아봅니다. 엔드포인트 구문, 필요한 매개변수, cURL 예제, 인증 가이드, 오류 응답 세부 정보, 여러 언어의 SDK 코드 예제가 포함됩니다."
weight: 190
---

이 REST API는 **Excel 워크시트에 창 고정**을 설정합니다.

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/freezepanes
```

요청 매개변수는 다음과 같습니다:

| 매개변수 이름   | 유형    | 위치   | 설명                                          |
| -------------- | ------- | ------ | --------------------------------------------- |
| name           | string  | path   | 워크북 파일의 이름입니다.                     |
| sheetName      | string  | path   | 창을 고정할 워크시트의 이름입니다.            |
| row            | integer | query  | **고정되지 않은** 첫 번째 행의 0부터 시작하는 인덱스입니다. |
| column         | integer | query  | **고정되지 않은** 첫 번째 열의 0부터 시작하는 인덱스입니다. |
| frozenRows     | integer | query  | 상단에서부터 고정할 행 수입니다.              |
| frozenColumns  | integer | query  | 왼쪽에서부터 고정할 열 수입니다.              |
| folder         | string  | query  | 워크북이 위치한 저장소의 폴더 경로입니다.     |
| storageName    | string  | query  | 저장소 서비스의 이름입니다.                   |

[OpenAPI 스펙](https://apireference.aspose.cloud/cells/#/Worksheets/PutWorksheetFreezePanes)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청(Request)" tabName2="응답(Response)" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/freezepanes?row=1&column=1&frozenRows=1&frozenColumns=1" \
-X PUT \
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

### 오류 응답

| HTTP 상태 코드            | 코드 | 메시지                            | 예시                                                     |
| ------------------------- | ---- | --------------------------------- | -------------------------------------------------------- |
| 400 Bad Request           | 400  | 잘못된 매개변수                   | `{ "Code": 400, "Message": "Invalid frozenRows value" }` |
| 401 Unauthorized          | 401  | JWT 토큰 누락 또는 유효하지 않음   | `{ "Code": 401, "Message": "Invalid access token" }`     |
| 404 Not Found             | 404  | 워크북 또는 워크시트를 찾을 수 없음 | `{ "Code": 404, "Message": "File not found" }`           |
| 500 Internal Server Error | 500  | 예기치 않은 서버 오류             | `{ "Code": 500, "Message": "Internal server error" }`    |

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 요청을 보내는 방법을 보여줍니다:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Objective C" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPutWorksheetFreezePanes.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-FreezePanes-freeze-panes.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PutWorksheetFreezePanes-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-set_freeze_panes-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-FreezePanes-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-FreezePanes-freeze-panes.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-FreezePanes-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "099a22da7db4d5602c0da3b90bc1dc30" >}}

{{< /tab >}}

{{< /tabs >}}