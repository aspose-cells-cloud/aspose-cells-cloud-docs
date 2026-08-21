---
title: "Aspose.Cells Cloud 웹 API – 로컬 Excel 테이블 데이터를 JSON 파일로 변환"
second_title: "문서"
ArticleTitle: "로컬 스프레드시트 테이블 데이터를 JSON 파일로 변환하는 방법: 단계별 가이드"
linktype: "docs"
url: /convert-table-to-json/
keywords: "Excel, API, JSON, 변환, 클라우드, 파일, 스프레드시트"
description: "Aspose.Cells Cloud API를 사용하여 단일 PUT 요청으로 로컬 Excel 테이블을 JSON 파일로 변환합니다. cURL 예제, 매개변수, C#, Java, Python 등 다양한 SDK 스니펫이 포함되어 있습니다."
weight: 100
---

Aspose.Cells Cloud 웹 API를 사용하여 로컬 스프레드시트/Excel 테이블을 **JSON** 파일로 변환합니다.

## **테이블을 JSON으로 변환 API**

### 웹 API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/json
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 강화되었으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름       | 유형   | 위치     | 설명                                                                                      |
| ------------------ | ------ | -------- | ----------------------------------------------------------------------------------------- |
| **Spreadsheet**    | 파일   | FormData | 업로드할 Excel 파일입니다.                                                                |
| **worksheet**      | 문자열 | 쿼리     | 테이블이 포함된 워크시트 이름입니다.                                                      |
| **tableName**      | 문자열 | 쿼리     | 변환할 테이블 이름입니다.                                                                 |
| **outPath**        | 문자열 | 쿼리     | (선택 사항) 생성된 JSON 파일이 저장될 폴더 경로입니다. 기본값은 **null**입니다.           |
| **outStorageName** | 문자열 | 쿼리     | (선택 사항) 출력 파일이 저장될 저장소 이름입니다.                                         |
| **fontsLocation**  | 문자열 | 쿼리     | (선택 사항) 변환 중 사용할 사용자 정의 글꼴 경로입니다.                                   |
| **region**         | 문자열 | 쿼리     | (선택 사항) 워크북에 대한 지역 설정입니다.                                                |
| **password**       | 문자열 | 쿼리     | (선택 사항) 보호된 워크북을 열기 위한 비밀번호입니다.                                     |

### 응답

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

| 코드 | 의미                  | 설명                                                           |
| ---- | --------------------- | -------------------------------------------------------------- |
| 200  | OK (성공)             | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보가 포함됨.      |
| 400  | 잘못된 요청           | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형).       |
| 401  | 인증되지 않음         | 잘못되거나 누락된 JWT 토큰.                                     |
| 413  | 페이로드가 너무 큼    | 업로드한 파일이 크기 제한을 초과함.                            |
| 500  | 내부 서버 오류        | 예기치 않은 서버 오류.                                          |

## **어디에서 테이블을 JSON으로 변환 API를 사용해야 하나요?**

- **실시간 대시보드** – Chart.js나 D3.js와 같은 차트 라이브러리에 사용하기 위해 실시간 Excel 데이터를 JSON으로 변환합니다.
- **스프레드시트 as a Service** – 다른 마이크로서비스에서 사용할 수 있도록 Excel 테이블을 JSON 엔드포인트로 노출합니다.
- **웹훅 페이로드** – 웹훅 알림을 위해 스프레드시트 데이터를 JSON으로 변환합니다.
- **신속한 데이터 프로토타이핑** – Python 또는 R 분석을 위해 정제된 Excel 데이터를 신속하게 JSON으로 변환합니다.
- **머신러닝 파이프라인** – 비즈니스 스프레드시트에 저장된 학습 데이터를 사전 처리합니다.
- **전자상거래 운영** – 제품 카탈로그 또는 가격표를 JSON을 통해 웹사이트와 동기화합니다.
- **보고 자동화** – 자동 보고를 위해 재무 모델에서 JSON 피드를 생성합니다.
- **앱 설정** – 기능 플래그, 설정 또는 A/B 테스트 매개변수를 Excel에서 JSON으로 관리합니다.
- **다국어 지원** – i18n 라이브러리를 위해 현지화 스프레드시트를 JSON으로 변환합니다.
- **동적 메뉴/내비게이션** – 웹사이트 내비게이션 구조를 Excel에 저장하고 JSON으로 배포합니다.

## 왜 테이블을 JSON으로 변환 API를 사용해야 하나요?

- **개발자 친화적** – Aspose.Cells Cloud는 다양한 언어에 대한 SDK를 제공하여 개발 작업을 줄이고 체계적인 문서를 제공합니다.
- **비용 효율적** – 워크북을 먼저 업로드하지 않고도 테이블 데이터를 변환할 수 있어 저장 공간을 절약하고 비용을 줄입니다.
- **최신 웹 및 모바일 호환성** – JSON은 웹의 기본 데이터 언어입니다. 이 API를 통해 복잡한 파싱 없이 React, Vue, Angular, 모바일 앱 또는 단일 페이지 애플리케이션에 실시간 스프레드시트 데이터를 직접 제공할 수 있습니다.
- **광범위한 언어 지원** – JSON은 거의 모든 프로그래밍 언어, 데이터베이스 및 웹 서비스와 호환됩니다.
- **구조화된 데이터 보존**
  - **지능형 구조 감지** – 테이블 데이터를 적절한 JSON 배열/객체로 자동 변환합니다.
  - **헤더 매핑** – 첫 번째 행을 JSON 키로 사용하여 깔끔한 객체 구조를 만듭니다.
  - **데이터 유형 보존** – 텍스트만이 아니라 숫자, 날짜 및 불리언도 보존합니다.

_버전 히스토리:_ 테이블을 JSON으로 변환 엔드포인트는 API 버전 **v4.0**(2024년)에서 도입되었으며 현재 안정적인 최신 릴리스입니다. 이전 v3.x 엔드포인트는 더 이상 사용되지 않습니다.

## SDK를 사용하여 테이블을 JSON으로 변환 API를 사용하는 방법은?

### 테이블을 JSON으로 변환 API 사양

[테이블을 JSON으로 변환 API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToJson){:target="\_blank" rel="noopener noreferrer"}은 공개적으로 접근 가능한 프로그래밍 인터페이스를 제공하여 웹 브라우저에서 직접 REST 요청을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예제는 cURL을 사용하여 클라우드 API에 호출을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/json?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.json
```

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/json?worksheet=Sheet1&tableName=MyTable" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/path/to/your/file.xlsx" \
     -F "outPath=output/folder" \
     -F "outStorageName=MyStorage"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 인코딩)",
  "contentType": "MIME 유형",
  "fileDownloadName": "선택적 파일 이름"
}
```

```
{
 "Code": 200,
 "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 낮은 수준의 세부 사항을 추상화하여 최소한의 코드로 스프레드시트 테이블을 JSON 파일로 변환할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 공식 GitHub 저장소를 참조하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스와 상호 작용하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToJson.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToJson.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToJson.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToJson.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToJson.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToJson.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToJson.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToJson.go" >}}  
{{</tab>}}  
{{< /tabs >}}