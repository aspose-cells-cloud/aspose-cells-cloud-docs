---
title: "Aspose.Cells Cloud – Excel 범위 내 브레이크드 링크 탐지 (API)"
secondtitle: "문서"
articletitle: "원격 Excel 범위 내 브레이크드 링크 찾기 및 수정 – 클라우드 스프레드시트 링크 체커"
linktitle: "원격 범위 내 브레이크드 링크 검색"
type: docs
url: /ko/search-broken-links-in-remote-range/
keywords: "Aspose, Cells, 브레이크드 링크, API, Excel 범위, 유효성 검사, 클라우드, 스프레드시트, 외부 참조, 체커"
description: "Aspose.Cells Cloud API를 사용해 특정 Excel 범위 내 외부 링크가 끊긴 항목, 잘못된 수식, 누락된 데이터 소스를 스캔하세요. 보안성과 속도를 갖춘 클라우드 기반 솔루션입니다."
weight: 100
---

## **원격 범위 내 브레이크드 링크 검색 API**

클라우드 스토리지에 저장된 Excel 파일의 범위 데이터에서 자동으로 브레이크드 링크를 감지합니다. 지정된 범위 내 외부 참조가 끊긴 링크, 잘못된 수식, 누락된 데이터 소스를 스캔합니다. 클라우드 스토리지 제공업체와 통합 가능하며, 원격 스프레드시트 감사 및 자동 품질 검사에 활용할 수 있습니다. 엔터프라이즈 워크플로 자동화를 위한 RESTful API입니다.

### **웹 API**

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/search/broken-links
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 강화되어 있으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

```bash
-H "Authorization: Bearer {access_token}"
```

### 요청 매개변수

| 매개변수 이름 | 유형   | 위치 | 설명                                                                                                                                                          |
| ------------- | ------ | ---- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name          | String | Path | **필수.** 브레이크드 링크를 스캔할 대상이 되는 클라우드 스토리지에 저장된 Excel 워크북 파일 이름 (예: `financial_report.xlsx`).                                 |
| worksheet     | String | Path | **필수.** 브레이크드 링크를 검색할 워크북 내 특정 워크시트 이름 (예: `Sheet1`, `Q4_Data`).                                                                    |
| cellArea      | String | Path | **필수.** 특정 워크시트 내에서 외부 참조, 수식, 링크가 끊긴 항목을 스캔할 대상 셀 범위 주소 (예: `A1:F100`).                                                    |
| folder        | String | Query | **선택 사항.** 대상 워크북이 위치한 클라우드 스토리지 내 디렉터리 경로. 생략 시 루트 디렉터리가 기본값으로 사용됩니다.                                             |
| storageName   | String | Query | **선택 사항.** 설정된 클라우드 스토리지 서비스 이름 (예: `DropboxBusiness`, `S3Bucket`). 지정하지 않으면 계정의 기본 스토리지가 사용됩니다.                        |
| region        | String | Query | **선택 사항.** 스캔 시 지역별 데이터 해석에 적용할 로케일 설정 (예: `en-GB`, `de-DE`).                                                                          |
| password      | String | Query | **선택 사항.** 암호 보호 워크북에 접근하기 위한 복호화 비밀번호. 파일이 암호화되어 있지 않다면 빈 값으로 둡니다.                                                   |

**요청 본문 예시**

```json
{
  "name": "financial_report.xlsx",
  "worksheet": "Sheet1",
  "cellArea": "A1:F100",
  "folder": "reports/2024",
  "storageName": "MyDropbox",
  "region": "en-US",
  "password": ""
}
```

### 응답

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

`BrokenLinks` 컬렉션은 **BrokenLink** 유형의 객체를 포함합니다. 각 객체는 다음 속성을 제공합니다:

- **CellName** – 브레이크드 참조가 포함된 셀의 주소 (예: `B12`).
- **LinkType** – 브레이크드된 링크의 유형 (예: `ExternalReference`, `Formula`).
- **ErrorMessage** – 링크가 브레이크드된 이유에 대한 설명.

**참고**: API는 요청 속도 제한을 적용합니다. 자세한 내용은 [가격 및 속도 제한](https://www.aspose.cloud/pricing) 페이지를 참조하세요.

### 오류 코드

- **400 Bad Request** – 잘못된 Aspose.Cells Cloud API URI.
- **401 Unauthorized** – 잘못된 액세스 토큰, 클라이언트 ID 또는 클라이언트 시크릿.
- **404 Not Found** – 스프레드시트 파일에 접근할 수 없음.
- **500 Server Error** – 계산 데이터를 가져오는 동안 스프레드시트에 문제가 발생함.

## 스프레드시트 범위 내 브레이크드 링크 검색 API는 어디에 사용해야 하나요?

- **대규모 재무 모델 정기 감사** – 월간 또는 분기 보고서를 발표하기 전, 외부 데이터 참조가 많은 핵심 계산 영역(예: `Dashboard!B5:K50`)을 자동으로 스캔해 모든 링크가 유효한 소스 파일을 가리키는지 확인합니다.
- **인수합병(M&A) 시 데이터 통합** – 부서별로 구성된 여러 스프레드시트 파일을 병합한 후, ‘개요’ 워크시트를 검토해 파일 경로 변경 또는 권한 문제로 인해 브레이크드된 링크를 식별합니다.
- **투자자 자료 패키지 준비** – 외부 데이터베이스 또는 시장 데이터 소스에 연결된 차트와 표가 포함된 발표 자료를 최종화하기 전, 모든 링크의 유효성을 검증합니다.

## 왜 스프레드시트 범위 내 브레이크드 링크 검색 API를 사용해야 하나요?

- **개발자 친화적** – Aspose.Cells Cloud는 여러 언어로 SDK 라이브러리를 제공하며, 체계적인 문서로 빠른 개발을 지원합니다. 맞춤 솔루션 구축에 비해 개발 노력이 크게 줄어듭니다.
- **인건비 절감** – 문서를 수동으로 통합할 전담 인력을 배치할 필요가 없습니다.
- **사용량 기준 과금** – 선불 투자가 필요 없으며, 실제로 호출한 API 요청만 비용이 발생합니다.
- **유지보수 비용 없음** – 서버 관리, 소프트웨어 업데이트, 호환성 문제 등이 없습니다.
- **복잡한 Excel 서식 보존** – 결과를 스타일 손실 없이 누구나 접근 가능한 PDF 형식으로 내보낼 수 있습니다.

## SDK를 사용하여 스프레드시트 범위 내 브레이크드 링크 검색 API 사용 방법

### OpenAPI 명세서

[OpenAPI 명세서](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchBrokenLinksInRemoteRange)는 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 최적화할 수 있습니다. SDK가 내부 세부 사항을 처리하므로, “범위 내 브레이크드 링크 검색” 기능을 최소한의 코드로 구현할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteRange.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteRange.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteRange.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteRange.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteRange.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteRange.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteRange.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteRange.go" >}}
{{</tab>}}
{{< /tabs >}}