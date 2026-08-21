---
title: "Aspose.Cells Cloud 텍스트 트리밍 웹 API - 여분의 공백 및 줄 바꿈 제거"
second_title: "문서"
ArticleTitle: "Excel 데이터 클리너 - 자동으로 문자, 공백 및 줄 바꿈 트리밍 – 온라인, 단축 코드"
linktype: "트림 문자"
type: docs
url: /ko/trim-character/
keywords: "Excel, 텍스트 트리밍, 공백 제거, 줄 바꿈, Aspose.Cells, 데이터 클리닝, 스프레드시트, 셀 서식 정규화"
description: "Aspose.Cells Cloud API를 사용하여 Excel 셀에서 여분의 공백, 줄 바꿈, 불필요한 문자를 트리밍하세요. 깨끗하고 일관된 스프레드시트 데이터를 보장합니다."
weight: 100
---

Aspose.Cells 트림 문자 API를 사용하여 Excel 셀에서 불필요한 문자, 여분의 공백 및 줄 바꿈을 자동으로 트리밍하세요. 데이터 입력을 정리하고 스프레드시트 전체에서 일관된 서식을 유지하세요.

## **개요**

- **첫 번째 및 마지막 공백 트리밍**
  - 텍스트 시작 및 끝에 있는 여분의 공백 제거
  - 데이터 외관의 깔끔함과 가독성 향상
- **단어 사이 여분의 공백 처리**
  - 단어 사이의 여분 공백 제거
  - 다중 소스 데이터로 인해 발생하는 서식 혼란 해결

- **특수 공백 제거**
  - 줄 바꿈 없이 유지되는 공백(Non-breaking space) 명시적으로 제거
  - 데이터 정확성 및 일관성 보장

- **줄 바꿈 관리**
  - 여분 또는 모든 줄 바꿈 제거
  - 셀 내용을 체계적이고 전문적인 외관으로 유지

## **TrimCharacter API**

API를 호출하기 전에 유효한 Aspose Cloud 계정, `client_id`/`client_secret`, 그리고 **Cells** 범위가 포함된 액세스 토큰이 필요합니다.

### 웹 API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/trim
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 보장되며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

```bash
-H "Authorization: Bearer {access_token}"
```

### **trimCharacter** API의 요청 매개변수

| 매개변수 이름            | 유형    | 경로/쿼리 문자열/HTTP 본문 | 설명                                                                                                                                                        |
| :---------------------- | :------ | :------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet             | 파일    | FormData                   | 처리할 스프레드시트 파일입니다. 지원되는 형식은 XLSX, XLS, ODS, CSV 등입니다.                                                                              |
| trimContent             | 문자열  | 쿼리                       | 셀 내용에서 트리밍할 특정 문자나 문자열을 지정합니다. 단일 문자, 다중 문자, 또는 사용자 정의 패턴이 가능합니다.                                             |
| trimLeading             | 불리언  | 쿼리                       | `true`인 경우, 지정된 문자를 각 셀 내용의 시작부에서 제거합니다.                                                                                           |
| trimTrailing            | 불리언  | 쿼리                       | `true`인 경우, 지정된 문자를 각 셀 내용의 끝부에서 제거합니다.                                                                                             |
| trimSpaceBetweenWordTo1 | 불리언  | 쿼리                       | `true`인 경우, 각 셀 내에서 단어 사이의 여러 연속 공백을 단일 공백으로 줄입니다.                                                                          |
| trimNonBreakingSpaces   | 불리언  | 쿼리                       | `true`인 경우, 셀 내용에서 줄 바꿈 없이 유지되는 공백 문자(유니코드 U+00A0)를 제거합니다.                                                                  |
| removeExtraLineBreaks   | 불리언  | 쿼리                       | `true`인 경우, 각 셀 내에서 여러 연속 줄 바꿈을 단일 줄 바꿈으로 줄입니다.                                                                                  |
| removeAllLineBreaks     | 불리언  | 쿼리                       | `true`인 경우, 셀 내용에서 모든 줄 바꿈 문자를 제거합니다.                                                                                                  |
| worksheet               | 문자열  | 쿼리                       | _(선택 사항)_ 텍스트 트리밍을 적용할 워크시트 이름입니다. 생략 시 첫 번째 워크시트에 작업이 적용됩니다.                                                     |
| range                   | 문자열  | 쿼리                       | _(선택 사항)_ 텍스트 트리밍을 적용할 셀 범위입니다(예: `"A1:C10"`). 생략 시 지정된 워크시트 내 사용된 모든 셀에 작업이 적용됩니다.                           |
| outPath                 | 문자열  | 쿼리                       | _(선택 사항)_ 처리된 워크북이 저장될 클라우드 스토리지 폴더 경로입니다. 생략 시 파일은 원본 폴더에 저장됩니다.                                              |
| outStorageName          | 문자열  | 쿼리                       | 출력 파일이 저장될 클라우드 스토리지의 이름입니다.                                                                                                          |
| region                  | 문자열  | 쿼리                       | _(선택 사항)_ 텍스트 처리를 위한 로케일을 설정합니다. 이는 특정 언어에 대한 공백 및 줄 바꿈 처리 방식에 영향을 줄 수 있습니다(예: `"en-US"`, `"ar-SA"`).    |
| password                | 문자열  | 쿼리                       | _(선택 사항)_ 업로드된 스프레드시트가 암호로 보호된 경우, 파일을 열고 처리하기 위해 암호를 제공하세요.                                                      |

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

**성공 예시(HTTP 200):** API는 트리밍된 워크북을 포함하는 파일 스트림을 반환합니다.

### 오류 코드

- **400 잘못된 요청(Bad Request)**: 잘못된 Aspose.Cells Cloud API URI입니다.
- **401 인증되지 않음(Unauthorized)**: 잘못된 액세스 토큰입니다. 또는 잘못된 클라이언트 ID 및 비밀번호입니다.
- **404 찾을 수 없음(Not Found)**: 스프레드시트 파일에 접근할 수 없습니다.
- **500 서버 오류(Server Error)**: 스프레드시트에서 계산 데이터를 가져오는 과정에서 이상이 발생했습니다.

## 트림 문자 API는 어디에 사용해야 하나요?

- **사용자 입력 정규화**: 수동으로 입력된 사용자 테이블 데이터를 정리하여 여분의 공백과 줄 바꿈을 제거합니다.
- **고객 데이터베이스 유지보수**: 고객 이름, 주소, 연락처 세부 정보의 불필요한 공백 및 서식 문제를 정리합니다.
- **자동 보고서 정리**: 자동 보고서 생성 전에 데이터 소스의 서식 문제를 정리합니다.
- **데이터 마이그레이션 준비**: 새로운 시스템으로 데이터를 마이그레이션하기 전에 서식 문제를 정리합니다.

## 왜 트림 문자 API를 사용해야 하나요?

- **노동 비용 절감**: 데이터 클리닝을 위한 시간 소모적인 수동 작업을 제거합니다.
- **에러 비용 절감**: 서식 문제로 인한 분석 오류를 방지합니다.
- **사용량 과금**: 고정 요금 없이 실제 처리량만 과금됩니다.
- **인프라 투자 없음**: 서버나 소프트웨어 유지보수가 필요 없습니다.
- **다중 형식 지원**: XLSX, XLS, CSV, ODS 등 다양한 형식 처리를 지원합니다.
- **개발자 친화적**: Aspose.Cells Cloud는 여러 언어로 SDK 라이브러리를 제공하여 빠른 개발을 가능하게 하며, 포괄적인 문서도 제공합니다. 사용자 정의 차트 렌더링 솔루션 구축에 비해 개발 작업량을 크게 줄여줍니다.
- **비용 효율성**: 워크북을 먼저 업로드하지 않고도 중복 문자를 제거할 수 있어 저장 공간을 절약하고 비용을 줄입니다.

## OpenAPI 사양

[OpenAPI 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/TrimCharacter)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

### Aspose.Cells Cloud SDK 사용

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 내부 세부 사항을 처리하므로, 최소한의 코드로 셀의 트림 문자 기능을 간단히 구현할 수 있습니다.
Aspose.Cells Cloud SDK 전체 목록은 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_TrimTextInSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_TrimTextInSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_TrimTextInSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_TrimTextInSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_TrimTextInSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_TrimTextInSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_TrimTextInSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_TrimTextInSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}