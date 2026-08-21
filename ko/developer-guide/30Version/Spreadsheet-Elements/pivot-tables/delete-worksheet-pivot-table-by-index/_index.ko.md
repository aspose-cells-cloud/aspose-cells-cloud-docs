---
title: "Excel 워크시트에서 피벗 테이블 삭제"
second_title: "문서"
linktype: Delete
type: docs
url: /ko/pivot-tables/delete/
aliases: [/ko/delete-worksheet-pivot-table-by-index/]
keywords: "Aspose.Cells, 피벗 테이블, 삭제, Excel, REST API"
description: "Aspose.Cells Cloud REST API(v3.0)를 사용하여 Excel 워크시트에서 피벗 테이블을 삭제합니다. 요청 형식, cURL 예제, 오류 코드, C#, Java, Python, Node.js용 SDK 스니펫 포함."
weight: 70
ArticleTitle: "Aspose.Cells Cloud로 Excel 워크시트에서 피벗 테이블을 삭제하는 방법"
---

이 REST API는 워크시트에서 인덱스를 기준으로 피벗 테이블을 삭제합니다.

**사전 요구 사항** – 유효한 Aspose.Cells Cloud JWT 액세스 토큰과 대상 Excel 파일이 지원되는 저장소 위치에 저장되어 있어야 합니다. API를 호출하기 전에 파일 이름, 워크시트 이름 및 저장소 세부 정보가 올바르게 지정되었는지 확인하십시오.

피벗 테이블은 **Excel 워크시트**에서 데이터를 요약하는 강력한 방법입니다. Aspose.Cells Cloud를 사용하면 단일 HTTP DELETE 요청을 통해 원치 않는 피벗 테이블을 프로그래밍 방식으로 제거할 수 있습니다. 이 작업은 워크시트를 정리하거나 보고서 생성을 자동화하거나 Excel 조작 기능을 애플리케이션에 통합해야 할 때 매우 유용합니다.

## DeleteWorksheetPivotTable API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 강화되어 있으며 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **요청 매개변수**

| 매개변수 이름   | 유형    | 위치 | 설명                                                    |
| --------------- | ------- | ---- | --------------------------------------------------------- |
| name            | string  | path | Excel 문서의 이름입니다.                                 |
| sheetName       | string  | path | 피벗 테이블이 포함된 워크시트의 이름입니다.             |
| pivotTableIndex | integer | path | 삭제할 피벗 테이블의 0부터 시작하는 인덱스입니다.       |
| folder          | string  | query | 문서가 저장된 폴더의 경로입니다.                         |
| storageName     | string  | query | 저장소 서비스의 이름입니다.                             |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/PivotTables/DeleteWorksheetPivotTable)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

**cURL 명령줄 도구**를 사용하여 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API로 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

**응답 예제**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

응답은 다음과 같은 간단한 JSON 스키마를 따릅니다:

```json
{
  "Code": integer,   // 작업의 HTTP 유사 상태 코드
  "Status": string   // 예: "OK"인 텍스트 설명
}
```

{{< /tab >}}

{{< /tabs >}}

### 오류 처리

일반적인 응답 상태 코드는 다음과 같습니다:

| HTTP 상태 코드 | 설명                                                         |
| -------------- | -------------------------------------------------------------- |
| 400            | 잘못된 요청 – 누락되거나 유효하지 않은 매개변수입니다.         |
| 401            | 인증되지 않음 – 잘못되거나 누락된 JWT 토큰입니다.             |
| 404            | 찾을 수 없음 – 파일, 워크시트 또는 피벗 테이블이 존재하지 않습니다. |
| 500            | 내부 서버 오류 – 서버에서 예기치 않은 조건이 발생했습니다.     |

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스로 요청을 보내는 방법을 보여줍니다:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-DeleteWorksheetPivotTableIndex-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-DeleteWorksheetPivotTableIndex-delete-worksheet-pivot-table-index.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteWorksheetPivotTablesByIndex.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-DeleteWorksheetPivotTableIndex-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-DeleteWorksheetPivotTableIndex-delete-worksheet-pivot-table-index.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-DeleteWorksheetPivotTableIndex-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "8798eca5f30bf41a4675b83583a72ec3" >}}

{{< /tab >}}

{{< /tabs >}}