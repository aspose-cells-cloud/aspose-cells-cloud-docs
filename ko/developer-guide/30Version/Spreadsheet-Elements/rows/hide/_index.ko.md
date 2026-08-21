---
title: "Excel 워크시트에서 행 숨기기"
second_title: "문서"
linktitle: "숨기기"
type: docs
url: /rows/hide/
aliases: [/hide-rows-in-excel-worksheet/]
keywords: "행 숨기기, Aspose.Cells Cloud, Excel API, REST, SDK"
description: "Aspose.Cells Cloud REST API를 사용해 Excel 워크시트에서 하나 또는 여러 개의 행을 숨기는 방법을 알아보세요. cURL 예제, SDK 코드 스니펫, 매개변수, 인증, 응답 세부정보, 오류 처리를 포함합니다."
weight: 40
ArticleTitle: "Aspose.Cells Cloud API를 사용해 Excel 워크시트에서 행 숨기기"
---

이 REST API는 Excel 워크시트의 행을 숨깁니다.

**필수 조건:** Aspose Cloud OAuth 엔드포인트에서 획득한 유효한 JWT Bearer 토큰, Aspose Cloud 저장소에 저장된 워크북, 숨길 행이 포함된 워크시트 이름. 이 API는 XLS, XLSX 및 기타 지원되는 형식의 Excel 파일과 함께 작동합니다.

## PostHideWorksheetRows API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/hide
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 강화되었으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수        | 유형    | 위치   | 설명                                                         |
| --------------- | ------- | ------ | ------------------------------------------------------------ |
| **name**        | string  | path   | 워크북 파일의 이름.                                           |
| **sheetName**   | string  | path   | 숨길 행이 포함된 워크시트의 이름.                             |
| **startrow**    | integer | query  | 숨길 첫 번째 행의 0 기반 인덱스.                               |
| **totalRows**   | integer | query  | **startrow**에서 시작하여 연속적으로 숨길 행의 수.            |
| **folder**      | string  | query  | 워크북이 위치한 저장소 내 폴더.                               |
| **storageName** | string  | query  | 저장소 서비스의 이름.                                         |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Cells/PostHideWorksheetRows)은 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 공개적으로 접근 가능한 프로그래밍 인터페이스를 제공합니다.

**cURL** 명령줄 도구를 사용해 Aspose.Cells 웹 서비스를 호출할 수 있습니다. 이 API는 Aspose Cloud OAuth 엔드포인트에서 획득한 JWT Bearer 토큰을 필요로 하며, 이를 `Authorization` 헤더에 포함시켜야 합니다. 아래 예제는 cURL을 사용해 행을 숨기는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/hide?startrow=1&totalRows=1" \
  -X POST \
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

**응답 상태 코드**

| 코드 | 설명 |
|------|-------------|
| 200 | 성공 – 행 숨김 처리 완료 |
| 400 | 잘못된 요청 – 유효하지 않은 매개변수 |
| 401 | 인증되지 않음 – JWT 토큰 누락 또는 유효하지 않음 |
| 404 | 존재하지 않음 – 워크북 또는 워크시트가 없음 |
| 500 | 서버 오류 – 내부 처리 실패 |

성공적인 호출은 `Code` 및 `Status` 필드를 포함하는 JSON 객체를 반환합니다. 오류 발생 시, 응답에는 `Message` 등의 추가 필드와 적절한 HTTP 상태 코드(예: 400, 401, 404, 500)가 포함됩니다.

**참고:** `startrow` 값이 워크시트의 행 범위 내에 있어야 합니다. 그렇지 않으면 API가 400 오류를 반환합니다. 행 인덱스는 0 기반이므로 `startrow=0`은 첫 번째 행을 의미합니다.

## Cloud SDK Family

SDK를 사용하면 이 기능을 애플리케이션에 통합하는 데 가장 빠른 방법입니다. SDK는 저수준 세부사항을 처리하므로 비즈니스 로직에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용해 행을 숨기는 방법을 보여줍니다. (예제 파일 이름은 과거 네이밍 규칙으로 인해 “Unhide”를 참조하지만, 각 gist 내부 코드는 **Hide** 작업을 수행합니다.)

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnhideWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnhideWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnhideWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnhideWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnhideWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnhideWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnhideWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnhideWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}