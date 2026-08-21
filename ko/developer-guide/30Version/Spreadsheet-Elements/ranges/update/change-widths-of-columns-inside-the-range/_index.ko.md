---
title: "범위 내 열 너비 변경"
ArticleTitle: "범위 내 열 너비 변경 – Aspose.Cells Cloud API"
second_title: "문서"
linktype: "문서"
url: /ranges/update/column-width/
aliases: [/change-widths-of-columns-inside-the-range/]
keywords: "Aspose.Cells, 열 너비, REST API, Excel, SDK, 범위, 클라우드"
description: "Aspose.Cells Cloud REST API 또는 SDK(C#, Java, Python 등)를 사용하여 범위 내 열 너비를 변경하는 방법을 알아보세요. cURL, 요청/응답 세부 정보, 인증 단계 포함."
weight: 74
---

이 REST API는 범위 내 열 너비를 설정합니다.

## 보안 및 인증
Aspose.Cells Cloud API는 보안이 강화되어 있으며, [JWT 토큰 기반 인증](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)이 필요합니다.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/columnWidth
```

**필수 조건** – 엔드포인트를 호출하기 전에 다음을 수행해야 합니다:

1. Aspose Cloud 계정을 생성하고 *클라이언트 ID* 및 *클라이언트 시크릿*을 획득합니다.  
2. OAuth 엔드포인트(`/connect/token`)를 호출하여 JWT 토큰을 요청합니다. 토큰은 `access_token` 필드에 반환됩니다.  
3. 대상 워크북을 Aspose Cloud 스토리지에 업로드하거나(또는 해당 폴더에 이미 존재하는지 확인) 합니다.  

요청 파라미터는 다음과 같습니다:

| 파라미터 이름 | 타입   | 위치 | 설명 |
|---------------|--------|------|------|
| name          | string | path | 워크북 파일 이름 |
| sheetName     | string | path | 워크시트 이름 |
| value         | number | query | 설정할 열 너비 값 |
| range         | object | body | 대상 셀을 정의하는 범위 객체 |
| folder        | string | query | 워크북이 저장된 폴더 경로 |
| storageName   | string | query | 스토리지 서비스 이름 |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeColumnWidth)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예시는 cURL을 사용하여 클라우드 API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

<h3 id="request">요청</h3>

```bash
# 워크북 *test.xlsx*, 워크시트 *Sheet1*에 대해 열 너비 엔드포인트를 호출하여
# 선택된 열의 너비를 20포인트로 설정합니다.
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/columnWidth?value=20" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "ColumnCount": 7,
        "ColumnWidth": 19,
        "FirstColumn": 0,
        "FirstRow": 9,
        "Name": "string",
        "RefersTo": "string",
        "RowCount": 1,
        "RowHeight": 15,
        "Worksheet": "Sheet1"
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

<h3 id="response">응답</h3>

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*가능한 오류 응답*  

| HTTP 코드 | 설명                               |
|-----------|-------------------------------------------|
| 400       | 잘못된 요청 – 유효하지 않은 JSON 또는 파라미터 |
| 401       | 인증되지 않음 – 누락 또는 유효하지 않은 토큰   |
| 404       | 찾을 수 없음 – 워크북 또는 워크시트 없음       |

{{< /tab >}}

{{< /tabs >}}

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예시는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeColumnWidth.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeColumnWidth.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeColumnWidth.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeColumnWidth.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeColumnWidth.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeColumnWidth.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeColumnWidth.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeColumnWidth.go" >}}

{{< /tab >}}

{{< /tabs >}}

## FAQ

**Q:** *Excel 워크북에서 범위의 열 너비를 설정하려면 어떤 엔드포인트를 호출해야 하나요?*  
**A:** `POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/columnWidth` (여기서 `{name}`은 워크북 파일 이름이고, `{sheetName}`은 대상 워크시트 이름입니다.)

**Q:** *열 너비 API를 사용할 때 요청을 인증하려면 어떻게 해야 하나요?*  
**A:** `Authorization: Bearer <jwt token>` 헤더를 포함하세요. 클라이언트 ID와 클라이언트 시크릿을 사용하여 Aspose Cloud OAuth 흐름(`/connect/token`)을 통해 JWT 토큰을 획득하세요.

**Q:** *열 A~C의 너비를 25포인트로 변경하려면 어떤 JSON 본문을 보내야 하나요?*  
**A:**  

```json
{
  "FirstColumn": 0,
  "ColumnCount": 3,
  "FirstRow": 0,
  "RowCount": 1
}
```

요청 URL에 쿼리 파라미터 `value=25`를 추가하세요.