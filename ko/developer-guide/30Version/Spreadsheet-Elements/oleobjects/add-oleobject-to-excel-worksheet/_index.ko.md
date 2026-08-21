---
title: "Excel 워크시트에 OLE 개체 추가"
second_title: "문서"
linktitle: "OLE 개체 추가"
type: docs
url: /ko/oleobjects/add/
aliases: [/add-oleobject-to-excel-worksheet/]
keywords: "OLE 개체 추가, Excel, Aspose.Cells Cloud, REST API, SDK"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트에 OLE 개체를 추가합니다. 이 API는 C#, Java, PHP, Ruby, Node.js, Python, Perl, Go SDK를 통해 직접 또는 SDK를 통해 호출할 수 있습니다."
ArticleTitle: "Aspose.Cells Cloud API를 사용하여 Excel 워크시트에 OLE 개체 추가"
weight: 20
---

Aspose.Cells Cloud API는 Excel 워크북의 프로그래밍 방식 조작을 가능하게 하며, Word 문서, PDF 또는 기타 바이너리 파일과 같은 OLE 개체를 워크시트에 직접 삽입할 수 있는 기능을 제공합니다.

이 REST API는 Excel 워크시트에 **OLE 개체**를 추가합니다.

**필수 조건** – 유효한 JWT 인증 토큰이 있어야 하며, `oleFile` 또는 `imageFile`에서 참조하는 소스 파일은 엔드포인트를 호출하기 전에 지정된 저장소 위치에 업로드되어 있어야 합니다.

## PutWorksheetOleObject API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름    | 유형    | 위치 | 설명                                             |
| ---------------- | ------- | ---- | ------------------------------------------------ |
| name             | string  | path | 워크북 파일 이름.                                |
| sheetName        | string  | path | 워크시트 이름.                                   |
| oleObject        | object  | body | OLE 개체 정의.                                   |
| upperLeftRow     | integer | query | 상단 왼쪽 코너의 행 인덱스 (기본값 0).            |
| upperLeftColumn  | integer | query | 상단 왼쪽 코너의 열 인덱스 (기본값 0).           |
| height           | integer | query | OLE 개체의 높이 (기본값 0).                      |
| width            | integer | query | OLE 개체의 너비 (기본값 0).                      |
| oleFile          | string  | query | OLE 소스 파일 이름.                              |
| imageFile        | string  | query | 미리보기 이미지 파일 이름.                       |
| folder           | string  | query | 워크북이 포함된 폴더.                            |
| storageName      | string  | query | 사용할 저장소 이름.                              |

**참고** – `upperLeftRow` 및 `upperLeftColumn`은 0부터 시작하는 인덱스를 사용합니다. `oleFile`(및 선택적으로 `imageFile`)은 대상 저장소에 미리 존재해야 하며, 그렇지 않으면 요청이 오류를 반환합니다.

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/OleObjects/PutWorksheetOleObject)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

**cURL** 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스를 호출할 수 있습니다. 아래 예제는 cURL을 사용하여 OLE 개체를 추가하는 방법을 보여줍니다. **모든 프로덕션 호출에는 HTTPS가 필요합니다.**

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/oleobjects" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"ImageSourceFullName":"aspose-logo.png", "IsAutoSize":true, "SourceFullName":"Sample_Book2.xls", "UpperLeftRow":15, "Top":10, "UpperLeftColumn":5, "Left":10, "Width":400, "Height":400}'
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

![Excel 워크시트에 삽입된 OLE 개체를 보여주는 스크린샷](/cells/images/ole-object-example.png)

**가능한 HTTP 상태 코드**

| 코드 | 설명                                           |
|------|------------------------------------------------|
| 200  | OLE 개체가 성공적으로 추가되었습니다.          |
| 400  | 잘못된 요청 – 누락되거나 잘못된 매개변수.       |
| 401  | 인증 실패 – 잘못되거나 누락된 JWT 토큰.         |
| 404  | 찾을 수 없음 – 워크북, 워크시트 또는 소스 파일이 존재하지 않음. |
| 500  | 내부 서버 오류 – 예기치 않은 실패.              |

일반적인 성공 응답은 다음과 같은 JSON 페이로드를 반환합니다:

```json
{
  "Code": 200,
  "Status": "OK",
  "Data": {
    "OleObjectId": "12345",
    "UpperLeftRow": 15,
    "UpperLeftColumn": 5,
    "Width": 400,
    "Height": 400,
    "SourceFullName": "Sample_Book2.xls",
    "ImageSourceFullName": "aspose-logo.png"
  }
}
```

## 클라우드 SDK 패밀리

SDK를 사용하면 개발 속도가 빨라집니다. SDK는 저수준 세부 사항을 추상화하여 비즈니스 로직에 집중할 수 있도록 도와줍니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}