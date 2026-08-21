---
title: "일괄 잠금 해제"
second: "문서"
type: docs
url: /batch/unlock
keywords: "일괄 잠금 해제, Aspose.Cells Cloud, Excel, REST API, 스프레드시트, 클라우드 SDK"
description: "Aspose.Cells Cloud REST API를 사용하여 여러 Excel 파일을 일괄적으로 잠금 해제합니다. C#, Java, Python 및 기타 언어용 SDK를 지원합니다."
weight: 100
---

이 REST API는 적격한 Excel 파일을 일괄적으로 잠금 해제합니다.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/unlock
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 적용되며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름 | 유형 | 위치 | 설명 |
|---------------|------|------|------|
| **BatchLockRequest** |  | body | 잠금 해제 설정을 포함한 요청 본문입니다. |

### **BatchLockRequest** 속성

| 이름            | 유형                     | 설명                                             | 비고 |
|-----------------|--------------------------|--------------------------------------------------|------|
| SourceFolder    | string                   | 소스 Excel 파일이 포함된 폴더입니다.             | [선택 사항] |
| MatchCondition  | MatchConditionRequest    | 잠금 해제를 위해 파일을 선택하는 데 사용되는 기준입니다. | [선택 사항] |
| Password        | string                   | 보호된 워크북에 적용된 비밀번호입니다.           | [선택 사항] |
| OutFolder       | string                   | 잠금 해제된 파일의 대상 폴더입니다.              | [선택 사항] |

### **MatchConditionRequest** 속성

| 이름               | 유형      | 설명                                 | 비고 |
|--------------------|-----------|--------------------------------------|------|
| RegexPattern       | string    | 파일 이름과 일치시킬 정규식입니다.   | [선택 사항] |
| FullMatchConditions| string[]  | 정확히 일치시킬 파일 이름 조건입니다. | [선택 사항] |

### 요청 본문 매개변수

| 매개변수 이름 | 유형 | 설명                                     |
|--------------|------|------------------------------------------|
| data         | file | 생성할 워크북 파일의 이진 콘텐츠입니다. |

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

| 코드 | 의미                         | 반환 시점                             |
|------|------------------------------|---------------------------------------|
| 200 OK | 워크북이 성공적으로 생성됨      | 정상 흐름                             |
| 201 Created | 워크북이 생성됨 (대체 응답)   | API가 생성 상태를 반환할 때           |
| 400 Bad Request | 잘못된 매개변수            | 클라이언트 측 오류                    |
| 401 Unauthorized | 누락되었거나 유효하지 않은 토큰 | 인증 오류                            |
| 409 Conflict | 파일이 존재하고 `isWriteOver=false` | 기존 파일과 충돌 시                  |

## SDK를 사용하여 PostBatchLock API 사용하는 방법

### PostBatchLock API 사양

[OpenAPI 사양](https://reference.aspose.cloud/cells/#/Batch/PostBatchUnlock)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예시는 cURL을 사용하여 Cloud API에 호출을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/unlock" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"SourceFolder":"CellsTests","OutFolder":"Output","MatchCondition":{"RegexPattern":"(^Book)(.+)(xlsx$)"},"Password":"123456"}'
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

### Aspose.Cells Cloud SDK 사용하기

SDK를 사용하는 것은 잠금 해제 기능을 개발하는 가장 빠른 방법입니다. SDK는 저수준 세부 사항을 추상화하여 비즈니스 로직에 집중할 수 있게 해줍니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하십시오.

다음 코드 예시는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostBatchUnlock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostBatchUnlock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostBatchUnlock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostBatchUnlock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostBatchUnlock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostBatchUnlock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostBatchUnlock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostBatchUnlock.go" >}}

{{< /tab >}}

{{< /tabs >}}