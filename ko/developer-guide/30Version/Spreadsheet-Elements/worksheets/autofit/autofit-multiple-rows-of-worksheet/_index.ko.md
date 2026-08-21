---
title: "Excel 워크시트에서 여러 행 자동 맞춤"
second_title: "문서"
linktitle: "행"
type: docs
url: /ko/worksheets/autofit/rows/
aliases: [  /ko/autofit-multiple-rows-of-worksheet/ ]
keywords: "행 자동 맞춤, Excel, Aspose.Cells Cloud, REST API, 워크시트, 스프레드시트"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트에서 여러 행을 자동 맞춤하는 방법을 배웁니다. 요청 구문, 매개변수, cURL 예제, SDK 스니펫, 오류 처리를 포함합니다."
weight: 40
ArticleTitle: "Excel 워크시트에서 여러 행 자동 맞춤 – Aspose.Cells Cloud API 문서"
---

이 REST API는 Excel 워크시트의 행 높이를 자동으로 조정합니다.

## 보안 및 인증
Aspose.Cells Cloud API는 안전하며 [JWT 토큰 기반 인증](https://docs.aspose.cloud/ko/total/getting-started/rest-api-overview/authenticating-api-requests/)이 필요합니다.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitrows
```

### **요청 매개변수**

| 매개변수 이름          | 유형     | 위치   | 설명                                                                                                                              | 필수 여부 |
| --------------------- | ------- | ------ | --------------------------------------------------------------------------------------------------------------------------------- | -------- |
| **name**              | string  | path   | Excel 파일의 이름.                                                                                                                | ✔ |
| **sheetName**         | string  | path   | 워크시트의 이름.                                                                                                                  | ✔ |
| **autoFitterOptions** | object  | body   | 행 자동 맞춤 방식을 제어하는 옵션(예: 숨겨진 행 무시). 아래 필드 설명 참조.                                                         | ✖ |
| **startRow**          | integer | query  | 자동 맞춤할 첫 번째 행(1부터 시작하는 인덱스).                                                                                     | ✔ |
| **endRow**            | integer | query  | 자동 맞춤할 마지막 행(포함).                                                                                                      | ✔ |
| **onlyAuto**          | boolean | query  | `true`인 경우, API는 Excel에서 자동으로 계산된 높이를 가진 행만 조정합니다. `false`인 경우 전체 자동 맞춤이 수행됩니다.           | ✖ |
| **folder**            | string  | query  | 문서가 포함된 폴더.                                                                                                               | ✖ |
| **storageName**       | string  | query  | 스토리지 서비스의 이름.                                                                                                           | ✖ |

**autoFitterOptions** 필드(모두 선택 사항):

- `AutoFitMergedCells` _(boolean)_ – `true`인 경우, 병합된 셀을 행 높이 계산 시 고려합니다.
- `IgnoreHidden` _(boolean)_ – `true`인 경우, 자동 맞춤 과정에서 숨겨진 행을 무시합니다.
- `OnlyAuto` _(boolean)_ – 쿼리 매개변수 `onlyAuto`와 동일한 기능을 수행하며, 설정 시 쿼리 값보다 우선합니다.

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetRows)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitrows?startRow=1&endRow=7" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt 토큰>" \
  -d '{"AutoFitMergedCells": true, "IgnoreHidden": true, "OnlyAuto": false}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

일반적인 오류 응답은 다음과 같습니다:

- **400 Bad Request** – 유효하지 않은 매개변수 값 또는 잘못된 형식의 JSON 본문.
- **401 Unauthorized** – 누락되었거나 유효하지 않은 JWT 토큰.
- **404 Not Found** – 지정된 파일 또는 워크시트가 존재하지 않음.
- **500 Internal Server Error** – 예기치 않은 서버 오류 발생.

**HTTP 상태 코드**

| 코드 | 의미                        | 설명                                               |
|------|-----------------------------|----------------------------------------------------|
| 200  | OK                          | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함. |
| 400  | Bad Request                 | 누락되거나 유효하지 않은 매개변수(예: 지원되지 않는 파일 형식). |
| 401  | Unauthorized                | 유효하지 않거나 누락된 JWT 토큰. |
| 413  | Payload Too Large           | 업로드된 파일이 크기 제한을 초과함. |
| 500  | Internal Server Error       | 예기치 않은 서버 오류. |

{{< /tab >}}

{{< /tabs >}}

## 클라우드 SDK 패밀리
SDK를 사용하면 가장 빠르게 개발할 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}
---