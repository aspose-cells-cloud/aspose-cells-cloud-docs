---
title: "엑셀 워크북에서 이름이 지정된 범위 가져오기"
second_title: "문서"
linktitle: "이름"
type: docs
url: /ranges/get/name/
aliases: [/get-named-ranges-inside-the-workbook/]
keywords: "이름이 지정된 범위, 엑셀, Aspose.Cells, 클라우드 API, 워크시트"
description: "Aspose.Cells Cloud REST API를 사용하여 엑셀 워크북에서 이름이 지정된 범위를 검색합니다. 요청 세부 정보, 샘플 cURL 명령어, 다양한 프로그래밍 언어의 SDK 예제를 포함합니다."
ArticleTitle: "엑셀 워크북에서 이름이 지정된 범위 가져오기 – Aspose.Cells Cloud API"
weight: 10
---

이 REST API는 워크시트 내에 정의된 이름이 지정된 범위에 대한 정보를 반환합니다.

**배경** – *이름이 지정된 범위*(named range)는 워크시트 내 특정 셀 또는 셀 블록을 가리키는 사용자 정의 식별자입니다. 이름이 지정된 범위는 수식 작성 간소화, 가독성 향상, 워크북에서 자주 사용하는 영역에 대한 프로그래밍 방식 접근을 가능하게 합니다.

**사전 요구 사항** – Aspose.Cells Cloud API에 접근하려면 유효한 JWT 액세스 토큰이 필요합니다. OAuth 2.0 토큰 엔드포인트를 통해 Aspose Cloud 클라이언트 ID 및 클라이언트 시크릿을 인증하여 토큰을 획득한 후, 모든 요청의 `Authorization: Bearer <jwt token>` 헤더에 토큰을 포함시켜야 합니다.

## GetNamedRanges API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/ranges
```

### **보안 및 인증**

Aspose.Cells Cloud API는 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>을 요구하는 안전한 API입니다.

### 요청 매개변수

| 매개변수 이름 | 유형   | 위치         | 설명                                     |
| ------------- | ------ | ------------ | ---------------------------------------- |
| name          | string | Path         | 엑셀 문서의 이름입니다.                  |
| folder        | string | Query string | 문서가 포함된 폴더입니다.               |
| storageName   | string | Query string | 문서가 위치한 저장소의 이름입니다.       |

**HTTP 상태 코드**

| 코드 | 의미                      | 설명                                                |
|------|---------------------------|-----------------------------------------------------|
| 200  | OK (성공)                 | 필터가 성공적으로 적용되었으며, 응답에 작업 세부 정보가 포함됩니다. |
| 400  | Bad Request (잘못된 요청) | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형)가 있습니다. |
| 401  | Unauthorized (인증되지 않음) | 잘못되거나 누락된 JWT 토큰입니다.                     |
| 413  | Payload Too Large (페이로드 너무 큼) | 업로드된 파일이 크기 제한을 초과했습니다.           |
| 500  | Internal Server Error (내부 서버 오류) | 예기치 않은 서버 오류가 발생했습니다.                |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Worksheets/GetNamedRanges)은 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스를 호출할 수 있습니다. 아래 예제는 cURL을 사용하여 이름이 지정된 범위를 검색하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/ranges" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Ranges": {
    "RangeList": [
      {
        "ColumnCount": 7,
        "ColumnWidth": 8.428571428571429,
        "FirstColumn": 1,
        "FirstRow": 9,
        "Name": "data",
        "RefersTo": "=Sheet1!$B$10:$H$10",
        "RowCount": 1,
        "RowHeight": 15,
        "Worksheet": "Sheet1"
      }
    ]
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**응답 모델**

| 필드           | 유형    | 설명                                                 |
|---------------|---------|------------------------------------------------------|
| `ColumnCount` | integer | 범위 내 열의 수입니다.                               |
| `ColumnWidth` | number  | 각 열의 너비(포인트 단위)입니다.                     |
| `FirstColumn` | integer | 범위의 첫 번째 열 인덱스(0부터 시작)입니다.          |
| `FirstRow`    | integer | 범위의 첫 번째 행 인덱스(0부터 시작)입니다.          |
| `Name`        | string  | 범위의 사용자 정의 이름입니다.                       |
| `RefersTo`    | string  | 셀 참조를 정의하는 수식(예: `=Sheet1!$B$10:$H$10`)입니다. |
| `RowCount`    | integer | 범위 내 행의 수입니다.                               |
| `RowHeight`   | number  | 각 행의 높이(포인트 단위)입니다.                     |
| `Worksheet`   | string  | 범위를 포함하는 워크시트의 이름입니다.               |

## 클라우드 SDK 패밀리

SDK를 사용하면 이 기능을 통합하는 데 가장 빠른 방법입니다. SDK는 저수준 세부 사항을 처리하므로 비즈니스 로직에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetNamedRanges.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetNamedRanges.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetNamedRanges.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetNamedRanges.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetNamedRanges.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetNamedRanges.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetNamedRanges.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetNamedRanges.go" >}}

{{< /tab >}}

{{< /tabs >}}