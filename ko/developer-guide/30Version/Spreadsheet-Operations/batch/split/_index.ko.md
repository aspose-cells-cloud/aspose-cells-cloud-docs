---
title: "배치 분할"
second_title: "문서"
type: docs
url: /ko/batch/split
keywords: "배치 분할, Aspose.Cells Cloud, REST API, Excel, PDF, CSV, JSON, 스프레드시트, 클라우드 SDK"
description: "Aspose.Cells Cloud 배치 분할 API에 대한 문서로, 스프레드시트 파일을 PDF, CSV 또는 JSON 등 여러 형식으로 분할합니다. 요청 세부 정보, 예제 cURL 명령어, 다양한 프로그래밍 언어에서의 SDK 사용법을 포함합니다."
weight: 100
---

이 REST API는 대상으로 지정된 파일의 **배치 분할**을 수행합니다.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/split
```

### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 파라미터

| 파라미터 이름      | 유형                | 경로/쿼리/문자열/HTTP 본문 | 설명                                      |
|------------------|---------------------|---------------------------|-------------------------------------------|
| BatchSplitRequest| BatchSplitRequest   | body                      | 분할 옵션을 포함하는 요청 페이로드입니다. |

### **BatchSplitRequest** 속성

| 이름             | 유형                  | 설명                                      | 비고        |
|------------------|-----------------------|-------------------------------------------|-------------|
| SourceFolder     | string                | 소스 파일이 포함된 폴더입니다.            | [선택 사항] |
| SourceStorage    | string                | 소스 파일이 저장된 저장소 이름입니다.     | [선택 사항] |
| MatchCondition   | MatchConditionRequest | 분할 대상 파일을 선택하는 데 사용되는 조건입니다. | [선택 사항] |
| Format           | string                | 원하는 출력 형식입니다(예: pdf, csv).     | [선택 사항] |
| FromIndex        | integer               | 분할할 페이지의 시작 인덱스입니다.        | [선택 사항] |
| ToIndex          | integer               | 분할할 페이지의 끝 인덱스입니다.          | [선택 사항] |
| OutFolder        | string                | 분할된 파일을 저장할 대상 폴더입니다.     | [선택 사항] |
| SaveOptions      | SaveOptions           | 출력 저장을 위한 추가 옵션입니다.         | [선택 사항] |

### **MatchConditionRequest** 속성

| 이름                 | 유형       | 설명                              | 비고        |
|----------------------|------------|-----------------------------------|-------------|
| RegexPattern         | string     | 파일 이름과 일치시킬 정규 표현식입니다. | [선택 사항] |
| FullMatchConditions | string[]   | 정확히 일치하는 조건 목록입니다.     | [선택 사항] |

### 요청 본문 파라미터

| 파라미터 이름 | 유형 | 설명                                  |
| ------------ | ---- | ------------------------------------- |
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

| 코드 | 의미                      | 반환 시점                            |
|------|---------------------------|-------------------------------------|
| 200 OK | 워크북이 성공적으로 생성됨 | 정상 흐름                            |
| 201 Created | 워크북이 생성됨 (대체 응답) | API가 생성 상태를 반환할 때         |
| 400 Bad Request | 잘못된 파라미터 | 클라이언트 측 오류                   |
| 401 Unauthorized | 토큰 누락 또는 잘못된 토큰 | 인증 오류                            |
| 409 Conflict | 파일이 존재하고 `isWriteOver=false` | 기존 파일과 충돌할 때               |


## SDK를 사용한 PostBatchSplit API 사용 방법

### PostBatchSplit API 사양

[OpenAPI 사양](https://reference.aspose.cloud/cells/#/Batch/PostBatchSplit)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예제는 cURL을 사용하여 클라우드 API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/split" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt 토큰>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Format\":\"pdf\"}"
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

SDK를 사용하면 개발 속도를 최적화할 수 있습니다. SDK는 저수준 세부 사항을 처리해주므로, 분할 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 요청을 보내는 방법을 보여줍니다:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< /tab >}}

{{< /tabs >}}
---