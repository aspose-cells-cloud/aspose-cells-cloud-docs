---
title: "Excel 워크시트에서 인덱스로 도형 가져오기"
second_title: "문서"
linktitle: "가져오기"
type: docs
url: /ko/shapes/get/
aliases: [  /ko/get-a-shape-by-index-inside-the-worksheet/ ]
keywords: "Aspose.Cells Cloud, Excel 도형 API, 인덱스로 도형 가져오기, 워크시트 도형, REST API, 도형 검색, Aspose.Cells SDK"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트에서 인덱스로 도형을 검색합니다. 요청 구문, 매개변수, 응답 세부정보 및 SDK 예제 포함."
weight: 20
ArticleTitle: "Excel 워크시트에서 인덱스로 도형 가져오기 – Aspose.Cells Cloud 문서"
---

이 REST API는 Excel 워크시트에서 도형(이미지 데이터 또는 메타데이터 포함)을 검색합니다.

## GetWorksheetShape API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes/{shapeindex}
```

**필수 조건**  
- 유효한 Aspose Cloud 엑세스 토큰(Bearer JWT).  
- 워크북은 Aspose Cloud 스토리지 또는 지정된 폴더에 저장되어 있어야 합니다.  

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 강화되었으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **요청 매개변수**

| 매개변수 이름 | 유형    | 위치 | 설명                                         |
| ------------- | ------- | ---- | --------------------------------------------- |
| name          | string  | path | Excel 문서 이름.                             |
| sheetName     | string  | path | 도형이 포함된 워크시트 이름.                 |
| shapeindex    | integer | path | 워크시트 내 도형의 0부터 시작하는 인덱스.    |
| folder        | string  | query | 문서가 저장된 폴더 경로.                    |
| storageName   | string  | query | 스토리지 서비스 이름.                        |

**참고:** `shapeindex`는 0부터 시작하며, 첫 번째 도형의 인덱스는 0입니다. 기본 스토리지를 사용하지 않는 경우, 워크북이 지정된 `folder` 및 `storageName`에 저장되어 있는지 확인하십시오.

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Shapes/GetWorksheetShape)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
# 수정된 엔드포인트 및 경로
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet4/shapes/1" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "Shape": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "Name": "string",
    "MsoDrawingType": "string",
    "AutoShapeType": "string",
    "Placement": "string",
    "UpperLeftRow": 0,
    "Top": 0,
    "UpperLeftColumn": 0,
    "Left": 0,
    "LowerRightRow": 0,
    "Bottom": 0,
    "LowerRightColumn": 0,
    "Right": 0,
    "Width": 0,
    "Height": 0,
    "X": 0,
    "Y": 0,
    "RotationAngle": 0,
    "HtmlText": "string",
    "Text": "string",
    "AlternativeText": "string",
    "TextHorizontalAlignment": "string",
    "TextHorizontalOverflow": "string",
    "TextOrientationType": "string",
    "TextVerticalAlignment": "string",
    "TextVerticalOverflow": "string",
    "IsGroup": true,
    "IsHidden": true,
    "IsLockAspectRatio": true,
    "IsLocked": true,
    "IsPrintable": true,
    "IsTextWrapped": true,
    "IsWordArt": true,
    "LinkedCell": "string",
    "ZOrderPosition": 0
  }
}
```

{{< /tab >}}

{{< /tabs >}}

**가능한 HTTP 상태 코드**

| 코드 | 설명 |
|------|------|
| **200 OK** | 도형이 성공적으로 검색되었습니다. |
| **400 Bad Request** | 요청이 잘못되었거나 필수 매개변수가 누락되었습니다. |
| **401 Unauthorized** | 인증에 실패했거나 토큰이 누락되었거나 유효하지 않습니다. |
| **404 Not Found** | 지정된 워크북, 워크시트 또는 도형 인덱스가 존재하지 않습니다. |
| **500 Internal Server Error** | 예기치 않은 서버 오류가 발생했습니다. |

**일반적인 실수:** 잘못된 기본 도메인(`api.aspose.com`) 또는 오래된 `/autoshapes/` 세그먼트를 사용하면 404 오류가 발생합니다. 항상 `api.aspose.cloud` 도메인과 `/shapes/` 세그먼트를 사용하십시오.

## Cloud SDK Family

SDK를 사용하면 개발 속도가 가장 빨라집니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}

관련 작업은 **[도형 추가](/shapes/add/)** 및 **[도형 업데이트](/shapes/update/)** 문서를 참조하십시오.