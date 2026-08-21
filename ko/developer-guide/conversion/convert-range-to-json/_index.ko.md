---
title: "Aspose.Cells Cloud 웹 API - 로컬 엑셀 범위 데이터를 JSON 파일로 변환 - 무료 온라인 도구"
secondtitle: "문서"
articletitle: "로컬 스프레드시트 범위 데이터를 JSON 파일로 변환하는 방법: 단계별 가이드"
linktitle: "범위를 JSON으로 변환"
type: docs
url: /ko/convert-range-to-json/
keywords: "범위를 json으로 변환, aspose.cells cloud, 엑셀을 json으로, 스프레드시트 변환, api"
description: "Aspose.Cells Cloud API를 사용하여 로컬 엑셀 스프레드시트의 특정 범위를 JSON으로 변환합니다."
weight: 100
---

Cloud API를 사용하여 로컬 엑셀 파일에서 범위 데이터를 JSON 파일로 내보냅니다.

## **범위를 JSON으로 변환 API**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/json
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 보장되며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **요청 매개변수:**

| 매개변수 이름 | 유형   | 경로/쿼리 문자열/HTTP 본문 | 설명                                                                   |
| ------------- | ------ | -------------------------- | ---------------------------------------------------------------------- |
| Spreadsheet   | 파일   | FormData                   | 스프레드시트 파일을 업로드합니다.                                       |
| worksheet     | 문자열 | 쿼리                       | 스프레드시트 내 워크시트의 이름입니다.                                   |
| range         | 문자열 | 쿼리                       | 변환할 셀 영역입니다. 예: A1:C10                                         |
| outPath       | 문자열 | 쿼리                       | (선택 사항) 워크북이 저장된 폴더 경로입니다. 기본값은 null입니다.         |
| outStorageName| 문자열 | 쿼리                       | 출력 파일 저장소의 이름입니다.                                          |
| fontsLocation | 문자열 | 쿼리                       | 사용자 정의 글꼴을 저장할 위치입니다.                                     |
| region        | 문자열 | 쿼리                       | 스프레드시트 지역 설정입니다.                                            |
| password      | 문자열 | 쿼리                       | 스프레드시트 파일을 열기 위한 비밀번호입니다.                             |

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

| 코드 | 의미                  | 설명                                                               |
| ---- | --------------------- | ------------------------------------------------------------------ |
| 200  | OK (성공)             | 필터가 성공적으로 적용됨; 응답에는 작업 세부정보가 포함됨.         |
| 400  | 잘못된 요청           | 누락되거나 유효하지 않은 매개변수(예: 지원되지 않는 파일 형식).     |
| 401  | 인증되지 않음         | 잘못되거나 누락된 JWT 토큰.                                         |
| 413  | 요청 본문이 너무 큼   | 업로드된 파일이 크기 제한을 초과함.                                  |
| 500  | 내부 서버 오류        | 예기치 않은 서버 오류.                                              |

## **어디에서 범위를 JSON으로 변환 API를 사용해야 하나요?**

- 실시간 대시보드: Chart.js 또는 D3.js와 같은 차트 라이브러리에 사용하기 위해 실시간 엑셀 데이터를 JSON으로 변환합니다.
- 스프레드시트-as-a-Service: 다른 서비스에서 사용할 수 있도록 엑셀 범위를 JSON 엔드포인트로 제공합니다.
- 웹훅 페이로드: 웹훅 알림을 위해 스프레드시트 데이터를 JSON으로 변환합니다.
- 빠른 데이터 프로토타이핑: Python 또는 R 분석을 위해 정제된 엑셀 데이터를 빠르게 JSON으로 변환합니다.
- 머신러닝 파이프라인: 비즈니스에서 유지보수하는 스프레드시트에서 학습 데이터를 사전 처리합니다.
- 전자상거래 운영: 제품 카탈로그 또는 가격표를 웹사이트와 JSON을 통해 동기화합니다.
- 보고 자동화: 자동 보고를 위해 재무 모델에서 JSON 데이터 피드를 생성합니다.
- 애플리케이션 구성: 기능 플래그, 설정 또는 A/B 테스트 매개변수를 엑셀에서 JSON으로 관리합니다.
- 다국어 지원: i18n 라이브러리에서 사용할 수 있도록 현지화 스프레드시트를 JSON으로 변환합니다.
- 동적 메뉴/내비게이션: 웹사이트 내비게이션 구조를 엑셀에 저장하고 JSON으로 배포합니다.

_기타 변환 옵션은 [범위를 CSV로 변환](/ko/convert-range-to-csv/) 가이드를 참조하십시오._

## **왜 범위를 JSON으로 변환 API를 사용해야 하나요?**

- **SDK 지원**: Aspose.Cells Cloud는 여러 언어에 대한 라이브러리를 제공하여 사용자 정의 코드 양을 줄입니다.
- **저장 비용 절감**: 전체 워크북을 먼저 업로드하지 않고도 범위를 변환할 수 있어 저장 공간을 절약할 수 있습니다.
- **웹 및 모바일 앱 호환성**: JSON은 React, Vue, Angular와 같은 최신 JavaScript 프레임워크의 기본 데이터 형식입니다.
- **광범위한 언어 지원**: 거의 모든 프로그래밍 언어와 데이터베이스가 JSON을 처리할 수 있습니다.
- **구조화된 데이터 보존**
  - **지능형 구조 감지**: 테이블 형식 데이터를 적절한 JSON 배열 또는 객체로 자동 변환합니다.
  - **헤더 매핑**: 첫 번째 행을 JSON 키로 사용하여 깔끔한 객체 구조를 만듭니다.
  - **데이터 유형 보존**: 일반 텍스트가 아닌 숫자, 날짜 및 부울 유형을 보존합니다.

## **SDK와 함께 범위를 JSON으로 변환 API를 사용하는 방법은?**

### **범위를 JSON으로 변환 API 사양**

[범위를 JSON으로 변환 API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToJson)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API에 호출을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/json?worksheet=Sheet1&range=A1:C10" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/path/to/your/file.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result.json"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

### **Aspose.Cells Cloud SDK 사용**

SDK를 사용하면 저수준 세부 정보를 추상화하여 범위 데이터를 JSON 파일로 변환하기 위한 간결한 코드로 빠르게 개발할 수 있습니다.  
Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 호출을 수행하는 방법을 보여줍니다:
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToJson.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToJson.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToJson.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToJson.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToJson.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToJson.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToJson.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToJson.go" >}}
{{</tab>}}
{{< /tabs >}}