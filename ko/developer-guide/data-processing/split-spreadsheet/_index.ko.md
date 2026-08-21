---
title: "Aspose.Cells Cloud 분할 엑셀 웹 API – 로컬에서 엑셀을 여러 파일로 분할 및 30개 이상 형식으로 내보내기"
second_title: "문서"
ArticleTitle: "엑셀 분할 도구 – 로컬 스프레드시트를 30개 이상 형식의 파일로 분할"
linktype: "분할 스프레드시트"
type: docs
url: /split-spreadsheet/
keywords: "분할, excel, aspose cells, spreadsheet API, pdf 내보내기, csv, json"
description: "Aspose.Cells Cloud API를 사용하여 로컬 엑셀 워크북을 별도의 파일로 분할합니다. 클라우드에 업로드하지 않고 PDF, CSV, JSON, XLSX, HTML 등 30개 이상의 형식으로 내보낼 수 있습니다."
weight: 100
---

로컬 엑셀 워크북을 별도의 파일로 완전히 분할합니다. 클라우드 저장소가 필요 없습니다. 출력은 PDF, CSV, JSON, ODS, XPS 등 30개 이상의 파일 형식을 지원합니다.

## **스프레드시트 분할 API**

### 웹 API

```http
PUT https://api.aspose.cloud/v4.0/cells/split/spreadsheet
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 확보되었으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

```bash
-H "Authorization: Bearer {access_token}"
```

### **요청 매개변수:**

| 매개변수 이름 | 유형    | 경로/쿼리 문자열/HTTP 본문 | 설명                                                                                                                                                               |
| :------------- | :------ | :------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Spreadsheet    | 파일    | FormData                   | 분할할 로컬 스프레드시트 파일입니다. XLSX, XLS, ODS, CSV 등이 지원됩니다. 파일은 클라우드 저장소 없이 서버에서 전체적으로 처리됩니다. |
| from           | 정수    | 쿼리                       | 분할할 워크시트 범위의 시작 인덱스(0부터 시작)입니다(예: 첫 번째 워크시트는 `0`).                                                                        |
| to             | 정수    | 쿼리                       | 분할할 워크시트 범위의 끝 인덱스(0부터 시작)입니다(예: `2`를 지정하면 워크시트 0, 1, 2를 분할).                                                                |
| outFormat      | 문자열  | 쿼리                       | 분할된 파일의 출력 형식입니다. `PDF`, `CSV`, `JSON`, `XLSX`, `HTML` 등 30개 이상의 형식을 지원합니다.                                                                 |
| outPath        | 문자열  | 쿼리                       | _(선택 사항)_ 분할된 출력 파일을 저장할 로컬 폴더 경로입니다. 생략 시 기본 임시 위치에 파일이 저장됩니다.                               |
| outStorageName | 문자열  | 쿼리                       | 출력 파일을 정리하기 위한 저장소 식별자입니다. 로컬 처리 모드에서는 일반적으로 세션 기반 또는 사용자 정의 저장소 레이블을 의미합니다.                     |
| fontsLocation  | 문자열  | 쿼리                       | _(선택 사항)_ PDF 또는 이미지 형식으로 내보낼 때 텍스트 렌더링 정확도를 보장하기 위한 로컬 또는 사용자 정의 글꼴 디렉토리를 지정합니다.                                         |
| region         | 문자열  | 쿼리                       | _(선택 사항)_ 출력 파일에서 숫자, 날짜, 통화 서식에 사용할 로케일을 설정합니다(예: `"en-US"`, `"de-DE"`).                                                  |
| password       | 문자열  | 쿼리                       | _(선택 사항)_ 업로드한 스프레드시트가 비밀번호로 보호되어 있는 경우, 파일을 열고 처리하기 위해 비밀번호를 입력합니다.                                                        |

## **응답**

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

파일은 `outPath`로 지정된 위치에서 직접 다운로드하거나 저장할 수 있습니다.

**성공 응답 세부 정보**

| 상태 코드 | 콘텐츠 유형               | 설명                                |
| ----------- | -------------------------- | ------------------------------------------ |
| 200 OK      | `application/octet-stream` | 병합된 워크북 파일의 바이너리 스트림입니다. |

**HTTP 상태 코드**

| 코드 | 의미               | 설명                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | 필터가 성공적으로 적용되었으며, 응답에 작업 세부 정보가 포함됩니다. |
| 400  | Bad Request           | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식)입니다.      |
| 401  | Unauthorized          | 잘못되거나 누락된 JWT 토큰입니다.                                     |
| 413  | Payload Too Large     | 업로드한 파일이 크기 제한을 초과합니다.                                 |
| 500  | Internal Server Error | 예기치 않은 서버 오류입니다.                                          |

## 어디서 Split Spreadsheet API를 사용해야 하나요?

- **부서별 데이터 배포**: 여러 부서의 데이터가 포함된 통합 워크북을 부서별 파일로 분할합니다.
- **지역별 보고서 배포**: 전국 매출 보고서를 각 지역별 보고서 파일로 분할합니다.
- **고객 데이터 마스킹 배포**: 민감 정보가 포함된 워크북을 필터링된 고객용 보고서 파일로 분할합니다.
- **주기적 보고서 분할**: 월간 요약 보고서를 주간 또는 일간 보고서로 자동 분할합니다.
- **다중 형식 배포**: 단일 엑셀 파일을 PDF, CSV, JSON 등 여러 형식으로 동시에 분할합니다.
- **템플릿 기반 분할**: 미리 정의된 템플릿에 따라 데이터 파일을 표준화된 출력 파일로 분할합니다.
- **데이터 소스 전처리**: 데이터베이스에 데이터를 로드하기 전, 엑셀 파일을 표준화된 CSV 파일로 분할합니다.
- **API 데이터 준비**: 대규모 데이터셋을 API 전송에 적합한 작은 청크로 분할합니다.

## 왜 Split Spreadsheet API를 사용해야 하나요?

- **개발자 친화적**: Aspose.Cells Cloud는 여러 언어로 SDK 라이브러리를 제공하여 빠른 개발을 가능하게 하며, 포괄적인 문서를 제공합니다. 사용자 정의 차트 렌더링 솔루션을 구축하는 것에 비해 개발 작업량을 크게 줄여줍니다.
- **인력 비용 절감**: 문서 통합 전담 인원의 필요성을 줄입니다.
- **사용량 기반 과금**: 초기 투자 없이 실제 사용한 API 호출만 결제합니다.
- **유지보수 비용 없음**: 서버 유지보수, 소프트웨어 업데이트, 호환성 문제 해결이 필요 없습니다.
- **복잡한 엑셀 서식 보존**: 보편적으로 접근 가능한 PDF 형식으로 복잡한 엑셀 서식을 보존합니다.

## SDK를 사용하여 Split Spreadsheet API 사용하기

### Split Spreadsheet API 사양

[Split Spreadsheet API 사양](https://reference.aspose.cloud/cells/#/DataProcessingController/SplitSpreadsheet)은 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있는 공개적으로 액세스 가능한 프로그래밍 인터페이스를 제공합니다.
cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예시는 cURL을 사용하여 클라우드 API에 호출을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/split/spreadsheet?outFormat=PDF" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o split-spreadsheet.zip
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

SDK를 사용하면 저수준 세부 정보를 추상화하여 짧은 코드로 스프레드시트를 별도의 파일로 분할할 수 있어 개발 속도가 가장 빠릅니다.
Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예시는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitLocalFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitLocalFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitLocalFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitLocalFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitLocalFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitLocalFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitLocalFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitLocalFile.go" >}}
{{</tab>}}
{{< /tabs >}}