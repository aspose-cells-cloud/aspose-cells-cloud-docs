---
title: "Aspose.Cells Cloud Web API – 스프레드시트를 대상 언어로 번역"
second title: "문서"
ArticleTitle: "Aspose.Cells Cloud AI 번역 API를 사용하여 전체 스프레드시트를 번역하는 방법"
linktitle: "스프레드시트 번역"
type: docs
url: /ko/translate-spreadsheet/
keywords: "Aspose.Cells Cloud, 스프레드시트 번역 API, AI 번역, 스프레드시트 번역, targetLanguage, 다중 시트 번역, 클라우드 스프레드시트 처리, Aspose.Cells Cloud 번역"
description: "Aspose.Cells Cloud AI를 사용하여 전체 Excel 워크북을 번역하세요. 공식, 차트, 서식을 그대로 유지한 채 텍스트를 지원되는 모든 언어로 변환합니다. 엔드포인트, 매개변수, SDK 예제, 제한사항 및 오류 처리 방법을 알아보세요."
weight: 100
---

**TranslateSpreadsheet** 엔드포인트는 **스프레드시트 번역 API**의 일부로, 워크북 내 모든 텍스트 요소를 읽어 AI 기반 번역 서비스로 전송한 후, 지정된 **targetLanguage**(대상 언어)로 텍스트 데이터를 변환한 새로운 스프레드시트 파일을 반환합니다. 이 작업은 원본 레이아웃, 셀 서식, 수식 및 **다중 시트 구조**를 그대로 보존하므로, 전 세계 사용자를 위한 보고서, 대시보드 및 데이터 기반 문서를 현지화하는 데 이상적입니다. 지원되는 파일 형식은 XLS, XLSX, XLSM, CSV, ODS입니다. 유효하지 않은 언어 코드, 인증 실패 또는 번역 서비스 장애 시 오류가 반환됩니다.

## **스프레드시트 번역 API**

### 웹 API

```http
PUT https://api.aspose.cloud/v4.0/cells/ai/translate/spreadsheet
```

### **요청 매개변수:**

| 매개변수 이름 | 타입   | 위치 | 필수/선택 | 설명                                                                                                                                                                                                 |
| :------------ | :----- | :--- | :-------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet   | 파일   | 필수 | FormData  | 번역할 Excel 워크북. 허용되는 확장자: .xls, .xlsx, .xlsm, .csv, .ods. 최대 파일 크기: 50MB. 예: `budget.xlsx`.                                                                                         |
| targetLanguage | 문자열 | 필수 | 쿼리      | 원하는 출력 언어의 ISO 639-1 언어 코드(예: 스페인어는 "es", 프랑스어는 "fr", 독일어는 "de"). 아래 AI 서비스에서 지원하는 언어여야 합니다.                                                           |
| region        | 문자열 | 선택 | 쿼리      | 스프레드시트 지역 식별자로, 날짜, 숫자 및 통화 등 로케일별 서식에 영향을 줍니다. 일반적인 값: "US", "EU", "CN". 생략 시 워크북의 원본 지역 설정이 사용됩니다.                                        |
| password      | 문자열 | 선택 | 쿼리      | 보호된 워크북을 열기 위한 비밀번호. 파일이 비밀번호로 보호되어 있지 않은 경우 비워 둡니다.                                                                                                           |

### **응답**

성공 응답(200 OK)  
헤더:  
Content-Type: application/octet-stream // 또는 CSV 출력 요청 시 text/csv  
Content-Disposition: attachment; filename="translated.xlsx"  
Content-Length: <바이트 단위 크기>

본문:  
<번역된 스프레드시트 파일을 포함한 바이너리 스트림>

오류 응답은 `code`, `message`, 선택적 `details` 필드를 포함하는 표준 Aspose.Cells Cloud 오류 모델(application/json)을 따릅니다.

**HTTP 상태 코드**

| 코드 | 의미                | 설명                                                     |
| ---- | ------------------- | -------------------------------------------------------- |
| 200  | OK(성공)           | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함.   |
| 400  | 잘못된 요청         | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식). |
| 401  | 인증되지 않음       | 잘못되거나 누락된 JWT 토큰.                              |
| 413  | 페이로드가 너무 큼  | 업로드된 파일이 크기 제한을 초과함.                      |
| 500  | 내부 서버 오류      | 예기치 않은 서버 오류.                                   |

## 스트레드시트 번역 API는 어디에 사용해야 하나요?

- **국제 회계 보고** – 지역 사무소를 위해 분기별 Excel 보고서를 여러 언어로 변환하되, 수식 및 차트 레이아웃은 그대로 유지합니다.
- **다국어 마케팅 대시보드** – 전 세계 팀을 위해 판매 성과 대시보드의 현지화 버전을 자동으로 생성합니다.
- **교육 콘텐츠 배포** – 수동 복사·붙여넣기 없이 다른 국가의 학생을 위한 성적부, 과제 시트, 커리큘럼 스프레드시트를 번역합니다.
- **규정 준수** – 유효성 검사 규칙 및 데이터 유효성 검사 목록을 유지한 채 언어별 규정 준수 스프레드시트를 작성합니다.

## 왜 스트레드시트 번역 API를 사용해야 하나요?

- **AI 기반 정확도** – 맥락 인식 고품질 언어 변환을 위해 최신 신경망 번역 모델을 활용합니다.
- **레이아웃 무손실** – 셀 수식, 조건부 서식, 차트 및 워크시트 순서를 원본 파일과 정확히 일치시킵니다.
- **단일 요청 다중 시트 처리** – 시트별 루프 없이 단일 요청으로 모든 워크시트를 번역합니다.
- **클라우드와의 원활한 통합** – Aspose.Cells Cloud 인증과 호환되어 CI/CD, 서버리스 함수, 엔터프라이즈 백엔드에서 자동화 파이프라인 구축이 가능합니다.

## SDK를 사용한 스트레드시트 번역 API 사용 방법

### 스트레드시트 번역 API 사양

[스프레드시트 번역 API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/AI/TranslateSpreadsheet)은 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 공개된 프로그래밍 인터페이스를 제공합니다.

## Excel API SDK

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 저수준 세부 사항을 추상화해 짧은 코드로 스프레드시트를 병합하는 등의 작업을 빠르게 개발할 수 있습니다.  
Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.  
아래 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스와 상호 작용하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v4.0_TranslateSpreadsheet.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v4.0_TranslateSpreadsheet.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v4.0_TranslateSpreadsheet.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v4.0_TranslateSpreadsheet.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v4.0_TranslateSpreadsheet.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v4.0_TranslateSpreadsheet.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v4.0_TranslateSpreadsheet.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v4.0_TranslateSpreadsheet.go" >}}  
{{</tab>}}  
{{< /tabs >}}