---
title: "엑셀 워크시트에서 OLE 개체 업데이트하기"
second_title: "문서"
linktitle: "업데이트"
type: docs
url: /ko/oleobjects/update/
aliases: [/update-a-specific-oleobject-from-excel-worksheet/]
keywords: "OLE 개체 업데이트, 엑셀, Aspose.Cells Cloud, REST API, SDK"
description: "Aspose.Cells Cloud REST API를 사용하여 엑셀 워크시트 내 OLE 개체(이미지, 차트 등)를 업데이트하는 방법을 알아보세요. cURL 및 SDK 예제, 인증 절차, 오류 처리가 포함됩니다."
weight: 30
author: "Aspose Cloud 문서 팀"
lastmod: "2024-03-01"
ArticleTitle: "엑셀 워크시트에서 OLE 개체 업데이트 – Aspose.Cells Cloud API 가이드"
---

이 REST API는 엑셀 워크시트 내 **OLE 개체**를 업데이트합니다.

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 적용되며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

## PostUpdateWorksheetOleObject API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}
```

요청 매개변수는 다음과 같습니다:

| 매개변수 이름     | 유형     | 매개변수 위치 | 설명                                                  |
| ---------------- | ------- | -------------- | ----------------------------------------------------- |
| name             | string  | path           | 워크북 이름.                                          |
| sheetName        | string  | path           | 워크시트 이름.                                        |
| oleObjectIndex   | integer | path           | 워크시트 내 OLE 개체의 인덱스.                        |
| ole              | object  | body           | 업데이트할 OLE 개체의 JSON 표현.                      |
| folder           | string  | query          | 워크북이 포함된 폴더.                                |
| storageName      | string  | query          | 스토리지 서비스 이름.                                 |

### 요청 본문 필드

| 필드                  | 유형      | 필수 여부 | 설명                                                     |
| -------------------- | -------- | --------- | -------------------------------------------------------- |
| ImageSourceFullName  | string   | 선택 사항 | OLE 개체에 사용되는 이미지 파일 경로.                   |
| IsAutoSize           | boolean  | 선택 사항 | OLE 개체를 자동 크기 조정할지 여부.                     |
| SourceFullName       | string   | 필수      | OLE 개체의 소스 파일(예: 이미지 또는 차트).             |
| UpperLeftRow         | integer  | 필수      | 왼쪽 상단 코너의 행 인덱스(0부터 시작).                 |
| UpperLeftColumn      | integer  | 필수      | 왼쪽 상단 코너의 열 인덱스(0부터 시작).                 |
| Left                 | integer  | 선택 사항 | 왼쪽 상단 코너로부터의 수평 오프셋(포인트 단위).         |
| Top                  | integer  | 선택 사항 | 왼쪽 상단 코너로부터의 수직 오프셋(포인트 단위).         |
| Width                | integer  | 필수      | OLE 개체의 너비(포인트 단위).                           |
| Height               | integer  | 필수      | OLE 개체의 높이(포인트 단위).                           |

[OpenAPI 사양서](https://apireference.aspose.cloud/cells/#/OleObjects/PostUpdateWorksheetOleObject)는 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

**cURL** 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/" \
  -X POST \
  -d '{"ImageSourceFullName":"aspose-logo.png","IsAutoSize":true,"SourceFullName":"Sample_Book2.xls","UpperLeftRow":15,"Top":10,"UpperLeftColumn":5,"Left":10,"Width":400,"Height":400}' \
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
  "OLEObject": {
    "Index": 0,
    "ImageSourceFullName": "aspose-logo.png",
    "IsAutoSize": true,
    "SourceFullName": "Sample_Book2.xls",
    "UpperLeftRow": 15,
    "UpperLeftColumn": 5,
    "Left": 10,
    "Top": 10,
    "Width": 400,
    "Height": 400
  }
}
```

{{< /tab >}}

{{< /tabs >}}

## 오류 응답

| HTTP 상태 코드 | 코드   | 메시지                                                       |
| -------------- | ------ | ------------------------------------------------------------ |
| 400            | 4000   | 잘못된 요청 – 누락되거나 유효하지 않은 매개변수.             |
| 401            | 4010   | 인증되지 않음 – 유효하지 않거나 누락된 JWT 토큰.             |
| 404            | 4040   | 찾을 수 없음 – 워크북, 워크시트 또는 OLE 개체가 존재하지 않음. |
| 500            | 5000   | 내부 서버 오류 – 서버 측에서 예기치 않은 실패 발생.          |

API는 응답 본문에 커스텀 **Code** 필드도 반환하며, 이는 HTTP 상태 코드와 매핑됩니다(예: 200 → 2000, 400 → 4000 등).

## 이 API를 언제 사용해야 하나요?

워크시트 전체를 다시 업로드하지 않고 기존 OLE 개체(임베딩된 이미지, 차트 또는 문서 등)를 수정해야 할 때 이 엔드포인트를 사용하세요. 일반적인 시나리오로는 이미지 소스 업데이트, 개체 크기 조정, 워크북 생성 후 위치 변경 등이 있습니다. 관련 작업은 [OLE 개체 추가](/ko/oleobjects/add/) 및 [OLE 개체 삭제](/ko/oleobjects/delete/)를 참조하세요.

## 클라우드 SDK 패밀리

SDK를 사용하면 개발 속도가 가장 빠릅니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트에 집중할 수 있도록 도와줍니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

아래는 Aspose.Cells Cloud SDK를 사용하여 OLE 개체를 업데이트하는 C# 예제입니다:

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var config = new Configuration
{
    AppSid = "<your-app-sid>",
    AppKey = "<your-app-key>"
};
var oleApi = new OleObjectsApi(config);
var request = new OleObjectUpdateRequest
{
    ImageSourceFullName = "aspose-logo.png",
    IsAutoSize = true,
    SourceFullName = "Sample_Book2.xls",
    UpperLeftRow = 15,
    UpperLeftColumn = 5,
    Left = 10,
    Top = 10,
    Width = 400,
    Height = 400
};

var response = oleApi.UpdateWorksheetOleObject("SampleBook.xlsx", "Sheet1", 0, request, folder: "myFolder");
Console.WriteLine($"상태: {response.Status}");
```

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUpdateWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUpdateWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUpdateWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUpdateWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUpdateWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUpdateWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUpdateWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUpdateWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}