---
title: "Excel 워크시트에서 행 자동 맞춤"
second_title: "문서"
linktitle: "행"
type: docs
url: /ko/worksheets/autofit/row/
aliases: [  /ko/autofit-single-row-of-worksheet/ ]
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트에서 행을 자동 맞추는 방법을 배워보세요. 엔드포인트, 매개변수, 인증, 오류 처리, cURL 요청 및 SDK 예제가 포함됩니다."
keywords: "행 자동 맞춤, Aspose.Cells Cloud, Excel API, REST, 워크시트, SDK, 스프레드시트, 클라우드 API"
weight: 30
ArticleTitle: "Aspose.Cells Cloud API를 사용한 Excel 워크시트에서 행 자동 맞춤"
---

이 REST API는 Excel 워크시트에서 **행을 자동 맞춥니다**.

## 보안 및 인증
Aspose.Cells Cloud API는 보안이 보장되며 [JWT 토큰 기반 인증](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)이 필요합니다.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitrow
```

### **요청 매개변수**

| 매개변수 이름       | 유형     | 위치   | 설명                                                                                                                                                                                              |
| ------------------- | -------- | ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name                | string   | path   | Excel 파일 이름.                                                                                                                                                                                  |
| sheetName           | string   | path   | 워크시트 이름.                                                                                                                                                                                    |
| rowIndex            | integer  | query  | 자동 맞춤할 행의 0부터 시작하는 인덱스.                                                                                                                                                           |
| firstColumn         | integer  | query  | 작업에 포함되는 첫 번째 열의 인덱스.                                                                                                                                                              |
| lastColumn          | integer  | query  | 작업에 포함되는 마지막 열의 인덱스.                                                                                                                                                               |
| autoFitterOptions   | object   | body   | 자동 맞춤 동작을 제어하는 개체(예: 병합된 셀 고려 여부, 텍스트 줄 바꿈 등). 자세한 내용은 [AutoFitterOptions](/cells/auto-fitter-options){:rel="noopener" title="자동 맞춤 동작 제어"} 참조. |
| folder              | string   | query  | 파일이 저장된 폴더.                                                                                                                                                                               |
| storageName         | string   | query  | 스토리지 이름.                                                                                                                                                                                    |

**예시 `autoFitterOptions` JSON 본문**

```json
{
  "IsMergedCells": true,
  "IsWrapped": false,
  "AutoFitMergedCells": true,
  "AutoFitWrappedCells": false
}
```

### 엔티티 정의

| 엔티티                | 설명                                                                                   |
| --------------------- | -------------------------------------------------------------------------------------- |
| `rowIndex`            | 대상 행의 0부터 시작하는 인덱스.                                                       |
| `firstColumn`         | 자동 맞춤 작업의 시작 열.                                                              |
| `lastColumn`          | 자동 맞춤 작업의 종료 열.                                                              |
| `autoFitterOptions`   | 행 자동 맞춤 방식에 영향을 주는 선택적 설정(병합된 셀, 텍스트 줄 바꿈 등).             |

[OpenAPI 사양](/cells/#/Worksheets/PostAutofitWorksheetRow)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예제는 cURL을 사용하여 API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitrow?rowIndex=2&firstColumn=1&lastColumn=10" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

| 필드   | 설명                                             |
| ------ | ------------------------------------------------ |
| Code   | `200` – 요청이 성공했습니다.                     |
| Status | `"OK"` – 행이 성공적으로 자동 맞춰졌습니다.      |

{{< /tab >}}

{{< /tabs >}}

## 오류 처리

API는 표준 HTTP 상태 코드를 반환합니다. 이 엔드포인트의 일반적인 오류 응답은 다음과 같습니다:

| HTTP 코드 | 예시 페이로드                                              | 의미                                                                           |
| --------- | ---------------------------------------------------------- | ------------------------------------------------------------------------------ |
| 400       | `{ "Code": 400, "Message": "Row index out of range." }`   | 제공된 `rowIndex`가 워크시트에 존재하지 않습니다.                               |
| 401       | `{ "Code": 401, "Message": "Invalid or expired token." }` | 인증 실패 – JWT 토큰을 확인하고 요청이 HTTPS를 통해 이루어졌는지 확인하세요.   |
| 404       | `{ "Code": 404, "Message": "File not found." }`           | 지정된 Excel 파일 또는 워크시트를 찾을 수 없습니다.                           |
| 500       | `{ "Code": 500, "Message": "Internal server error." }`    | 예기치 않은 서버 측 문제가 발생했습니다.                                       |

## 클라우드 SDK 패밀리

SDK를 사용하면 개발 속도가 가장 빠릅니다. SDK는 저수준 세부 사항을 추상화하여 비즈니스 로직에 집중할 수 있게 해줍니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud){:rel="noopener noreferrer"}를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetRow.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetRow.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetRow.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetRow.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2c4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetRow.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetRow.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetRow.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetRow.go" >}}
{{< /tab >}}

{{< /tabs >}}

**참고:** [열 자동 맞춤](/worksheets/autofit/column/), [여러 행 자동 맞춤](/worksheets/autofit/rows/), [AutoFitterOptions](/cells/auto-fitter-options)도 참조하세요.