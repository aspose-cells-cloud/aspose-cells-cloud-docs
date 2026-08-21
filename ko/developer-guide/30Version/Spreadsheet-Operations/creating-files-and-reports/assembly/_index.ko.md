---
title: "엑셀 보고서 생성을 위한 데이터 조합"
second_title: "문서"
linktype: "데이터 조합"
type: docs
url: /assembly-data-for-the-creation-of-an-excel-report/
aliases: [/assembly/]
keywords: "Aspose.Cells, 엑셀 보고서, 데이터 조합, 클라우드 API, REST, SDK, cURL, PDF, ODS"
description: "Aspose.Cells Cloud의 Assembly API를 사용하여 데이터를 엑셀(XLSX, PDF, ODS) 보고서에 병합하는 방법을 알아보세요. 엔드포인트, 매개변수, cURL 예제, SDK 코드, 인증 가이드 및 오류 처리를 포함합니다."
weight: 40
---

이 REST API는 데이터를 **엑셀 파일에 조합**합니다.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/assembly
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 위해 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수


| 매개변수 이름 | 유형   | 위치                      | 설명                                                            |
| ------------- | ------ | ------------------------- | -------------------------------------------------------------- |
| file          | 파일   | formData (multipart body) | 업로드할 스프레드시트 파일입니다.                              |
| DataSource    | 문자열 | 쿼리 스트링               | 조합에 사용할 데이터를 제공하는 데이터 소스의 식별자입니다.     |
| format        | 문자열 | 쿼리 스트링               | 원하는 출력 형식(예: `xlsx`, `pdf`)입니다.                      |

### **응답**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[file2 name]",
    "Filesize" : [파일 크기],
    "FileContent" : "[Base64String]"
}
```

**HTTP 상태 코드**

| 코드 | 의미                        | 설명                                               |
|------|-----------------------------|----------------------------------------------------|
| 200  | 성공                        | 필터가 성공적으로 적용되었으며, 응답에 작업 세부 정보가 포함됩니다. |
| 400  | 잘못된 요청                 | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식)입니다.     |
| 401  | 인증되지 않음               | 잘못되었거나 누락된 JWT 토큰입니다.                 |
| 413  | 요청 크기 초과              | 업로드된 파일이 크기 제한을 초과했습니다.          |
| 500  | 내부 서버 오류              | 예기치 않은 서버 오류입니다.                        |

## SDK를 사용한 PostAssemble API 사용 방법

### PostAssemble API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/LightCells/PostAssemble)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/assembly?DataSource=ds&format=pdf" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'template=@template.xlsx' \
  -F 'data=@data.json'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "report1",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "report2",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 API에 가장 빠르게 개발할 수 있습니다. SDK는 저수준 세부 사항을 추상화하여 비즈니스 로직에 집중할 수 있도록 해줍니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAssemble.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAssemble.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAssemble.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAssemble.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAssemble.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAssemble.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAssemble.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAssemble.go" >}}

{{< /tab >}}

{{< /tabs >}}