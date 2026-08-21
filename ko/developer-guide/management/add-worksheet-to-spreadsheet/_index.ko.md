---
title: "Aspose.Cells Cloud Excel 워크시트 추가 웹 API - 유형 및 위치 제어로 새 시트 삽입"
second_title: "문서"
ArticleTitle: "Excel에 워크시트 추가 방법 - 특정 위치에 새 시트 삽입"
linktitle: "스프레드시트에 워크시트 추가"
type: docs
url: /ko/add-worksheet-to-spreadsheet/
keywords: "excel, 워크시트 추가, aspose cells api, 스프레드시트, 클라우드 api, 시트 유형, 시트 위치"
description: "Aspose.Cells Cloud API를 사용하여 Excel 워크북에 새 워크시트, 차트 시트, 매크로 시트를 프로그래밍 방식으로 추가하는 방법을 알아보세요. 단일 REST 호출로 시트 유형, 이름 및 삽입 위치를 제어합니다."
weight: 100
---

Programmatically add worksheets to Excel files with full control over sheet type and location. Insert standard worksheets, chart sheets, or macro sheets at any position in the workbook. This RESTful operation enables automated Excel workbook management and organization.

**사전 요구 사항**

- 유효한 JWT 액세스 토큰이 있는 활성 Aspose.Cells Cloud 계정.
- 워크북이 저장될 클라우드 저장소 이름(예: `CompanyOneDrive`)이 구성되어 있어야 합니다.
- 대상 워크북이 지정된 저장소에서 접근 가능해야 하며, 보호된 경우 올바른 암호를 제공해야 합니다.

| **워크시트 유형**       | 설명                                              |
| :--------------------- | :------------------------------------------------ |
| **VB**                 | 비주얼 베이직 모듈                                |
| **Worksheet**          | 일반 워크시트                                     |
| **Chart**              | 차트 시트                                         |
| **BIFF4Macro**         | BIFF4 매크로 시트                                 |
| **InternationalMacro** | 국제 매크로 시트                                  |
| **Other**              | 위에 나열되지 않은 사용자 정의 또는 드문 시트 유형 |
| **Dialog**             | 대화 상자 워크시트                                |

## **스프레드시트에 워크시트 추가 API**

### 웹 API

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/add/worksheet
```

### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름      | 유형    | 위치     | 설명                                                                                                                                                                                           |
| :---------------- | :------ | :------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Spreadsheet**   | 파일    | FormData | **필수.** 새 워크시트를 추가할 Excel 워크북(.xlsx, .xls 등)입니다.                                                                                                                            |
| **sheetType**     | 문자열  | 쿼리     | **선택 사항.** 생성할 시트 유형입니다. 사용 가능한 값은 `worksheet`(기본값), `chartsheet`, `macrosheet`, `vbmodule`, `dialog`입니다.                                                           |
| **position**      | 정수    | 쿼리     | **선택 사항.** 새 시트를 삽입할 0부터 시작하는 인덱스입니다. `0`은 첫 번째 시트 앞에 삽입하고, `2`는 세 번째 시트로 삽입합니다. 생략하면 시트가 끝에 추가됩니다.                                |
| **sheetName**     | 문자열  | 쿼리     | **선택 사항.** 새 워크시트의 이름입니다. 워크북 내에서 고유해야 합니다. 생략하면 "SheetX"와 같은 기본 이름이 생성됩니다.                                                                       |
| **outPath**       | 문자열  | 쿼리     | **선택 사항.** 수정된 워크북이 저장될 클라우드 저장소의 대상 디렉터리입니다. `null`이거나 생략 시, 원본 파일과 동일한 위치 또는 기본 경로에 저장됩니다.                                          |
| **outStorageName**| 문자열  | 쿼리     | **필수.** 출력 파일을 저장할 구성된 클라우드 저장소의 식별자(예: `CompanyOneDrive`)입니다.                                                                                                     |
| **region**        | 문자열  | 쿼리     | **선택 사항.** 새 워크시트의 서식 및 지역 규칙에 영향을 줄 수 있는 로케일 설정(예: `ko-KR`)입니다.                                                                                               |
| **password**      | 문자열  | 쿼리     | **선택 사항.** 암호로 보호된 워크북을 해독하고 수정하기 위한 암호입니다. 파일이 암호화되지 않았다면 생략하세요.                                                                                  |

### 응답

성공 시 API는 **HTTP 200 OK** 또는(새 파일이 생성된 경우) **201 Created** 상태 코드와 함께 업데이트된 워크북 파일을 반환합니다.

```json
{
  "Name": "ResponseFile",
  "DataType": {
    "Identifier": "File",
    "Reference": "Stream"
  }
}
```

**HTTP 상태 코드**

| 코드 | 의미                  | 설명                                                           |
| ---- | --------------------- | -------------------------------------------------------------- |
| 200  | OK                    | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함.          |
| 400  | Bad Request           | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형).        |
| 401  | Unauthorized          | 잘못되거나 누락된 JWT 토큰.                                      |
| 413  | Payload Too Large     | 업로드된 파일이 크기 제한을 초과함.                             |
| 500  | Internal Server Error | 예기치 않은 서버 오류.                                          |

## 어디에서 스프레드시트에 워크시트 추가 API를 사용해야 하나요?

- **자동 보고서 생성** – 재무 제표 생성 중 월별 워크시트(예: `2024-05`)를 동적으로 생성 및 삽입합니다.
- **대량 템플릿 초기화** – 대량으로 영업 견적서 또는 제안서를 생성할 때, 고객 또는 프로젝트마다 전용 분석 워크시트를 추가합니다.
- **대시보드 동적 확장** – 새로운 데이터 차원이 사용 가능해질 때 실시간으로 새 차트 시트를 삽입합니다.
- **규정 준수 및 감사 아카이브** – 연간 감사 중 증거 수집 시트를 자동으로 추가하여 각 검사 포인트를 분리 유지합니다.
- 시트를 삭제하려면 **[워크시트 삭제](/delete-worksheet/)** 작업을 참조하세요.
- 시트를 이동하려면 **[워크시트 이동](/move-worksheet/)** 작업을 참조하세요.

## 왜 스프레드시트에 워크시트 추가 API를 사용해야 하나요?

- **개발자 친화적** – Aspose.Cells Cloud는 여러 언어의 SDK를 제공하여 개발 작업을 줄이고 방대한 문서를 제공합니다.
- **인건비 절감** – 수동 워크시트 생성 및 반복적인 복사/붙여넣기 작업이 불필요해집니다.
- **사용량 과금** – 실제로 호출한 API 수에 대해서만 비용을 지불합니다.
- **유지보수 없음** – 관리할 서버 없음, 소프트웨어 업데이트 없음, 호환성 문제 없음.

## SDK를 사용하여 스프레드시트에 워크시트 추가 API 사용하기

### 스프레드시트에 워크시트 추가 API 사양

[스프레드시트에 워크시트 추가 API 사양](https://reference.aspose.cloud/cells/#/ManagementController/AddWorksheetToSpreadsheet)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예제는 cURL을 사용하여 클라우드 API에 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/add/worksheet?worksheetName=Sheet1" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json" \
     -F "Spreadsheet=@/path/to/Book1.xlsx"
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

SDK를 사용하면 저수준 세부 사항을 추상화하여 최소한의 코드로 워크시트를 추가할 수 있습니다. SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용하여 서비스를 호출하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AddWorksheet.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AddWorksheet.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AddWorksheet.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AddWorksheet.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AddWorksheet.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AddWorksheet.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AddWorksheet.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AddWorksheet.go" >}}  
{{</tab>}}  
{{< /tabs >}}