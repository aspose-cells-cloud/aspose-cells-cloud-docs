---
title: "엑셀 파일 일괄 변환"
second_title: "문서"
type: docs
url: /batch/convert
keywords: "일괄 변환, 엑셀, Aspose.Cells Cloud, REST API, PDF, CSV, JSON, Markdown, 스프레드시트"
description: "Aspose.Cells Cloud API를 사용하여 여러 엑셀 파일을 PDF, CSV, JSON, Markdown 등 다양한 형식으로 일괄 변환하는 방법을 알아보세요. 이 가이드에는 REST 엔드포인트 세부 정보, 요청 매개변수, cURL 예제 및 다양한 언어의 SDK 코드 스니펫이 포함되어 있습니다."
weight: 100
---

이 REST API는 변환 가능 파일의 **일괄 변환**을 지원합니다.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/convert
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 위해 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름       | 타입   | 위치 | 설명                                           |
|----------------------|--------|----------|-------------------------------------------------------|
| **batchConvertRequest** | object | body     | 변환 설정이 포함된 요청 본문입니다.         |

#### BatchConvertRequest 속성

| 이름          | 타입                | 설명                                           | 비고 |
|---------------|---------------------|-------------------------------------------------------|-------|
| **SourceFolder** | string              | 원본 엑셀 파일이 포함된 폴더 경로입니다. | [선택 사항] |
| **MatchCondition** | MatchConditionRequest | 변환할 파일을 선택하는 데 사용되는 조건입니다.      | [선택 사항] |
| **Format**        | string              | 변환 대상 형식입니다(예: `pdf`, `csv`).   | [선택 사항] |
| **OutFolder**     | string              | 변환된 파일이 저장될 대상 폴더입니다. | [선택 사항] |
| **SaveOptions**   | SaveOptions         | 파일 저장 방식을 제어하는 추가 옵션입니다. | [선택 사항] |

#### MatchConditionRequest 속성

| 이름               | 타입      | 설명                                          | 비고 |
|--------------------|-----------|------------------------------------------------------|-------|
| **RegexPattern**   | string    | 파일 이름을 필터링하는 데 사용되는 정규 표현식입니다.       | [선택 사항] |
| **FullMatchConditions** | string[] | 일치시킬 정확한 파일 이름 조건 목록입니다.    | [선택 사항] |


### 요청 본문 매개변수

| 매개변수 이름 | 타입 | 설명                                    |
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
| 200 OK | 워크북이 성공적으로 생성됨 | 정상 흐름                              |
| 201 Created | 워크북이 생성됨 (대체 응답) | API가 생성 상태를 반환할 때 |
| 400 Bad Request | 잘못된 매개변수 | 클라이언트 측 오류                        |
| 401 Unauthorized | 토큰 누락 또는 유효하지 않은 토큰 | 인증 오류                    |
| 409 Conflict | 파일이 존재하고 `isWriteOver=false`인 경우 | 기존 파일과 충돌    

## SDK를 사용한 PostBatchConvert API 사용 방법

### PostBatchConvert API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/PostBatchConvert)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/convert" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Format\":\"pdf\",\"SaveOptions\":{\"SaveFormat\":\"pdf\",\"CalculateFormula\":true,\"EnableHTTPCompression\":true,\"OnePagePerSheet\":true,\"CreateDirectory\":false,\"Compliance\":\"None\"}}"
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

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 요청을 보내는 방법을 보여줍니다:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Batch-Convet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-Batch-Convet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-Batch-Convet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Batch-Convet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Examples-Batch-Convet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Examples-Batch-Convet.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Batch-Convet.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "d763dc80b0aff6275403dc1d82ad59a5" "Examples-Batch-Convet.go" >}}

{{< /tab >}}

{{< /tabs >}}