---
title: "엑셀 워크시트에서 목록 개체 업데이트하기"
ArticleTitle: "엑셀 워크시트에서 목록 개체 업데이트하기 – Aspose.Cells Cloud API 문서"
second_title: "문서"
linktitle: "업데이트"
type: docs
url: /list-objects/update/
aliases:
  - /update-a-list-object-or-table-inside-the-worksheet/
  - /tables/update/
keywords: "Aspose.Cells, ListObject, 테이블 업데이트, 엑셀 API, REST, 클라우드 SDK, 목록 개체 업데이트, 엑셀 워크시트, 테이블"
description: "Aspose.Cells Cloud API(v3.0)를 사용하여 엑셀 테이블을 업데이트하는 방법을 알아보세요. 엔드포인트, 매개변수, 샘플 cURL, 오류 코드, SDK 예제를 포함합니다."
weight: 20
---

이 REST API는 엑셀 워크시트 내의 **목록 개체**(테이블)의 속성을 업데이트합니다.

## 보안 및 인증

Aspose.Cells Cloud API는 [JWT 토큰 기반 인증](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)이 필요합니다.

## 요청 본문 스키마

`listObject` DTO는 다음 필드를 포함합니다. 요청 본문에는 변경하려는 필드만 필요합니다.

| 필드                                             | 유형               | 필수 여부 | 설명                                                                         |
| ------------------------------------------------ | ------------------ | -------- | ---------------------------------------------------------------------------- |
| **DisplayName**                                  | string             | 선택 사항 | 테이블에 표시되는 이름.                                                       |
| **StartRow** / **StartColumn**                   | integer            | 선택 사항 | 테이블의 첫 번째 행/열의 0부터 시작하는 인덱스.                                |
| **EndRow** / **EndColumn**                       | integer            | 선택 사항 | 테이블의 마지막 행/열의 0부터 시작하는 인덱스.                                 |
| **Range**                                        | string             | 선택 사항 | 테이블 범위를 정의하는 A1 스타일 주소(예: `A1:D10`).                            |
| **ShowHeaderRow**                                | boolean            | 선택 사항 | 헤더 행을 표시할지 여부 (`true`이면 표시).                                     |
| **ShowTotals**                                   | boolean            | 선택 사항 | 합계 행을 표시할지 여부 (`true`이면 표시).                                      |
| **TableStyleName**                               | string             | 선택 사항 | 적용할 내장 테이블 스타일 이름.                                                 |
| **TableStyleType**                               | string             | 선택 사항 | 스타일 유형(`TableStyleLight`, `TableStyleMedium` 등).                         |
| **ListColumns**                                  | object 배열         | 선택 사항 | 열 정의 모음(`Name`, `TotalsCalculation`).                                     |
| **Sorter**, **AutoFilter**, **ShowTableStyle…** | object             | 선택 사항 | 고급 스타일링 및 필터링 옵션(자세한 내용은 OpenAPI 명세서 참조).                |

### 최소 예제 페이로드

```json
{
  "DisplayName": "SalesData",
  "Range": "A1:E20",
  "ShowHeaderRow": true,
  "ShowTotals": false
}
```

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}
```

### **요청 매개변수**

| 매개변수 이름        | 유형    | 위치  | 설명                                     |
| ------------------- | ------- | ----- | ---------------------------------------- |
| **name**            | string  | path  | 문서 이름.                               |
| **sheetName**       | string  | path  | 워크시트 이름.                           |
| **listObjectIndex** | integer | path  | 업데이트할 목록 개체의 인덱스.            |
| **listObject**      | object  | body  | 요청 본문에 포함된 ListObject DTO.        |
| **folder**          | string  | query | 문서가 포함된 폴더.                       |
| **storageName**     | string  | query | 스토리지 이름.                            |

[OpenAPI 명세서](https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObject)는 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

### 요청

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet7/listobjects/0" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
    "DisplayName": "SalesData",
    "Range": "A1:E20",
    "ShowHeaderRow": true,
    "ShowTotals": false,
    "ListColumns": [
      { "Name": "Product", "TotalsCalculation": "None" },
      { "Name": "Quantity", "TotalsCalculation": "Sum" },
      { "Name": "Price", "TotalsCalculation": "Average" }
    ]
  }'
```

{{< /tab >}}

### 응답

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

성공적인 응답은 다음 필드를 포함합니다:

| 필드                        | 유형   | 설명                                           |
| --------------------------- | ------ | ---------------------------------------------- |
| Code                        | integer| HTTP 상태 코드(성공 시 200).                    |
| Status                      | string | 상태에 대한 텍스트 설명.                        |
| UpdatedObject *(선택 사항)* | object | 수정된 속성을 포함하는 업데이트된 `ListObject` 표현. |

{{< /tab >}}

{{< /tabs >}}

## 오류 응답

| HTTP 코드 | 설명                                                           | 샘플 페이로드                                            |
| --------- | -------------------------------------------------------------- | -------------------------------------------------------- |
| **400**   | 잘못된 요청 – 필수 필드 누락 또는 JSON 형식 오류.              | `{ "Code": 400, "Message": "Invalid request body." }`    |
| **401**   | 인증 실패 – JWT 토큰 누락 또는 유효하지 않음.                   | `{ "Code": 401, "Message": "Authentication failed." }`   |
| **404**   | 찾을 수 없음 – 지정된 워크북, 워크시트 또는 목록 개체가 없음. | `{ "Code": 404, "Message": "Resource not found." }`      |
| **500**   | 내부 서버 오류 – 서버 측에서 예기치 않은 조건 발생.             | `{ "Code": 500, "Message": "Server error." }`            |

## FAQ

<details>  
<summary>Aspose.Cells Cloud API를 사용하여 목록 개체를 어떻게 업데이트하나요?</summary>

`POST /cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}` 엔드포인트를 사용합니다. 요청 본문에 변경하려는 속성(예: `DisplayName`, `ShowHeaderRow`)을 JSON으로 포함합니다. `Authorization` 헤더에 JWT 토큰을 사용하여 인증합니다.

</details>

<details>  
<summary>업데이트가 성공하면 어떤 응답을 받을 수 있나요?</summary>

`Code: 200` 및 `Status: "OK"`가 포함된 JSON 객체가 반환됩니다. 오류가 발생하면 적절한 HTTP 상태 코드와 문제를 설명하는 `Error` 객체가 포함된 응답이 반환됩니다.

</details>

<details>  
<summary>목록 개체 속성의 일부만 업데이트할 수 있나요?</summary>

네. 요청 본문에 수정하려는 필드만 포함하면 되며, 생략된 필드는 변경되지 않습니다.

</details>

## 관련 문서

- [목록 개체 추가](https://docs.aspose.cloud/cells/list-objects/add/)
- [목록 개체 조회](https://docs.aspose.cloud/cells/list-objects/get/)
- [목록 개체 삭제](https://docs.aspose.cloud/cells/list-objects/delete/)

## 클라우드 SDK 패밀리

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObject.go" >}}

{{< /tab >}}

{{< /tabs >}}