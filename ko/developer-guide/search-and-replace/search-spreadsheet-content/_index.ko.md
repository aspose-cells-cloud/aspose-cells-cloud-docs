---
title: "스프레드시트 콘텐츠 검색 – Aspose.Cells Cloud API(Excel에서 텍스트 찾기)"
second_title: "문서"
ArticleTitle: "로컬 Excel 스프레드시트에서 텍스트 검색 – 특정 데이터 찾기"
linktype: "docs"
url: /ko/search-spreadsheet-content/
keywords: "Aspose.Cells, Excel 검색 API, 스프레드시트 콘텐츠 검색, 클라우드 스프레드시트 API, 텍스트 조회"
description: "Aspose.Cells Cloud API를 사용하여 로컬 Excel 파일에서 텍스트, 숫자 또는 수식을 검색합니다. 대소문자 구분 없는 쿼리, 워크시트 단위 범위, 보안 인증을 지원합니다."
weight: 100
---

## **스프레드시트 콘텐츠 검색 API**

Aspose.Cells Cloud API를 사용하여 프로그래밍 방식으로 Excel 스프레드시트 내 특정 텍스트를 검색합니다. 이 API는 클라우드에 저장된 로컬 파일에서 텍스트, 숫자 또는 수식을 찾아내어 자동화된 데이터 탐색, 콘텐츠 분석 및 스프레드시트 감사 워크플로우를 가능하게 합니다.


### **웹 API**

```
PUT https://api.aspose.cloud/v4.0/cells/search/content
```

직접 HTTP 요청을 사용하는 것을 선호하는 경우, 다음 cURL 예제와 동일한 요청을 수행합니다:

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/search/content?searchText=Invoice&ignoringCase=true" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: multipart/form-data" \
     -F "spreadsheet=@/path/to/your/file.xlsx"
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 갖추고 있으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

```bash
-H "Authorization: Bearer {access_token}"
```

### **요청 파라미터**

| 파라미터     | 타입     | 위치      | 설명                                                                              |
| ------------ | ------- | -------- | --------------------------------------------------------------------------------- |
| spreadsheet  | File    | FormData | 검색할 Excel 파일.                                                                |
| searchText   | String  | Query    | 워크북 내에서 찾고자 하는 텍스트(또는 숫자 값).                                    |
| ignoringCase | Boolean | Query    | 대소문자 구분 없이 검색하려면 `true`로 설정.                                      |
| worksheet    | String  | Query    | 검색 범위를 제한할 워크시트 이름. 생략 시 모든 워크시트가 검색됩니다.             |
| cellArea     | String  | Query    | 검색 영역을 제한하는 A-1 스타일 범위(예: `A1:C10`).                               |
| region       | String  | Query    | 서비스의 지리적 영역(예: `us-east-1`).                                            |
| password     | String  | Query    | 보호된 워크북을 열기 위한 비밀번호.                                               |


### **응답**

API는 일치하는 셀 배열을 포함하는 `SearchResult` 객체를 반환합니다. 각 요소는 워크시트 이름, 셀 주소 및 일치한 텍스트를 제공합니다.

```json
{
  "textItems": [
    {
      "cellName": "A1",
      "text": "Total",
      "occurrences": 1
    },
    {
      "cellName": "B5",
      "text": "Total",
      "occurrences": 2
    }
  ],
  "code": 200,
  "status": "OK"
}
```

### 오류 코드

- **400 Bad Request** – 요청 URI 또는 파라미터가 잘못되었습니다.
- **401 Unauthorized** – 액세스 토큰 누락 또는 유효하지 않거나, 클라이언트 자격 증명이 잘못되었습니다.
- **404 Not Found** – 지정된 스프레드시트에 접근할 수 없습니다.
- **500 Internal Server Error** – 워크북 처리 중 예기치 않은 서버 오류가 발생했습니다.

## 스프레드시트 내 콘텐츠 검색 API는 어디에 사용해야 하나요?

- **포괄적인 워크북 규정 준수 감사** – 데이터 보안 및 규정 준수 검사를 위해 “기밀 조항”, “내부 데이터”와 같은 민감한 용어를 워크북 전체에서 검색합니다.
- **워크시트 간 데이터 연관 쿼리** – 여러 워크시트에 나타나는 프로젝트 번호 또는 고객 이름을 찾아 빠르게 워크시트 간 통합을 수행합니다.
- **대량 템플릿 콘텐츠 검증** – 보고서 생성 후 `{{Date}}`와 같은 모든 플레이스홀더가 일괄 Excel 파일에서 올바르게 교체되었는지 확인합니다.
- **역사적 데이터 보관 및 마이닝** – 특정 이벤트 코드 또는 비즈니스 용어를 찾아 레거시 Excel 파일에서 데이터 아케올로지 및 분석을 가속화합니다.

## 왜 스프레드시트 내 콘텐츠 검색 API를 사용해야 하나요?

- **개발자 친화적** – 다양한 언어에 대한 SDK가 제공되며, 사용자 정의 솔루션 구축에 비해 개발 노력이 적게 듭니다.
- **인력 비용 절감** – 수동으로 스프레드시트를 검사해야 했던 작업을 자동화합니다.
- **사용량 과금** – 실제로 호출한 API 요청만 요금이 부과됩니다.
- **유지보수 불필요** – 관리할 서버가 없고, 소프트웨어 업데이트도 필요 없으며, 호환성 문제도 없습니다.
- **복잡한 서식 보존** – 결과는 원래 Excel 레이아웃을 유지한 채 PDF로 내보낼 수 있습니다.

## SDK를 사용하여 스프레드시트 API 내에서 링크 오류 검색을 어떻게 사용하나요?

### OpenAPI 스펙

[OpenAPI 스펙](https://reference.aspose.cloud/cells/#/SearchControllor/SearchSpreadsheetContent)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

### Aspose.Cells Cloud SDK 사용

SDK를 사용하는 것이 검색 기능을 통합하는 가장 빠른 방법입니다. SDK는 HTTP 계층을 추상화하여 최소한의 코드로 API를 호출할 수 있게 해줍니다. SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)에서 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 스프레드시트 콘텐츠 검색 작업을 호출하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInLocalFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInLocalFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInLocalFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInLocalFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInLocalFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInLocalFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInLocalFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInLocalFile.go" >}}
{{</tab>}}
{{< /tabs >}}