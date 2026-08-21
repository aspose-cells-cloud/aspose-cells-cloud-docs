---
title: "Aspose.Cells Cloud – 단어 대문자/소문자 변경 (대문자, 소문자, 첫글자 대문자, 문장 첫글자 대문자)"
ArticleTitle: "엑셀 대문자 변환기 – 대문자, 소문자, 첫글자 대문자, 문장 첫글자 대문자"
linktype: "단어 대문자 변경"
type: docs
url: /change-word-case/
keywords: "단어 대문자 변경 API, Aspose.Cells, 엑셀 대문자 변환, 대문자, 소문자, 첫글자 대문자, 문장 첫글자 대문자, 텍스트 서식"
description: "Aspose.Cells Cloud API를 사용해 엑셀 파일 내 텍스트의 대문자/소문자를 손쉽게 변환합니다. 대문자(UpperCase), 소문자(LowerCase), 첫글자 대문자(ProperCase), 문장 첫글자 대문자(SentenceCase)를 지원합니다. C#, Java, Python 등 다양한 언어의 코드 예제 제공."
weight: 100
---

## **단어 대문자 변경**

Aspose.Cells Cloud Web API를 사용해 스프레드시트 내 텍스트의 대문자/소문자를 즉시 변환하세요. 선택한 범위 내에서 대문자, 소문자, 첫글자 대문자(각 단어의 첫 글자를 대문자로), 문장 첫글자 대문자(각 문장의 첫 글자를 대문자로)로 전환할 수 있습니다. 변환은 문자열 셀만 적용되며, 숫자, 논리값, 오류, 빈 셀은 무시됩니다. 수식, 서식, 데이터 유효성 검사는 그대로 유지됩니다.

- **UpperCase** – 모든 문자를 대문자로 변환합니다.
- **LowerCase** – 모든 문자를 소문자로 변환합니다.
- **ProperCase** – 각 단어의 첫 글자만 대문자로, 나머지는 소문자로 변환합니다.
- **SentenceCase** – 각 문장의 첫 글자만 대문자로, 나머지는 소문자로 변환합니다.

<img src="images/result.png" alt="대문자/소문자 변환 전후 스크린샷" width="800" height="450" />

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/wordcase
```


### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

```bash
-H "Authorization: Bearer {access_token}"
```
### **UpdateWordCase** API 요청 파라미터

| 파라미터 이름 | 타입   | 위치 | 설명                                                                                                                                                           |
| :------------- | :----- | :------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| spreadsheet    | File   | FormData | 처리할 스프레드시트 파일입니다. 지원 형식은 XLSX, XLS, ODS, CSV 등이 포함됩니다.                                                                             |
| wordCaseType   | String | Query    | 텍스트 대문자/소문자 변환 유형을 지정합니다: `UpperCase`, `LowerCase`, `ProperCase`, `SentenceCase`.                                                                   |
| worksheet      | String | Query    | _(선택)_ 대문자/소문자 변환이 적용될 워크시트 이름입니다. 생략 시 워크북의 첫 번째 워크시트에 적용됩니다.               |
| range          | String | Query    | _(선택)_ 대문자/소문자 변환이 적용될 셀 범위입니다 (예: `"A1:C10"`). 생략 시 지정된 워크시트 내 사용된 모든 셀에 적용됩니다. |
| outPath        | String | Query    | _(선택)_ 처리된 워크북이 저장될 클라우드 스토리지 폴더 경로입니다. 생략 시 원본 폴더에 저장됩니다.                            |
| outStorageName | String | Query    | 출력 파일이 저장될 클라우드 스토리지의 이름입니다.                                                                                                   |
| region         | String | Query    | _(선택)_ 텍스트 대문자/소문자 변환 규칙에 사용될 로케일을 설정합니다. 언어별 대문자 규칙(예: `"en-US"`, `"tr-TR"`) 적용 시 특히 중요합니다.                 |
| password       | String | Query    | _(선택)_ 업로드된 스프레드시트가 암호로 보호되어 있는 경우, 파일을 열고 처리하기 위한 암호를 입력합니다.                                                    |

### 응답

성공 시, 서비스는 **200 OK** 또는 **202 Accepted** 상태 코드와 처리된 워크북의 바이너리 스트림을 포함하는 JSON 페이로드를 반환합니다.

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

### 오류 코드

- **400 Bad Request** – 유효하지 않은 Aspose.Cells Cloud API URI입니다.
- **401 Unauthorized** – 유효하지 않은 액세스 토큰 또는 잘못된 클라이언트 인증 정보입니다.
- **404 Not Found** – 스프레드시트 파일에 접근할 수 없습니다.
- **500 Server Error** – 스프레드시트 처리 중 내부 오류가 발생했습니다.

## 변경 단어 대문자 API는 어떤 경우에 사용해야 하나요?

### 데이터 클렌징 및 표준화

- **고객 데이터 관리** – 고객 이름 및 주소 정보의 대문자/소문자를 표준화합니다(예: `john doe` → `John Doe`).
- **제품 카탈로그 처리** – 제품 제목 및 설명 텍스트의 대문자/소문자를 표준화합니다(예: `IPHONE 15 PRO` → `iPhone 15 Pro`).
- **재무 보고서 생성** – 재무 제표 내 품목명 및 설명 필드를 표준화합니다.

### 다중 소스 데이터 통합

- **데이터 웨어하우스 ETL** – 다양한 시스템에서 데이터를 불러올 때 텍스트 형식을 표준화합니다.
- **API 데이터 수신** – 외부 API에서 반환된 일관되지 않은 대문자/소문자 데이터를 처리합니다.
- **부서 간 데이터 병합** – 서로 다른 부서의 엑셀 보고서에서 텍스트 형식을 표준화합니다.

### 콘텐츠 관리 시스템

- **자동 뉴스 릴리스** – 뉴스 헤드라인 및 콘텐츠를 자동으로 서식화합니다(제목 대문자 규칙).
- **제품 문서 생성** – 기술 문서 용어의 서식 일관성을 확보합니다.
- **지식베이스 유지보수** – FAQ 및 도움말 문서의 텍스트 형식을 표준화합니다.

### 엔터프라이즈 애플리케이션 통합

- **CRM 시스템 통합** – 고객 데이터를 가져오기/내보낼 때 이름 및 회사 정보를 자동으로 서식화합니다.
- **ERP 데이터 처리** – 자재 설명, 공급업체 이름 등 주요 필드를 표준화합니다.
- **HR 관리 시스템** – 직원 정보 및 직무명을 표준화합니다.

### 대량 문서 처리

- **법률 문서 작성** – 계약서 및 협약서의 조항 서식을 일괄 처리합니다.
- **마케팅 자료 생성** – 광고 카피 및 이메일 템플릿의 텍스트 서식을 표준화합니다.
- **학술 논문 서식화** – 참고문헌 및 제목의 서식 요구사항을 표준화합니다.

### 실시간 데이터 처리

- **사용자 입력 유효성 검사** – 사용자가 제출한 폼 데이터를 실시간으로 서식화합니다.
- **챗봇 응답** – 자동 생성된 응답의 텍스트 서식을 표준화합니다.
- **즉시 보고서 생성** – 일관된 서식의 비즈니스 보고서를 동적으로 생성합니다.

### 국제화 및 현지화

- **다국어 데이터 처리** – 다양한 언어의 대문자 규칙 차이를 처리합니다.
- **현지화 콘텐츠 준비** – 지역별로 서식화된 현지 콘텐츠를 준비합니다.
- **번역 프로젝트 관리** – 번역 전후 텍스트 서식의 일관성을 확보합니다.

## 변경 단어 대문자 API를 사용해야 하는 이유는 무엇인가요?

- **개발자 친화적** – Aspose.Cells Cloud는 여러 언어의 SDK 라이브러리를 제공하여 빠른 개발과 체계적인 문서를 가능하게 합니다. 사용자 정의 솔루션 구축에 비해 개발 부담을 크게 줄여줍니다.
- **비용 효율적** – 워크북을 먼저 업로드하지 않고도 단어 대문자를 변경할 수 있어 저장 공간 절약과 비용 절감이 가능합니다.

## OpenAPI 사양

[OpenAPI Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/UpdateWordCase)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 요청을 수행할 수 있도록 합니다.

### Aspose.Cells Cloud SDK 사용하기

SDK를 사용하는 것이 개발 속도를 극대화하는 최선의 방법입니다. SDK는 내부 세부 사항을 처리해주므로, **UpdateWordCase** 기능을 최소한의 코드로 구현할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UpdateWordCase.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UpdateWordCase.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UpdateWordCase.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UpdateWordCase.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UpdateWordCase.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UpdateWordCase.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UpdateWordCase.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UpdateWordCase.go" >}}
{{</tab>}}
{{< /tabs >}}
---