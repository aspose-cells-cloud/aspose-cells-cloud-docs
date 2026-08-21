---
title: "Aspose.Cells Cloud Web API – 스프레드시트를 JSON으로 변환"
second_title: "문서"
ArticleTitle: "로컬 스프레드시트를 Aspose.Cells Cloud API를 사용하여 JSON으로 변환하는 방법"
linktitle: "스프레드시트를 JSON으로 변환"
type: docs
url: /convert-spreadsheet-to-json/
keywords: "Aspose Cells Cloud, 스프레드시트를 JSON으로 변환, Excel을 JSON API로 변환, Aspose.Cells Cloud API, REST API, 스프레드시트 변환"
description: "Aspose.Cells Cloud API를 사용하여 로컬 Excel 파일을 JSON으로 변환하는 방법을 알아보세요. 엔드포인트, 매개변수, 샘플 코드, 오류 처리를 포함하여 원활한 통합을 지원합니다."
weight: 100
---

**ConvertSpreadsheetToJson** 엔드포인트는 로컬 드라이브에 저장된 스프레드시트를 Aspose.Cells Cloud 서버 내에서 완전히 JSON 파일로 변환합니다. 스프레드시트를 `multipart/form-data` 형태로 전송하면 서비스는 다운로드 또는 후속 처리가 가능한 JSON 스트림을 반환합니다. 이 클라우드 네이티브 변환을 통해 파일을 먼저 스토리지에 업로드할 필요가 없으며, 저장 비용을 줄이고 분석, 보고 또는 데이터 교환을 위해 JSON 형식의 스프레드시트 데이터가 필요한 애플리케이션의 워크플로우를 간소화합니다.

**필수 조건**: Aspose Cloud 계정, 유효한 JWT 액세스 토큰, Aspose.Cells Cloud SDK 또는 API 키가 구성되어 있어야 합니다.

**배경**: 스프레드시트를 JSON으로 변환하는 것은 Excel 데이터를 웹 서비스, NoSQL 데이터베이스 또는 클라이언트 측 JavaScript 애플리케이션과 통합할 때 흔히 수행되는 단계입니다. 스프레드시트를 JSON으로 변환하는 API는 원본 파일을 저장할 필요 없이 빠르고 서버 측에서 변환을 수행합니다.

## 스프레드시트를 JSON으로 변환하는 API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/json
```

### **보안 및 인증**

Aspose.Cells Cloud API는 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>을 요구하는 보안 서비스입니다.

### 요청 매개변수

| 매개변수 이름    | 유형                       | 위치     | 필수/선택 사항 | 설명                                                                                                                                                                     |
| :------------- | :------------------------- | :------- | :---------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Spreadsheet    | File (multipart/form-data) | FormData | 필수              | 소스 스프레드시트 파일(예: .xls, .xlsx, .xlsm). 예: `curl -F "Spreadsheet=@myfile.xlsx"`                                                                           |
| outPath        | String                     | Query    | 선택 사항          | 변환된 JSON 파일이 저장될 클라우드 스토리지의 대상 폴더 경로입니다. 생략 시 JSON 응답은 직접 응답 스트림으로 반환됩니다. 예: `outPath=/output/`. |
| outStorageName | String                     | Query    | 선택 사항          | 출력 파일을 저장할 클라우드 스토리지(예: Amazon S3, Azure Blob)의 이름입니다. `outPath`를 비기본 스토리지와 함께 사용할 경우에만 필요합니다.               |
| fontsLocation  | String                     | Query    | 선택 사항          | 서버 상의 사용자 정의 폰트 폴더 경로입니다. 스프레드시트에서 기본 라이브러리에 없는 폰트를 참조할 때 사용합니다.                                      |
| region         | String                     | Query    | 선택 사항          | 스프레드시트 지역/언어 설정(예: `en-US`, `fr-FR`). 변환 중 숫자, 날짜 및 통화 형식에 영향을 줍니다.                                               |
| password       | String                     | Query    | 선택 사항          | 암호로 보호된 스프레드시트를 열기 위한 암호입니다. 암호가 없는 파일의 경우 생략합니다.                                                                                                  |

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

| 코드 | 의미                 | 설명                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK (성공)             | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함. |
| 400  | Bad Request (잘못된 요청) | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식).      |
| 401  | Unauthorized (인증되지 않음) | 잘못되거나 누락된 JWT 토큰.                                     |
| 413  | Payload Too Large (페이로드가 너무 큼) | 업로드된 파일이 크기 제한을 초과함.                                 |
| 500  | Internal Server Error (내부 서버 오류) | 예기치 않은 서버 오류.                                          |

## Convert Spreadsheet to JSON API는 어디에 사용해야 하나요?

- **데이터 마이그레이션 파이프라인** – 레거시 Excel 보고서를 JSON으로 변환하여 최신 NoSQL 데이터베이스 또는 데이터 레이크로 수집합니다.
- **모바일 또는 웹 애플리케이션** – 사용자가 업로드한 스프레드시트를 클라이언트 측 렌더링을 위해 JSON으로 빠르게 변환하며, 원본 파일을 클라우드에 저장하지 않습니다.
- **자동 보고 생성** – 스프레드시트 입력에서 직접 JSON 페이로드를 생성하여 다운스트림 분석 서비스(예: Power BI, Tableau)에 제공합니다.
- **서버리스 함수** – AWS Lambda 또는 Azure Functions 내에서 API를 사용하여 임시 저장소를 관리하지 않고 실시간 변환을 수행합니다.

## 왜 Convert Spreadsheet to JSON API를 사용해야 하나요?

- 클라우드 네이티브 변환을 통해 처리 전에 큰 파일을 스토리지에 업로드할 필요가 없어 지연 시간과 저장 비용을 줄입니다.
- 단일 요청 워크플로우: 스프레드시트를 업로드하고 동일한 HTTP 호출에서 JSON을 수신하여 통합 로직을 간소화합니다.
- 암호로 보호된 스프레드시트와 지역별 스프레드시트를 지원하여 로케일에 따른 정확한 데이터 표현을 보장합니다.
- Aspose의 인프라에서 확장 가능: 사용자의 서버 리소스에 영향을 주지 않고 대규모 워크북과 복잡한 수식을 처리합니다.

## SDK를 사용하여 Convert Spreadsheet to JSON API 사용하는 방법

### Convert Spreadsheet to JSON API 사양

[Convert Spreadsheet to JSON API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertSpreadsheetToJson)은 웹 브라우저에서 직접 REST 상호 작용을 실행할 수 있는 공개적으로 접근 가능한 프로그래밍 인터페이스를 제공합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예시는 cURL을 사용하여 Cloud API에 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/json?outPath=/output/result.json" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@myWorkbook.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 저수준 세부 사항을 추상화하여 몇 줄의 코드로 스프레드시트를 JSON으로 변환할 수 있으므로 개발 속도가 가장 빠릅니다.  
Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하세요.  
다음 코드 예시는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스와 상호 작용하는 방법을 보여줍니다.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertSpreadsheetToJson.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertSpreadsheetToJson.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertSpreadsheetToJson.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertSpreadsheetToJson.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertSpreadsheetToJson.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertSpreadsheetToJson.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertSpreadsheetToJson.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertSpreadsheetToJson.go" >}}
{{</tab>}}
{{< /tabs >}}