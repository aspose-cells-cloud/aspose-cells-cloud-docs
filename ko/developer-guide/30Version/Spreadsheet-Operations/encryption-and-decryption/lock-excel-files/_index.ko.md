---
title: "엑셀 파일 잠금"
second_title: "문서"
linktitle: "엑셀 파일 잠금"
type: docs
url: /ko/lock-excel-files/
aliases: [  /ko/lock/without-storage/ , /ko/lock/ , /ko/lock/without-using-storage/ ]
keywords: "잠금, 엑셀, API, Aspose.Cells, 클라우드, REST, 워크북, 스프레드시트, SDK"
description: "Aspose.Cells Cloud REST API(v3.0)를 사용하여 엑셀 워크북을 잠그는 방법을 알아보세요. HTTPS 엔드포인트, 인증, cURL 요청, 응답 스키마, C#, Java, Python 등 다양한 언어의 SDK 코드 예제가 포함됩니다."
ArticleTitle: "엑셀 파일 잠금 – Aspose.Cells Cloud API 문서"
weight: 70
---

**API 버전:** v3.0(현재 버전)

이 REST API는 **엑셀 워크북을 잠급니다**.

## PostLock API

```http
POST https://api.aspose.cloud/v3.0/cells/lock
```

**필수 조건** – 요청은 **HTTPS**를 통해 전송되어야 하며, `Authorization` 헤더에 유효한 OAuth 2.0 Bearer 토큰이 포함되어야 합니다.

### 요청 파라미터

| 파라미터 이름 | 유형   | 위치                     | 설명                                    |
| ------------- | ------ | ------------------------ | --------------------------------------- |
| file          | 파일   | form-data(멀티파트 본문) | 업로드 및 잠그려는 엑셀 워크북.         |
| password      | 문자열 | 쿼리 문자열              | 워크북 비밀번호(선택 사항).             |

<a href="https://apireference.aspose.cloud/cells/#/LightCells/PostLock" target="_blank" rel="noopener noreferrer">OpenAPI 사양</a>은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용해 클라우드 API를 **호출**하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/lock?password=123456" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access_token>" \
  -F "file=@Sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "Sample.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

*요청을 테스트하려면 샘플 워크북 — [Sample.xlsx](https://example.com/Sample.xlsx) — 을 다운로드할 수 있습니다.*

**참고:** API는 최대 100MB 크기의 파일을 지원합니다. 더 큰 크기의 페이로드는 413(Payload Too Large) 응답이 반환될 수 있습니다.

### **응답 세부 정보**

| 필드          | 유형             | 설명                                      |
| ------------- | ---------------- | ----------------------------------------- |
| Filename      | string           | 서비스에서 반환된 잠긴 워크북의 이름.     |
| FileSize      | integer          | 잠긴 파일의 크기(바이트 단위).            |
| FileContent   | string (Base64)  | Base64로 인코딩된 잠긴 워크북.            |

잠긴 워크북을 가져오려면, 응답에 포함된 `FileContent` 값을 Base64에서 디코딩하고 `Filename`을 사용해 저장합니다.

### **오류 처리**

– API는 표준 HTTP 상태 코드(`400 Bad Request`, `401 Unauthorized`, `500 Internal Server Error` 등)와 함께 `Code` 및 `Message` 필드를 포함하는 JSON 오류 객체를 반환합니다.

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 작업에 집중할 수 있도록 도와줍니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostLock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostLock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostLock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostLock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostLock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostLock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostLock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostLock.go" >}}

{{< /tab >}}

{{< /tabs >}}