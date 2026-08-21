---
title: "Aspose.Cells Cloud Add Text API – 여러 Excel 셀에 한 번에 텍스트 추가 – 접두사, 접미사 및 라벨 삽입"
second_title: "문서"
ArticleTitle: "Excel 대량 텍스트 삽입 – 셀에 접두사, 접미사 및 사용자 정의 텍스트 추가 – 단계별 가이드"
linktype: "AddText"
type: docs
url: /ko/add-text/
keywords: "Aspose Cells API, Excel 텍스트 추가, 대량 텍스트 삽입, Excel 접두사 접미사, 스프레드시트 텍스트 교체, Excel 자동화, 클라우드 스프레드시트 API"
description: "Aspose.Cells Cloud를 사용해 한 번의 호출로 여러 Excel 셀에 접두사, 접미사 또는 사용자 정의 라벨을 삽입합니다. 텍스트 시작, 끝, 특정 텍스트 앞/뒤 등 원하는 위치에 삽입 가능. 범위, 워크시트 및 빈 셀 처리를 지원합니다."
weight: 100
---

한 번의 작업으로 여러 Excel 셀에 텍스트를 삽입합니다. Aspose.Cells API를 사용해 셀 내 시작 부분, 끝 부분, 또는 특정 텍스트 앞/뒤에 접두사, 접미사, 라벨 또는 사용자 정의 문자를 추가합니다.

## 개요

대상 범위의 모든 셀에 한 번의 호출로 접두사, 접미사 또는 특정 위치 기반 텍스트를 일괄 삽입합니다—수식이나 보조 열은 필요 없습니다.

- 각 셀 내 **임의의 위치**에 사용자 정의 텍스트 삽입

| 값               | 설명                                                              |
| ---------------- | ----------------------------------------------------------------- |
| `None`           | 원래 콘텐츠를 대체                                                |
| `AtTheBeginning` | 시작 부분에 삽입 (접두사)                                         |
| `AtTheEnd`       | 끝 부분에 삽입 (접미사)                                           |
| `BeforeText`     | `selectText`의 첫 번째 출현 **앞**에 삽입; 없으면 건너뜀          |
| `AfterText`      | `selectText`의 첫 번째 출현 **뒤**에 삽입; 없으면 건너뜀          |

- 네 가지 위치 모드: 접두사, 접미사, 특정 하위 문자열 앞/뒤 삽입
- 불필요한 삽입을 방지하기 위해 빈 셀 건너뛰기 지원
- API는 **문자열 유형** 값만 처리합니다. 숫자, 논리값, 수식은 먼저 텍스트로 변환됩니다.
- **빈 셀 처리**
  - `skipEmptyCells = true` → 빈 셀은 건너뜁니다.
  - `skipEmptyCells = false` → 빈 셀에 텍스트가 삽입됩니다 (셀 유형이 텍스트로 변경됨).

- **앵커 텍스트 미존재 시**: `position = BeforeText | AfterText`이고 `selectText`가 **존재하지 않을** 경우, 셀 값은 변경되지 않습니다.

### **웹 API**

```http
PUT https://api.aspose.cloud/v4.0/cells/content/add/text
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 확보되었으며 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

```bash
-H "Authorization: Bearer {access_token}"
```

### **AddText** API 요청 매개변수는 다음과 같습니다:

| 매개변수 이름    | 유형      | 경로/쿼리 문자열/HTTP 본문 | 설명                                                                                                                                              | 필수 여부 |
| :------------- | :------ | :------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------ | :------- |
| Spreadsheet    | File    | FormData                   | 처리할 스프레드시트 파일입니다. 지원 포맷: XLSX, XLS, ODS, CSV 등.                                                                               | 예       |
| text           | String  | Query                      | 스프레드시트 내 지정된 셀에 추가할 텍스트 콘텐츠입니다.                                                                                           | 예       |
| position       | String  | Query                      | 기존 셀 콘텐츠 대비 텍스트 삽입 위치를 지정합니다. 옵션: `AtTheBeginning`, `AtTheEnd`, `BeforeText`, `AfterText`, `None`.                         | 예       |
| selectText     | String  | Query                      | _(선택 사항)_ 지정된 하위 문자열을 포함하는 셀에만 텍스트를 추가합니다. `position` 매개변수와 함께 사용됩니다.                                    | 아니요   |
| skipEmptyCells | Boolean | Query                      | `true`일 경우 빈 셀을 건너뜁니다; `false`일 경우 빈 셀에도 텍스트를 추가합니다.                                                                   | 아니요   |
| worksheet      | String  | Query                      | _(선택 사항)_ 텍스트를 추가할 워크시트 이름입니다. 생략 시 기본적으로 첫 번째 워크시트에 적용됩니다.                                              | 아니요   |
| range          | String  | Query                      | _(선택 사항)_ 텍스트를 추가할 셀 범위입니다 (예: `"A1:C10"`). 생략 시 지정된 워크시트 내 사용된 모든 셀에 적용됩니다.                             | 아니요   |
| outPath        | String  | Query                      | _(선택 사항)_ 처리된 워크북을 저장할 클라우드 스토리지 폴더 경로입니다. 생략 시 원본 폴더에 저장됩니다.                                           | 아니요   |
| outStorageName | String  | Query                      | 출력 파일을 저장할 클라우드 스토리지 이름입니다.                                                                                                  | 아니요   |
| region         | String  | Query                      | _(선택 사항)_ 출력 파일의 숫자, 날짜, 통화 서식을 위한 로케일을 설정합니다 (예: `"en-US"`, `"zh-CN"`, `"de-DE"`).                                | 아니요   |
| password       | String  | Query                      | _(선택 사항)_ 업로드한 스프레드시트가 암호로 보호되어 있는 경우, 파일을 열고 처리하기 위한 암호를 입력합니다.                                      | 아니요   |

**cURL 예시**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/content/add/text?text=Report&position=AtTheBeginning&skipEmptyCells=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/workbook.xlsx" \
  -F "outPath=output/workbook_modified.xlsx"
```

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

| 코드 | 설명 |
| ---- | ----------- |
| **400** Bad Request | 잘못된 Aspose.Cells Cloud API URI 또는 필수 매개변수 누락 |
| **401** Unauthorized | 잘못된 액세스 토큰 또는 잘못된 클라이언트 ID 및 비밀번호 |
| **404** Not Found | 스프레드시트 파일에 접근할 수 없음 |
| **500** Server Error | 수치 계산 데이터를 가져오는 동안 스프레드시트에 문제가 발생함 |

## 어디서 스프레드시트용 텍스트 추가 API를 사용해야 하나요?

- **동적 보고서 라벨링**: 자동 생성된 재무제표 및 영업 보고서에 동적 제목, 날짜 태그 또는 메모를 자동 추가합니다.
- **일괄 파일 워터마킹**: 일괄 Excel 파일에 회사 로고, 기밀성 워터마크, 버전 정보 등을 추가합니다.
- **템플릿 데이터 채우기**: 계약서 또는 인보이스 템플릿의 지정된 위치에 고객 이름, 금액 등 텍스트를 자동으로 채웁니다.
- **데이터 분류 태깅**: 분석 결과에 따라 데이터 행에 분류 태그 또는 상태 라벨(예: “검토 대기 중”, “승인됨”)을 자동으로 추가합니다.
- **데이터 품질 주석**: 데이터 클리닝 중 문제가 있는 데이터에 메모를 자동 추가합니다.
- **대량 텍스트 서식**: 제품명 또는 고객명에 일관되게 접두사 또는 접미사를 추가합니다.

## 왜 스프레드시트용 텍스트 추가 API를 사용해야 하나요?

- **대량 텍스트 추가**: 수백 개의 셀 또는 파일에 동시에 텍스트를 추가해 수동 작업 대비 최대 95% 시간 절약 가능.
- **정밀 위치 제어**: 셀 시작, 끝, 또는 특정 텍스트 앞/뒤 등 6가지 위치에 정확히 텍스트를 삽입 가능.
- **스마트 조건부 처리**: 셀이 빈 셀인지, 특정 텍스트를 포함하는지 여부에 따라 텍스트 추가 여부를 결정할 수 있습니다.
- **다중 위치 전략 지원**:
  - `AtTheBeginning`: 선택된 모든 셀 콘텐츠 앞에 동일한 텍스트 추가
  - `AtTheEnd`: 선택된 모든 셀 콘텐츠 뒤에 텍스트 추가
  - `BeforeText` / `AfterText`: 특정 텍스트가 포함된 셀에만 텍스트를 앞/뒤에 추가
  - `None`: 원래 콘텐츠를 대체
- **정밀 범위 제어**: 작업을 수행할 특정 워크시트 또는 셀 범위를 지정 가능.
- **조건부 건너뛰기 옵션**: 불필요한 텍스트 추가를 방지하기 위해 빈 셀 건너뛰기 지원.
- **개발자 친화적**: Aspose.Cells Cloud는 여러 언어의 SDK 라이브러리를 제공해 빠른 개발이 가능하며, 종합적인 문서도 함께 제공됩니다. 사용자 정의 차트 렌더링 솔루션 구축에 비해 개발 작업량을 크게 줄여줍니다.
- **비용 효율적**: 워크북을 먼저 업로드하지 않고도 셀에 텍스트를 추가할 수 있어 저장 공간 절약 및 비용 절감 가능.

## OpenAPI 스펙

[OpenAPI 스펙](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/AddText)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

### Aspose.Cells Cloud SDK 사용하기

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 하위 세부 사항을 모두 처리해 주므로, 최소한의 코드만으로 셀에 텍스트를 추가하는 기능을 구현할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예시는 여러 SDK를 사용해 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AddText.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AddText.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AddText.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AddText.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AddText.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AddText.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AddText.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AddText.go" >}}
{{</tab>}}
{{< /tabs >}}
---