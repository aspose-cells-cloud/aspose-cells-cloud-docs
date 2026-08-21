---
title: "셀 값 설정 – Aspose.Cells Cloud API 참조 (v3.0)"  
type: docs  
url: /ko/set-value-of-a-cell-in-a-worksheet/  
weight: 70  
keywords: "Aspose Cells API 셀 값 설정, Excel 셀 업데이트 REST, Aspose.Cells Cloud cURL 예제"  
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트의 특정 셀 값 설정 방법을 배워보세요. 요청 구문, 매개변수, HTTPS cURL 예제, SDK 코드 샘플이 포함되어 있습니다."  
---  

이 REST API는 Excel 파일 내 **셀 값**을 설정합니다.

## REST API  

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}
```  

## 보안 및 인증

Aspose.Cells Cloud API는 [JWT 토큰 기반 인증](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)을 요구하며, 안전하게 설계되었습니다.


**요청 매개변수**

| 이름            | 유형     | 위치   | 설명                                          |
|-----------------|----------|--------|-----------------------------------------------|
| name            | string   | path   | Excel 문서 이름 (확장자 포함).                |
| sheetName       | string   | path   | 워크시트 이름 (대소문자 구분).                 |
| cellName        | string   | path   | 대상 셀의 A1 스타일 주소 (예: `A1`).           |
| value           | string   | query  | 셀에 할당할 값.                               |
| type            | string   | query  | 값의 데이터 유형 (`int`, `string`, `float` 등). |
| formula         | string   | query  | 셀에 적용할 수식 (선택 사항).                 |
| folder          | string   | query  | 문서가 포함된 폴더 (선택 사항).               |
| storageName     | string   | query  | 파일이 저장된 저장소 이름 (선택 사항).        |

## **응답**

CellResponse를 반환합니다.

- **응답 필드 개요**

| 필드             | 유형    | 설명                                             |
| ---------------- | ------- | ------------------------------------------------ |
| `Name`           | string  | 셀의 주소 (예: `F341`).                           |
| `Row`            | integer | 0부터 시작하는 행 인덱스.                        |
| `Column`         | integer | 0부터 시작하는 열 인덱스.                        |
| `Value`          | string  | 셀에 표시된 값.                                  |
| `Type`           | string  | 셀의 데이터 유형 (예: `IsString`).               |
| `Formula`        | string  | 셀에 수식이 포함된 경우 수식 텍스트.             |
| `IsFormula`      | bool    | 셀에 수식이 포함되어 있는지 여부.                |
| `IsMerged`       | bool    | 셀이 병합 범위의 일부인지 여부.                   |
| `IsArrayHeader`  | bool    | 셀이 배열 헤더인지 여부.                         |
| `IsInArray`      | bool    | 셀이 배열의 일부인지 여부.                       |
| `IsErrorValue`   | bool    | 셀에 오류 값이 포함되어 있는지 여부.             |
| `IsInTable`      | bool    | 셀이 테이블 내부에 있는지 여부.                   |
| `IsStyleSet`     | bool    | 셀에 스타일이 적용되어 있는지 여부.              |
| `HtmlString`     | string  | 셀 값의 HTML 인코딩 표현.                        |
| `Style.link`     | object  | 스타일 리소스로 향하는 하이퍼링크.               |


```json
{
  "Status":"OK",
  "Code":200,
  "Cell":{
    "Name":"A1",
    "Row": 0,
    "Column":0,
    "Value": "",
    "Type":"String",
    "Formula" : "=Sum(A2:A15)",
    ...
  }
}
```

**HTTP 상태 코드**

| 코드 | 의미                      | 설명                                          |
|------|---------------------------|-----------------------------------------------|
| 200  | OK                        | 필터가 성공적으로 적용됨; 응답에 작업 세부정보 포함. |
| 400  | Bad Request               | 누락되거나 잘못된 매개변수 (예: 지원되지 않는 파일 유형). |
| 401  | Unauthorized              | 잘못되거나 누락된 JWT 토큰.                     |
| 413  | Payload Too Large         | 업로드된 파일이 크기 제한을 초과함.             |
| 500  | Internal Server Error     | 예기치 않은 서버 오류.                          |

## SDK를 사용하여 PostWorksheetCellSetValue API 사용 방법

### PostWorksheetCellSetValue API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetCellSetValue)은 개발자가 브라우저 또는 모든 HTTP 클라이언트에서 REST 엔드포인트를 직접 호출할 수 있도록 하는 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의합니다.

**cURL** 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스를 호출할 수 있습니다. 아래 예제는 cURL을 사용하여 셀 값을 설정하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3?value=1234&type=int" \
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
  "Status": "OK",
  "Cell":{
    "Name":"A3",
    "Row": 2,
    "Column":0,
    "Value": "",
    "Type":"String",
    "Formula" : "=Sum(A2:A15)",
    ...
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 저수준 세부 사항을 처리해 주므로 프로젝트 개발에 집중할 수 있어 개발 속도가 빨라집니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellSetValue.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellSetValue.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellSetValue.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellSetValue.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellSetValue.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellSetValue.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellSetValue.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellSetValue.go" >}}

{{< /tab >}}

{{< /tabs >}}
---