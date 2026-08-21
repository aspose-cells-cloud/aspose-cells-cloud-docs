---
title: "여러 셀 스타일 업데이트 – Aspose.Cells Cloud API 참조 (v3.0)"
type: docs
url: /ko/update-multiple-cells-style/
weight: 20
keywords: ["Aspose.Cells", "여러 셀 스타일 업데이트", "Excel 셀 스타일 API", "클라우드 SDK", "REST API", "cURL 예제", "JSON 요청", "JWT 인증"]
description: "Aspose.Cells Cloud REST API v3.0을 사용하여 Excel 워크북의 셀 범위 스타일을 업데이트하는 방법을 알아보세요. 엔드포인트, HTTP 메서드, 매개변수, cURL 및 SDK 예제, 인증, 오류 처리, 버전 정보가 포함됩니다."
ArticleTitle: "여러 셀 스타일 업데이트 – Aspose.Cells Cloud API 참조 (v3.0)"
---

## REST API

이 REST API는 Excel 워크북에서 셀 범위의 **스타일**을 설정합니다.

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/style
```

## 보안 및 인증

Aspose.Cells Cloud API는 [JWT 토큰 기반 인증](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)이 필요합니다.

### 요청 매개변수

| 매개변수 이름 | 유형   | 위치 | 설명 |
|---------------|--------|------|------|
| **name**      | string | path | 워크북 이름. |
| **sheetName** | string | path | 워크시트 이름. |
| **range**     | string | query | 셀 범위 (예: `A1:A10`). |
| **style**     | object | body | 적용할 스타일을 정의하는 JSON 객체. |
| **folder**    | string | query | 워크북이 포함된 폴더. |
| **storageName**| string | query | 스토리지 이름. |

#### Style 객체
`style` JSON 객체는 셀 서식을 나타냅니다. 다음 선택적 속성 중 하나 이상을 포함할 수 있습니다:

- **Font** – 글꼴 설정 (`Name`, `Size`, `IsBold`, `IsItalic`, `Color` 등).  
- **BackgroundColor** – ARGB 형식의 배경색.  
- **ForegroundColor** – ARGB 형식의 전경색.  
- **Name**, **CultureCustom**, **Custom** – 추가 스타일 메타데이터.

## **응답**

CellCloudResponse를 반환합니다.

- **응답 필드 개요**

| 필드            | 유형    | 설명                                           |
| --------------- | ------- | ---------------------------------------------- |
| `Status`        | string  |                                                |
| `Code`          | integer | 200, 400, 401, 500,...                         |


```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP 상태 코드**

| 코드 | 의미                        | 설명                                           |
|------|-----------------------------|------------------------------------------------|
| 200  | OK                          | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함. |
| 400  | Bad Request                 | 누락되었거나 잘못된 매개변수 (예: 지원되지 않는 파일 형식). |
| 401  | Unauthorized                | 잘못되었거나 누락된 JWT 토큰. |
| 413  | Payload Too Large           | 업로드된 파일이 크기 제한을 초과함. |
| 500  | Internal Server Error       | 예기치 않은 서버 오류. |

## SDK를 사용한 PostUpdateWorksheetRangeStyle API 사용 방법

### PostUpdateWorksheetRangeStyle API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Cells/PostUpdateWorksheetRangeStyle)에서 전체 스키마를 확인할 수 있습니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
cURL -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/style?range=a1%3Aa10" \
  -X POST \
  -d '{
        "Font": {
          "Color": { "A":255, "R":255, "G":255, "B":0 },
          "Size": 22,
          "IsBold": true,
          "IsItalic": true,
          "IsStrikeout": true,
          "IsSubscript": true,
          "IsSuperscript": true,
          "Name": "Arial"
        },
        "Name": "string",
        "CultureCustom": "string",
        "Custom": "string",
        "BackgroundColor": { "A":10, "R":10, "G":10, "B":10 },
        "ForegroundColor": { "A":255, "R":255, "G":255, "B":0 }
      }' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}


### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeStyle.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeStyle.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeStyle.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeStyle.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeStyle.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeStyle.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeStyle.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeStyle.go" >}}

{{< /tab >}}

{{< /tabs >}}
---