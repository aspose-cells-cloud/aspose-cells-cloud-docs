---
title: "엑셀 파일 보호"
second_title: "문서"
linktype: "엑셀 파일 암호화"
type: docs
url: /ko/protect-excel-files/
aliases:
  [
    "/protect/without-storage/",
    "/protect/without-using-storage/",
    "/protect/without-using-storage/",
  ]
keywords: "Aspose.Cells, 엑셀 보호 API, 엑셀 워크북 암호화, 클라우드 스프레드시트 보안, REST API"
description: "Aspose.Cells Cloud REST API를 사용하여 엑셀 파일을 보호하는 방법을 설명합니다. 이 가이드는 2026년 기준 HTTP POST, cURL 및 여러 프로그래밍 언어용 SDK를 통해 워크북을 암호화하는 방법을 보여줍니다."
weight: 40
---

이 REST API는 엑셀 파일을 보호합니다.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/protect
```

### 보안 및 인증

Aspose.Cells Cloud API는 보안이 적용되며 [JWT 토큰 기반 인증](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)이 필요합니다.

### 요청 매개변수

| 매개변수 이름 | 유형   | 위치                  | 설명                               |
| -------------- | ------ | ------------------------- | ------------------------------------- |
| file           | 파일   | formData (body)           | 업로드할 파일                        |
| password       | 문자열 | 쿼리 문자열 (`password`) | 워크북 보호에 사용되는 암호 |

### 응답


```json
{
  "Status":"OK",
  "Code":200,
  "Files": [
    {
      "Filename": "protected filename: smaple1.xlsx",
      "FileSize": size,
      "FileContent": "-----sample1의 Base64 문자열-----"
    },
    {
      "Filename": "protected filename: sample2.xlsx",
      "FileSize": size,
      "FileContent": "-----sample2의 Base64 문자열-----"
    }
  ]
}
```

**HTTP 상태 코드**

| 코드 | 의미                         | 설명                                             |
|------|-----------------------------|--------------------------------------------------|
| 200  | 성공 (OK)                   | 필터가 성공적으로 적용되었으며, 응답에 작업 세부 정보가 포함됩니다. |
| 400  | 잘못된 요청 (Bad Request)   | 누락되거나 유효하지 않은 매개변수(예: 지원되지 않는 파일 유형). |
| 401  | 인증되지 않음 (Unauthorized) | 잘못되거나 누락된 JWT 토큰. |
| 413  | 페이로드가 너무 큼 (Payload Too Large) | 업로드된 파일이 크기 제한을 초과합니다. |
| 500  | 내부 서버 오류 (Internal Server Error) | 예기치 않은 서버 오류. |

## SDK를 사용하여 PostProtect API 사용하는 방법

### PostProtect API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/LightCells/PostProtect)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/protect?password=MySecretPwd" \
  -X POST \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'file1=@sample1.xlsx' \
  -F 'file2=@sample2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "sample1.xlsx",
      "FileSize": 274022,
      "FileContent": "-----sample1의 Base64 문자열-----"
    },
    {
      "Filename": "sample2.xlsx",
      "FileSize": 274022,
      "FileContent": "-----sample2의 Base64 문자열-----"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### **오류 처리**

– API는 다음과 같은 상태 코드를 반환할 수 있습니다:

| HTTP 코드 | 의미                                      | 예시 JSON 오류 페이로드                             |
| --------- | ----------------------------------------- | --------------------------------------------------- |
| 400       | 잘못된 요청(예: 파일 누락)                | `{"Code":400,"Message":"File is required."}`        |
| 401       | 인증되지 않음(잘못되거나 누락된 토큰)     | `{"Code":401,"Message":"Invalid access token."}`    |
| 403       | 접근 거부(권한 부족)                      | `{"Code":403,"Message":"Access denied."}`           |
| 500       | 내부 서버 오류                            | `{"Code":500,"Message":"Unexpected server error."}` |

### Aspose.Cells Cloud SDK 사용하기

SDK를 사용하는 것이 가장 빠른 개발 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostProtect.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostProtect.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostProtect.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostProtect.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostProtect.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostProtect.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostProtect.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostProtect.go" >}}

{{< /tab >}}

{{< /tabs >}}