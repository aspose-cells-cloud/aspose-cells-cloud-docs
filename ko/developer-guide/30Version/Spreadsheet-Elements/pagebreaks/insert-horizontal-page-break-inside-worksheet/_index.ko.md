---
title: "가로 페이지 나누기 추가"
second_title: "문서"
linktitle: "가로 페이지 나누기 추가"
type: docs
url: /ko/page-breaks/add-horizontal-page-break/
aliases: [  /ko/insert-horizontal-page-break-inside-worksheet/ ]
keywords: "가로 페이지 나누기, Aspose.Cells Cloud, Excel API, REST, SDK, 워크시트, cURL"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트에 가로 페이지 나누기를 추가하는 방법을 배워보세요. 요청 세부 정보, cURL 예제, 여러 프로그래밍 언어의 SDK 코드 스니펫이 포함되어 있습니다."
weight: 30
ArticleTitle: "가로 페이지 나누기 추가 – Aspose.Cells Cloud API"
---

**가로 페이지 나누기 추가** API는 Excel 워크시트에 가로 페이지 나누기를 삽입합니다.

**사전 요구 사항 및 인증**  
Aspose.Cells Cloud API에 대한 모든 호출에는 유효한 JWT 토큰이 필요합니다. 인증 가이드에 설명된 OAuth 2.0 워크플로를 통해 토큰을 획득하고 요청 헤더에 `Authorization: Bearer <jwt token>` 형태로 포함해야 합니다. 대상 워크북은 API가 접근 가능한 저장소 위치(기본 저장소 또는 지정한 사용자 정의 `storageName`)에 있어야 합니다.

## PutHorizontalPageBreak API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 강화되어 있으며 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름 | 유형    | 위치 | 설명                                                               |
| ------------- | ------- | ---- | ------------------------------------------------------------------ |
| name          | string  | path | Excel 파일 이름.                                                   |
| sheetName     | string  | path | 나누기를 추가할 워크시트 이름.                                     |
| cellname      | string  | query | 페이지 나누기 시작 지점을 나타내는 셀 참조(예: **A1**).            |
| row           | integer | query | 페이지 나누기의 0부터 시작하는 행 인덱스.                          |
| column        | integer | query | 페이지 나누기의 0부터 시작하는 열 인덱스.                          |
| startColumn   | integer | query | 나누기 삽입 시 범위의 시작 열.                                     |
| endColumn     | integer | query | 나누기 삽입 시 범위의 끝 열.                                       |
| folder        | string  | query | Excel 파일이 포함된 폴더 경로.                                     |
| storageName   | string  | query | Aspose Cloud 저장소 이름.                                          |

<a href="https://apireference.aspose.cloud/cells/#/PageBreaks/PutHorizontalPageBreak" target="_blank" rel="noopener noreferrer">OpenAPI 사양</a>은 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 공개적으로 접근 가능한 인터페이스를 정의합니다.

**cURL** 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL로 API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
# 암호화된 통신을 위해 HTTPS 사용
curl -v "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/horizontalpagebreaks?row=18" \
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

JWT 토큰이 누락되었거나 유효하지 않을 때의 오류 응답 예시:

```json
{
  "Code": 401,
  "Status": "Unauthorized",
  "Message": "Invalid or missing JWT token."
}
```

**HTTP 상태 코드**

| 코드 | 의미                         | 설명                                              |
|------|------------------------------|---------------------------------------------------|
| 200  | OK                           | 필터가 성공적으로 적용됨; 응답에는 작업 세부 정보 포함. |
| 400  | Bad Request                  | 누락되었거나 잘못된 매개변수(예: 지원되지 않는 파일 유형). |
| 401  | Unauthorized                 | 유효하지 않거나 누락된 JWT 토큰.                    |
| 413  | Payload Too Large            | 업로드된 파일이 크기 제한을 초과함.                 |
| 500  | Internal Server Error        | 예기치 않은 서버 오류.                              |

관련 작업에 대한 자세한 내용은 **[가로 페이지 나누기 가져오기](../get-horizontal-page-breaks/)** 및 **[가로 페이지 나누기 삭제](../delete-horizontal-page-break/)** API 페이지를 참조하세요.

## 클라우드 SDK Family

SDK를 사용하는 것이 가장 빠른 개발 방법입니다. SDK는 저수준 세부 정보를 추상화하여 프로젝트에 집중할 수 있게 해줍니다. Aspose.Cells Cloud SDK 전체 목록은 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutHorizontalPageBreak.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutHorizontalPageBreak.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutHorizontalPageBreak.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutHorizontalPageBreak.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutHorizontalPageBreak.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutHorizontalPageBreak.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutHorizontalPageBreak.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutHorizontalPageBreak.go" >}}
{{< /tab >}}

{{< /tabs >}}