---
title: "특정 문서 속성 삭제"
second_title: "문서"
linktitle: "삭제"
type: docs
url: /ko/document-properties/delete/
aliases: [  /ko/remove-a-particular-document-property/ ]
keywords: "Aspose.Cells, 문서 속성 삭제, 엑셀 메타데이터 API, REST, 클라우드 SDK, cURL 예제"
description: "Aspose.Cells Cloud REST API v3.0을 사용하여 엑셀 워크북에서 특정 문서 속성을 삭제합니다. C#, Java, Python 등 다양한 언어의 cURL 및 SDK 예제를 포함합니다."
weight: 50
---

이 REST API는 워크북에서 문서 속성을 삭제합니다.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}
```

### 요청 매개변수

| 매개변수 이름 | 유형   | 위치 | 필수 여부 | 설명                                      |
| ------------- | ------ | ---- | --------- | ----------------------------------------- |
| name          | string | path | 예        | 엑셀 워크북의 이름입니다.                 |
| propertyName  | string | path | 예        | 삭제할 문서 속성의 이름입니다.            |
| folder        | string | query| 아니요    | 워크북이 저장되어 있는 폴더 경로입니다.   |
| storageName   | string | query| 아니요    | 스토리지 서비스의 이름입니다.             |

[OpenAPI 스펙](https://apireference.aspose.cloud/cells/#/Properties/DeleteDocumentProperty)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 통신을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API로 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties/author" \
     -X DELETE \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <jwt token>"
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

### 오류 응답

| HTTP 상태 코드 | 설명                                                           | 예시 JSON                                                    |
| -------------- | -------------------------------------------------------------- | ------------------------------------------------------------ |
| 400            | 잘못된 요청 – 필수 매개변수 누락 또는 유효하지 않은 값.        | `{"Code":400,"Message":"필수 매개변수 'name'이(가) 누락되었습니다."}` |
| 401            | 인증되지 않음 – 잘못되거나 누락된 JWT 토큰.                    | `{"Code":401,"Message":"잘못된 액세스 토큰입니다."}`         |
| 404            | 찾을 수 없음 – 워크북 또는 지정된 속성이 존재하지 않음.        | `{"Code":404,"Message":"문서 속성을 찾을 수 없습니다."}`    |
| 500            | 내부 서버 오류 – 서버에서 예기치 않은 조건이 발생함.           | `{"Code":500,"Message":"예기치 않은 오류가 발생했습니다."}`  |

## 클라우드 SDK 패밀리

SDK를 사용하면 개발 속도를 극대화할 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스로 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDocumentProperty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDocumentProperty.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDocumentProperty.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDocumentProperty.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteDocumentProperty.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDocumentProperty.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDocumentProperty.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDocumentProperty.go" >}}

{{< /tab >}}

{{< /tabs >}}