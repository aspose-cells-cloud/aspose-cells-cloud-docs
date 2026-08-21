---
title: "워크시트에서 범위 복사 시 붙여넣기 옵션 사용하기"
second_title: "Document"
linktitle: "복사"
type: docs
url: /ranges/copy/
aliases: [/copy-range-in-a-worksheet-with-paste-options/]
keywords: "Aspose.Cells Cloud, REST API, 엑셀, 범위 복사, 워크시트, 붙여넣기 옵션"
description: "Aspose.Cells Cloud REST API를 사용하여 엑셀 워크시트 내 범위를 전체 붙여넣기 옵션 지원과 함께 복사합니다. 여러 프로그래밍 언어에 대한 SDK 예제가 포함됩니다."
weight: 20
ArticleTitle: "워크시트에서 범위 복사 시 붙여넣기 옵션 사용하기 – Aspose.Cells Cloud API"
---

이 REST API는 엑셀 워크북의 워크시트 내 범위를 복사합니다. 관련 작업은 **범위 조회(Get Range)** 및 **범위 업데이트(Update Range)** 문서를 참조하십시오.

**필수 조건:** 이 엔드포인트를 사용하려면 유효한 OAuth 2.0 / JWT 토큰이 필요하며, API 버전이 요청 URL과 일치하는지 확인해야 합니다.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges
```

### **요청 매개변수**

| 매개변수 이름 | 유형   | 위치 | 설명                                                                      |
| ------------- | ------ | ---- | --------------------------------------------------------------------------- |
| name          | string | path | 워크북의 이름입니다.                                                        |
| sheetName     | string | path | 워크시트의 이름입니다.                                                      |
| rangeOperate  | string | body | 수행할 작업: `copydata`, `copystyle`, `copyto`, 또는 `copyvalue`입니다.   |
| folder        | string | query | 워크북이 포함된 폴더입니다.                                                 |
| storageName   | string | query | 저장소 서비스의 이름입니다.                                                 |

**참고:** `rangeOperate` 필드는 복사할 내용을 결정합니다. `copydata`는 셀 값만 복사하고, `copystyle`은 서식만 복사하며, `copyto`는 데이터와 서식 모두를 복사하며, `copyvalue`는 수식 없이 값만 복사합니다. API는 최대 100만 셀까지의 범위를 지원하며, 그보다 큰 범위는 타임아웃이 발생할 수 있습니다.

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangesCopyCopy)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/ranges" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "Operate": "string",
        "Source": {
          "ColumnCount": 0,
          "ColumnWidth": 0,
          "FirstColumn": 0,
          "FirstRow": 0,
          "Name": "string",
          "RefersTo": "string",
          "RowCount": 0,
          "RowHeight": 0,
          "Worksheet": "string"
        },
        "Target": {
          "ColumnCount": 0,
          "ColumnWidth": 0,
          "FirstColumn": 0,
          "FirstRow": 0,
          "Name": "string",
          "RefersTo": "string",
          "RowCount": 0,
          "RowHeight": 0,
          "Worksheet": "string"
        },
        "PasteOptions": {
          "OnlyVisibleCells": true,
          "PasteType": "string",
          "SkipBlanks": true,
          "Transpose": true
        }
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

성공적인 응답은 `200 OK` 상태 코드를 반환합니다. 오류 발생 시 API는 다음과 같은 페이로드를 반환할 수 있습니다:

```json
{
  "Code": 400,
  "Message": "Bad Request – invalid parameters."
}
```

또는

```json
{
  "Code": 401,
  "Message": "Unauthorized – authentication token missing or invalid."
}
```

이러한 오류 객체는 HTTP 상태 코드와 문제 진단에 도움이 되는 설명 메시지를 포함합니다.

{{< /tab >}}

{{< /tabs >}}

복사 작업을 테스트할 수 있는 샘플 워크북을 다운로드하려면 [여기](https://example.com/sample.xlsx)를 클릭하십시오.

## Cloud SDK 패밀리

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangesCopy.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangesCopy.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangesCopy.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangesCopy.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangesCopy.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangesCopy.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangesCopy.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangesCopy.go" >}}

{{< /tab >}}

{{< /tabs >}}