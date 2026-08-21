---
title: "Excel 워크시트에 피벗 테이블 추가"
second_title: "문서"
linktype: Add
type: docs
url: "/ko/pivot-tables/add/"
aliases: [/add-a-pivot-table-in-a-worksheet/]
keywords: "피벗 테이블 추가, Excel 워크시트, Aspose.Cells Cloud, REST API, SDK, Excel 피벗 테이블"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트에 피벗 테이블을 추가합니다. C#, Java, PHP, Python, Node.js, Android, Swift, Perl, Go SDK를 통해 제공됩니다."
weight: 30
ArticleTitle: "Aspose.Cells Cloud를 사용하여 Excel 워크시트에 피벗 테이블 추가하는 방법"
---

이 REST API는 워크시트에 피벗 테이블을 추가합니다.

**필수 조건:**  
- 유효한 JWT 액세스 토큰이 있는 Aspose.Cells Cloud 계정  
- 대상 워크북은 지원되는 저장소 위치(기본 저장소 또는 사용자 지정 저장소)에 저장되어 있어야 합니다.  
- `sheetName`으로 지정된 워크시트가 워크북에 존재해야 합니다.  

## PutWorksheetPivotTable API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 보장되며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **요청 파라미터**

| 파라미터 이름 | 유형    | 위치   | 설명                                                                                                                         |
| ------------- | ------- | ------ | ---------------------------------------------------------------------------------------------------------------------------- |
| name          | string  | path   | Excel 문서의 이름입니다.                                                                                                     |
| sheetName     | string  | path   | 피벗 테이블이 생성될 워크시트의 이름입니다.                                                                                  |
| request       | object  | body   | 피벗 테이블 정의를 포함하는 `CreatePivotTableRequest` DTO입니다.                                                            |
| folder        | string  | query  | 문서가 위치한 폴더입니다.                                                                                                    |
| storageName   | string  | query  | 문서가 저장된 저장소의 이름입니다.                                                                                            |
| sourceData    | string  | query  | 새 피벗 테이블 캐시의 소스 데이터를 제공하는 범위(예: `A5:E10`)입니다.                                                      |
| destCellName  | string  | query  | 피벗 테이블 보고서가 삽입될 상단-왼쪽 셀의 주소입니다.                                                                      |
| tableName     | string  | query  | 새 피벗 테이블에 할당된 이름입니다.                                                                                          |
| useSameSource | boolean | query  | `true`인 경우, 새 피벗 테이블은 기존 소스 데이터를 재사용하여 다른 피벗 테이블이 이미 이 소스를 사용한 경우 메모리를 절약합니다. |

[OpenAPI 스펙](https://apireference.aspose.cloud/cells/#/PivotTables/PutWorksheetPivotTable)은 공개적으로 사용 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

**cURL** 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API를 호출하는 방법을 보여줍니다.

**보안 참고사항:** API를 호출할 때는 항상 `https://`를 사용하고 JWT 토큰을 기밀로 유지해야 합니다. 평문 HTTP로 전송할 경우 토큰이 가로채일 위험이 있습니다.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/pivottables" \
-X PUT \
-d '{"Name":"MyPivot","SourceData":"A5:E10","DestCellName":"H20","UseSameSource":true,"PivotFieldRows":[1],"PivotFieldColumns":[1],"PivotFieldData":[1]}' \
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

**HTTP 상태 코드**

| 코드 | 의미               | 설명                                              |
|------|--------------------|---------------------------------------------------|
| 200  | OK (성공)          | 필터가 성공적으로 적용됨; 응답에 작업 세부정보 포함 |
| 400  | Bad Request        | 누락되거나 잘못된 파라미터(예: 지원되지 않는 파일 형식) |
| 401  | Unauthorized       | 잘못되거나 누락된 JWT 토큰                          |
| 413  | Payload Too Large  | 업로드된 파일이 크기 제한을 초과함                  |
| 500  | Internal Server Error | 예기치 않은 서버 오류 발생                         |

## 클라우드 SDK Family

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-AddPivottableWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-AddPivottableWorksheet-add-pivot-table-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddPivotTableInw" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-AddPivottableWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-AddPivottableWorksheet-add-pivot-table-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-AddPivottableWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "980246b631d7816f257f2ad4664788ea" >}}

{{< /tab >}}

{{< /tabs >}}

더 많은 작업은 관련 API 페이지를 참조하세요: **[피벗 테이블 조회](https://docs.aspose.cloud/cells/pivot-tables/get/)**, **[피벗 테이블 삭제](https://docs.aspose.cloud/cells/pivot-tables/delete/)**, **[피벗 테이블 업데이트](https://docs.aspose.cloud/cells/pivot-tables/update/)**.