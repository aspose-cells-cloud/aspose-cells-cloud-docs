---
title: "수직 페이지 나누기 추가"
second_title: "문서"
linktitle: "수직 페이지 나누기 추가"
type: docs
url: /page-breaks/add-vertical-page-break/
aliases: [/insert-vertical-page-break-inside-worksheet/]
keywords: "Aspose.Cells Cloud, 수직 페이지 나누기, REST API, Excel, SDK, cURL"
description: "Aspose.Cells Cloud REST API(v3.0)를 사용하여 Excel 워크시트에 수직 페이지 나누기를 삽입하는 방법을 배워보세요. 요청 구문, cURL 예제, SDK 샘플, 인증 가이드, 오류 처리 세부 정보가 포함됩니다."
weight: 40
ArticleTitle: "수직 페이지 나누기 추가 – Aspose.Cells Cloud API"
---

이 REST API는 워크시트에 수직 페이지 나누기를 삽입합니다.

## 보안 및 인증
Aspose.Cells Cloud API는 [JWT 토큰 기반 인증](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)이 필요합니다.

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks
```

### 요청 매개변수

| 매개변수 이름 | 유형    | 위치 | 설명                                                             |
| ------------- | ------- | ---- | ----------------------------------------------------------------- |
| name          | string  | path | Excel 워크북의 이름입니다.                                         |
| sheetName     | string  | path | 페이지 나누기가 추가될 워크시트의 이름입니다.                     |
| cellname      | string  | query | 페이지 나누기 위치를 정의하는 셀 참조(예: **A1**)입니다.          |
| column        | integer | query | 페이지 나누기가 시작되는 열의 0부터 시작하는 인덱스입니다.         |
| row           | integer | query | 페이지 나누기가 시작되는 행의 0부터 시작하는 인덱스입니다.         |
| startRow      | integer | query | 페이지 나누기 범위의 첫 번째 행입니다.                             |
| endRow        | integer | query | 페이지 나누기 범위의 마지막 행입니다.                              |
| folder        | string  | query | 워크북이 위치한 스토리지의 폴더 경로입니다.                        |
| storageName   | string  | query | 스토리지 서비스의 이름입니다.                                      |

**필수 매개변수** – `cellname` 또는 `column` 중 하나를 반드시 제공해야 합니다. `column`을 사용할 경우 `row`, `startRow`, `endRow`를 추가로 제공하여 범위를 정의할 수 있습니다. 나머지 필드는 모두 선택 사항입니다.

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/PageBreaks/PutVerticalPageBreak)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

### cURL 예제

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/SampleBreaks.xlsx/worksheets/Sheet1/verticalpagebreaks?column=9" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

#### 응답

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**HTTP 상태 코드**

| 코드 | 의미                  | 설명                                              |
|------|-----------------------|---------------------------------------------------|
| 200  | OK                    | 필터가 성공적으로 적용되었으며, 응답에 작업 세부 정보가 포함됩니다. |
| 400  | 잘못된 요청           | 누락되었거나 유효하지 않은 매개변수(예: 지원되지 않는 파일 유형)입니다. |
| 401  | 인증되지 않음         | 유효하지 않거나 누락된 JWT 토큰입니다.              |
| 413  | 페이로드가 너무 큼    | 업로드된 파일이 크기 제한을 초과했습니다.           |
| 500  | 내부 서버 오류        | 예기치 않은 서버 오류가 발생했습니다.               |

## 클라우드 SDK 패밀리

SDK를 사용하면 개발 속도를 가장 빠르게 향상시킬 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 호출을 수행하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutVerticalPageBreak.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutVerticalPageBreak.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutVerticalPageBreak.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutVerticalPageBreak.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutVerticalPageBreak.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutVerticalPageBreak.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutVerticalPageBreak.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutVerticalPageBreak.go" >}}

{{< /tab >}}

{{< /tabs >}}