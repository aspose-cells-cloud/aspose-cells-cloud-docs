---
title: "여러 Excel 파일을 하나의 스프레드시트로 병합 – Aspose.Cells Cloud API"
second_title: "문서"
ArticleTitle: "여러 Excel 파일을 하나로 통합 – 30개 이상의 형식으로 스프레드시트 일괄 병합"
linktype: "스프레드시트 병합"
type: docs
url: /merge-spreadsheets/
keywords: "Aspose.Cells, 스프레드시트 병합, Excel API, 클라우드 스프레드시트, 일괄 병합, PDF 변환, CSV 병합, ODS 병합, API 참조, SDK"
description: "여러 로컬 Excel, CSV 또는 ODS 파일을 하나의 워크북으로 통합한 후, 그 결과를 30개 이상의 형식(PDF, HTML 등)으로 변환합니다. 엔드포인트, 매개변수, 인증 가이드, SDK 예제 포함."
weight: 100
---

Aspose.Cells Cloud API를 사용하여 여러 로컬 Excel, CSV 또는 ODS 파일을 하나의 워크북으로 병합하고, 결과를 30개 이상의 출력 형식으로 변환합니다.

### 웹 API

```http
PUT https://api.aspose.cloud/v4.0/cells/merge/spreadsheet
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 강화되어 있으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **요청 매개변수**

| 매개변수 이름     | 유형     | 위치           | 설명                                                                                      |
| ----------------- | -------- | -------------- | ----------------------------------------------------------------------------------------- |
| Spreadsheet       | 파일     | FormData       | 업로드할 로컬 스프레드시트 파일. XLSX, XLS, CSV, ODS 등 지원.                           |
| outFormat         | 문자열   | Query          | 원하는 출력 형식 (예: `XLSX`, `PDF`, `CSV`, `HTML`). 30개 이상의 형식을 지원.             |
| mergeInOneSheet   | 불리언   | Query          | `true` → 모든 데이터를 하나의 워크시트로 병합; `false` → 기존 시트 각각 보존.             |
| outPath           | 문자열   | Query (선택)   | 병합된 파일을 저장할 클라우드 폴더 경로. 생략 시 기본 위치가 사용됩니다.                  |
| outStorageName    | 문자열   | Query          | 사용할 클라우드 저장소 이름 (기본 또는 사용자 정의).                                     |
| fontsLocation     | 문자열   | Query (선택)   | 올바른 PDF/이미지 렌더링을 위한 사용자 정의 글꼴이 포함된 클라우드 폴더.                  |
| region            | 문자열   | Query (선택)   | 숫자, 날짜 및 통화 서식에 사용할 로케일 (예: `en-US`, `zh-CN`).                          |
| password          | 문자열   | Query (선택)   | 보호된 스프레드시트를 열기 위한 비밀번호.                                                |

### **응답**

```json
{
  "Name": "ResponseFile",
  "DataType": {
    "Identifier": "File",
    "Reference": "Stream"
  }
}
```

파일은 `outPath`로 지정된 위치에서 직접 다운로드하거나 저장할 수 있습니다.

**성공 응답 세부 정보**

| 상태 코드 | 콘텐츠 유형                | 설명                                          |
| --------- | -------------------------- | --------------------------------------------- |
| 200 OK    | `application/octet-stream` | 병합된 워크북 파일의 바이너리 스트림.         |

**HTTP 상태 코드**

| 코드 | 의미                  | 설명                                                            |
| ---- | --------------------- | --------------------------------------------------------------- |
| 200  | OK                    | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함.          |
| 400  | 잘못된 요청           | 누락되거나 잘못된 매개변수 (예: 지원되지 않는 파일 유형).       |
| 401  | 인증되지 않음         | 잘못되거나 누락된 JWT 토큰.                                     |
| 413  | 페이로드가 너무 큼    | 업로드된 파일이 크기 제한을 초과함.                             |
| 500  | 내부 서버 오류        | 예기치 않은 서버 오류.                                          |

## 스프레드시트 병합 API는 어떤 경우에 사용해야 하나요?

### **교육 및 학술 분야**

- **학생 과제 채점** – 여러 학생의 과제 파일을 통합하여 일관된 코멘트 및 채점을 수행합니다.
- **연구 데이터 수집** – 다양한 실험 그룹에서 수집한 데이터 스프레드시트를 통합합니다.
- **강의 자료 제작** – 여러 챕터의 연습 문제를 하나의 문제 은행 워크북으로 병합합니다.

### **데이터 처리 및 분석**

- **작은 데이터 세트 통합** – 서로 다른 출처에서 내보낸 CSV 또는 Excel 파일을 병합합니다.
- **데이터 분석 전처리** – 분석을 수행하기 전에 관련 데이터 파일들을 통합합니다.
- **템플릿 데이터 채우기** – 미리 설정된 보고서 템플릿에 병합된 데이터를 입력합니다.

### **개발 및 기술 지원**

- **테스트 데이터 준비** – 자동화 테스트를 위해 여러 테스트 케이스 파일을 병합합니다.
- **로그 파일 분석** – 다양한 기간의 시스템 로그 Excel 보고서를 통합합니다.
- **설정 관리** – 여러 설정 스프레드시트를 하나의 통합 설정 파일로 병합합니다.

## 왜 스프레드시트 병합 API를 사용해야 하나요?

- **개발자 친화적** – 다양한 언어에서 사용 가능한 SDK 라이브러리를 통해 사용자 정의 솔루션 구축보다 개발 작업을 줄일 수 있습니다.
- **인건비 절감** – 수동 문서 통합을 위한 전담 인력을 배치할 필요가 없습니다.
- **사용량 과금** – 실제로 호출한 API 요청에 대해서만 요금이 부과되며, 초기 투자가 필요 없습니다.
- **유지보수 비용 없음** – 서버 유지보수, 소프트웨어 업데이트, 호환성 문제 등이 없습니다.

## SDK와 함께 스프레드시트 병합 API 사용하기

### OpenAPI 사양

<a href="https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheets" rel="noopener noreferrer">OpenAPI 사양</a>은 기계가 읽을 수 있는 방식으로 API를 설명하여 직접 REST 요청을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/merge/spreadsheet?outFormat=PDF&mergeInOneSheet=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/Book1.xlsx" \
  -F "Spreadsheet=@/path/to/Book2.xlsx"
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

SDK를 사용하면 저수준 세부 사항을 추상화하여 단축된 코드로 스프레드시트 워크시트에 데이터를 가져올 수 있어 가장 빠르게 개발할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeSpreadsheets.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeSpreadsheets.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeSpreadsheets.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeSpreadsheets.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeSpreadsheets.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeSpreadsheets.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeSpreadsheets.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeSpreadsheets.go" >}}
{{</tab>}}
{{< /tabs >}}

---