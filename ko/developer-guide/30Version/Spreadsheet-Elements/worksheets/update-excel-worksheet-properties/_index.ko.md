---
title: "워크시트 속성 업데이트 – Aspose.Cells Cloud API 참조 (v3.0)"
second_title: "문서"
linktitle: "업데이트"
type: docs
url: /ko/worksheets/update-properties/
aliases: [  /ko/update-excel-worksheet-properties/ ]
weight: 20
keywords:
  [
    "Aspose.Cells",
    "Excel",
    "워크시트",
    "속성 업데이트",
    "REST API",
    "클라우드",
    "v3.0",
  ]
description: "Aspose.Cells Cloud REST API v3.0을 사용하여 Excel 워크시트의 기본 속성(예: 영점 표시, 눈금자 표시 여부)을 업데이트하는 방법을 알아보세요. cURL 요청, SDK 샘플, 매개변수 및 오류 처리 방법을 포함합니다."
ArticleTitle: "워크시트 속성 업데이트 – Aspose.Cells Cloud API 참조 (v3.0)"
---

이 REST API는 워크시트 기본 속성을 업데이트합니다.

## REST API

**필수 조건:** 유효한 Aspose Cloud 계정이 있어야 하며, JWT 액세스 토큰을 획득하고, 대상 워크북이 지원되는 저장소 위치에 저장되어 있어야 합니다. 모든 요청은 **HTTPS**를 통해 이루어져야 합니다.

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

### **요청 매개변수**

| 매개변수 이름 | 유형   | 경로/쿼리 문자열/HTTP 본문 | 설명                                                                                       |
| ------------- | ------ | -------------------------- | ------------------------------------------------------------------------------------------ |
| name          | string | path                       | 워크북 파일 이름(확장자 포함).                                                             |
| sheetName     | string | path                       | 업데이트할 워크시트의 이름.                                                                |
| sheet         | object | body                       | 워크시트 속성의 키/값 쌍을 포함하는 JSON 객체(예: `DisplayZeros`, `IsRulerVisible`).     |
| folder        | string | query                      | 워크북이 위치한 저장소 내 폴더 경로.                                                       |
| storageName   | string | query                      | 사용할 저장소 이름.                                                                        |

**sheet** 객체는 요청 본문에 JSON 형식으로 전송됩니다. 수정 가능한 속성 예시로는 `DisplayZeros`, `IsRulerVisible`, `IsGridlinesVisible` 등 API 사양에서 정의된 속성이 있습니다.

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Worksheets/PostUpdateWorksheetProperty)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예시는 cURL을 사용하여 클라우드 API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1" \
-X POST \
-d '{"DisplayZeros":"true","IsRulerVisible":"true"}' \
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

일반적인 응답 코드:

- **200** – 성공. 워크시트 속성이 업데이트되었습니다.
- **400** – 잘못된 요청(예: 잘못된 형식의 JSON 또는 필수 매개변수 누락).
- **401** – 인증되지 않음 – 누락되거나 유효하지 않은 JWT 토큰.
- **404** – 워크북 또는 워크시트를 찾을 수 없음.
- **500** – 내부 서버 오류.

| 코드 | 의미 |
|------|------|
| 200 | 성공 – 워크시트 속성이 업데이트되었습니다. |
| 400 | 잘못된 요청 – 잘못된 형식의 JSON 또는 필수 매개변수 누락. |
| 401 | 인증되지 않음 – 누락되거나 유효하지 않은 JWT 토큰. |
| 404 | 찾을 수 없음 – 워크북 또는 워크시트가 존재하지 않습니다. |
| 500 | 내부 서버 오류. |

## 클라우드 SDK 패밀리

SDK를 사용하면 개발 속도를 가장 빠르게 높일 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예시는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 요청을 보내는 방법을 보여줍니다:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Objective C" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPostUpdateWorksheetProperty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-UpdateWorksheetProperties-update-worksheet-properties.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PostUpdateWorksheetProperty-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-update_worksheet_property-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-UpdateWorksheetProperties-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-UpdateWorksheetProperties-update-worksheet-properties.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-UpdateWorksheetProperties-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "ce38cb4feb118132fada7801c7f5cd43" >}}

{{< /tab >}}

{{< /tabs >}}