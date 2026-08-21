---
title: "Aspose.Cells – 단어 대문자 변환 API"
second_title: "문서"
linktitle: "단어 대문자"
type: docs
url: /ko/post-update-word-case/
keywords: "Aspose.Cells, 단어 대문자 변환 API, 텍스트 대문자 변환, Excel, CSV, Google 시트, REST API"
description: "Aspose.Cells Cloud의 단어 대문자 변환 API를 사용해 Excel, CSV 또는 Google 시트 파일의 텍스트 대문자를 변환합니다. 대문자/소문자, 제목 대문자, 첫글자 대문자 변환을 지원합니다."
weight: 100
ArticleTitle: "Aspose.Cells – 단어 대문자 변환 API 문서"
---

**API 버전:** 3.0

스preadsheet(Excel, Google 시트, CSV)에서 불일치하는 텍스트 대문자 처리는 대규모 데이터셋일수록 특히 번거롭습니다. **PostUpdateWordCase 웹 API**는 텍스트 대문자 변환을 자동화하여 최소한의 노력으로 깔끔하고 표준화된 데이터를 제공합니다.


## **Excel 웹 API – 단어 대문자 변환 API**

```http
POST https://api.aspose.cloud/v3.0/cells/updatewordcase
```
### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **기능 설명**

PostUpdateWordCase 웹 API는 스프레드시트에서 흔히 발생하는 텍스트 대문자 불일치 문제를 해결합니다. 이 문제는 데이터 분석 및 처리에 큰 영향을 미칠 수 있습니다. 이 API는 대문자 변환을 자동화하여 데이터를 깔끔하고 표준화된 상태로 만들어 추가 조작이나 분석에 바로 사용할 수 있도록 합니다.

- **자동 텍스트 대문자 변환**
  - **대문자 → 소문자** – 모든 대문자를 소문자로 변환합니다.
  - **소문자 → 대문자** – 모든 소문자를 대문자로 변환합니다.
  - **첫 글자 대문자화** – 각 단어의 첫 글자를 대문자로 변환합니다.
  - **제목 대문자** – 주요 단어의 첫 글자를 대문자로 변환하여 제목 대문자로 바꿉니다.

- **다양한 형식 지원** – 이 API는 Excel, OpenOffice, JSON, CSV 등 다양한 스프레드시트 형식을 지원합니다. 이러한 다재다능함은 다양한 데이터 처리 요구사항에 적합합니다.

### **요청 파라미터**

| 파라미터 이름     | 타입   | 위치         | 설명                                                                                                               |
| ----------------- | ------ | ------------ | ------------------------------------------------------------------------------------------------------------------------- |
| `wordCaseOptions` | object | 요청 본문    | 소스 범위, 대상 대문자 유형 및 추가 설정 등 원하는 대문자 변환 옵션을 정의합니다. |

**`wordCaseOptions` 스키마**

```json
{
  "Range": "A1:B10", // 처리할 Excel 스타일 범위 (필수)
  "CaseType": "Upper", // 열거형: Upper, Lower, Capitalize, Title (필수)
  "IgnoreBlank": true // 논리형, 선택사항 – true일 경우 빈 셀은 변경되지 않음
}
```

**요청 본문 예시**

```json
{
  "Range": "A1:B10",
  "CaseType": "Upper",
  "IgnoreBlank": true
}
```

- **Range** – 대문자 변환이 적용될 셀 범위 (예: `A1:C5`).
- **CaseType** – 대문자 변환 유형. 허용되는 값은 `Upper`, `Lower`, `Capitalize`, `Title`입니다.
- **IgnoreBlank** – `true`일 경우 빈 셀은 무시됩니다. 기본값은 `false`입니다.

### **응답**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[병합된 파일 이름]",
    "Filesize" : [파일 크기],
    "FileContent" : "[Base64String]"
}
```

- **Filename** – 처리된 파일의 이름.
- **FileSize** – 바이트 단위의 파일 크기.
- **FileContent** – 변환된 파일의 Base64 인코딩 콘텐츠.

**HTTP 상태 코드**

| 코드 | 의미                         | 설명                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | 성공 (OK)                   | 필터가 성공적으로 적용됨; 응답에는 작업 세부정보가 포함됨. |
| 400  | 잘못된 요청 (Bad Request)   | 누락되거나 잘못된 파라미터 (예: 지원되지 않는 파일 형식). |
| 401  | 인증되지 않음 (Unauthorized) | 잘못되거나 누락된 JWT 토큰. |
| 413  | 요청 데이터가 너무 큼 (Payload Too Large) | 업로드된 파일이 크기 제한을 초과함. |
| 500  | 내부 서버 오류 (Internal Server Error) | 예기치 않은 서버 오류. |
## SDK를 사용해 PostUpdateWordCase API 사용하는 방법

### PostUpdateWordCase API 사양

<a href="https://reference.aspose.cloud/cells/#/TextProcessingController/PostUpdateWordCase" target="_blank" rel="noopener noreferrer">OpenAPI 사양</a>은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 요청을 수행할 수 있도록 합니다.

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_PostUpdateWordCase.cs" >}}
{{</ tab>}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_PostUpdateWordCase.java" >}}
{{</ tab>}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_PostUpdateWordCase.php" >}}
{{</ tab>}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_PostUpdateWordCase.rb" >}}
{{</ tab>}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_PostUpdateWordCase.ts" >}}
{{</ tab>}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_PostUpdateWordCase.py" >}}
{{</ tab>}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_PostUpdateWordCase.pl" >}}
{{</ tab>}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_PostUpdateWordCase.go" >}}
{{</ tab>}}
{{</ tabs >}}
---