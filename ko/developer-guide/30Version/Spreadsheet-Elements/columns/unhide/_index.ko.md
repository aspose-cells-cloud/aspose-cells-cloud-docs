---
title: "Excel 워크시트에서 열 숨김 해제하기"
ArticleTitle: "Excel 워크시트에서 열 숨김 해제하기 - Aspose.Cells Cloud API"
second_title: "문서"
linktype: "docs"
url: /columns/unhide/
aliases:
  [/unhide-columns-in-an-excel-worksheet/, /unhide-columns-in-excel-worksheet/]
keywords: "Aspose.Cells, 클라우드 API, 열 숨김 해제, Excel, REST, SDK"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트에서 열의 숨김을 해제하는 방법을 알아보세요. 요청 세부 정보, cURL 예제, 여러 프로그래밍 언어의 SDK 코드 샘플을 포함합니다."
weight: 50
---

이 REST API는 워크시트 열의 숨김을 해제합니다.

**사전 조건** – Aspose.Cells Cloud의 모든 엔드포인트는 HTTPS와 유효한 OAuth 2.0 액세스 토큰을 필요로 합니다. 액세스 토큰을 발급받아 요청의 `Authorization` 헤더에 포함해야 합니다.

## PostUnhideWorksheetColumns API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/unhide
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 위해 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>을 요구합니다.

### 요청 매개변수

| 매개변수 이름 | 유형     | 위치   | 설명                                      |
| ------------- | -------- | ------ | ----------------------------------------- |
| name          | string   | path   | 워크북 이름.                               |
| sheetName     | string   | path   | 워크시트 이름.                             |
| startColumn   | integer  | query  | 처리할 첫 번째 열의 인덱스.                |
| totalColumns  | integer  | query  | 처리할 열의 개수.                          |
| width         | number   | query  | 원하는 열 폭 (기본값 = 50.0).              |
| folder        | string   | query  | 문서가 포함된 폴더.                        |
| storageName   | string   | query  | 스토리지 서비스의 이름.                    |

<a href="https://apireference.aspose.cloud/cells/#/Cells/PostUnhideWorksheetColumns" target="_blank" rel="noopener noreferrer">OpenAPI 명세서</a>는 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

**cURL** 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예제는 cURL을 사용해 클라우드 API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/unhide?startColumn=1&totalColumns=1&width=15" -H "accept: application/json"
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

**일반적인 HTTP 상태 코드**

| 코드 | 설명                                            |
|------|-------------------------------------------------|
| 200  | OK – 열의 숨김이 성공적으로 해제되었습니다.     |
| 400  | Bad Request – 잘못된 매개변수입니다.            |
| 401  | Unauthorized – 토큰이 누락되었거나 유효하지 않습니다. |
| 404  | Not Found – 워크북 또는 워크시트를 찾을 수 없습니다. |
| 500  | Internal Server Error – 예기치 않은 오류입니다.   |

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnhideWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnhideWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnhideWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnhideWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnhideWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnhideWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnhideWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnhideWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}