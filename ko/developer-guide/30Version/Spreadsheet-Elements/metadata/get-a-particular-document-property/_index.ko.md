---
title: "특정 문서 속성 가져오기"
second_title: "문서"
linktitle: "가져오기"
type: docs
url: /ko/document-properties/get/
aliases: [  /ko/get-a-particular-document-property/ ]
keywords: "Aspose.Cells, 클라우드 API, 문서 속성 가져오기, Excel 메타데이터, REST GET, SDK 예제"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 파일에서 특정 이름의 문서 속성(예: 작성자, 제목)을 검색합니다. cURL 예제, SDK 스니펫 및 응답 스키마가 포함됩니다."
weight: 20
---

이 REST API는 이름으로 문서 속성을 읽습니다.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}
```

### 요청 매개변수

| 매개변수 이름    | 타입     | 위치   | 설명                                            |
| ---------------- | -------- | ------ | ----------------------------------------------- |
| name             | string   | path   | Excel 파일의 이름입니다.                        |
| propertyName     | string   | path   | 검색할 문서 속성의 이름입니다.                  |
| folder           | string   | query  | 파일이 포함된 폴더(선택 사항)입니다.            |
| storageName      | string   | query  | 스토리지 이름(선택 사항)입니다.                 |

[OpenAPI 사양서](https://apireference.aspose.cloud/cells/#/Properties/GetDocumentProperty)는 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

**cURL 명령줄 도구**를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties/author" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt 토큰>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "DocumentProperty": {
    "Name": "Author",
    "Value": "",
    "BuiltIn": "True",
    "link": {
      "Href": "/test.xlsx/documentproperties/Author",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### 응답 세부정보

API에서 반환되는 JSON 객체는 다음 필드를 포함합니다:

| 필드                             | 타입    | 설명                                                         |
| -------------------------------- | ------- | ------------------------------------------------------------ |
| **DocumentProperty.Name**       | string  | 속성의 이름(예: `Author`)입니다.                             |
| **DocumentProperty.Value**      | string  | 속성의 값입니다. 설정되지 않았을 경우 빈 문자열일 수 있습니다. |
| **DocumentProperty.BuiltIn**    | boolean | 이 속성이 내장 Excel 속성인지를 나타냅니다.                  |
| **DocumentProperty.link.Href**  | string  | 속성 리소스에 대한 상대 URL입니다.                           |
| **DocumentProperty.link.Rel**   | string  | 관계 유형으로, 일반적으로 `self`입니다.                      |
| **DocumentProperty.link.Title** | string  | 사람이 읽을 수 있는 제목( null일 수 있음)입니다.             |
| **DocumentProperty.link.Type**  | string  | 링크된 리소스의 MIME 유형( null일 수 있음)입니다.            |
| **Code**                        | integer | 서비스에서 반환된 HTTP 상태 코드입니다.                       |
| **Status**                      | string  | 상태에 대한 텍스트 설명(예: `OK`)입니다.                     |

### 오류 응답

| HTTP 상태 코드 | 코드                   | 설명                                             |
| -------------- | ---------------------- | ------------------------------------------------ |
| 400            | `InvalidParameter`     | 하나 이상의 요청 매개변수가 유효하지 않습니다.     |
| 401            | `AuthenticationFailed` | JWT 토큰이 누락되었거나 유효하지 않습니다.         |
| 404            | `PropertyNotFound`     | 지정된 문서 속성이 존재하지 않습니다.              |
| 500            | `InternalError`        | 서버에서 예기치 않은 오류가 발생했습니다.        |

일반적인 오류 본문은 다음과 같습니다:

```json
{
  "Code": 404,
  "Status": "Property not found"
}
```

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 요청을 보내는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetDocumentProperty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetDocumentProperty.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetDocumentProperty.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetDocumentProperty.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetDocumentProperty.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetDocumentProperty.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetDocumentProperty.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetDocumentProperty.go" >}}

{{< /tab >}}

{{< /tabs >}}

### 용어 정의

| 용어                  | 정의                                                                                      |
| --------------------- | ----------------------------------------------------------------------------------------- |
| **문서 속성**         | Excel 워크북과 관련된 메타데이터 조각(예: 작성자, 제목, 생성일)입니다.                     |
| **메타데이터**        | 다른 데이터를 설명하는 데이터를 일반적으로 의미하며, 여기서는 문서 속성을 의미합니다.      |
| **사용자 정의 속성**  | 내장 속성 세트에 포함되지 않은 사용자가 정의한 속성입니다.                                 |

### 자주 묻는 질문

**Q:** _Aspose Cloud에 저장된 Excel 파일의 작성자 속성을 어떻게 검색할 수 있나요?_  
**A:** 유효한 Bearer 토큰을 포함하여 `https://api.aspose.cloud/v3.0/cells/{fileName}/documentproperties/author`에 GET 요청을 보냅니다. 응답 JSON에는 `DocumentProperty.Name = "Author"` 및 해당 `Value`가 포함됩니다.

**Q:** _요청한 속성이 존재하지 않을 경우 어떤 오류가 반환되나요?_  
**A:** API는 HTTP 404 상태 코드와 `Code: 404`, `Status: "Property not found"`를 포함하는 JSON 본문을 반환합니다.

**Q:** _파일이 기본 스토리지에 있을 경우 `storageName`을 지정해야 하나요?_  
**A:** 아닙니다. `storageName` 쿼리 매개변수는 선택 사항이며, 계정에 구성된 기본 스토리지를 사용하려면 생략하면 됩니다.

---