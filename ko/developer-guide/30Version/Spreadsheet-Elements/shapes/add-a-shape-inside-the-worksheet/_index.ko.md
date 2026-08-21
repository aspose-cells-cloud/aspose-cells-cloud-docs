---
title: "Excel 워크시트에 도형 추가"
second_title: "문서"
linktype: "추가"
type: docs
url: /shapes/add/
aliases: [/add-a-shape-inside-the-worksheet/]
keywords: "Aspose.Cells, 도형 추가, Excel, REST API, 클라우드 SDK, shapeDTO, 드로잉 유형"
description: "Aspose.Cells Cloud REST API v3.0을 사용하여 Excel 워크시트에 도형(호선, 선, 사각형 등)을 추가하는 방법을 배웁니다. 요청 구문, 필요한 매개변수, 인증 단계 및 샘플 SDK 코드가 포함됩니다."
weight: 30
ArticleTitle: "Aspose.Cells Cloud API를 사용하여 Excel 워크시트에 도형 추가"
---

이 REST API는 Excel 워크시트에 도형을 추가합니다.  
엔드포인트는 **API 버전 v3.0**에 속하며, Aspose Cloud OAuth2 흐름(client-id/client-secret)을 통해 획득한 JWT 액세스 토큰을 사용하고 `Authorization: Bearer <token>` 헤더에 포함시켜야 합니다.

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 우수하며 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

## PutWorksheetShape API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes
```

### **요청 매개변수**

| 매개변수 이름        | 유형     | 위치   | 설명                                                                                           |
| ------------------- | ------- | ------ | ---------------------------------------------------------------------------------------------- |
| name                | string  | path   | 문서 이름.                                                                                      |
| sheetName           | string  | path   | 워크시트 이름.                                                                                  |
| shapeDTO            | object  | body   | 추가할 도형을 설명하는 JSON 객체(전체 스키마는 OpenAPI 사양 참조).                             |
| drawingType         | string  | query  | 도형 개체 유형(예: `arc`, `line`, `rectangle`).                                                |
| upperLeftRow        | integer | query  | 도형의 왼쪽 위 행 인덱스.                                                                       |
| upperLeftColumn     | integer | query  | 도형의 왼쪽 위 열 인덱스.                                                                       |
| top                 | integer | query  | 도형의 상단 가장자리로부터의 수직 오프셋(픽셀 단위).                                            |
| left                | integer | query  | 도형의 왼쪽 가장자리로부터의 수평 오프셋(픽셀 단위).                                            |
| width               | integer | query  | 도형의 너비(픽셀 단위).                                                                         |
| height              | integer | query  | 도형의 높이(픽셀 단위).                                                                         |
| folder              | string  | query  | 문서가 포함된 폴더.                                                                             |
| storageName         | string  | query  | 스토리지 이름.                                                                                  |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Shapes/PutWorksheetShape)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예시는 cURL을 사용하여 클라우드 API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes?DrawingType=arc&upperLeftRow=1&upperLeftColumn=1&top=1&left=1&width=100&height=100" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "ShapeId": 5
}
```

_성공적인 응답은 HTTP 상태 코드, 텍스트 상태 및 새로 생성된 도형의 식별자(`ShapeId`)를 반환합니다._

{{< /tab >}}

{{< /tabs >}}

**HTTP 상태 코드**

| 코드 | 의미                   | 설명                                                    |
|------|------------------------|---------------------------------------------------------|
| 200  | OK                     | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함.   |
| 400  | Bad Request            | 누락되었거나 유효하지 않은 매개변수(예: 지원되지 않는 파일 유형). |
| 401  | Unauthorized           | 유효하지 않거나 누락된 JWT 토큰.                         |
| 413  | Payload Too Large      | 업로드된 파일이 크기 제한을 초과함.                      |
| 500  | Internal Server Error  | 예기치 않은 서버 오류.                                   |

일반적인 오류 응답은 다음과 같습니다:

- **400 Bad Request** – 누락되었거나 유효하지 않은 매개변수.  
- **401 Unauthorized** – 유효하지 않거나 누락된 JWT 토큰.  
- **404 Not Found** – 지정된 워크시트 또는 문서가 존재하지 않음.

각 오류는 `Code` 및 `Message` 필드가 포함된 JSON 객체로 반환됩니다.

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하십시오.

다음 코드 예시는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}