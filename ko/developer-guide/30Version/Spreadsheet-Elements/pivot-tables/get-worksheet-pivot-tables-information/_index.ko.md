---
title: "엑셀 워크시트에서 모든 피벗 테이블 가져오기"
second_title: "문서"
linktitle: 모두 가져오기
type: docs
url: /ko/pivot-tables/get-all/
aliases: [  /ko/get-worksheet-pivot-tables-information/ ]
keywords: "모든 피벗 테이블 가져오기, Aspose.Cells Cloud API, 엑셀 피벗테이블, REST API"
description: "Aspose.Cells Cloud API를 통해 엑셀 워크시트에서 모든 피벗 테이블을 검색합니다. 피벗테이블 API에 대한 엔드포인트, 매개변수, 인증 단계, cURL 및 SDK 샘플을 포함합니다."
weight: 20
ArticleTitle: "엑셀 워크시트에서 모든 피벗 테이블 가져오기 – Aspose.Cells Cloud API"
---

**피벗 테이블**(PivotTable)은 엑셀에서 대규모 데이터 세트를 재조직하고 분석할 수 있도록 해주는 데이터 요약 도구입니다. 이 REST API는 지정된 워크시트의 **모든** 피벗 테이블에 대한 정보를 검색합니다.

## 보안 및 인증

Aspose.Cells Cloud API는 보안이 확보되었으며, [JWT 토큰 기반 인증](https://docs.aspose.cloud/ko/total/getting-started/rest-api-overview/authenticating-api-requests/)이 필요합니다.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### **요청 매개변수**

| 매개변수 이름 | 유형   | 위치 | 설명                              |
| ------------- | ------ | ---- | ----------------------------------- |
| name          | string | path | 엑셀 문서의 이름입니다.            |
| sheetName     | string | path | 워크시트의 이름입니다.             |
| folder        | string | query | 문서가 저장된 폴더입니다.         |
| storageName   | string | query | 스토리지 서비스의 이름입니다.     |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/PivotTables/GetWorksheetPivotTables)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

### 요청

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

### 응답

{{< tab tabNum="2" >}}

```json
{
  "PivotTables": {
    "PivotTableList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self"
        }
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### 오류 응답

| HTTP 코드 | 설명                                                       | 샘플 JSON 페이로드                                           |
| --------- | ---------------------------------------------------------- | ------------------------------------------------------------ |
| 400       | 잘못된 요청 – 필수 매개변수 누락.                          | `{ "Code": "400", "Message": "필수 매개변수가 누락되었습니다." }` |
| 401       | 인증되지 않음 – 잘못되었거나 누락된 토큰.                 | `{ "Code": "401", "Message": "인증에 실패했습니다." }`      |
| 404       | 찾을 수 없음 – 워크북, 워크시트 또는 피벗 테이블이 존재하지 않음. | `{ "Code": "404", "Message": "리소스를 찾을 수 없습니다." }` |
| 500       | 내부 서버 오류 – 서버에서 예기치 않은 조건 발생.          | `{ "Code": "500", "Message": "서버 오류입니다." }`          |

## 클라우드 SDK 패밀리

SDK를 사용하면 개발 속도가 가장 빠릅니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-GetWorksheetPivotTables-1.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-GetPivotTableWorksheet-GetPivotTableWorksheet-12345.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetWorksheetPivotTablesInformation.py" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-GetWorksheetPivotTables-1.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-GetPivotTableWorksheet-GetPivotTableWorksheet-12345.java" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-GetWorksheetPivotTables-1.pl" >}}
{{< /tab >}}

{{< tab tabNum="10" >}}
{{< gist "aspose-cells-cloud-gists" "6b30a17927feeb2899283e4dbe566c42" >}}
{{< /tab >}}

{{< /tabs >}}