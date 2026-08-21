---
title: "Excel 워크북에 디지털 서명 추가"
ArticleTitle: "Excel 워크북에 디지털 서명 추가 – Aspose.Cells Cloud API"
second_title: "문서"
linktype: "docs"
url: /excel-digital-signature/
aliases:
  - /protect/digital-signature/
  - /workbook/digital-signature/
keywords: "Aspose.Cells Cloud, 디지털 서명, Excel 워크북, REST API, .pfx, JWT, signature API"
description: "Aspose.Cells Cloud REST API(v4.0)를 사용하여 Excel 워크북에 디지털 서명을 추가하는 방법을 알아보세요. 엔드포인트, 매개변수, 인증, 응답 스키마, 오류 처리 및 여러 언어의 SDK 예제를 포함합니다."
weight: 35
---


**사전 조건:**  
이 엔드포인트를 호출하기 전에 다음 사항을 확인하세요:

- Aspose Cloud 인증을 통해 유효한 JWT 액세스 토큰을 획득했는지 확인하세요.  
- 대상 워크북이 Aspose Cloud 저장소에 업로드되어 있는지 확인하세요.  
- `.pfx` 또는 `.p12` 형식의 디지털 서명 파일과 그 비밀번호를 준비하세요.

이 REST API는 Excel 워크북에 **디지털 서명**을 추가합니다.

## PostDigitalSignature API

```http
POST https://api.aspose.cloud/v4.0/cells/{name}/digitalsignature
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 적용되며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름           | 유형   | 위치                 | 설명                                                |
| ------------------------ | ------ | -------------------- | --------------------------------------------------- |
| **name**                 | string | `<code>path</code>`  | 워크북의 이름입니다.                                |
| **digitalsignaturefile** | string | `<code>query</code>` | 디지털 서명 파일(`.pfx` 또는 `.p12`)의 경로입니다. |
| **password**             | string | `<code>query</code>` | 워크북이 보호되어 있는 경우의 비밀번호입니다.       |
| **folder**               | string | `<code>query</code>` | 워크북이 저장된 폴더입니다.                         |
| **storageName**          | string | `<code>query</code>` | 사용할 저장소 서비스의 이름입니다.                  |

*참고: 파일 이름에 특수문자가 포함된 경우, 쿼리 문자열에 추가하기 전에 URL 인코딩을 수행해야 합니다.*

### 오류 처리

| HTTP 상태 코드 | 의미                                                   |
| -------------- | ------------------------------------------------------ |
| 200            | 서명이 성공적으로 적용되었습니다.                      |
| 400            | 잘못된 요청 – 누락되었거나 잘못된 매개변수입니다.      |
| 401            | 인증되지 않음 – 유효하지 않거나 만료된 OAuth 토큰입니다. |
| 403            | 접근 거부 – 권한이 부족하거나 접근이 거부되었습니다.    |
| 500            | 내부 서버 오류 – 예기치 않은 실패입니다.               |

### HTTP 상태 코드 오류 응답

| HTTP 상태 코드 | 코드                | 설명                                                 |
| -------------- | ------------------- | ---------------------------------------------------- |
| 400            | BadRequest          | 누락되었거나 잘못된 매개변수입니다.                   |
| 401            | Unauthorized        | 유효하지 않거나 누락된 액세스 토큰입니다.             |
| 404            | NotFound            | 지정된 폴더/저장소에서 워크북을 찾을 수 없습니다.     |
| 500            | InternalServerError | 예기치 않은 서버 오류입니다.                          |


## SDK를 사용하여 PostDigitalSignature API 사용하기

### PostDigitalSignature API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Protection/PostDigitalSignature)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스를 호출할 수 있습니다. 아래 예제는 API에 대한 요청을 보여줍니다:

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/digitalsignature?digitalsignaturefile=signature.pfx&password=YourPassword" \
  -X POST \
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

**응답 스키마**  
API는 다음 필드를 포함하는 JSON 객체를 반환합니다:

| 필드          | 유형   | 설명                                               |
| ------------- | ------ | -------------------------------------------------- |
| `Code`        | int    | 결과를 나타내는 HTTP 유사 상태 코드입니다.         |
| `Status`      | string | 결과를 설명하는 짧은 텍스트(예: `OK`)입니다.      |
| `SignatureId` | string | 적용된 디지털 서명의 식별자입니다 (선택 사항).     |
| `Message`     | string | 추가 정보 또는 오류 세부 정보입니다 (선택 사항).   |

### Aspose.Cells Cloud SDK 사용하기

SDK를 사용하면 통합이 간편해지고 보일러플레이트 코드가 줄어듭니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostDigitalSignature.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostDigitalSignature.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostDigitalSignature.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostDigitalSignature.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82a2de2e4189bc27ae92abf73c36b4df0" "Example_PostDigitalSignature.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostDigitalSignature.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostDigitalSignature.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostDigitalSignature.go" >}}

{{< /tab >}}

{{< /tabs >}}