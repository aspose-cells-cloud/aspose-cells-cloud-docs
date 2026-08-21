---
title: "피벗 테이블에 피벗 필드 추가"
second_title: "Document"
linktitle: "피벗 필드 추가"
type: docs
url: /ko/pivot-tables/add-pivot-field/
aliases: [  /ko/add-a-pivot-table-in-a-worksheet/ ]
keywords: "Aspose.Cells Cloud, Excel, 피벗 테이블, 피벗 필드 추가, REST API, SDK"
description: "Aspose.Cells Cloud REST API를 사용하여 기존 피벗 테이블에 피벗 필드를 추가합니다. 요청 세부 정보, cURL 예제, SDK 스니펫 포함."
weight: 40
ArticleTitle: "피벗 테이블에 피벗 필드 추가 – Aspose.Cells Cloud 문서"
---

이 REST API는 **기존 피벗 테이블에 피벗 필드를 추가**합니다.

> **사전 조건:** 이 엔드포인트를 호출하려면 `Authorization` 헤더에 유효한 JWT 인증 토큰을 포함해야 하며, 워크북이 지정된 폴더 또는 기본 저장소에 저장되어 있어야 합니다.

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotField
```

### 요청 매개변수

| 매개변수 이름     | 유형     | 위치   | 설명                                                            |
| ---------------- | ------- | ------ | -------------------------------------------------------------- |
| name             | string  | path   | 문서 이름.                                                       |
| sheetName        | string  | path   | 워크시트 이름.                                                    |
| pivotTableIndex  | integer | path   | 피벗 테이블의 인덱스.                                             |
| pivotFieldType   | string  | query  | 필드 영역 유형(예: Row, Column).                                  |
| request          | object  | body   | 추가할 필드 인덱스를 포함하는 DTO.                                |
| needReCalculate  | boolean | query  | 작업 후 피벗 테이블을 다시 계산하려면 **true**로 설정합니다.       |
| folder           | string  | query  | 문서가 저장된 폴더.                                               |
| storageName      | string  | query  | 저장소 이름.                                                      |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/PivotTables/PutPivotTableField)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

**cURL** 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스를 호출할 수 있습니다. 아래 예제는 cURL을 사용하여 피벗 필드를 추가하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/PivotField?pivotFieldType=Row" \
  -X PUT \
  -d '{"Data":[1,2]}' \
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

성공적인 응답은 `Code` 및 `Status` 필드를 포함하는 JSON 객체를 반환합니다. 예시 스키마:

```json
{
  "Code": 0,        // HTTP 상태 코드를 나타내는 정수
  "Status": "OK"    // 문자열 메시지
}
```

가능한 오류 응답은 매개변수 누락 시 **400 Bad Request**, 토큰이 유효하지 않을 경우 **401 Unauthorized**, 서버 측 문제 시 **500 Internal Server Error** 등이 있습니다.

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 이 기능을 통합하는 가장 빠른 방법입니다. SDK는 저수준 세부 사항을 처리하므로 비즈니스 로직에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="Ruby" tabName4="Python" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-AddPivotFieldInPivottable-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-AddPivotFieldInPivottable-add-pivot-field.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddPivotFieldInPivotTable.py" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-AddPivotFieldInPivottable-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-AddPivotFieldInPivottable-add-pivot-field.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-AddPivotFieldInPivottable-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "8f9b66d50f7cfa2b14c24fa7ddb396e7" >}}

{{< /tab >}}

{{< /tabs >}}

**참조:**  
- [피벗 테이블 추가](https://docs.aspose.cloud/cells/pivot-tables/add-pivot-table/)  
- [피벗 필드 삭제](https://docs.aspose.cloud/cells/pivot-tables/delete-pivot-field/)