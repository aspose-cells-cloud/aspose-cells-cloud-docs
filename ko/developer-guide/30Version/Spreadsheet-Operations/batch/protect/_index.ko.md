---
title: "Excel 파일 일괄 보호"
second_title: "문서"
type: docs
url: /batch/protect
keywords: "Excel 파일 일괄 보호, Aspose Cells Cloud, REST API, Excel 보호, 일괄 보호"
description: "Aspose.Cells Cloud REST API를 사용하여 여러 Excel 파일을 일괄적으로 보호하는 방법을 알아보세요. 요청 세부 정보, cURL 예제, 다양한 언어에 대한 SDK 코드 샘플이 포함되어 있습니다."
weight: 100
---

이 REST API는 적합한 Excel 파일의 **일괄 보호**를 지원합니다.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/protect
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 강화되어 있으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름        | 유형                | 위치 | 설명                                                                                              |
|-----------------------|---------------------|----------|----------------------------------------------------------------------------------------------------------|
| batchProtectRequest   | BatchProtectRequest | body     | 소스 폴더, 일치 조건, 보호 유형, 암호 및 출력 폴더를 지정하는 JSON 페이로드입니다. |

### BatchProtectRequest 속성

| 이름            | 유형                     | 설명                                                                                 | 비고 |
|-----------------|--------------------------|---------------------------------------------------------------------------------------------|-------|
| SourceFolder    | string                   | 소스 Excel 파일이 포함된 폴더입니다.                                                   | 선택 사항 |
| MatchCondition  | MatchConditionRequest   | 보호 대상 파일을 선택하는 데 사용되는 기준입니다.                                               | 선택 사항 |
| ProtectionType  | string                   | 적용할 보호 유형(예: `All`, `ReadOnly`)입니다.                                      | 선택 사항 |
| Password        | string                   | 보호된 파일에 설정할 암호입니다.                                                    | 선택 사항 |
| OutFolder       | string                   | 보호된 파일을 저장할 대상 폴더입니다.                                                 | 선택 사항 |

### MatchConditionRequest 속성

| 이름                | 유형       | 설명                                   | 비고 |
|---------------------|------------|-----------------------------------------------|-------|
| RegexPattern        | string     | 파일 이름과 일치시키는 데 사용되는 정규 표현식입니다. | 선택 사항 |
| FullMatchConditions | string[]   | 정확한 파일 이름 조건 목록입니다.          | 선택 사항 |

### 요청 본문 매개변수

| 매개변수 이름 | 유형 | 설명                                    |
| -------------- | ---- | ---------------------------------------------- |
| data           | file | 생성할 워크북 파일의 이진 콘텐츠입니다. |

  
### **응답**

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```
**HTTP 상태 코드**

| 코드 | 의미                     | 반환 시점                           |
|------|-----------------------------|-----------------------------------------|
| 200 OK | 워크북이 성공적으로 생성되었습니다 | 정상적인 흐름                              |
| 201 Created | 워크북이 생성되었습니다 (대체 응답) | API가 생성 상태를 반환할 때 |
| 400 Bad Request | 잘못된 매개변수 | 클라이언트 측 오류                        |
| 401 Unauthorized | 토큰 누락 또는 잘못된 토큰 | 인증 오류                    |
| 409 Conflict | 파일이 존재하고 `isWriteOver=false`인 경우 | 기존 파일과 충돌    

## SDK를 사용한 PostProtectConvert API 사용 방법

### PostProtectConvert API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/PostProtectConvert)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/protect" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Password\":\"123456\",\"ProtectionType\":\"All\"}"
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

### Aspose.Cells Cloud SDK 사용

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 요청을 보내는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostBatchProtect.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostBatchProtect.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostBatchProtect.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostBatchProtect.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostBatchProtect.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostBatchProtect.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostBatchProtect.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostBatchProtect.go" >}}

{{< /tab >}}

{{< /tabs >}}