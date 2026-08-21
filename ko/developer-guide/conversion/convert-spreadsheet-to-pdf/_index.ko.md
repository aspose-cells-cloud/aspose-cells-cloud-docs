---
title: "Aspose.Cells Cloud 웹 API – 스프레드시트를 PDF로 변환"
second_title: "문서"
ArticleTitle: "Aspose.Cells Cloud API를 사용하여 로컬 스프레드시트를 PDF로 변환하는 방법"
linktitle: "스프레드시트를 PDF로 변환"
type: docs
url: /convert-spreadsheet-to-pdf/
keywords: "Aspose.Cells Cloud, 스프레드시트를 PDF로, Excel 변환, 클라우드 API, PDF 생성, REST API, v4.0"
description: "Aspose.Cells Cloud API를 사용하여 로컬 스프레드시트를 PDF로 변환하는 단계별 가이드입니다. 요청 구문, 매개변수, 응답 세부 정보, 오류 처리 및 실용적인 사용 사례를 포함합니다."
weight: 100
---

**ConvertSpreadsheetToPdf** 엔드포인트는 로컬 드라이브에서 업로드한 스프레드시트 파일을 읽어 Aspose.Cells Cloud 서버에서 처리한 후, 결과 PDF 문서를 바이너리 스트림 형태로 클라이언트에 반환합니다. 이 클라우드 기반 변환 기능은 원본 파일을 스토리지에 업로드할 필요를 없애고, 리소스 소비를 줄이며, PDF를 클라이언트에 직접 전달하여 워크플로우를 간소화합니다. 지원되는 형식은 기본 라이브러리에 따라 달라지며, API는 파일 존재 여부, 권한 및 변환 무결성을 검증하고, 유효하지 않은 입력이나 처리 실패 시 적절한 HTTP 오류를 반환합니다.

## **스프레드시트를 PDF로 변환 API**

### 웹 API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/pdf
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 위해 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **요청 매개변수:**

| 매개변수 이름     | 유형   | 위치     | 필수/선택 | 설명                                                                                                                                                                      |
| :---------------- | :----- | :------- | :---------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet       | 파일   | FormData | 필수        | 변환할 원본 스프레드시트 파일(XLS, XLSX, CSV 등). 유효하고 읽을 수 있는 파일이어야 하며, 최대 크기는 100 MB입니다. 예: `myWorkbook.xlsx`.                                     |
| outPath           | 문자열 | Query    | 선택        | 서버에 변환된 PDF를 저장할 대상 폴더 경로(저장하려는 경우). 생략 시 파일은 응답에 직접 반환됩니다. 예: `/output/reports/`.                                                  |
| outStorageName    | 문자열 | Query    | 선택        | 대상 스토리지 서비스 이름(예: `MyCloudStorage`). `outPath`가 사용되고 기본 스토리지가 아닐 경우에만 필요합니다.                                                             |
| fontsLocation     | 문자열 | Query    | 선택        | PDF에서 텍스트 렌더링을 올바르게 수행하기 위한 서버의 사용자 지정 폰트 폴더 경로. 예: `/fonts/custom/`.                                                                     |
| region            | 문자열 | Query    | 선택        | 스프레드시트 지역/언어 설정(예: `en-US`, `fr-FR`). 숫자 서식, 날짜 파싱 및 로케일 관련 동작에 영향을 미칩니다.                                                             |
| password          | 문자열 | Query    | 선택        | 보호된 스프레드시트를 열기 위해 필요한 암호. 파일이 암호화되어 있지 않으면 생략할 수 있습니다.                                                                           |

### **응답**

성공 응답 (200 OK)  
Content-Type: application/pdf  
Content-Disposition: attachment; filename="converted.pdf"  
Content-Length: `<바이트 단위 크기>`

본문: 생성된 PDF 파일의 바이너리 스트림

**HTTP 상태 코드**

| 코드 | 의미                 | 설명                                                       |
| ---- | -------------------- | ---------------------------------------------------------- |
| 200  | OK (성공)           | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함.     |
| 400  | Bad Request (잘못된 요청) | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식). |
| 401  | Unauthorized (인증되지 않음) | 잘못되거나 누락된 JWT 토큰.                             |
| 413  | Payload Too Large (ペ이로드가 너무 큼) | 업로드한 파일이 크기 제한을 초과함.                  |
| 500  | Internal Server Error (내부 서버 오류) | 예기치 않은 서버 오류.                                 |

## Convert Spreadsheet To Pdf API는 어디에 사용해야 하나요?

- **자동 보고서 파이프라인** – 수동 작업 없이 매일 생성된 Excel 보고서를 PDF로 변환하여 보관 또는 이메일 배포에 활용합니다.
- **문서 관리 시스템(DMS)** – 변환 후 PDF를 직접 DMS에 저장하고, 원본 스프레드시트는 클라이언트 측에만 유지합니다.
- **온더플라이 내보내기 기능이 있는 웹 애플리케이션** – 브라우저에서 편집 중인 스프레드시트의 PDF 버전을 사용자에게 다운로드할 수 있도록 지원하며, 클라우드 변환을 통해 레이아웃을 보존합니다.
- **규정 준수** – 감사 추적을 위해 재무 스프레드시트의 불변 PDF 스냅샷을 생성하고, 원본 파일이 클라이언트 환경 밖으로 나가지 않도록 보장합니다.
- **다중 형식 변환 워크플로우** – [스프레드시트를 CSV로 변환](/convert-spreadsheet-to-csv/) API 등 다른 변환 엔드포인트와 결합하여 다중 형식 아카이브를 생성합니다.

## Convert Spreadsheet To Pdf API를 사용해야 하는 이유는 무엇인가요?

- **업로드 없는 워크플로우** – 원본 파일을 클라우드 스토리지에 업로드할 필요 없이, 업로드된 스트림에서 직접 변환이 이루어져 대역폭 및 스토리지 비용을 절약합니다.
- **고신뢰도 렌더링** – Aspose.Cells는 PDF로 변환 시 복잡한 수식, 차트 및 서식을 보존하여 데스크톱 Excel 출력과 동일한 품질을 제공합니다.
- **확장 가능한 클라우드 실행** – 클라이언트 하드웨어와 무관하게 빠르고 안정적인 변환을 위해 Aspose의 클라우드 인프라를 활용합니다.
- **간단한 REST 인터페이스** – 선택적 쿼리 매개변수와 함께 단일 `PUT` 요청만으로 사용 가능하며, 바로 다운로드 가능한 PDF 스트림을 반환하여 어떤 언어든 통합이 간편합니다.

## SDK를 사용하여 Convert Spreadsheet To Pdf API 사용하기

### Convert Spreadsheet To Pdf API 사양

[Convert Spreadsheet To Pdf API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/ConversionController/ConvertSpreadsheetToPdf)은 웹 브라우저에서 직접 REST 상호작용을 실행할 수 있도록 공개적으로 접근 가능한 프로그래밍 인터페이스를 제공합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API에 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/pdf" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.pdf
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 인코딩됨)",
  "contentType": "MIME 유형",
  "fileDownloadName": "선택적 파일 이름"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용하기

SDK를 사용하면 저수준 세부 정보를 추상화하여 간단한 코드로 스프레드시트를 다른 스프레드시트에 병합하는 등 개발 속도를 높일 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하십시오. 다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스와 상호작용하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertSpreadsheetToPdf.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertSpreadsheetToPdf.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertSpreadsheetToPdf.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertSpreadsheetToPdf.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertSpreadsheetToPdf.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertSpreadsheetToPdf.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertSpreadsheetToPdf.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertSpreadsheetToPdf.go" >}}
{{</tab>}}
{{< /tabs >}}