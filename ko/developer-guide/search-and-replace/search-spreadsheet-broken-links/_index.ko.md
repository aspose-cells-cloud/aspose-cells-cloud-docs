---
title: "스프레드시트 링크 끊김 검색 – Aspose.Cells Cloud API"
second_title: "문서"
ArticleTitle: "Excel에서 끊긴 링크 찾기 및 수정 – 클라우드 스프레드시트 링크 검사기"
linktitle: "스프레드시트 끊긴 링크 검색"
type: docs
url: /ko/search-spreadsheet-broken-links/
keywords: "Aspose Cells, 끊긴 링크, 스프레드시트 감사, Excel API, 클라우드 스프레드시트, 링크 검사기"
description: "Aspose.Cells Cloud API를 통해 Excel 워크북의 끊긴 링크를 탐지하고 수정합니다. 범위를 스캔하고 자세한 JSON 결과를 가져온 후, 모든 언어 SDK와 통합하세요."
weight: 100
---

## **스프레드시트 끊긴 링크 검색 API**

Excel 파일 내 끊긴 링크를 자동으로 탐지합니다. 이 API는 지정된 범위에서 끊긴 외부 참조, 유효하지 않은 수식, 누락된 데이터 소스를 검사합니다. 원격 스프레드시트 감사, 자동 품질 검사 및 클라우드 스토리지 제공자와의 통합을 지원합니다. 엔터프라이즈 워크플로 자동화를 위한 RESTful API입니다.

**요약:** 이 엔드포인트를 사용해 워크북 내 유효하지 않은 링크를 빠르게 식별하고 수정하여, 재무 모델, M&A 데이터셋 및 투자자용 보고서 패키지 등에서 데이터 무결성을 확보하세요.

### **Web API**

```bash
PUT https://api.aspose.cloud/v4.0/cells/search/broken-links
```

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/search/broken-links?worksheet=Sheet1" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@sample.xlsx"
```

### 보안 및 인증

Aspose.Cells Cloud API는 보안이 확보되었으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

```bash
-H "Authorization: Bearer {access_token}"
```

### 요청 매개변수

| 매개변수 이름 | 유형   | 위치              | 설명                                                                                                           |
| ------------- | ------ | ----------------- | -------------------------------------------------------------------------------------------------------------- |
| Spreadsheet   | 파일   | FormData (multipart) | **필수.** 분석할 Excel 워크북 파일(`.xlsx`, `.xls` 등).                                                     |
| worksheet     | 문자열 | 쿼리              | **선택 사항.** 분석할 워크시트 이름. 생략 시 첫 번째 워크시트가 사용됩니다.                                  |
| cellArea      | 문자열 | 쿼리              | **선택 사항.** A1 표기법으로 지정된 대상 셀 범위(예: `B2:D10`). 지정하지 않으면 사용된 전체 범위가 분석됩니다. |
| region        | 문자열 | 쿼리              | **선택 사항.** 지역 설정(예: `ko-KR`)으로, 날짜, 숫자, 통화 해석에 영향을 줄 수 있습니다.                     |
| password      | 문자열 | 쿼리              | **선택 사항.** 암호화된 워크북의 비밀번호. 파일이 보호되지 않은 경우 비워 두세요.                             |

### 응답

```json
{
  "BrokenLinks": [
    {
      "CellName": "B5",
      "Link": "C:\\Data\\source.xlsx",
      "ErrorMessage": "파일을 찾을 수 없습니다",
      "Status": "끊김"
    },
    {
      "CellName": "C12",
      "Link": "http://example.com/data.csv",
      "ErrorMessage": "404 Not Found",
      "Status": "끊김"
    }
  ],
  "Code": 200,
  "Status": "OK"
}
```

### 오류 코드

| 코드 | 설명 |
|------|------|
| **400 Bad Request** | 잘못된 Aspose.Cells Cloud API URI입니다. |
| **401 Unauthorized** | 잘못된 액세스 토큰, 클라이언트 ID 또는 클라이언트 비밀번호입니다. |
| **404 Not Found** | 스프레드시트 파일에 접근할 수 없습니다. |
| **429 Too Many Requests** | 속도 제한 초과(분당 60회 호출 제한). |
| **500 Server Error** | 계산 데이터를 가져오는 동안 스프레드시트에 이상이 발생했습니다. |


## 스프레드시트 끊긴 링크 검색 API는 어디에 사용해야 하나요?

- **대규모 재무 모델 정기 감사**: 월간/분기 보고서를 배포하기 전, 외부 데이터 참조가 많은 핵심 계산 영역(예: `Dashboard!B5:K50`)을 자동으로 스캔하여 모든 링크가 유효한 소스 파일을 가리키는지 확인하세요.  
- **인수합병(M&A)을 위한 데이터 통합**: 부서별를 나타내는 여러 스프레드시트 파일을 병합한 후, "개요" 워크시트를 검사해 파일 경로 변경이나 권한 문제로 인해 끊긴 링크를 식별하세요.  
- **투자자 데이터 패키지 준비**: 외부 데이터베이스 또는 시장 데이터 소스와 연결된 차트 및 표를 포함한 최종 발표 자료를 작성하기 전, 모든 링크의 유효성을 확인하세요.

## 왜 스프레드시트 끊긴 링크 검색 API를 사용해야 하나요?

- **개발자 친화적** – Aspose.Cells Cloud는 여러 언어의 SDK 라이브러리를 제공하여 빠른 개발과 풍부한 문서화를 지원합니다. 사용자 정의 솔루션을 구축하는 것에 비해 개발 부담을 크게 줄여줍니다.  
- **인건비 절감** – 문서 링크를 수동으로 검증하기 위한 전담 인력이 필요 없어집니다.  
- **사용량 과금** – 사전 투자가 필요 없으며, 실제로 사용한 API 호출 수에만 요금이 부과됩니다.  
- **유지보수 비용 없음** – 유지 관리할 서버가 없고, 소프트웨어 업데이트 및 호환성 문제도 없습니다.  
- **복잡한 Excel 서식 유지** – 원본 워크북의 레이아웃을 유지한 채, 범용적으로 접근 가능한 JSON 형식으로 결과를 반환합니다.

## SDK를 사용한 스프레드시트 끊긴 링크 검색 API 사용 방법

### OpenAPI 사양

[OpenAPI 사양](https://reference.aspose.cloud/cells/#/SearchController/SearchSpreadsheetBrokenLinks){:target="_blank" rel="noopener noreferrer"}은 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있는 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의합니다.

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 극대화할 수 있습니다. SDK는 내부 세부 사항을 처리해 주므로, 최소한의 코드로 끊긴 링크 검색 기능만 구현하면 됩니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud){:target="_blank" rel="noopener noreferrer"}를 확인하세요.

아래 코드 예제는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchSpreadsheetBrokenLinks.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchSpreadsheetBrokenLinks.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchSpreadsheetBrokenLinks.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchSpreadsheetBrokenLinks.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchSpreadsheetBrokenLinks.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchSpreadsheetBrokenLinks.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchSpreadsheetBrokenLinks.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchSpreadsheetBrokenLinks.go" >}}
{{</tab>}}
{{< /tabs >}}