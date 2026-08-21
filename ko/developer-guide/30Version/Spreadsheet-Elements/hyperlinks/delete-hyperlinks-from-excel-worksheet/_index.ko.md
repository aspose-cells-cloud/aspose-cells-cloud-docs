---
title: "하이퍼링크 지우기"
type: docs
url: /hyperlinks/clear/
aliases: [/add-hyperlinks-to-excel-worksheet/]
keywords: "Aspose.Cells Cloud, Excel, 하이퍼링크 지우기, 하이퍼링크 삭제, REST API, 워크시트, SDK"
description: "Aspose.Cells Cloud REST API 또는 지원되는 SDK(C#, Java, Python, Node.js, Go, PHP, Ruby, Perl 등)를 사용하여 Excel 워크시트에서 모든 하이퍼링크를 제거하는 방법을 알아보세요."
weight: 40
ArticleTitle: "하이퍼링크 지우기 – Aspose.Cells Cloud API 문서"
---

이 REST API는 Excel 워크시트의 **모든 하이퍼링크**를 삭제합니다.

## 보안 및 인증
Aspose.Cells Cloud API는 안전하며, [JWT 토큰 기반 인증](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)이 필요합니다.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks
```

### 요청 매개변수

| 매개변수 이름 | 유형   | 위치   | 설명                                 |
| -------------- | ------ | ------ | ------------------------------------ |
| name           | string | path   | Excel 파일의 이름입니다.             |
| sheetName      | string | path   | 워크시트의 이름입니다.               |
| folder         | string | query  | 문서가 포함된 폴더입니다.            |
| storageName    | string | query  | 스토리지 서비스 이름입니다.          |

### 오류 응답

| HTTP 코드 | 이유                                               | 예시 본문                                                           |
| --------- | -------------------------------------------------- | ------------------------------------------------------------------- |
| **400**   | 잘못된 요청 – 누락되거나 유효하지 않은 매개변수.   | `{ "Code":"400", "Message":"Invalid parameter value." }`            |
| **401**   | 인증되지 않음 – 누락되거나 유효하지 않은 JWT 토큰. | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**   | 찾을 수 없음 – 워크북 또는 워크시트가 존재하지 않음. | `{ "Code":"404", "Message":"File not found." }`                     |
| **500**   | 내부 서버 오류 – 예기치 않은 서버 장애.             | `{ "Code":"500", "Message":"An unexpected error occurred." }`       |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Hyperlinks/DeleteWorksheetHyperlinks)은 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의합니다.

**cURL** 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스를 호출할 수 있습니다. 아래 예제는 워크시트에서 모든 하이퍼링크를 삭제하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test1.xlsx/worksheets/Sheet1/hyperlinks" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## 클라우드 SDK 패밀리
SDK를 사용하면 저수준 세부 사항을 처리해 주므로 개발 속도가 빨라집니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 방문하세요.

다음 코드 예제는 다양한 SDK를 사용하여 워크시트 하이퍼링크를 삭제하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetHyperlinks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetHyperlinks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetHyperlinks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetHyperlinks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetHyperlinks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetHyperlinks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetHyperlinks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetHyperlinks.go" >}}

{{< /tab >}}

{{< /tabs >}}
---