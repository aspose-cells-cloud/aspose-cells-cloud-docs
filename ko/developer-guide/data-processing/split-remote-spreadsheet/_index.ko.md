---
title: "Aspose.Cells Cloud 스프레드시트 분할기 웹 API - Excel 워크북을 30개 이상의 형식으로 여러 파일로 분할"
second_title: "문서"
ArticleTitle: "클라우드에서 Excel 파일을 분할하여 별도의 파일로 분리하고 30개 이상의 형식으로 내보내기"
linktitle: "클라우드에서 원격 스프레드시트 분할"
type: docs
url: /split-remote-spreadsheet/
keywords: "Aspose.Cells Cloud, Excel 워크북 분할, 스프레드시트 분할기, 클라우드 API, PDF로 내보내기, CSV로 내보내기, JSON으로 내보내기, 다중 형식 내보내기, 클라우드 스프레드시트 처리"
description: "클라우드 스토리지에 저장된 Excel 워크북을 Aspose.Cells Cloud API를 사용해 워크시트별로 분할하고, 각 파일을 PDF, CSV, JSON, XLSX, HTML, ODS, XPS 등 30개 이상의 형식으로 내보냅니다."
weight: 100
---

클라우드에 저장된 대용량 Excel 워크북을 워크시트별로 분리하여 별도의 파일로 분할하고, 각 파일을 PDF, CSV, JSON, ODS, XPS 등 30개 이상의 출력 형식으로 내보내려면 Aspose.Cells Cloud를 사용하세요.

## **원격 스프레드시트 분할 API**

### 웹 API

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/split/spreadsheet
```

### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **요청 매개변수:**

| 매개변수 이름 | 유형    | 경로/쿼리 문자열/HTTP 본문 | 설명                                                                                                                           |
| :------------- | :------ | :-------------------------- | :------------------------------------------------------------------------------------------------------------------------------------ |
| name           | String  | 경로                        | 분할할 워크북 파일 이름(예: `data.xlsx`)으로, 지정된 클라우드 스토리지 폴더 내에 위치합니다.                         |
| folder         | String  | 쿼리                        | 소스 워크북이 저장된 클라우드 스토리지 폴더 경로입니다.                                                                    |
| from           | Integer | 쿼리                        | 분할 작업을 시작할 워크시트 인덱스(0부터 시작)입니다. 예: `0`은 첫 번째 워크시트를 의미합니다.                       |
| to             | Integer | 쿼리                        | 분할 작업을 종료할 워크시트 인덱스(0부터 시작)입니다. 예: `2`는 워크시트 0, 1, 2를 분할합니다.                         |
| outFormat      | String  | 쿼리                        | 분할된 파일의 출력 파일 형식입니다. 지원되는 형식은 `XLSX`, `PDF`, `CSV`, `JSON`, `HTML` 및 이 외 30개 이상이 포함됩니다.           |
| storageName    | String  | 쿼리                        | _(선택 사항)_ 소스 워크북이 저장된 클라우드 스토리지 이름입니다. 생략 시 기본 클라우드 스토리지가 사용됩니다.          |
| outPath        | String  | 쿼리                        | _(선택 사항)_ 분할된 파일이 저장될 대상 클라우드 폴더 경로입니다. 생략 시 소스 폴더에 파일이 저장됩니다.      |
| outStorageName | String  | 쿼리                        | 분할된 출력 파일이 저장될 클라우드 스토리지 이름입니다.                                                            |
| fontsLocation  | String  | 쿼리                        | _(선택 사항)_ PDF/이미지 출력 시 텍스트가 올바르게 렌더링되도록 하는 글꼴 파일이 포함된 사용자 지정 클라우드 폴더 경로입니다.               |
| region         | String  | 쿼리                        | _(선택 사항)_ 출력 파일에서 숫자, 날짜, 통화 형식에 사용할 로케일을 설정합니다(예: `"en-US"`, `"zh-CN"`, `"de-DE"`). |
| password       | String  | 쿼리                        | _(선택 사항)_ 소스 워크북이 암호로 보호되어 있는 경우, 파일을 열기 위한 암호를 입력합니다.                                     |

## **응답**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

파일은 `outPath`로 지정된 위치에서 직접 다운로드하거나 저장할 수 있습니다.

**성공 응답 세부 정보**

| 상태 코드 | 콘텐츠 유형               | 설명                                |
| ----------- | -------------------------- | ------------------------------------------ |
| 200 OK      | `application/octet-stream` | 병합된 워크북 파일의 이진 스트림입니다. |

**HTTP 상태 코드**

| 코드 | 의미               | 설명                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK (성공)                    | 필터가 성공적으로 적용되었으며, 응답에 작업 세부 정보가 포함되어 있습니다. |
| 400  | Bad Request (잘못된 요청)           | 매개변수 누락 또는 잘못된 값(예: 지원되지 않는 파일 형식)입니다.      |
| 401  | Unauthorized (인증되지 않음)          | 잘못되거나 누락된 JWT 토큰입니다.                                     |
| 413  | Payload Too Large (페이로드 너무 큼)     | 업로드된 파일이 크기 제한을 초과합니다.                                 |
| 500  | Internal Server Error (내부 서버 오류) | 예기치 않은 서버 오류입니다.                                          |

## 분할 원격 스프레드시트 API를 어디에 사용해야 하나요?

- **부서별 데이터 배포**: 여러 부서의 데이터가 포함된 통합 워크북을 부서별 전용 파일로 분할합니다.
- **지역별 보고서 배포**: 국가별 매출 보고서를 지역별로 별도의 보고서 파일로 분할합니다.
- **고객 데이터 마스킹 배포**: 민감 정보가 포함된 워크북을 고객용 전용 뷰 파일로 분할합니다.
- **주기적 보고서 분할**: 월간 요약 보고서를 주간 또는 일간 보고서로 자동 분할합니다.
- **다중 형식 배포**: 단일 Excel 파일을 PDF, CSV, JSON 등 여러 형식 버전으로 동시에 분할합니다.
- **템플릿 기반 분할**: 미리 정의된 템플릿에 따라 데이터 파일을 표준화된 출력 파일로 분할합니다.
- **데이터 소스 전처리**: 데이터베이스에 데이터를 로드하기 전에 Excel 파일을 표준화된 CSV 파일로 분할합니다.
- **API 데이터 준비**: 대용량 데이터 세트를 API 전송에 적합한 소규모 청크로 분할합니다.
- **마이크로서비스 데이터 배포**: 중앙 데이터 파일을 각 마이크로서비스에서 필요로 하는 개별 데이터 파일로 분할합니다.

## 왜 분할 원격 스프레드시트 API를 사용해야 하나요?

- **개발자 친화적**: Aspose.Cells Cloud는 여러 언어의 SDK 라이브러리를 제공하여 빠른 개발이 가능하며, 체계적인 문서도 제공됩니다. 자체 차트 렌더링 솔루션을 구축하는 것에 비해 개발 작업량을 크게 줄입니다.
- **인건비 절감**: 문서 통합 전담 인력을 줄일 수 있습니다.
- **사용량 기반 과금**: 초기 투자가 필요 없으며, 실제로 사용한 API 호출에만 요금이 부과됩니다.
- **유지보수 비용 없음**: 서버 유지보수, 소프트웨어 업데이트, 호환성 문제 해결이 필요 없습니다.
- **복잡한 Excel 서식 보존**: 보편적으로 접근 가능한 PDF 형식으로 복잡한 Excel 서식을 그대로 보존합니다.

## SDK를 사용한 분할 원격 스프레드시트 API 사용 방법

### 분할 원격 스프레드시트 API 사양

[분할 원격 스프레드시트 API 사양](https://reference.aspose.cloud/cells/#/DataProcessingController/SplitRemoteSpreadsheet)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 가능하게 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예시는 cURL을 사용해 클라우드 API에 호출을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/Report.xlsx/split/spreadsheet?folder=Input&outFormat=PDF&from=0&to=2" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
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

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 저수준 세부 사항을 추상화하여 짧은 코드로 클라우드에 저장된 스프레드시트를 별도의 파일로 분할할 수 있어 개발 속도가 가장 빠릅니다.  
Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.  
다음 코드 예시는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스에 호출을 수행하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitFileInRemote.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitFileInRemote.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitFileInRemote.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitFileInRemote.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitFileInRemote.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitFileInRemote.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitFileInRemote.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitFileInRemote.go" >}}
{{</tab>}}
{{< /tabs >}}