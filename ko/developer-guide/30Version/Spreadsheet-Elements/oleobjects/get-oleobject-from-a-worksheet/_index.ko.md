---
title: "Excel 워크시트에서 OLE 개체 가져오기 – Aspose.Cells Cloud API"
second_title: "문서"
linktitle: "가져오기"
type: docs
url: /ko/oleobjects/get/
aliases: [/get-oleobject-from-a-worksheet/]
keywords: "aspose, cells, ole 개체, excel, 워크시트, ole 개체 가져오기, rest api"
description: "Aspose.Cells Cloud REST API를 사용하여 워크시트에서 OLE 개체(이미지, 차트 또는 포함된 파일)를 검색합니다. HTTPS 엔드포인트, 필수 매개변수, 샘플 cURL 및 여러 언어의 SDK 코드 포함."
ArticleTitle: "Excel 워크시트에서 OLE 개체 가져오기 – Aspose.Cells Cloud API"
weight: 10
---

이 REST API는 Excel 워크시트에서 **OLE 개체**를 검색합니다.

## 보안 및 인증
Aspose.Cells Cloud API는 보안이 유지되며, [JWT 토큰 기반 인증](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)이 필요합니다.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}?format={format}
```

### 요청 매개변수

| 매개변수 이름 | 유형    | 위치 | 설명                                                       |
| ------------- | ------- | ---- | ----------------------------------------------------------- |
| name          | string  | path | 문서 이름.                                                  |
| sheetName     | string  | path | 워크시트 이름.                                              |
| objectNumber  | integer | path | 워크시트 내 개체 번호.                                      |
| format        | string  | query | 개체의 원하는 내보내기 형식(예: `png`, `jpeg`).             |
| folder        | string  | query | 문서가 포함된 폴더.                                         |
| storageName   | string  | query | 사용할 스토리지 이름.                                       |

### 스토리지 옵션

- **folder** – 워크북이 위치한 기본 스토리지의 하위 폴더를 지정합니다.
- **storageName** – 워크북이 다른 위치에 저장된 경우 기본 스토리지 이름을 재정의합니다.

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/OleObjects/GetWorksheetOleObject)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

**cURL** 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스를 호출할 수 있습니다. 아래 예제는 OLE 개체를 PNG 이미지로 요청하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

### 바이너리 이미지 응답

`format`을 이미지 형식(`png` 등)으로 설정하면 API는 다음 헤더와 함께 바이너리 이미지 데이터를 반환합니다:

```
Content-Type: image/png
```

_(이미지 파일은 클라이언트에 직접 스트리밍됩니다.)_

### JSON 메타데이터 응답

`format`이 생략되거나 `json`으로 설정된 경우, API는 OLE 개체를 설명하는 JSON 페이로드를 반환합니다:

```json
{
  "Code": 200,
  "Status": "OK",
  "OLEObject": {
    "Name": "Object1",
    "Width": 200,
    "Height": 150,
    "Left": 10,
    "Top": 20,
    "IsLocked": false,
    "FileFormat": "png"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

## 오류 응답

| HTTP 상태 코드 | 오류 코드   | 설명                                     |
| -------------- | ----------- | ----------------------------------------- |
| 400            | BadRequest  | 누락되거나 잘못된 매개변수.               |
| 401            | Unauthorized | 잘못되거나 누락된 JWT 토큰.               |
| 404            | NotFound    | 워크북, 워크시트 또는 OLE 개체를 찾을 수 없음. |
| 500            | ServerError | 예기치 않은 서버 오류.                    |

**예시 404 응답**

```json
{
  "Code": 404,
  "Status": "NotFound",
  "Message": "워크시트 'Sheet1'에서 번호 0인 요청된 OLE 개체를 찾을 수 없습니다."
}
```

## 클라우드 SDK 패밀리
SDK를 사용하는 것이 API를 통합하는 가장 빠른 방법입니다. SDK는 저수준 세부 사항을 처리하므로 비즈니스 로직에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}