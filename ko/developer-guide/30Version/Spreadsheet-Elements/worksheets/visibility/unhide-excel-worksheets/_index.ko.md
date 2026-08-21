---
title: "Excel 워크시트 숨김 해제"
second_title: "문서"
linktitle: "숨김 해제"
type: docs
url: /ko/worksheets/unhide/
aliases: [/unhide-excel-worksheets/]
keywords: "Aspose.Cells, 워크시트 숨김 해제, Excel API, 클라우드 스프레드시트, REST, 워크시트 표시 여부, Excel 워크북"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크북에서 워크시트의 숨김을 해제하는 방법을 배워보세요. 요청 세부 정보, cURL 예제, 여러 프로그래밍 언어의 SDK 코드 스니펫이 포함되어 있습니다."
weight: 60
---

이 REST API는 Excel 워크북에서 **워크시트 숨김을 해제하는** 엔드포인트를 제공합니다.

**사전 요구 사항**  
이 작업을 호출하기 전에 다음이 필요합니다:

* `Authorization` 헤더에 포함된 유효한 Aspose Cloud 액세스 토큰(JWT)  
* `folder` 및 `storageName` 쿼리 매개변수로 지정한 지원되는 저장소 위치에 저장된 워크북  
* 워크북은 Aspose.Cells에서 지원하는 형식(.xls, .xlsx, .xlsm 등)이어야 합니다  

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/visible
```

### **요청 매개변수**

| 매개변수 이름 | 유형      | 위치   | 설명                                      |
| ------------- | --------- | ------ | ----------------------------------------- |
| name          | string    | path   | 문서 이름                                 |
| sheetName     | string    | path   | 워크시트 이름                             |
| isVisible     | boolean   | query  | 워크시트 표시 여부 값 (`true`)            |
| folder        | string    | query  | 문서 폴더                                 |
| storageName   | string    | query  | 저장소 이름                               |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Worksheets/PutChangeVisibilityWorksheet)은 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 하는 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스를 쉽게 호출할 수 있습니다. 아래 예제는 cURL을 사용하여 요청을 만드는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/visible?isVisible=true" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt 토큰>"   # <jwt 토큰>을 실제 액세스 토큰으로 대체
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**가능한 응답 코드**

| HTTP 코드 | 의미                                      | 샘플 본문 (해당 시)                                          |
|-----------|-------------------------------------------|-------------------------------------------------------------|
| 200       | 워크시트 표시 여부가 성공적으로 업데이트됨 | `{ "Code": 200, "Status": "OK" }`                           |
| 400       | 잘못된 요청 – 누락 또는 잘못된 매개변수    | `{ "Code": 400, "Message": "Invalid request parameters." }` |
| 401       | 인증 실패 – 누락 또는 잘못된 JWT 토큰      | `{ "Code": 401, "Message": "Authentication failed." }`      |
| 404       | 없음 – 워크북 또는 워크시트가 존재하지 않음 | `{ "Code": 404, "Message": "File or worksheet not found." }` |
| 500       | 내부 서버 오류                            | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

{{< /tab >}}

{{< /tabs >}}

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 가장 빠른 개발 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Perl" tabName8="Android" tabName9="Objective C" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Worksheet-UnhideWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-UnhideWorksheet-unhide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PutChangeVisibilityWorksheet-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-change_worksheet_visibility-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UnhideExcelWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-UnhideWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-UnhideWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-UnhideWorksheet-unhide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "e30ac521e9cdb174baa702a743be16ae" >}}

{{< /tab >}}

{{< /tabs >}}