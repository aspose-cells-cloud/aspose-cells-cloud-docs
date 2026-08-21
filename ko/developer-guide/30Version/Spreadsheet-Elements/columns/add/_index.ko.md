---
title: "Excel 워크시트에 빈 열 추가하기 - Aspose.Cells Cloud API"
second_title: "문서"
linktitle: "열 추가"
type: docs
url: /ko/columns/add/
aliases:
  - /add-an-empty-column-in-an-excel-worksheet/
  - /add-an-empty-column-in-a-worksheet/
keywords: "추가, 열, Excel, API, Aspose.Cells, 클라우드, REST, 삽입"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 시트에 새 열을 삽입하는 방법을 알아보세요. 요청 구문, cURL 예제, SDK 코드 예제 포함."
weight: 20
ArticleTitle: "Aspose.Cells Cloud API를 사용하여 Excel 워크시트에 빈 열 추가하기"
---

이 REST API는 워크시트에 하나 이상의 열을 삽입합니다.

**사전 요구 사항**  
이 엔드포인트를 호출하기 전에 다음 단계를 완료했는지 확인하세요:

- 유효한 OAuth 2.0 액세스 토큰을 획득하고 `Authorization` 헤더에 포함하세요.  
- 대상 워크북을 선택한 스토리지(기본값 = “Default”)에 저장하거나 적절한 `folder` 및 `storageName` 매개변수를 지정하세요.  
- `sheetName`에 제공된 워크시트 이름이 워크북에 실제로 존재하는지 확인하세요.

## PutInsertWorksheetColumns API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}?totalColumns=1
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 구현되었으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름       | 유형    | 위치 | 설명                                                         |
| -------------------- | ------- | ------ | ------------------------------------------------------------ |
| **name**             | string  | path   | 워크북 파일 이름.                                            |
| **sheetName**        | string  | path   | 워크시트 이름.                                               |
| **columnIndex**      | integer | path   | 열 삽입이 시작되는 열의 0부터 시작하는 인덱스.               |
| **totalColumns**     | integer | query  | 삽입할 열의 수.                                              |
| **updateReference**  | boolean | query  | **true**인 경우, 셀 참조가 삽입을 반영하도록 업데이트됨.     |
| **folder**           | string  | query  | 워크북이 포함된 폴더 경로.                                   |
| **storageName**      | string  | query  | 스토리지 서비스 이름.                                        |

**참고 사항**

- `columnIndex`는 워크시트의 현재 열 수 범위 내(0부터 현재 열 수 미만)여야 합니다. 기존 범위를 초과하여 삽입할 경우 시트가 자동으로 확장됩니다.  
- 여러 열(`totalColumns` > 1)을 삽입하면 기존 열이 오른쪽으로 이동합니다.  
- `updateReference` 플래그의 기본값은 `false`입니다. 수식 및 이름 지정된 범위를 업데이트하려면 `true`로 설정하세요.

[OpenAPI 사양서](https://apireference.aspose.cloud/cells/#/Cells/PutInsertWorksheetColumns)는 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스를 호출할 수 있습니다. 다음 예제는 인증 및 올바른 경로 매개변수를 포함한 전체 요청을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/1?totalColumns=1&updateReference=true" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: application/json"
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

**응답 코드**

| 코드 | 설명                                         |
|------|----------------------------------------------|
| 200  | 열이 성공적으로 삽입되었습니다.               |
| 400  | 잘못된 요청 — 누락되거나 잘못된 매개변수.     |
| 401  | 인증되지 않음 — 잘못되거나 누락된 토큰.       |
| 404  | 워크북 또는 워크시트를 찾을 수 없습니다.     |
| 500  | 내부 서버 오류.                               |

**예시 오류 응답**

```json
// 400 Bad Request – 누락되거나 잘못된 매개변수
{
  "Code": 400,
  "Message": "Invalid parameter: totalColumns must be a positive integer."
}

// 401 Unauthorized – 잘못되거나 누락된 토큰
{
  "Code": 401,
  "Message": "Authentication failed. Access token is missing or invalid."
}

// 404 Not Found – 워크북 또는 워크시트가 존재하지 않음
{
  "Code": 404,
  "Message": "Workbook 'test.xlsx' not found."
}

// 500 Internal Server Error
{
  "Code": 500,
  "Message": "An unexpected error occurred on the server."
}
```

## 클라우드 SDK 패밀리

SDK를 사용하면 가장 빠르게 개발할 수 있습니다. SDK가 저수준 세부 사항을 처리하므로 프로젝트 로직에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 저장소</a>를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutInsertWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutInsertWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutInsertWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutInsertWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutInsertWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutInsertWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutInsertWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutInsertWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}