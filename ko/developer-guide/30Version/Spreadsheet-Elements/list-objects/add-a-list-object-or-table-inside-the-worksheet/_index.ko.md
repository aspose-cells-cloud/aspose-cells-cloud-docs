---
title: "Excel 워크시트에 목록 개체(테이블) 추가"
second_title: "문서"
linktitle: "추가"
type: docs
url: /ko/list-objects/add/
aliases: [  /ko/add-a-list-object-or-table-inside-the-worksheet/ , /ko/tables/add/ ]
keywords: "Aspose.Cells Cloud, Excel API, 목록 개체, 테이블, REST API, 워크시트"
description: "Aspose.Cells Cloud REST API를 사용하여 워크시트에 목록 개체(Excel 테이블)를 추가하는 방법을 알아보세요. 엔드포인트, 매개변수, 인증 단계, cURL 예제 및 SDK 코드 샘플 포함."
weight: 10
ArticleTitle: "Excel 워크시트에 목록 개체(테이블) 추가 – Aspose.Cells Cloud 문서"
---

이 REST API는 Excel 워크시트에 **목록 개체(테이블)** 를 추가합니다.

이 엔드포인트를 사용하기 전에 유효한 JWT 토큰을 보유하고 있으며, 워크북이 지원되는 클라우드 저장소에 저장되어 있고 워크시트가 존재하는지 확인하십시오.

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects
```

### 요청 매개변수

| 매개변수 이름   | 유형    | 위치   | 설명                                                      |
| --------------- | ------- | ------ | --------------------------------------------------------- |
| **name**        | string  | path   | 워크북 파일 이름.                                         |
| **sheetName**   | string  | path   | 워크시트 이름.                                            |
| **startRow**    | integer | query  | 테이블 범위의 첫 번째 행(0부터 시작하는 인덱스).            |
| **startColumn** | integer | query  | 테이블 범위의 첫 번째 열(0부터 시작하는 인덱스).           |
| **endRow**      | integer | query  | 테이블 범위의 마지막 행(0부터 시작하는 인덱스).             |
| **endColumn**   | integer | query  | 테이블 범위의 마지막 열(0부터 시작하는 인덱스).            |
| **hasHeaders**  | boolean | query  | 첫 번째 행에 열 제목이 포함되어 있으면 `true`, 그렇지 않으면 `false`. |
| **listObject**  | object  | body   | 목록 개체 정의(참조: **요청 본문 스키마**).              |
| **folder**      | string  | query  | 워크북이 포함된 폴더.                                     |
| **storageName** | string  | query  | 저장소 이름.                                              |

### 요청 본문 스키마

**listObject** 개체는 생성될 테이블을 설명합니다. 가장 일반적인 속성만 표시되며, 전체 목록은 OpenAPI 사양을 참조하십시오.

```json
{
  "displayName": "MyTable",
  "showTotals": false,
  "style": "TableStyleMedium2"
}
```

### 예제 요청(cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects?startRow=1&startColumn=1&endRow=10&endColumn=12&hasHeaders=true" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "displayName": "MyTable",
        "showTotals": false,
        "style": "TableStyleMedium2"
      }'
```

### 예제 응답

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### 오류 코드

| HTTP 상태 코드 | 이유                  | 설명                                           |
| -------------- | --------------------- | ---------------------------------------------- |
| **400**        | Bad Request           | 잘못된 범위 매개변수 또는 잘못된 형식의 JSON 본문. |
| **401**        | Unauthorized          | JWT 토큰 누락 또는 만료.                        |
| **404**        | Not Found             | 지정된 워크북 또는 워크시트가 존재하지 않음.     |
| **500**        | Internal Server Error | 예기치 않은 서버 측 오류.                       |

**400 응답 예제**

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "Invalid range parameters."
}
```

**401 응답 예제**

```json
{
  "Code": 401,
  "Status": "Unauthorized",
  "Message": "Authentication token is missing or expired."
}
```

이 작업의 전체 계약은 [OpenAPI 사양](https://apireference.aspose.cloud/cells/#/ListObjects/PutWorksheetListObject)에서 확인할 수 있습니다.

## 클라우드 SDK 패밀리

SDK를 사용하면 개발 속도를 높이는 데 가장 좋습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. [GitHub 저장소](https://github.com/aspose-cells-cloud)에서 Aspose.Cells Cloud SDK 전체 목록을 확인하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetListObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetListObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetListObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetListObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetListObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetListObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetListObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetListObject.go" >}}

{{< /tab >}}

{{< /tabs >}}