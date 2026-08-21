---
title: "Aspose.Cells Cloud Web API – 스프레드시트를 CSV로 변환"
second_title: "문서"
ArticleTitle: "Aspose.Cells Cloud API를 사용하여 스프레드시트를 CSV로 변환하는 방법"
linktitle: "스프레드시트를 CSV로 변환"
type: docs
url: /ko/convert-spreadsheet-to-csv/
keywords: "Aspose Cells, CSV 변환, Excel API, 클라우드 변환"
description: "Aspose.Cells Cloud API를 사용하여 Excel 파일(XLS, XLSX, XLSM 등)을 CSV로 변환하는 방법을 알아보세요. 인증 단계, cURL 샘플, SDK 코드 스니펫, 오류 처리를 포함합니다."
weight: 100
---

**ConvertSpreadsheetToCsv** 엔드포인트는 로컬 드라이브에서 업로드된 스프레드시트 파일을 읽어 Aspose.Cells Cloud 서버에서 변환을 완료한 후 결과 CSV 파일을 바이너리 스트림 형태로 반환합니다. 이 클라우드 네이티브 작업은 소스 파일을 클라우드 스토리지에 업로드할 필요가 없으며, 저장 비용을 줄이고 빠른 스프레드시트에서 CSV로의 변환이 필요한 개발자의 워크플로우를 간소화합니다. 지원되는 형식은 기본 라이브러리에 따라 달라지며, 소스 파일을 읽기 위한 적절한 권한이 필요합니다. 파일 누락, 요청 오류, 변환 실패와 같은 오류는 표준 HTTP 상태 코드로 반환됩니다.

## **스프레드시트를 CSV로 변환하는 API**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/csv
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 강화되어 있으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **요청 매개변수:**

| 매개변수 이름     | 유형     | 위치       | 필수 여부 | 설명                                                                                                                                                   |
| :---------------- | :------- | :--------- | :-------- | :----------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet       | 파일     | FormData   | 필수      | 변환할 스프레드시트 파일입니다. .xls, .xlsx, .xlsm 등 일반적인 형식을 지원합니다. multipart/form-data 형식으로 제공해야 합니다. 예: `myWorkbook.xlsx`. |
| outPath           | 문자열   | Query      | 선택 사항 | 변환된 CSV를 저장할 대상 폴더 경로입니다. 생략 시 CSV는 응답 본문에 직접 반환됩니다. 예: `/output/reports/`.                                           |
| outStorageName    | 문자열   | Query      | 선택 사항 | 출력 파일을 저장할 클라우드 스토리지 서비스 이름입니다. 지정하지 않으면 Aspose.Cells 계정에 설정된 기본 스토리지가 사용됩니다.                          |
| fontsLocation     | 문자열   | Query      | 선택 사항 | 스프레드시트에서 사용하는 사용자 정의 글꼴이 포함된 폴더 경로입니다. 비표준 글꼴이 포함된 셀을 올바르게 렌더링할 수 있도록 합니다.                     |
| region            | 문자열   | Query      | 선택 사항 | 스프레드시트 지역/언어 설정(예: `en-US`, `fr-FR`)입니다. 숫자 서식, 날짜 파싱, 지역별 동작에 영향을 줍니다.                                             |
| password          | 문자열   | Query      | 선택 사항 | 암호로 보호된 스프레드시트를 열 때 사용하는 암호입니다. 파일이 암호화되었는데 암호가 누락되거나 잘못된 경우 400/401 오류가 반환됩니다.                  |

### **응답**

성공 시 API는 헤더 `Content-Type: application/octet-stream`과 함께 **HTTP 200**(또는 비동기 처리 시 **202**) 상태 코드를 반환합니다. 응답 본문에는 생성된 CSV 파일이 바이너리 스트림 형태로 포함됩니다.

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

| 코드 | 의미                  | 설명                                                      |
| ---- | --------------------- | --------------------------------------------------------- |
| 200  | OK                    | 필터 적용 성공; 응답에 작업 세부 정보가 포함됩니다.       |
| 400  | Bad Request           | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식).  |
| 401  | Unauthorized          | 잘못되거나 누락된 JWT 토큰.                                |
| 413  | Payload Too Large     | 업로드된 파일이 크기 제한을 초과했습니다.                 |
| 500  | Internal Server Error | 예기치 않은 서버 오류.                                     |

## 어디에서 Convert Spreadsheet To CSV API를 사용해야 할까요?

- **보고 시스템을 위한 데이터 내보내기** – 수동 파일 처리 없이 Excel 기반 보고서에서 CSV 추출물을 생성하여 BI 도구나 데이터 웨어하우스에 공급합니다.
- **자동화된 배치 처리** – 로컬에 저장된 대량의 스프레드시트를 서버 측 작업에서 CSV로 변환한 후 결과를 다운스트림 서비스로 직접 스트리밍합니다.
- **파일 업로드 기능이 있는 웹 애플리케이션** – 사용자가 Excel 파일을 업로드하면 즉시 CSV 버전을 받아 추가 분석이나 다른 플랫폼으로의 import에 활용할 수 있도록 합니다.
- **레거시 시스템 통합** – 레거시 스프레드시트 형식을 일반 텍스트 구분 기호 파일만 허용하는 시스템에 사용 가능한 CSV로 변환합니다.

## 왜 Convert Spreadsheet To CSV API를 사용해야 할까요?

- **제로 업로드 아키텍처** – 소스 파일을 클라우드 스토리지에 저장할 필요 없이 업로드된 스트림에서 직접 변환을 수행해 시간과 저장 비용을 절약합니다.
- **고성능 클라우드 처리** – 확장 가능한 클라우드 서버에서 Aspose.Cells의 최적화된 변환 엔진을 활용해 대규모 워크북도 빠르게 CSV로 출력합니다.
- **간편한 통합** – 선택적 쿼리 매개변수와 함께 단일 PUT 요청만으로 CSV를 바로 다운로드 가능한 바이너리 스트림으로 반환해 후속 처리 단계를 생략합니다.
- **전체 기능 지원** – 암호로 보호된 파일, 사용자 정의 글꼴, 지역별 설정을 모두 처리해 복잡한 스프레드시트도 정확하게 변환합니다.

## SDK를 사용하여 Convert Spreadsheet To CSV API 사용하기

### Convert Spreadsheet To CSV API 사양

[Convert Spreadsheet To CSV API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertSpreadsheetToCsv)은 웹 브라우저에서 직접 REST 상호작용을 실행할 수 있도록 공개적으로 접근 가능한 프로그래밍 인터페이스를 제공합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예시는 cURL을 사용하여 Cloud API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

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

### Aspose.Cells Cloud SDK 사용하기

SDK를 사용하면 저수준 세부 사항을 추상화해 간결한 코드로 스프레드시트를 다룰 수 있어 개발 속도가 가장 빠릅니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요. 다음 코드 예시는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스와 상호작용하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertSpreadsheetToCsv.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertSpreadsheetToCsv.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertSpreadsheetToCsv.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertSpreadsheetToCsv.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertSpreadsheetToCsv.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertSpreadsheetToCsv.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertSpreadsheetToCsv.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertSpreadsheetToCsv.go" >}}
{{</tab>}}
{{< /tabs >}}