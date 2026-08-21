---
title: "Aspose.Cells Cloud 웹 API – 워크시트를 JSON으로 변환"
second_title: "문서"
ArticleTitle: "Aspose.Cells Cloud API를 사용하여 스프레드시트 워크시트를 JSON으로 변환하는 방법"
linktitle: "워크시트를 JSON으로 변환"
type: docs
url: /convert-worksheet-to-json/
keywords: "Aspose.Cells, 워크시트를 JSON으로, 엑셀 변환, 클라우드 API, API v4, 데이터 내보내기"
description: "Aspose.Cells Cloud API를 사용하여 엑셀 워크시트를 JSON으로 변환하는 단계별 가이드, 요청 매개변수, 응답 처리, 오류 코드 및 SDK 예제 포함."
weight: 100
---

**ConvertWorksheetToJson** 엔드포인트는 로컬 파일 시스템에서 스프레드시트 파일을 읽어 지정된 워크시트를 추출한 후, 그 내용을 JSON 파일로 반환합니다. 이 변환은 모두 Aspose.Cells Cloud 서버에서 수행되므로 중간 업로드나 저장이 필요 없습니다. 비밀번호로 보호된 워크북, 사용자 정의 글꼴 위치 및 지역 설정을 지원하여 워크시트 데이터를 JSON 형식으로 내보내 하위 처리에 활용하기 위한 빠르고 클라우드 네이티브한 솔루션을 제공합니다.

## **워크시트를 JSON으로 변환 API**

### 웹 API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/json
```

### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **요청 매개변수:**

| 매개변수 이름     | 유형   | 위치       | 필수/선택 사항 | 설명                                                                                                                                                                                                 |
| :---------------- | :----- | :--------- | :-------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet       | 파일   | FormData   | 필수            | 처리할 엑셀 워크북. 지원되는 형식(xls, xlsx, csv 등)이어야 하며 multipart/form-data로 전송됩니다. 예: `Spreadsheet=@C:\Docs\Sample.xlsx`.                                                              |
| worksheet         | 문자열 | Query      | 필수            | 변환할 워크시트의 정확한 이름(대소문자 구분). 지정하지 않거나 존재하지 않으면 API가 오류를 반환합니다. 예: `worksheet=Sheet1`.                                                                        |
| outPath           | 문자열 | Query      | 선택 사항       | 설정된 클라우드 스토리지 내에서 생성된 JSON 파일을 저장할 대상 폴더. 지정하지 않으면 JSON 응답이 직접 응답 스트림으로 반환됩니다. 예: `outPath=/converted/`.                                          |
| outStorageName    | 문자열 | Query      | 선택 사항       | `outPath`를 포함하는 대상 스토리지의 이름(예: "MyStorage"). 생략 시 기본 스토리지를 사용합니다.                                                                                                        |
| fontsLocation     | 문자열 | Query      | 선택 사항       | 워크시트 텍스트를 정확하게 렌더링하기 위해 필요한 사용자 정의 글꼴을 보유한 서버 측 폴더. 예: `fontsLocation=/fonts/custom/`.                                                                          |
| region            | 문자열 | Query      | 선택 사항       | 생성된 JSON 내 숫자, 날짜, 통화 서식에 영향을 주는 문화/지역 식별자(예: `en-US`, `fr-FR`).                                                                                                           |
| password          | 문자열 | Query      | 선택 사항       | 암호화된 워크북을 열기 위한 비밀번호. 워크북이 비밀번호로 보호되어 있지 않으면 이 매개변수를 생략합니다.                                                                                              |

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

| 코드 | 의미               | 설명                                                       |
| ---- | ------------------ | ---------------------------------------------------------- |
| 200  | OK(성공)           | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함.     |
| 400  | 잘못된 요청        | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식).   |
| 401  | 인증되지 않음      | 잘못되거나 누락된 JWT 토큰.                                 |
| 413  | 페이로드 너무 큼   | 업로드된 파일이 크기 제한을 초과함.                         |
| 500  | 내부 서버 오류     | 예기치 않은 서버 오류.                                      |

## 워크시트를 JSON으로 변환 API는 어디에 사용하면 좋을까요?

- **웹 대시보드** – 차트 라이브러리(예: Chart.js, D3.js)에서 사용할 수 있도록 워크시트 데이터를 JSON으로 내보냅니다.
- **데이터 마이그레이션** – 레거시 엑셀 데이터를 JSON을 소비하는 NoSQL 데이터베이스 또는 REST 서비스로 이전합니다.
- **모바일 또는 오프라인 앱** – 서버에서 워크시트 내용을 JSON으로 변환한 후, 경량 페이로드를 모바일 기기와 동기화합니다.
- **보고 파이프라인** – 중간 CSV 단계 없이 JSON 입력을 받아들이는 분석 엔진에 워크시트 데이터를 직접 제공합니다.

## 왜 워크시트를 JSON으로 변환 API를 사용해야 할까요?

- **업로드 불필요 워크플로우** – 먼저 스토리지에 업로드하지 않고도 클라우드에서 로컬 파일을 처리하여 대역폭 및 스토리지 비용을 절약합니다.
- **완전한 변환 기능** – 비밀번호로 보호된 워크북, 사용자 정의 글꼴, 지역별 서식을 지원하여 정확한 데이터 표현이 가능합니다.
- **빠르고 확장 가능한 실행** – 클라우드 인프라에서 고성능 Aspose.Cells 엔진을 활용해 대규모 워크시트도 효율적으로 처리합니다.
- **간소화된 통합** – 단일 PUT 호출로 즉시 사용 가능한 JSON 파일을 반환하거나 직접 저장하므로 클라이언트 애플리케이션의 코드 복잡성이 줄어듭니다.

## SDK와 함께 워크시트를 JSON으로 변환 API 사용하기

### 워크시트를 JSON으로 변환 API 사양

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToJson" rel="noopener noreferrer">워크시트를 JSON으로 변환 API 사양</a>은 웹 브라우저에서 REST 상호 작용을 직접 실행할 수 있는 공개적으로 접근 가능한 프로그래밍 인터페이스를 제공합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스를 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/json?worksheet=Sheet1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.json
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

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용하기

SDK를 사용하면 저수준 세부 사항을 추상화해 간결한 코드로 스프레드시트를 다룰 수 있어 개발 속도가 가장 빠릅니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.  
다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스와 상호 작용하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertWorksheetToJson.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertWorksheetToJson.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertWorksheetToJson.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertWorksheetToJson.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertWorksheetToJson.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertWorksheetToJson.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertWorksheetToJson.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertWorksheetToJson.go" >}}
{{</tab>}}
{{< /tabs >}}