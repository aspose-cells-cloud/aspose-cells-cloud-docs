---
title: "텍스트 분할 API – Excel 셀을 열로 분할 | Aspose.Cells Cloud"
second_title: "문서"
ArticleTitle: "Excel 텍스트 분할기 – 셀 내용을 여러 열로 분할 | Aspose.Cells Cloud"
linktitle: "텍스트 분할"
type: docs
url: /ko/split-text/
keywords: "Aspose, Cells, 텍스트 분할 API, Excel, 구분자, 텍스트 분할, 클라우드 API"
description: "Aspose.Cells Cloud를 사용하여 Excel 셀 텍스트를 별도의 열이나 행으로 쉽게 분할합니다. 사용자 정의 구분자, 마스크, 줄 바꿈을 지원하며 구분자를 유지할지 여부도 선택 가능합니다. 몇 분 안에 curl 또는 SDK를 사용해 시작하세요."
weight: 100
---

사용자 정의 분할 규칙을 사용하여 Excel 셀 텍스트를 여러 열로 분할합니다. Aspose.Cells Cloud의 텍스트 분할 웹 API를 사용하여 콘텐츠를 구분자로 분할하고 지정된 범위에 결과를 출력합니다.

## **소개**: 텍스트 분할

텍스트 분할 API는 지정된 구분자, 패턴 또는 줄 바꿈을 기준으로 셀 콘텐츠를 여러 셀로 나누어 결과를 대상 범위에 출력합니다. 유연한 분할 방식, 방향성 출력(열 또는 행), 구분자 유지 옵션을 지원하며, 연결된 데이터, CSV 스타일 콘텐츠 또는 여러 줄 텍스트를 구조화된 형식으로 파싱하는 데 이상적입니다.

- **특정 문자로 셀 분할** – 임의의 문자(쉼표, 공백, 세미콜론 등)를 구분자로 선택하여 셀 콘텐츠를 여러 셀로 분해합니다.
- **문자열로 셀 분할** – 지정한 문자 조합으로 셀을 분리합니다.
- **마스크로 텍스트 분할** – 와일드카드를 사용하여 특정 패턴에 따라 텍스트를 분할하여 텍스트 분할을 더욱 유연하고 강력하게 수행합니다.
- **줄 바꿈으로 셀 내용 분할** – 줄 바꿈을 기준으로 분할하여 더 체계적인 표현을 만듭니다.
- **열 또는 행으로 셀 분할** – 분할 결과를 연속된 열 또는 행에 기록할지 선택합니다.
- **구분자 제거 또는 유지** – 분할된 셀의 시작 또는 끝에 구분자를 유지할지 여부를 결정합니다.

## **SplitText API**

**사전 조건**: 이 API를 사용하려면 유효한 Aspose Cloud 액세스 토큰이 필요하며, 처리할 워크북은 Aspose Cloud 스토리지에 업로드되었거나 요청에 직접 제공되어야 합니다. 이 API는 XLSX, XLS, ODS, CSV 등 일반적인 스프레드시트 형식을 지원합니다.

### 웹 API

```http
POST https://api.aspose.cloud/v4.0/cells/content/split/text
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 제공하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

```bash
-H "Authorization: Bearer {access_token}"
```

### **splitText** API의 요청 매개변수

| 매개변수 이름                  | 유형    | 위치       | 필수 여부 | 기본값         | 설명                                                                                                                                               |
| ------------------------------ | ------- | ---------- | --------- | -------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| spreadsheet                    | 파일    | FormData   | 예        | —              | 처리할 스프레드시트 파일. XLSX, XLS, ODS, CSV 등이 지원됩니다.                                                                                     |
| delimiters                     | 문자열  | Query      | 아니요    | —              | 셀 내 텍스트를 분할하는 데 사용되는 하나 이상의 구분자 문자(예: `","`, `";"`, `Space`, `LineBreak`, `Tab`, `Pipe`, `Custom`).                     |
| keepDelimitersInResultingCells | 불리언  | Query      | 아니요    | false          | `true`로 설정하면 분할된 결과 셀에 구분자 문자가 유지됩니다.                                                                                      |
| keepDelimitersPosition         | 문자열  | Query      | 아니요    | None           | `keepDelimitersInResultingCells`가 `true`일 때 구분자를 유지할 위치. 옵션: `None`, `AtTheBeginning`, `AtTheEnd`, `BeforeText`, `AfterText`.     |
| howToSplit                     | 문자열  | Query      | 아니요    | SplitToColumns | 텍스트 분할 방식. 옵션: `None`, `SplitToColumns`, `SplitToRows`.                                                                                  |
| outPositionRange               | 문자열  | Query      | 예        | —              | 분할 결과를 기록할 대상 범위(예: `"D1:F10"`).                                                                                                      |
| worksheet                      | 문자열  | Query      | 아니요    | —              | 텍스트 분할이 적용될 워크시트 이름. 생략 시 첫 번째 워크시트가 사용됩니다.                                                                         |
| range                          | 문자열  | Query      | 아니요    | —              | 분할 작업이 적용될 원본 셀 범위(예: `"A1:A10"`). 생략 시 워크시트 내 사용된 모든 셀이 처리됩니다.                                                   |
| outPath                        | 문자열  | Query      | 아니요    | —              | 처리된 워크북이 저장될 클라우드 스토리지 폴더 경로. 생략 시 파일이 원본 폴더에 저장됩니다.                                                          |
| outStorageName                 | 문자열  | Query      | 아니요    | —              | 출력 파일이 저장될 클라우드 스토리지 이름.                                                                                                         |
| region                         | 문자열  | Query      | 아니요    | —              | 텍스트 분할에 사용할 로케일로, 구분자 해석 및 문자 인코딩에 영향을 줄 수 있음(예: `"en-US"`, `"ja-JP"`).                                            |
| password                       | 문자열  | Query      | 아니요    | —              | 암호 보호 스프레드시트를 열기 위한 암호.                                                                                                           |

### **응답**

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

- **400 Bad Request** – 잘못된 Aspose.Cells Cloud API URI 또는 잘못된 형식의 매개변수.
- **401 Unauthorized** – 누락되거나 잘못된 액세스 토큰(또는 클라이언트 ID/비밀번호).
- **404 Not Found** – 지정된 스프레드시트 파일에 액세스할 수 없음.
- **500 Server Error** – 스프레드시트 처리 중 내부 오류 발생.

## 텍스트 분할 API는 어디에 사용해야 하나요?

### **CSV 및 텍스트 파일 임포트 정리**

외부 시스템에서 데이터를 임포트할 때 필드가 종종 단일 셀에 연결되어 저장됩니다:

- **ERP/CRM 데이터 임포트** – `"John Doe;johndoe@email.com;555-1234"`를 이름, 이메일, 전화번호 열로 분할합니다.
- **데이터베이스 내보내기** – `"ORD-2024-001|Premium|Express"`와 같은 결합 키를 주문 ID, 등급, 배송 방법으로 파싱합니다.
- **로그 파일 분석** – `"2024-01-15 10:30:00|ERROR|ConnectionTimeout"`과 같은 반구조화된 로그를 필터링하기 위해 분할합니다.

### **레거시 시스템 마이그레이션**

- 오래된 시스템에서 다중 값 필드를 단일 셀에 덤프하므로, 이를 분할하여 새 데이터베이스 스키마와 일치시킵니다.
- 평면 파일 내보내기를 정규화된 Excel 테이블로 변환하여 Power BI 또는 Tableau에 바로 사용할 수 있도록 합니다.

### **데이터 클리닝 및 표준화**

- **구분자 정규화** – 혼합 구분자(`"A,B;C|D"`)를 여러 구분자 분할을 사용하여 일관된 형식으로 변환합니다.
- **공백 정리** – 단어 간 공백을 분할하여 추가 공백을 식별하고 제거합니다.
- **금융 데이터** – `"DEP-CHK-3847"`과 같은 결합 거래 코드를 거래 유형, 출처, 참조로 분할합니다.
- **의료 기록** – `"Smith,Jane_F_1985"`와 같은 환자 데이터를 성, 이름, 성별, 출생 연도로 파싱합니다.

## 왜 텍스트 분할 API를 사용해야 하나요?

- **특정 문자** – 쉼표, 세미콜론, 탭, 공백 등 단일 문자로 분할합니다.
- **문자열 조합** – `||`, `->`, 또는 사용자 정의 구분자와 같은 다중 문자 구분자를 사용합니다.
- **줄 바꿈** – 여러 줄 셀을 즉시 별도의 행으로 파싱합니다(주소, 코멘트, 설명 등).
- **사용자 정의 구분자** – 고유 데이터 형식을 위해 임의의 문자 조합을 구분자로 정의합니다.
- **개발자 친화적** – Aspose.Cells Cloud는 여러 언어로 SDK 라이브러리를 제공하여 빠른 개발을 지원하며, 포괄적인 문서도 제공됩니다. 사용자 정의 솔루션 구축에 비해 개발 작업량을 크게 줄여줍니다.
- **비용 효율적** – 워크북을 먼저 업로드하지 않고도 중복 문자를 제거할 수 있어 저장 공간을 절약하고 비용을 줄입니다.

## OpenAPI 사양

[OpenAPI 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/SplitText)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

### Aspose.Cells Cloud SDK 사용

SDK를 사용하는 것이 개발을 가속화하는 최선의 방법입니다. SDK는 기본 세부 사항을 처리하므로 최소한의 코드로 셀 텍스트 분할 기능을 간단히 구현할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitText.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitText.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitText.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitText.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitText.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitText.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitText.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitText.go" >}}  
{{</tab>}}  
{{< /tabs >}}