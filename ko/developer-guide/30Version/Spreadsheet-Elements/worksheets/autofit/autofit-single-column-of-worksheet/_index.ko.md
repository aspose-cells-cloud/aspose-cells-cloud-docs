---
title: "Aspose.Cells Cloud API로 Excel에서 열 자동 맞춤 – 빠른 가이드"
second_title: "문서"
linktitle: "열"
type: docs
url: /worksheets/autofit/column/
aliases: [/autofit-single-column-of-worksheet/]
keywords: "Aspose.Cells Cloud, 열 자동 맞춤, Excel API, REST API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트에서 열(또는 열 범위)을 자동으로 크기 조정하는 방법을 알아보세요. cURL 및 SDK 예제(C#, Java, Python 등)와 전체 요청/응답 세부 정보 포함."
weight: 10
---

이 REST API는 Excel 워크시트에서 단일 열 또는 연속된 열 범위의 너비를 자동으로 조정합니다.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitcolumns
```

### 요청 매개변수

| 매개변수 이름        | 유형     | 위치   | 설명                                                                                   |
| ------------------- | -------- | ------ | -------------------------------------------------------------------------------------- |
| name                | string   | path   | Excel 파일의 이름입니다.                                                               |
| sheetName           | string   | path   | 워크시트의 이름입니다.                                                                 |
| firstColumn         | integer  | query  | 자동 맞춤할 첫 번째 열의 0부터 시작하는 인덱스입니다.                                  |
| lastColumn          | integer  | query  | 자동 맞춤할 마지막 열의 0부터 시작하는 인덱스입니다.                                   |
| autoFitterOptions   | object   | body   | 자동 맞춤 동작을 제어하는 옵션(자세한 내용은 [AutoFitterOptions](/cells/auto-filter-options) 참조) |
| firstRow            | integer  | query  | 열 너비 계산 시 고려할 첫 번째 행의 0부터 시작하는 인덱스입니다.                        |
| lastRow             | integer  | query  | 열 너비 계산 시 고려할 마지막 행의 0부터 시작하는 인덱스입니다.                         |
| folder            | string   | query  | 파일이 위치한 스토리지 폴더입니다.                                                     |
| storageName         | string   | query  | 스토리지 서비스의 이름입니다.                                                          |

### 오류 응답

| HTTP 상태 코드 | 의미                                     | 예시 JSON 본문                                             |
| -------------- | ---------------------------------------- | ---------------------------------------------------------- |
| 400            | 잘못된 매개변수                            | `{"Code":400,"Message":"Invalid parameter 'firstColumn'."}` |
| 401            | 인증 실패 – JWT 토큰 누락 또는 유효하지 않음 | `{"Code":401,"Message":"Authorization failed."}`            |
| 404            | 파일 또는 워크시트를 찾을 수 없음          | `{"Code":404,"Message":"Worksheet 'Sheet1' not found."}`    |
| 500            | 내부 서버 오류                            | `{"Code":500,"Message":"An unexpected error occurred."}`    |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetColumns)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

**cURL** 명령줄 도구를 사용하여 Aspose.Cells Cloud 서비스를 호출할 수 있습니다. 아래 예제는 열 자동 맞춤 엔드포인트를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitcolumns?firstColumn=2&lastColumn=2" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"AutoFitMergedCells": true, "IgnoreHidden": true, "OnlyAuto": true}'
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

## 클라우드 SDK 패밀리

SDK를 사용하면 API를 애플리케이션에 통합하는 데 가장 빠른 방법입니다. SDK는 저수준 세부 사항을 처리하므로 비즈니스 로직에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용하여 열 자동 맞춤 엔드포인트를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}