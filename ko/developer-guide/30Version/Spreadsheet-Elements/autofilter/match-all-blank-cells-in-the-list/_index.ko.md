---
title: "Excel 워크시트의 모든 빈 셀 일치시키기"
ArticleTitle: "Excel 워크시트의 모든 빈 셀 일치시키기 – Aspose.Cells Cloud API 가이드"
second_title: "문서"
linktype: "docs"
url: /autofilter/match-all-blank/
aliases: [/match-all-blank-cells-in-the-list/]
keywords: "Aspose.Cells, 빈 셀, AutoFilter, REST API, Excel"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트에서 빈 셀을 필터링하고 일치시키는 방법을 알아보세요. 엔드포인트, 매개변수, 인증 단계, cURL 예제, C#, Java, Python 등 다양한 언어의 SDK 스니펫을 포함합니다."
weight: 100
---

이 REST API는 Excel 워크시트의 필터 목록에서 모든 **빈 셀**을 일치시킵니다.

**사전 요구 사항:** 이 엔드포인트를 호출하기 전에 유효한 JWT 액세스 토큰이 있어야 하며, 워크북이 Aspose Cloud 스토리지에 업로드되어 있어야 하고, 스토리지 폴더(해당하는 경우)를 알고 있어야 합니다. 파일이 기본 루트 폴더에 있지 않은 경우 `folder` 및 `storageName` 매개변수를 제공하세요.

## PostWorksheetMatchBlanks API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/matchBlanks
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 구축되었으며 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.


### 요청 매개변수

| 매개변수 이름 | 타입    | 위치 | 설명                                                            |
|---------------|---------|------|-------------------------------------------------------------------|
| name          | string  | path | 워크북 파일의 이름입니다.                                          |
| sheetName     | string  | path | 필터가 포함된 워크시트의 이름입니다.                               |
| fieldIndex    | integer | query| 필터를 적용할 열의 0부터 시작하는 인덱스입니다.                   |
| folder        | string  | query| 워크북이 위치한 스토리지 내 폴더 경로입니다.                      |
| storageName   | string  | query| Aspose Cloud 스토리지의 이름입니다.                                |

### **응답**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP 상태 코드**

| 코드 | 의미                     | 설명                                      |
|------|---------------------------|---------------------------------------------|
| 200  | OK (성공)                | 필터가 성공적으로 적용되었으며, 응답에는 작업 세부 정보가 포함됩니다. |
| 400  | Bad Request (잘못된 요청) | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식)입니다. |
| 401  | Unauthorized (인증되지 않음) | 유효하지 않거나 누락된 JWT 토큰입니다. |
| 413  | Payload Too Large (페이로드가 너무 큼) | 업로드된 파일이 크기 제한을 초과했습니다. |
| 500  | Internal Server Error (내부 서버 오류) | 예기치 않은 서버 오류입니다. |

## SDK를 사용하여 PostWorksheetMatchBlanks API 사용 방법

### PostWorksheetMatchBlanks API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/AutoFilter/PostWorksheetMatchBlanks)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}
```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/matchBlanks?fieldIndex=0" \
  -X POST \
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

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 작업에 집중할 수 있도록 해줍니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetMatchBlanks.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetMatchBlanks.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetMatchBlanks.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetMatchBlanks.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetMatchBlanks.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetMatchBlanks.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetMatchBlanks.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetMatchBlanks.go" >}}
{{< /tab >}}

{{< /tabs >}}