---
title: "Excel 범위를 CSV로 변환 – Aspose.Cells Cloud API"
second_title: "문서"
ArticleTitle: "로컬 스프레드시트 범위를 CSV 파일로 변환하는 방법: 단계별 가이드"
linktitle: "범위를 CSV로 변환"
type: docs
url: /convert-range-to-csv/
keywords: "Aspose Cells, 범위를 CSV로 변환, Excel을 CSV로, Excel API, 클라우드 스프레드시트, 변환, Excel, CSV, Aspose.Cells, 클라우드 API"
description: "로컬 Excel 워크북(XLSX 또는 XLS)에서 특정 범위를 Aspose.Cells Cloud REST API를 사용해 CSV로 변환하는 방법을 알아보세요. 요청 구문, 매개변수, 오류 처리 및 SDK 예제 포함."
---

Aspose.Cells Cloud API를 사용하여 로컬 Excel 파일에서 특정 범위를 CSV로 내보냅니다.

## **범위를 CSV로 변환 API**

**사전 요구 사항**  
이 엔드포인트를 호출하려면 유효한 Aspose Cloud **클라이언트 ID** 및 **클라이언트 시크릿**이 필요하며, **JWT 액세스 토큰**을 획득하고, 소스 스프레드시트가 **XLSX** 또는 **XLS** 형식인지 확인해야 합니다.

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/csv
```

**cURL 예제**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/csv?worksheet=Sheet1&range=A1:C10" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@sample.xlsx"
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 위해 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>을 요구합니다.

### **요청 매개변수:**

| 매개변수 이름     | 유형   | 경로/쿼리 문자열/HTTP 본문 | 설명                                                                 |
| :---------------- | :----- | :------------------------- | :------------------------------------------------------------------- |
| Spreadsheet       | 파일   | FormData                   | 스프레드시트 파일 업로드.                                            |
| worksheet         | 문자열 | 쿼리                       | 스프레드시트 워크시트 이름.                                          |
| range             | 문자열 | 쿼리                       | 셀 영역 지정(예: A1:C10).                                            |
| outPath           | 문자열 | 쿼리                       | 워크북이 저장될 폴더 경로(선택 사항). 기본값은 null입니다.           |
| outStorageName    | 문자열 | 쿼리                       | 출력 저장소 이름.                                                    |
| fontsLocation     | 문자열 | 쿼리                       | 필요 시 사용자 정의 글꼴 지정.                                       |
| region            | 문자열 | 쿼리                       | 스프레드시트 지역 설정 정의.                                         |
| password          | 문자열 | 쿼리                       | 스프레드시트 파일을 열기 위해 필요한 비밀번호.                       |

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

_반환된 CSV 콘텐츠 예제(처음 몇 행):_

```csv
이름,날짜,금액
홍길동,2023-01-15,1250.00
김철수,2023-01-16,980.50
```

**HTTP 상태 코드**

| 코드 | 의미               | 설명                                                           |
| ---- | ------------------ | -------------------------------------------------------------- |
| 200  | 성공(OK)           | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함.         |
| 400  | 잘못된 요청(Bad Request) | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식).      |
| 401  | 인증되지 않음(Unauthorized) | 잘못되거나 누락된 JWT 토큰.                                   |
| 413  | 페이로드가 너무 큼(Payload Too Large) | 업로드된 파일이 크기 제한을 초과함.                          |
| 500  | 내부 서버 오류(Internal Server Error) | 예기치 않은 서버 오류.                                        |

## 범위를 CSV로 변환 API는 어디에 사용해야 하나요?

### **1. 데이터 내보내기 및 마이그레이션 시나리오**

- **데이터베이스 통합**: 특정 Excel 범위를 데이터베이스 시스템으로 직접 내보내기.
- **애플리케이션 통합**: 선택한 스프레드시트 데이터를 SaaS 애플리케이션에 공급.
- **시스템 마이그레이션**: 레거시 및 최신 시스템 간 특정 데이터 범위 전송.
- **크로스 플랫폼 공유**: 다양한 플랫폼 간 특정 데이터 하위 집합 공유.

### **2. 보고서 및 분석**

- **집중적 보고서 작성**: 특정 보고서 섹션을 CSV로 내보내어 집중 분석.
- **대시보드 데이터 피드**: 특정 데이터 범위를 BI 대시보드 도구에 제공.
- **성과 지표**: KPI 범위를 추출하여 성과 추적 시스템에 제공.
- **재무 보고**: 재무 제표 섹션을 외부 감사용으로 내보내기.

### **3. 개발 및 테스트**

- **테스트 데이터 관리**: 테스트 목적으로 특정 데이터 범위 내보내기.
- **개발 환경**: 샘플 데이터 범위를 개발 팀과 공유.
- **API 테스트**: 특정 스프레드시트 섹션에서 CSV 테스트 데이터 생성.
- **프로토타입 개발**: 애플리케이션 프로토타입을 위한 집중적인 데이터 세트 제공.

### **4. 비즈니스 운영**

- **선택적 데이터 공유**: 특정 데이터 범위를 외부 파트너와 공유.
- **부분 데이터 백업**: 중요한 데이터 범위를 CSV 형식으로 백업.
- **부서 간 데이터 전송**: 특정 데이터를 부서 간에 공유.
- **규정 보고**: 규정 준수 제출을 위해 규제 데이터 범위 내보내기.

### **5. 자동화 워크플로우**

- **예약된 범위 내보내기**: 특정 범위를 정해진 일정에 따라 자동으로 내보내기.
- **트리거 기반 추출**: 비즈니스 이벤트 또는 트리거에 따라 범위 내보내기.
- **워크플로우 통합**: 범위 내보내기를 비즈니스 프로세스 워크플로우에 통합.
- **배치 범위 처리**: 여러 특정 범위를 배치 작업으로 처리.

## 왜 범위를 CSV로 변환 API를 사용해야 하나요?

- 워크북을 먼저 업로드하지 않고도 스프레드시트 범위를 변환할 수 있어 저장 공간 절약 및 비용 절감.
- 기존 Aspose.Cells Cloud SDK를 사용하면 개발을 빠르게 완료할 수 있음.
- **간단한 통합**: 명확한 문서화가 제공된 REST API.
- **확장 가능한 아키텍처**: 소규모에서 엔터프라이즈 규모 작업까지 모두 처리 가능.

## SDK와 함께 범위를 CSV로 변환 API를 사용하는 방법은?

### OpenAPI 사양

[OpenAPI 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToCSV)은 웹 브라우저에서 직접 REST 상호작용을 가능하게 하는 공개 액세스 API를 정의합니다.

## Aspose.Cells Cloud SDK 사용

SDK를 사용하면 저수준 세부 정보를 추상화하여 최소한의 코드로 데이터 범위를 CSV 파일로 변환할 수 있어 개발 속도가 가장 빠릅니다.  
Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)에서 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다. Gist에서 로딩이 차단된 경우 저장소에서 예제를 직접 다운로드할 수 있습니다.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToCSV.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToCSV.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToCSV.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToCSV.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToCSV.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToCSV.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToCSV.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToCSV.go" >}}
{{</tab>}}
{{< /tabs >}}