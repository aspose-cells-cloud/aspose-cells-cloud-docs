---
title: "Excel 파일에서 페이지 수 가져오기"
second_title: "문서"
linktitle: "페이지"
type: docs
url: /get-page-count-from-an-excel-file/
aliases: [/workbook/page-count/, /workbook/get/page-count/]
keywords: "Aspose.Cells, 클라우드 API, Excel 페이지 수, 워크북 페이지 매김"
description: "Aspose.Cells Cloud REST API(v3.0)를 사용하여 Excel 워크북의 인쇄 가능한 총 페이지 수를 조회합니다. 요청 형식, 필수 매개변수, cURL 예제, 응답 스키마, 오류 처리, 여러 언어에 대한 SDK 스니펫이 포함됩니다."
weight: 10
version: "v3.0"
ArticleTitle: "Aspose.Cells Cloud API를 사용하여 Excel 파일에서 페이지 수 가져오기"
---

이 REST API는 워크북의 **페이지 수**를 반환합니다.

## 보안 및 인증
Aspose.Cells Cloud API는 [JWT 토큰 기반 인증](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)이 필요합니다.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/pagecount
```

### 요청 매개변수

| 매개변수 이름 | 유형   | 위치 | 필수 여부 | 설명                           |
| ------------- | ------ | ---- | --------- | ------------------------------ |
| name          | string | path | Yes       | Excel 문서의 이름입니다.       |
| folder        | string | query| No        | 문서가 포함된 폴더입니다.      |
| storageName   | string | query| No        | 사용할 스토리지의 이름입니다.  |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Workbook/GetPageCount)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells REST API에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 엔드포인트를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/YourFile.xlsx/pagecount" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

*`YourFile.xlsx`를 조회하려는 워크북의 실제 파일 이름으로 바꾸세요.*

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
13
```

{{< /tab >}}

{{< /tabs >}}

### 응답 스키마

| HTTP 상태 코드 | 데이터 유형 | 설명                                    |
| -------------- | ----------- | --------------------------------------- |
| 200            | integer     | 워크북의 인쇄 가능한 총 페이지 수(예: `13`). |
| 4xx‑5xx        | JSON        | 오류 객체(참조: _오류 처리_ 섹션).        |

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetPageCount.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetPageCount.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetPageCount.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetPageCount.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82deb2e4189bc27ae92abf73c36b4df0" "Example_GetPageCount.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetPageCount.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetPageCount.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetPageCount.go" >}}

{{< /tab >}}

{{< /tabs >}}

## 오류 처리

| HTTP 상태 코드 | 설명                                 | 예시 JSON 본문                                                                            |
| -------------- | ------------------------------------ | ----------------------------------------------------------------------------------------- |
| 401            | 유효하지 않거나 누락된 JWT 토큰입니다. | `{ "Code": "InvalidAuthenticationToken", "Message": "액세스 토큰이 누락되었거나 유효하지 않습니다." }` |
| 404            | 지정된 워크북을 찾을 수 없습니다.    | `{ "Code": "FileNotFound", "Message": "요청한 파일이 존재하지 않습니다." }`                |
| 400            | 잘못된 요청 – 필수 매개변수 누락.    | `{ "Code": "BadRequest", "Message": "필수 매개변수 'name'이 누락되었습니다." }`           |
| 500            | 내부 서버 오류입니다.                | `{ "Code": "InternalError", "Message": "예기치 않은 오류가 발생했습니다." }`              |