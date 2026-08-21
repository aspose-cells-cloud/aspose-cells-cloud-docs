---
title: "Aspose.Cells Cloud API – Excel 차트를 PDF로 변환"
second_title: "문서"
ArticleTitle: "로컬 스프레드시트 차트를 PDF 파일로 변환하는 방법: 단계별 가이드"
linktitle: "차트를 PDF로 변환"
type: docs
url: /ko/convert-chart-to-pdf/
keywords: "Aspose Cells, 차트, PDF, Excel, 변환, 클라우드 API"
description: "Aspose.Cells Cloud REST API를 사용하여 로컬 Excel 파일의 차트를 PDF 형식으로 내보냅니다. XLSX 및 XLS 파일을 지원합니다."
weight: 100
---

클라우드 API를 사용하여 로컬 Excel 파일에서 차트를 [PDF](https://docs.fileformat.com/pdf/) 형식으로 변환합니다.

## **차트를 PDF로 변환하는 웹 API**

### 웹 API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/chart/pdf
```

### **보안 및 인증**

Aspose.Cells Cloud API는 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>을 요구하는 안전한 서비스입니다.

### **요청 매개변수:**

| 매개변수 이름 | 유형    | 경로/쿼리 문자열/HTTP 본문 | 설명                                                                         |
| ------------- | ------- | -------------------------- | ---------------------------------------------------------------------------- |
| Spreadsheet   | 파일    | FormData                   | 스프레드시트 파일을 업로드합니다.                                             |
| worksheet     | 문자열  | 쿼리                       | 차트가 포함된 워크시트의 이름입니다.                                         |
| chartIndex    | 정수    | 쿼리                       | 변환할 차트의 인덱스입니다.                                                  |
| outPath       | 문자열  | 쿼리                       | (선택사항) 변환된 파일이 저장될 폴더 경로입니다. 기본값은 null입니다.        |
| outStorageName| 문자열  | 쿼리                       | 출력 파일 저장소 이름입니다.                                                 |
| fontsLocation | 문자열  | 쿼리                       | 필요에 따라 사용자 정의 글꼴을 사용합니다.                                   |
| region        | 문자열  | 쿼리                       | 스프레드시트 지역 설정입니다.                                                 |
| password      | 문자열  | 쿼리                       | 스프레드시트 파일을 열기 위한 비밀번호입니다.                                |

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

**HTTP 상태 코드**

| 코드 | 의미                  | 설명                                                              |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK (성공)             | 필터가 성공적으로 적용되었으며, 응답에 작업 세부정보가 포함되어 있습니다. |
| 400  | Bad Request (잘못된 요청) | 매개변수가 누락되었거나 잘못되었습니다(예: 지원되지 않는 파일 형식).     |
| 401  | Unauthorized (인증되지 않음) | JWT 토큰이 잘못되었거나 누락되었습니다.                             |
| 413  | Payload Too Large (페이로드가 너무 큼) | 업로드한 파일이 크기 제한을 초과했습니다.                           |
| 500  | Internal Server Error (내부 서버 오류) | 예기치 않은 서버 오류가 발생했습니다.                                |

## 차트를 PDF로 변환하는 API는 어디에 사용해야 하나요?

### **1. 비즈니스 리포팅 및 자동화**

- **재무 부서**: 월별 재무 리포트 차트 → PDF 아카이브
- **영업 팀**: 성과 추이 차트 → PDF 고객 보고서
- **마케팅 분석**: 캠페인 성과 차트 → PDF 경영진 브리핑
- **운영 관리**: 생산 모니터링 차트 → PDF 규정 준수 문서

### **2. 소프트웨어 개발 및 통합**

- **SaaS 애플리케이션**: 사용자 생성 차트 데이터 → 다운로드 가능한 PDF 리포트
- **엔터프라이즈 시스템**: ERP/CRM 시스템 차트 → PDF 감사 문서
- **모바일 애플리케이션**: 앱 내 분석 차트 → 공유 가능한 PDF 파일
- **웹 애플리케이션**: 대시보드 차트 → PDF 내보내기 기능

### **3. 문서 처리 워크플로우**

- **배치 처리**: 여러 Excel 파일 차트를 동시에 PDF로 변환
- **예약 작업**: 자동화된 일간/주간 차트 리포트 생성
- **템플릿 기반 출력**: 표준 차트 형식 → PDF 문서
- **문서 조합**: PDF 형식으로 차트를 다른 콘텐츠와 결합

### **4. 산업별 응용**

- **연구 기관**: 실험 데이터 차트 → PDF 논문 그림
- **교육 분야**: 교육 자료 차트 → PDF 강의 자료
- **컨설팅 회사**: 분석 차트 → PDF 고객 제공물
- **제조업**: 품질 관리 차트 → PDF 검사 보고서
- **의료**: 환자 데이터 차트 → PDF 의무기록
- **정부 기관**: 통계 차트 → PDF 공식 출판물

### **5. 콘텐츠 관리 및 배포**

- **디지털 자산 관리**: 표준화된 PDF 형식으로 차트 아카이빙
- **지식 베이스**: 내장된 차트 PDF를 포함한 기술 문서
- **고객 포털**: 이해관계자에게 안전한 PDF 리포트 전달
- **규정 준수**: 감사 준비가 가능한 PDF 문서 생성

## 왜 차트를 PDF로 변환하는 API를 사용해야 하나요?

- 워크북을 먼저 업로드하지 않고도 차트를 변환할 수 있어 저장 공간을 절약하고 비용을 줄일 수 있습니다.
- 기존 Aspose.Cells Cloud SDK를 통해 개발을 빠르게 완료할 수 있습니다.
- **간편한 통합**: 명확한 문서화가 제공된 REST API.
- **확장 가능한 아키텍처**: 소규모에서 엔터프라이즈 규모 작업까지 처리 가능.

## SDK를 사용하여 차트를 PDF로 변환하는 API를 어떻게 사용하나요?

### 차트를 PDF로 변환하는 API 사양

[차트를 PDF로 변환하는 API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertChartToPDF)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

## Aspose.Cells Cloud SDK 사용

SDK를 사용하면 저수준 세부 정보를 추상화하여 최소한의 코드로 차트를 PDF 파일로 변환할 수 있어 개발 속도가 가장 빠릅니다.  
다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertChartToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertChartToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertChartToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertChartToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertChartToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertChartToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertChartToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertChartToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}