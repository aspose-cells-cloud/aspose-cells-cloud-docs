---
title: "원격 엑셀 스프레드시트에서 텍스트 검색 – Aspose.Cells Cloud API"
secondtitle: "문서"
articletitle: "원격 엑셀 스프레드시트에서 텍스트 검색 – 특정 데이터 찾기"
linktitle: "원격 스프레드시트 콘텐츠 검색"
type: docs
url: /search-content-in-remote-spreadsheet/
keywords: "Aspose.Cells, 엑셀 검색 API, 클라우드 스프레드시트, 텍스트 검색, REST"
description: "클라우드 스토리지에 저장된 엑셀 파일에서 텍스트, 숫자 또는 수식을 검색합니다. Aspose.Cells Cloud를 사용하면 대소문자 구분 없이 쿼리를 실행하고, 폴더를 지정하며, 암호로 보호된 워크북도 검색할 수 있습니다."
weight: 100
---

### **원격 스프레드시트 콘텐츠 검색 API**

Aspose.Cells Cloud API를 사용하여 엑셀 스프레드시트 내에서 특정 텍스트를 프로그래밍 방식으로 검색합니다. 클라우드 스토리지에 저장된 파일에서 텍스트, 숫자 또는 수식을 찾아냅니다. 이 RESTful API는 자동화된 데이터 탐색, 콘텐츠 분석 및 스프레드시트 감사 워크플로우를 가능하게 합니다.

### **웹 API**

```bash
PUT https://api.aspose.cloud/v4.0/cells/{name}/search/content
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 강화되어 있으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

```bash
-H "Authorization: Bearer {access_token}"
```

### **요청 매개변수:**

| 매개변수 이름 | 유형    | 경로/쿼리 문자열/HTTP 본문 | 설명                                                                                                                                                   |
| :------------ | :------ | :------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------- |
| name          | String  | Path                       | **필수**. 텍스트 검색을 수행할 엑셀 워크북의 파일 이름(확장자 포함)입니다. 예: `sales_data.xlsx`                                                       |
| searchText    | String  | Query                      | **필수**. 전체 워크북 또는 워크시트에서 찾을 정확한 문자열, 숫자 또는 부분 콘텐츠입니다.                                                               |
| ignoringCase  | Boolean | Query                      | **선택 사항**. 대소문자 구분 여부를 결정합니다. 대소문자 구분 없이 매칭하려면 `true`로 설정(예: “Report”는 “REPORT”와 매칭됨). 기본값은 `false`입니다. |
| folder        | String  | Query                      | **선택 사항**. 대상 워크북이 위치한 클라우드 스토리지 내 디렉터리 경로입니다. 생략 시 루트 폴더가 기본값으로 사용됩니다.                               |
| storageName   | String  | Query                      | **선택 사항**. 사용자 정의 클라우드 스토리지 서비스의 이름 식별자입니다. 지정하지 않으면 계정과 연결된 기본 스토리지를 사용합니다.                     |
| region        | String  | Query                      | **선택 사항**. 검색 시 적용되는 로케일 설정(예: `es-ES`)으로, 텍스트 정규화 또는 정렬 규칙에 영향을 줄 수 있습니다.                                    |
| password      | String  | Query                      | **선택 사항**. 암호로 보호된 엑셀 파일에 접근하기 위한 복호화 비밀번호입니다. 파일이 암호화되어 있지 않다면 이 매개변수를 생략하세요.                  |

**용어 설명**

- **searchText** – 검색할 정확한 문자열로, 부분 일치도 가능합니다.
- **ignoringCase** – `true`로 설정하면 대소문자를 구분하지 않고 검색하고, `false`이면 구분합니다.
- **folder** – 워크북이 위치한 디렉터리 경로입니다.
- **storageName** – 사용자 정의 스토리지 설정의 식별자입니다.
- **region** – 텍스트 비교 규칙에 영향을 주는 로케일 코드입니다.
- **password** – 보호된 워크북을 복호화하기 위한 비밀번호입니다.

### **응답**

```json
{
  "Code": 200,
  "Status": "OK",
  "TextItems": [
    {
      "Filename": "string",
      "Worksheet": "string",
      "Position": "string",
      "Content": "string"
    }
  ]
}
```

응답은 검색한 텍스트가 발견된 셀 목록(`CellName`)과 함께 워크시트 이름 및 일치하는 텍스트를 포함합니다. 일치 항목이 없을 경우 `TextItems` 배열은 비어 있으며, 요청은 여전히 HTTP 200 OK를 반환합니다.

### 오류 코드

- **400 Bad Request** – 잘못된 Aspose.Cells Cloud API URI입니다.
  ```json
  { "code": 400, "message": "Invalid request URI" }
  ```
- **401 Unauthorized** – 잘못된 액세스 토큰, 클라이언트 ID 또는 클라이언트 시크릿입니다.
  ```json
  { "code": 401, "message": "Invalid access token" }
  ```
- **404 Not Found** – 스프레드시트 파일에 접근할 수 없습니다.
  ```json
  { "code": 404, "message": "File not found" }
  ```
- **500 Server Error** – 예기치 않은 조건으로 인해 API가 요청을 완료하지 못했습니다.
  ```json
  { "code": 500, "message": "Internal server error" }
  ```

## 스프레드시트 콘텐츠 검색 API는 어디에 사용해야 하나요?

- **종합적인 워크북 준수 감사** – 기업 데이터 보안 및 준수 검사를 위해 전체 엑셀 파일을 빠르게 스캔하여 모든 민감한 용어(예: “기밀 조항”, “내부 데이터”)를 식별합니다.
- **워크시트 간 데이터 연관성 쿼리** – 프로젝트 정보가 여러 워크시트에 분산된 경우, 특정 프로젝트 번호나 고객 이름을 검색하여 관련 모든 데이터를 즉시 찾습니다.
- **일괄 템플릿 콘텐츠 검증** – 자동 보고서 생성 후, 여러 엑셀 파일을 일괄적으로 스캔하여 모든 사전 설정된 자리표시자(예: `{{Date}}`)가 올바르게 교체되었는지 확인하여 보고서의 완성도와 정확성을 보장합니다.
- **역사적 데이터 보관 및 마이닝** – 레거시 파일을 분석하여 특정 이벤트 코드나 비즈니스 용어를 검색하고, 데이터 고고학을 위해 역사적 비즈니스 로직을 빠르게 파악합니다.

## 왜 스프레드시트 콘텐츠 검색 API를 사용해야 하나요?

- **개발자 친화적** – Aspose.Cells Cloud는 다양한 언어의 SDK 라이브러리를 제공하며, 체계적인 문서를 통해 빠른 개발을 지원합니다. 맞춤형 솔루션 구축에 비해 개발 작업량을 크게 줄여줍니다.
- **인력 비용 절감** – 반복적인 검색 작업을 자동화하여 개발자가 수동 데이터 추출 작업에서 해방됩니다.
- **사용량 과금** – 초기 투자 없이 실제로 사용한 API 호출에만 요금이 부과됩니다.
- **유지보수 불필요** – Aspose가 서버, 업데이트 및 호환성을 관리하므로 애플리케이션 로직 개발에 집중할 수 있습니다.
- **복잡한 엑셀 서식 보존** – 결과를 원래 스타일을 유지하며 보편적으로 접근 가능한 PDF 형식으로 내보낼 수 있습니다.

## 스프레드시트 API 범위 내의 링크 오류 검색을 SDK와 함께 사용하는 방법

### OpenAPI 사양

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchContentInRemoteSpreadsheet" rel="noopener noreferrer">OpenAPI 사양</a>은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

### Aspose.Cells Cloud SDK 사용

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 내부 세부 사항을 처리하므로 셀의 스프레드시트 내 콘텐츠 검색을 최소한의 코드로 간편하게 구현할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 설명합니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInRemoteSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInRemoteSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInRemoteSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInRemoteSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInRemoteSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInRemoteSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInRemoteSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInRemoteSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}

---
