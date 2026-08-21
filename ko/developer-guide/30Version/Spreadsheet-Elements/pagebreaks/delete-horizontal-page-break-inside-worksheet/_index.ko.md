---
title: "가로 페이지 나누기 삭제"
ArticleTitle: "Aspose.Cells Cloud – 가로 페이지 나누기 삭제 (REST API)"
second_title: "문서"
linktitle: "가로 페이지 나누기 삭제"
type: docs
url: /page-breaks/delete-horizontal-page-break/
aliases: [/delete-horizontal-page-break-inside-worksheet/]
keywords: "Aspose.Cells Cloud, 가로 페이지 나누기 삭제, Excel 워크시트, REST API, SDK"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트에서 가로 페이지 나누기를 삭제합니다. C#, Java, PHP, Ruby, Node.js, Python, Perl, Go용 SDK를 제공합니다."
weight: 50
---

이 REST API는 **가로** 페이지 나누기를 삭제합니다.

**필수 조건**: 이 엔드포인트를 호출하려면 유효한 Aspose Cloud JWT 액세스 토큰이 필요합니다. [인증 가이드](https://docs.aspose.cloud/cells/authentication/)를 따라 토큰을 획득하세요.

## DeleteHorizontalPageBreak API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks/{index}
```

*모든 API 호출은 **HTTPS**를 통해 이루어져야 합니다.*

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 위해 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>을 요구합니다.

### 요청 매개변수

| 매개변수 이름 | 유형    | 위치 | 설명                                                  |
| ------------- | ------- | ---- | ----------------------------------------------------- |
| `name`        | string  | path | Excel 파일(워크북)의 이름입니다.                       |
| `sheetName`   | string  | path | 페이지 나누기가 포함된 워크시트의 이름입니다.         |
| `index`       | integer | path | 삭제할 가로 페이지 나누기의 0부터 시작하는 인덱스입니다. |
| `folder`      | string  | query | 파일이 위치한 저장소의 선택적 폴더 경로입니다.        |
| `storageName` | string  | query | 선택적 저장소 서비스 이름입니다.                       |

### 오류 응답

| HTTP 코드 | 설명                                                                |
| --------- | ------------------------------------------------------------------- |
| 401       | 인증 실패 – 토큰이 누락되었거나 유효하지 않습니다.                   |
| 404       | 찾을 수 없음 – 지정된 파일, 워크시트 또는 페이지 나누기 인덱스가 존재하지 않습니다. |
| 400       | 잘못된 요청 – 요청 구문이 잘못되었거나 매개변수가 유효하지 않습니다.  |
| 500       | 내부 서버 오류 – 예기치 않은 조건이 발생했습니다.                   |

**참고:**  
- [가로 페이지 나누기 추가](/page-breaks/add-horizontal-page-break/)  
- [가로 페이지 나누기 가져오기](/page-breaks/get-horizontal-page-breaks/)  
- [세로 페이지 나누기 삭제](/page-breaks/delete-vertical-page-break/)

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/PageBreaks/DeleteHorizontalPageBreak)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

**cURL** 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/horizontalpagebreaks/0" \
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

**응답 스키마**

| 필드     | 유형    | 설명                                    |
|---------|---------|-------------------------------------------|
| Code    | integer | HTTP 상태 코드(예: 200).                   |
| Status  | string  | 텍스트 상태 메시지(예: "OK").             |
| Message | string  | 선택적 오류 상황에 대한 추가 정보입니다. |

{{< /tab >}}

{{< /tabs >}}

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리해주므로, 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteHorizontalPageBreak.cs" >}}
*예제가 로드되지 않으면 [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/8a5b324fdf3e574dbd747c1a1e24b05d)에서 확인하세요.*

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteHorizontalPageBreak.java" >}}
*예제가 로드되지 않으면 [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/c59aa5c02f735466a5e34751cee73f5f)에서 확인하세요.*

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteHorizontalPageBreak.php" >}}
*예제가 로드되지 않으면 [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/84283c8ba766ed815f47e6dfb0891152)에서 확인하세요.*

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteHorizontalPageBreak.rb" >}}
*예제가 로드되지 않으면 [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/36ed8b8727561b92692939513d365fca)에서 확인하세요.*

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteHorizontalPageBreak.ts" >}}
*예제가 로드되지 않으면 [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/e82de2e4189bc27ae92abf73c36b4df0)에서 확인하세요.*

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteHorizontalPageBreak.py" >}}
*예제가 로드되지 않으면 [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/61e922de11e6e7144db88adcad6501c1)에서 확인하세요.*

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteHorizontalPageBreak.pl" >}}
*예제가 로드되지 않으면 [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/f82a3a00251e34ff8766116282c8c9ca)에서 확인하세요.*

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteHorizontalPageBreak.go" >}}
*예제가 로드되지 않으면 [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/2b824d4e13644368d12682856aa49185)에서 확인하세요.*

{{< /tab >}}

{{< /tabs >}}