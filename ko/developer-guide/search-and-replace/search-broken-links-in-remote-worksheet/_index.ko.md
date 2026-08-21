---
title: "Aspose.Cells Cloud – Excel 링크 끊김 감지 API – 원격 워크시트의 스프레드시트 링크 스캔 및 검증"
second_title: "문서"
ArticleTitle: "원격 Excel 워크시트에서 끊긴 링크 찾기 및 수정 – 클라우드 스프레드시트 링크 검사기"
linktype: "search-broken-links-in-remote-worksheet/"
type: docs
url: /search-broken-links-in-remote-worksheet/
keywords: "Aspose Cells, 끊긴 링크, Excel API, 클라우드 스프레드시트, 링크 검증"
description: "클라우드 스토리지에 저장된 Excel 워크시트 내 외부 링크의 끊김을 감지하고 수정합니다. Aspose.Cells Cloud API를 사용해 특정 범위를 스캔하고 링크 세부 정보를 반환하며 품질 검사 프로세스를 자동화합니다."
weight: 100
---

## **원격 워크시트에서 끊긴 링크 검색 API**

클라우드 스토리지에 저장된 Excel 워크시트에서 끊긴 링크를 자동으로 감지합니다. 이 API는 지정된 범위를 스캔하여 끊긴 외부 참조, 잘못된 수식, 누락된 데이터 소스를 찾아냅니다. 클라우드 스토리지 제공업체와 통합 가능한 원격 스프레드시트 감사, 자동 품질 검사 및 RESTful API 기반의 엔터프라이즈 워크플로 자동화를 지원합니다.

### **Web API**

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/broken-links
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 강화되었으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

```bash
-H "Authorization: Bearer {access_token}"
```

### **요청 매개변수:**

| 매개변수 이름 | 유형   | 경로/쿼리 문자열/HTTP 본문 | 설명                                                                                                                                                                                                 |
| :------------- | :----- | :-------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name           | String | Path                        | **필수.** 끊긴 링크를 검색할 Excel 워크북의 파일 이름(확장자 포함)입니다(예: `Annual_Report.xlsx`).                                                                                                 |
| worksheet      | String | Path                        | **필수.** 링크 스캔을 수행할 워크시트의 정확한 이름입니다(예: `DataSheet1`).                                                                                                                          |
| folder         | String | Query                       | **선택 사항.** 대상 워크북이 위치한 클라우드 스토리지 내 디렉터리 경로입니다. 생략 시 루트 폴더가 사용됩니다.                                                                                           |
| storageName    | String | Query                       | **선택 사항.** 사용자 정의로 구성된 클라우드 스토리지의 식별자입니다. 제공되지 않을 경우 계정의 기본 스토리지가 사용됩니다.                                                                             |
| region         | String | Query                       | **선택 사항.** 검색 시 적용할 로케일 설정입니다(예: `fr-FR`). 이 설정은 특정 수식이나 지역 데이터 형식 해석에 영향을 미칠 수 있습니다. _지원되는 로케일 코드에는 `en-US`, `fr-FR`, `de-DE`, `es-ES` 등이 포함됩니다._ |
| password       | String | Query                       | **선택 사항.** 암호로 보호된 스프레드시트를 해독하기 위한 비밀번호입니다. 파일이 암호화되지 않았다면 생략합니다.                                                                                       |

**예시 cURL 요청**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/Annual_Report.xlsx/worksheets/DataSheet1/search/broken-links?folder=Reports&storageName=MyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

### **응답**

```json
{
  "Code": 200,
  "Status": "OK",
  "BrokenLinks": [
    {
      "Address": "='C:\\Data\\Source.xlsx'!A1",
      "ErrorCode": "404",
      "ErrorMessage": "소스 파일을 찾을 수 없음"
    }
  ]
}
```

응답 객체는 **BrokenLinksResponse** 유형이며 다음을 포함합니다:

- **BrokenLinks** – `BrokenLink` 항목의 컬렉션으로, 각각 문제 있는 참조(주소, 오류 코드, 메시지)를 설명합니다.
- **Code** – 서비스에서 반환된 숫자 상태 코드입니다.
- **Status** – 결과에 대한 텍스트 설명입니다.

**참고**: API는 결과를 페이징하지 않습니다. 요청당 최대 10,000개의 끊긴 링크를 반환할 수 있습니다. 계정당 분당 100회로 요청 속도 제한이 적용됩니다.

### 오류 코드

- **400 Bad Request** – 잘못된 Aspose.Cells Cloud API URI입니다.
- **401 Unauthorized** – 잘못되었거나 누락된 액세스 토큰입니다.
- **404 Not Found** – 스프레드시트 파일에 접근할 수 없습니다.
- **500 Server Error** – 계산 데이터를 가져오는 도중 오류가 발생했습니다.

## 스프레드시트 워크시트 내 끊긴 링크 검색 API를 어디에 사용해야 하나요?

- **대규모 재무 모델의 정기 감사**: 월간 또는 분기 보고서를 배포하기 전에, 많은 외부 데이터 참조가 포함된 주요 계산 영역(예: `Dashboard!B5:K50`)을 자동으로 스캔하여 모든 링크가 유효한 소스 파일을 가리키고 있는지 확인합니다.
- **인수합병(M&A)을 위한 데이터 통합**: 부서별를 나타내는 여러 스프레드시트 파일을 병합한 후, 병합 과정에서 소스 파일 경로 변경 또는 권한 문제로 인해 끊긴 링크가 생겼는지 "개요(Overview)" 워크시트를 검사합니다.
- **투자자 데이터 패키지 작성**: 외부 데이터베이스 또는 시장 데이터 소스와 연결된 차트와 표가 포함된 프레젠테이션 자료를 최종화하기 전에 모든 링크의 유효성을 검증합니다.

## 왜 스프레드시트 워크시트 내 끊긴 링크 검색 API를 사용해야 하나요?

- **개발자 친화적**: Aspose.Cells Cloud는 다양한 언어의 SDK 라이브러리를 제공하여 빠른 개발을 가능하게 하며, 체계적인 문서도 함께 제공됩니다. 맞춤형 차트 렌더링 솔루션 구축에 비해 개발 부하를 크게 줄여줍니다.
- **인력 비용 절감**: 수동 문서 통합 및 링크 검증에 전담 인력을 두는 필요성을 줄입니다.
- **사용량 과금**: 초기 투자 없이 실제로 사용한 API 호출만 비용이 발생합니다.
- **유지보수 비용 제로**: 서버 유지보수, 소프트웨어 업데이트, 호환성 문제 관리가 필요 없습니다.
- **복잡한 Excel 서식 보존**: 범용적으로 접근 가능한 PDF 형식으로 보존합니다.

## SDK를 사용하여 스프레드시트 워크시트 내 끊긴 링크 검색 API를 사용하는 방법

### OpenAPI 사양

[OpenAPI 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceContentInRemoteWorksheet)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

### Aspose.Cells Cloud SDK 사용

SDK 사용은 개발 가속화를 위한 최선의 방법입니다. SDK는 내부 세부 사항을 처리하므로 스프레드시트 워크시트 내 끊긴 링크 검색을 최소한의 코드로 간단히 구현할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하십시오.

다음 코드 예시는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}