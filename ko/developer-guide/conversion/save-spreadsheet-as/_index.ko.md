---
title: "스프레드시트를 다른 형식으로 저장 – Aspose.Cells Cloud API(v4.0)"
second_title: "문서"
ArticleTitle: "원격 스토리지에 있는 스프레드시트를 다른 형식 파일로 저장하는 방법: 단계별 가이드"
linktype: "save-spreadsheet-as"
type: docs
url: /ko/save-spreadsheet-as/
keywords: "Aspose Cells, 스프레드시트 변환, 다른 형식으로 저장, API, XLSX를 PDF로, 클라우드 스토리지, Excel을 PDF로, CSV 내보내기, 클라우드 변환"
description: "Aspose.Cells Cloud의 스프레드시트 저장 API를 사용하여 Aspose Cloud에 저장된 스프레드시트를 다른 형식(XLSX, PDF, CSV 등)으로 저장하는 방법을 알아보세요. 요청 구문, 매개변수, curl 예제, SDK 코드 포함."
weight: 100
---

클라우드 스토리지에 있는 스프레드시트 또는 Excel 파일을 다른 형식으로 저장합니다.

## **스프레드시트 저장 API**

### 웹 API

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/saveas
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 우수하며 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **요청 매개변수**

| 매개변수 이름     | 유형   | 위치   | 설명                                                                                             |
| :---------------- | :----- | :----- | :----------------------------------------------------------------------------------------------- |
| name              | String | Path   | **필수.** 변환할 워크북 파일 이름입니다.                                                        |
| format            | String | Query  | **필수.** 원하는 출력 형식(예: `Xlsx`, `PDF`, `CSV`)입니다.                                    |
| saveOptionsData   | Class  | Body   | 선택적 저장 옵션 데이터입니다. 생략 시 기본값은 `null`입니다.                                   |
| folder            | String | Query  | 선택적. 원본 워크북이 저장된 폴더 경로입니다. 생략 시 기본값은 `null`입니다.                    |
| storageName       | String | Query  | 선택적. 사용자 정의 스토리지 이름입니다. 생략 시 기본 스토리지가 사용됩니다.                     |
| outPath           | String | Query  | 선택적. 변환된 파일의 출력 경로입니다. 생략 시 기본값은 `null`입니다.                           |
| outStorageName    | String | Query  | 선택적. 출력 파일을 저장할 스토리지 이름입니다.                                                 |
| fontsLocation     | String | Query  | 선택적. 사용자 정의 폰트 위치입니다.                                                            |
| region            | String | Query  | 선택적. 스프레드시트 지역 설정입니다.                                                           |
| password          | String | Query  | 선택적. 스프레드시트 파일을 열 때 사용할 비밀번호입니다.                                        |

**지원되는 출력 형식**

| 형식   | 확장자                                           |
| :----- | :----------------------------------------------- |
| Xlsx   | .xlsx                                            |
| Pdf    | .pdf                                             |
| Csv    | .csv                                             |
| Html   | .html                                            |
| Ods    | .ods                                             |
| Xls    | .xls                                             |
| Txt    | .txt                                             |
| Mhtml  | .mhtml                                           |
| Tiff   | .tiff                                            |
| Pptx   | .pptx                                            |
| … (기타) | 전체 목록은 API 사양 참조(20가지 이상의 형식)    |

### **응답**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**오류 응답 예시 (400 Bad Request)**

```json
{
  "Code": 400,
  "Message": "Invalid request parameters."
}
```

**HTTP 상태 코드**

| 코드 | 의미                  | 설명                                                       |
| ---- | --------------------- | ---------------------------------------------------------- |
| 200  | OK                    | 필터 적용 성공; 응답에 작업 세부 정보 포함.               |
| 400  | Bad Request           | 누락되었거나 잘못된 매개변수(예: 지원되지 않는 파일 형식). |
| 401  | Unauthorized          | 잘못되었거나 누락된 JWT 토큰.                               |
| 413  | Payload Too Large     | 업로드된 파일이 크기 제한을 초과했습니다.                  |
| 500  | Internal Server Error | 예기치 않은 서버 오류입니다.                               |

## 어디에서 스프레드시트 저장 API를 사용해야 할까요?

### 기업 문서 관리 시스템

- 재무 보고서를 PDF 아카이브로 자동 저장.
- 영업 데이터를 정기적으로 CSV 형식으로 백업.
- 프로젝트 계획을 읽기 전용 파일로 저장하여 실수 변경 방지.

### 데이터 통합 및 ETL 프로세스

- CRM 시스템 데이터를 내보내 표준 Excel 템플릿으로 저장.
- ERP 데이터를 CSV로 변환하여 다른 시스템에 가져오기.
- 원시 데이터를 JSON으로 저장하여 API 전송에 사용.

### 개발 및 자동화 시나리오

- 웹 애플리케이션의 백엔드 처리.
- 자동 보고서 생성 시스템.
- 클라우드 협업 플랫폼.
- 승인 프로세스 통합.
- 데이터 백업 및 마이그레이션.

## 왜 스프레드시트 저장 API를 사용해야 할까요?

- **개발자 친화적** – 다양한 언어에 대한 SDK와 자세한 문서를 제공하여 통합을 간소화합니다.
- **작업 효율성 향상** – 서버 측에서 변환을 처리하여 사용자 정의 변환 코드 작성 필요를 줄입니다.
- **사용량 기반 요금 체계** – 사전 라이선스 비용 없이 수행된 API 호출에만 요금이 부과됩니다.
- **서버 유지보수 불필요** – 클라우드에서 서비스가 실행되므로 변환 인프라 관리가 필요 없습니다.
- **다양한 형식 지원** – 20가지 이상의 스프레드시트 형식 간 변환을 지원합니다.
- **데이터 정확성 보장** – 변환 시 레이아웃, 수식 및 스타일을 유지합니다.

## SDK를 사용하여 스프레드시트 저장 API를 어떻게 사용하나요?

### 스프레드시트 저장 API 사양

[스프레드시트 저장 API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/SaveSpreadsheetAs)은 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의합니다.

**요청 본문 및 curl을 사용한 예시**

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예시는 cURL을 사용하여 클라우드 API에 요청하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/saveas?format=pdf&outPath=output.pdf" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{"SaveOptions":{"SaveFormat":"pdf"}}'
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

SDK를 사용하면 저수준 세부 사항을 추상화하여 최소한의 코드로 스프레드시트를 다른 형식으로 저장할 수 있어 개발 속도가 가장 빠릅니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하세요.

다음 코드 예시는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_WorkbookSaveAs.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_WorkbookSaveAs.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_WorkbookSaveAs.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_WorkbookSaveAs.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_WorkbookSaveAs.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_WorkbookSaveAs.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_WorkbookSaveAs.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_WorkbookSaveAs.go" >}}
{{</tab>}}
{{< /tabs >}}