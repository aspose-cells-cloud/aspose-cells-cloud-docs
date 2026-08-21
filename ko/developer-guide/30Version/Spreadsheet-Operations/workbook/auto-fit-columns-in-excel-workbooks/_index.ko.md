---
title: "Excel 파일의 열 자동 맞춤"
second_title: "문서"
linktitle: "열"
type: docs
url: /ko/autofit-columns-on-an-excel-file/
aliases:
  [
    /auto-fit-columns-in-excel-workbooks,
    /autofit-columns-in-excel-workbooks/,
    /columns/autofit/,
    /workbook/autofit/columns/,
  ]
keywords: "열 자동 맞춤, Excel, Aspose.Cells Cloud, REST API, SDK, cURL, API"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크북에서 열을 자동 맞추는 방법을 배워보세요. 요청 세부 정보, cURL 예제, 여러 언어의 SDK 코드 예제가 포함되어 있습니다."
weight: 90
---

이 REST API는 Excel 워크북의 열 자동 맞춤을 지원합니다.

## PostAutofitWorkbookColumns API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/autofitcolumns
```

요청 매개변수는 다음과 같습니다:

| 매개변수 이름        | 유형    | 위치   | 설명                                              |
| -------------------- | ------- | ------ | ------------------------------------------------- |
| **name**             | string  | path   | 워크북 파일의 이름입니다.                         |
| **autoFitterOptions**| object  | body   | 자동 맞춤 동작을 제어하는 옵션입니다.             |
| **startColumn**      | integer | query  | 자동 맞춤할 첫 번째 열의 0부터 시작하는 인덱스입니다. |
| **endColumn**        | integer | query  | 자동 맞춤할 마지막 열의 0부터 시작하는 인덱스입니다. |
| **folder**           | string  | query  | 워크북이 포함된 폴더입니다.                       |
| **storageName**      | string  | query  | 스토리지 서비스의 이름입니다.                     |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Workbook/PostAutofitWorkbookColumns){:rel="noopener noreferrer"}은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/autofitcolumns" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt 토큰>" \
-d '{"AutoFitMergedCells":true, "IgnoreHidden":true}'
```

> **참고:** 프로덕션 환경에서는 항상 HTTPS 엔드포인트를 사용하고 JWT 토큰을 비밀로 유지하세요.

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

### 사전 조건
이 작업을 호출하기 전에 유효한 Aspose Cloud API 키, 생성된 JWT 토큰, 그리고 대상 워크북이 지정된 스토리지 위치에 이미 존재하는지 확인해야 합니다.

**HTTP 상태 코드**

| 코드 | 의미                      | 설명                                            |
|------|---------------------------|-------------------------------------------------|
| 200  | 성공                      | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함 |
| 400  | 잘못된 요청               | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형) |
| 401  | 인증되지 않음             | 잘못되거나 누락된 JWT 토큰                        |
| 413  | 페이로드가 너무 큼        | 업로드된 파일이 크기 제한을 초과함                |
| 500  | 내부 서버 오류            | 예기치 않은 서버 오류                             |

API는 다음과 같은 HTTP 상태 코드를 반환할 수 있습니다:

| 코드 | 설명                             |
|------|----------------------------------|
| 200  | 성공 – 열이 자동 맞춤됨          |
| 400  | 잘못된 요청 – 누락되거나 잘못된 매개변수 |
| 401  | 인증되지 않음 – 잘못되거나 만료된 JWT |
| 500  | 서버 오류 – 내부 처리 실패        |

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 개발 속도를 높이는 가장 효율적인 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 로직에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud){:rel="noopener noreferrer"}를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorkbookColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorkbookColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorkbookColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorkbookColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorkbookColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorkbookColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorkbookColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorkbookColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}