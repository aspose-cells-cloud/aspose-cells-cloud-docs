---
title: "Aspose.Cells Cloud Web API – AI 기반 언어 변환을 통한 텍스트 파일 번역"
second_title: "문서"
ArticleTitle: "Aspose.Cells Cloud AI 번역 API를 사용하여 텍스트 파일 번역하는 방법"
linktitle: "텍스트 파일 번역"
type: docs
url: /translate-text-file/
keywords: "Aspose.Cells, 클라우드 API, AI 번역, 텍스트 파일 번역, 다국어 변환, REST PUT, 대상 언어 코드, 파일 업로드 번역, 원시 텍스트 번역, 스프레드시트 AI"
description: "Aspose.Cells Cloud AI TranslateTextFile 엔드포인트를 사용하여 텍스트 파일을 지원되는 언어로 변환하는 방법을 알아보세요. 멀티파트 파일 업로드 및 원시 텍스트 페이로드를 모두 지원하며, 포맷을 유지하고 다운로드 가능한 번역된 파일을 반환합니다."
weight: 100
---

**TranslateTextFile** 엔드포인트는 Aspose.Cells Cloud AI 서비스를 활용하여 텍스트 파일의 내용을 지정된 대상 언어로 번역합니다. 두 가지 작업 모드를 지원합니다: (1) **파일 업로드 모드** – multipart/form-data를 통해 텍스트 파일을 전송하고 번역된 파일을 받습니다; (2) **직접 콘텐츠 모드** – 요청 본문에 원시 텍스트를 게시하고 번역된 텍스트를 직접 받습니다. 이 서비스는 원본 줄 바꿈 및 포맷을 유지하며, 파일 이름에 자동으로 "_translated" 접미사를 추가하고 결과를 다운로드 가능한 스트림으로 반환합니다. 문서 일괄 번역, 다국어 워크플로우 통합, 사용자 생성 콘텐츠의 실시간 번역에 적합합니다.

## **텍스트 파일 번역 API**

### 웹 API

```http
PUT https://api.aspose.cloud/v4.0/cells/ai/translate/text-file
```

### **요청 매개변수:**

| 매개변수 이름 | 유형   | 위치 | 필수/선택 | 설명                                                                                                                                                                                                 |
| :------------ | :----- | :--- | :-------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet   | 파일   | 필수 | FormData  | 번역할 원본 텍스트 파일입니다. 일반 텍스트(.txt) 또는 지원되는 스프레드시트 형식이어야 합니다. 예: "file"이라는 이름의 multipart/form-data 필드를 통해 `document.txt`를 업로드합니다.                     |
| targetLanguage | 문자열 | 필수 | 쿼리     | 원하는 출력 언어의 ISO-639-1 언어 코드입니다(예: 스페인어는 "es", 프랑스어는 "fr", 독일어는 "de"). 코드는 대소문자를 구분하지 않습니다.                                                                    |
| region        | 문자열 | 선택 | 쿼리      | 날짜, 숫자, 통화 등 로케일 특정 포맷에 영향을 주는 스프레드시트 지역 식별자입니다. 일반적인 값: "US", "EU", "CN". 생략 시 워크북의 원본 지역 설정이 사용됩니다.                                           |
| password      | 문자열 | 선택 | 쿼리      | 암호화된 스프레드시트 파일을 열 때 필요한 비밀번호입니다. 일반 텍스트 파일에는 필요하지 않습니다.                                                                                                         |

### **응답**

성공 응답 (200 OK)
헤더:
Content-Type: application/octet-stream // 번역된 파일의 이진 스트림
Content-Disposition: attachment; filename="<원본_이름>\_translated.txt"
Content-Length: <바이트 단위 크기>

본문: 원본 줄 바꿈 및 포맷을 유지한 채 번역된 텍스트를 포함한 이진 스트림.

**HTTP 상태 코드**

| 코드 | 의미                 | 설명                                               |
| ---- | -------------------- | -------------------------------------------------- |
| 200  | OK                   | 필터가 성공적으로 적용되었으며, 응답에 작업 세부 정보가 포함됩니다. |
| 400  | Bad Request          | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형)입니다.      |
| 401  | Unauthorized         | 잘못되거나 누락된 JWT 토큰입니다.                                  |
| 413  | Payload Too Large    | 업로드된 파일이 크기 제한을 초과했습니다.                         |
| 500  | Internal Server Error | 예기치 않은 서버 오류입니다.                                      |

## Where should we use the Translate Text File API?

- **다국어 문서 포털** – 사용자 매뉴얼 또는 도움말 파일을 텍스트 문서로 업로드하여 자동으로 번역하고, 요청 시 현지화된 버전을 제공합니다.
- **콘텐츠 관리 시스템(CMS)** – CMS 워크플로우에 통합하여 블로그 게시물이나 기사를 국제 독자에게 게시하기 전에 번역합니다.
- **기업 데이터 파이프라인** – 대량의 CSV 또는 TXT 보고서를 처리하는 일괄 작업에서 사용하여, 원본 포맷을 유지한 채 지역 사무소 언어로 변환합니다.
- **고객 지원 플랫폼** – 다양한 언어로 작업하는 지원 담당자를 위해 들어오는 일반 텍스트 티켓 또는 채팅 로그를 실시간으로 번역합니다.

## Why should you use the Translate Text File API?

- **AI 기반 정확도** – 자연스럽고 문맥을 고려한 출력을 위해 최신 신경망 번역 모델을 활용합니다.
- **이중 입력 유연성** – 파일 업로드와 원시 텍스트 페이로드 모두 수락하여 다양한 클라이언트 애플리케이션과의 통합을 간소화합니다.
- **원본 레이아웃 유지** – 줄 바꿈, 들여쓰기 및 특수 문자를 유지하여 후속 처리 정리 작업을 불필요하게 합니다.
- **원활한 파일 처리** – 자동 생성된 "_translated" 접미사가 포함된 다운로드 준비 완료 파일을 반환하여 클라이언트 측 코드 복잡성을 줄입니다.

## How to Use the Translate Text File API with SDKs

### Translate Text File API Specification

[Translate Text File API Specification](https://reference.aspose.cloud/cells/#/AIController/TranslateTextFile)은 웹 브라우저에서 직접 REST 상호작용을 실행할 수 있도록 공개적으로 접근 가능한 프로그래밍 인터페이스를 제공합니다.

## Excel API SDK

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 저수준 세부 정보를 추상화하여 스프레드시트를 다른 스프레드시트로 병합하는 등의 작업을 간단한 코드로 빠르게 개발할 수 있습니다.
Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.
다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스와 상호 작용하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v4.0_TranslateTextFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v4.0_TranslateTextFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v4.0_TranslateTextFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v4.0_TranslateTextFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v4.0_TranslateTextFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v4.0_TranslateTextFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v4.0_TranslateTextFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v4.0_TranslateTextFile.go" >}}
{{</tab>}}
{{< /tabs >}}