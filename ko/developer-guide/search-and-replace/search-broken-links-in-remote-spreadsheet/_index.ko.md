---
title: "Aspose.Cells Cloud – Excel 링크 끊김 감지 API – 원격 워크북의 스프레드시트 링크 검사 및 유효성 검사"
second title: "문서"
ArticleTitle: "원격 Excel 파일의 끊긴 링크 찾기 및 수정 – 클라우드 스프레드시트 링크 검사기"
linktitle: "원격 스프레드시트 끊긴 링크 검색"
type: docs
url: /ko/search-broken-links-in-remote-spreadsheet/
keywords: "Excel, 끊긴 링크, API, 클라우드, 스프레드시트, 유효성 검사, Aspose.Cells"
description: "Aspose.Cells Cloud API를 사용하여 원격 Excel 워크북에서 끊긴 외부 링크, 잘못된 수식, 누락된 데이터 소스를 검사합니다."
weight: 100
---

## **원격 스프레드시트에서 끊긴 링크 검색 API**

클라우드 저장소에 저장된 Excel 파일에서 끊긴 링크를 자동으로 감지합니다. 이 API는 지정된 범위 내에서 끊긴 외부 참조, 잘못된 수식, 누락된 데이터 소스를 검사합니다. 클라우드 스토리지 제공업체와의 통합을 지원하며, 원격 스프레드시트 감사 및 자동 품질 검사에 활용할 수 있습니다. RESTful API를 사용하여 엔터프라이즈 수준의 워크플로우를 자동화할 수 있습니다.

### **웹 API**

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/search/broken-links
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 우수하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

```bash
-H "Authorization: Bearer {access_token}"
```

### **요청 매개변수:**

| 매개변수 이름 | 유형   | 경로/쿼리 문자열/HTTP 본문 | 설명                                                                                                                                               |
| :------------- | :----- | :------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name           | String | Path                       | **필수.** 끊긴 링크를 검사할 Excel 워크북 파일의 이름(예: `Quarterly_Report.xlsx`).                                         |
| worksheet      | String | Query                      | **필수.** 검색 작업을 수행할 워크시트의 이름입니다. 워크북에 표시되는 정확한 시트 이름을 지정합니다.         |
| cellArea       | String | Query                      | **필수.** 끊긴 링크를 분석할 셀 범위이며, A1 표기법으로 표현됩니다(예: `C5:J50`). API는 이 영역 내에서만 검색합니다.          |
| folder         | String | Query                      | **선택 사항.** 클라우드 저장소에 있는 워크북이 포함된 디렉터리 경로입니다. 생략 시 루트 디렉터리가 기본값으로 사용됩니다.                         |
| storageName    | String | Query                      | **선택 사항.** 사용자 정의 클라우드 저장소 구성의 이름입니다. 생략 시 시스템의 기본 저장소가 사용됩니다.                                      |
| region         | String | Query                      | **선택 사항.** 처리 중 적용되는 로케일 설정(예: `en-US`)입니다. 지역별 수식 구문 또는 참조 해석에 영향을 줄 수 있습니다. |
| password       | String | Query                      | **선택 사항.** 암호화된 스프레드시트를 열기 위한 비밀번호입니다. 파일이 비밀번호 보호되지 않은 경우 생략합니다.                                             |

**샘플 cURL 요청**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/Quarterly_Report.xlsx/search/broken-links?worksheet=Sheet1&cellArea=C5:J50" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

### **응답**

```json
{
  "Name": "BrokenLinksResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "Properties": [
    {
      "Name": "BrokenLinks",
      "DataType": {
        "Identifier": "Container",
        "Reference": "BrokenLink",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "BrokenLink"
        }
      }
    },
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer"
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String"
      }
    }
  ]
}
```

**샘플 JSON 응답**

```json
{
  "BrokenLinks": [
    {
      "Worksheet": "Sheet1",
      "CellName": "D12",
      "Link": "https://example.com/data/source.xlsx",
      "IsValid": false,
      "ErrorMessage": "파일을 찾을 수 없음"
    },
    {
      "Worksheet": "Sheet1",
      "CellName": "F30",
      "Link": "C:\\LocalFolder\\data.xlsx",
      "IsValid": false,
      "ErrorMessage": "클라우드 모드에서는 외부 참조를 지원하지 않음"
    }
  ],
  "Code": 200,
  "Status": "OK"
}
```

### 오류 코드

- **400 Bad Request** – 잘못된 Aspose.Cells Cloud API URI입니다.  
- **401 Unauthorized** – 잘못된 액세스 토큰, 클라이언트 ID 또는 클라이언트 비밀번호입니다.  
- **404 Not Found** – 스프레드시트 파일에 접근할 수 없습니다.  
- **500 Server Error** – 계산 데이터를 가져오는 중 예외가 발생했습니다.

## 스프레드시트 끊긴 링크 검색 API는 어디에 사용해야 하나요?

- **대규모 재무 모델의 정기 감사** – 월간 또는 분기 보고서를 배포하기 전에, 많은 외부 데이터 참조를 포함하는 주요 계산 영역(예: `Dashboard!B5:K50`)을 자동으로 검사하여 모든 링크가 유효한 소스 파일을 가리키는지 확인합니다.  
- **인수·합병(M&A) 시 데이터 통합** – 사업부를 나타내는 여러 스프레드시트를 병합한 후, 병합된 파일의 “개요” 워크시트를 검사하여 파일 경로 변경 또는 권한 문제로 인해 끊긴 링크가 있는지 확인합니다.  
- **투자자 데이터 패키지 준비** – 외부 데이터베이스 또는 시장 데이터 소스에 연결된 차트와 표를 포함한 최종 발표 자료를 준비하기 전에 모든 링크의 유효성을 검증합니다.

## 왜 스프레드시트 끊긴 링크 검색 API를 사용해야 하나요?

- **개발자 친화적** – Aspose.Cells Cloud는 여러 언어로 SDK 라이브러리를 제공하며, 체계적인 문서를 통해 빠른 개발을 지원합니다. 사용자 정의 솔루션 구축에 비해 개발 노력이 크게 줄어듭니다.  
- **인件비 절감** – 링크 유효성 검사를 자동화하여, 별도 인원을 투입해 문서를 수동으로 통합할 필요가 없습니다.  
- **사용량 과금** – 사전 투자가 필요 없으며, 실제로 사용한 API 호출에만 비용이 발생합니다.  
- **유지보수 비용 없음** – 서버 유지보수, 소프트웨어 업데이트, 호환성 문제 등이 없습니다.

## SDK를 사용하여 스프레드시트 끊긴 링크 검색 API 사용 방법

### OpenAPI 사양

[OpenAPI 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchBrokenLinksInRemoteSpreadsheet)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 요청을 수행할 수 있도록 합니다.

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 최대한 높일 수 있습니다. SDK는 기본 HTTP 세부 사항을 추상화하여, 최소한의 코드로 끊긴 링크 감지를 구현할 수 있습니다. 사용 가능한 Aspose.Cells Cloud SDK 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스와 상호 작용하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteSpreadsheet.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteSpreadsheet.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteSpreadsheet.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteSpreadsheet.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteSpreadsheet.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteSpreadsheet.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteSpreadsheet.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteSpreadsheet.go" >}}  
{{</tab>}}  
{{< /tabs >}}