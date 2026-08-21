---
title: "Excel 파일 일괄 잠금"
second_title: "문서"
type: docs
url: /batch/lock
keywords: "일괄 잠금, Excel, Aspose.Cells, 클라우드 API, 스프레드시트, 파일 보호"
description: "Aspose.Cells 클라우드 API는 여러 Excel 파일을 일괄적으로 잠그는 기능을 제공합니다. REST 엔드포인트 또는 지원되는 SDK(C#, Java, PHP, Ruby, Node.js, Python, Perl, Go 등)를 사용하여 파일을 대량으로 잠글 수 있습니다."
weight: 100
---

이 REST API는 적합한 Excel 파일을 **일괄 잠금**할 수 있도록 합니다.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/lock
```

### **보안 및 인증**

Aspose.Cells 클라우드 API는 보안이 강화되어 있으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름   | 유형               | 위치 | 설명                                 |
|------------------|--------------------|----------|---------------------------------------------|
| BatchLockRequest | BatchLockRequest   | body     | 잠금 매개변수가 포함된 JSON 본문.      |

#### **BatchLockRequest** 속성

| 이름          | 유형                     | 설명                                            | 참고    |
|---------------|--------------------------|--------------------------------------------------------|----------|
| SourceFolder  | string                   | 소스 Excel 파일이 포함된 폴더.           | 선택 사항 |
| MatchCondition| MatchConditionRequest    | 잠글 파일을 선택하는 데 사용되는 조건.         | 선택 사항 |
| Password      | string                   | 잠긴 파일에 적용할 암호.                | 선택 사항 |
| OutFolder     | string                   | 잠긴 파일의 저장 폴더.              | 선택 사항 |

#### **MatchConditionRequest** 속성

| 이름               | 유형      | 설명                                          | 참고    |
|--------------------|-----------|------------------------------------------------------|----------|
| RegexPattern       | string    | 파일 이름과 일치하는 정규표현식 패턴.      | 선택 사항 |
| FullMatchConditions| string[]  | 잠글 파일 이름의 정확한 일치 조건.                 | 선택 사항 |

### 요청 본문 매개변수

| 매개변수 이름 | 유형 | 설명                                    |
| -------------- | ---- | ---------------------------------------------- |
| data           | file | 생성할 워크북 파일의 이진 콘텐츠. |

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
| 200 OK | 워크북이 성공적으로 생성됨 | 정상 흐름                              |
| 201 Created | 워크북이 생성됨 (대체 응답) | API가 생성 상태를 반환할 경우 |
| 400 Bad Request | 잘못된 매개변수 | 클라이언트 측 오류                        |
| 401 Unauthorized | 토큰 누락 또는 잘못된 토큰 | 인증 오류                    |
| 409 Conflict | 파일이 존재하고 `isWriteOver=false`인 경우 | 기존 파일과 충돌 |

## SDK를 사용한 PostBatchLock API 사용 방법

### PostBatchLock API 사양

[OpenAPI 사양](https://reference.aspose.cloud/cells/#/Batch/PostBatchLock)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

**cURL** 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예시는 cURL을 사용해 클라우드 API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/lock" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt 토큰>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Password\":\"123456\"}"
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

### Aspose.Cells 클라우드 SDK 사용

SDK를 사용하면 개발 속도가 가장 빠릅니다. SDK는 저수준 세부 사항을 추상화해 잠금 작업에 집중할 수 있도록 도와줍니다. 지원되는 Aspose.Cells 클라우드 SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하십시오.

다음 코드 예제는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostBatchLock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostBatchLock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostBatchLock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostBatchLock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostBatchLock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostBatchLock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostBatchLock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostBatchLock.go" >}}

{{< /tab >}}

{{< /tabs >}}