---
title: "Excel에서 문자 제거 – Aspose.Cells Cloud API (POST /cells/removecharacters)"
second_title: "문서"
linktitle: "문자 제거"
type: docs
url: /ko/excel-remove-characters/
keywords: "문자 제거, Aspose.Cells, Excel API, 텍스트 처리, 클라우드"
description: "Aspose.Cells Cloud API를 사용하여 Excel 워크시트에서 문자, 문자 집합 또는 하위 문자열을 제거하는 방법을 알아보세요. 요청 스키마, cURL 예제, SDK 코드, 오류 처리가 포함됩니다."
weight: 100
ArticleTitle: "Excel에서 문자 제거 – Aspose.Cells Cloud API (POST /cells/removecharacters)"
---

## Excel 웹 API에서 문자 제거

선택한 셀 내 텍스트 콘텐츠를 정리하기 위한 종합적인 도구 세트입니다. 이 API는 특정 문자, 미리 정의된 문자 집합 또는 하위 문자열을 제거하여 워크시트 텍스트를 표준화하고 원치 않는 기호를 제거합니다.

**사전 요구 사항**

- 활성화된 Aspose Cloud 계정  
- 인증 가이드에 따라 얻은 유효한 JWT 액세스 토큰  
- 이 엔드포인트를 호출하기 전에 Excel 파일을 스토리지에 업로드해야 합니다  
- 지원되는 파일 형식은 `.xlsx`, `.xls`, `.xlsm` 등 일반적인 Excel 형식 포함  

```http
POST https://api.aspose.cloud/v3.0/cells/removecharacters
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 보장되며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/ko/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 기능 설명

- **사용자 정의 문자 제거** – 삭제하려는 특정 문자를 지정합니다. _사용자 정의 문자 제거_ 필드에 각 문자를 입력하면, API는 선택한 셀에서 해당 문자의 모든 발생을 제거합니다.  
- **문자 집합 제거** – 미리 정의된 집합 중 하나를 선택합니다:  
  - **인쇄 불가능한 문자** – 줄 바꿈과 첫 번째 32개의 인쇄 불가능한 ASCII 문자(0~31), 그리고 추가 코드(127, 129, 141, 143, 144, 157)를 제거합니다.  
  - **문자** – 모든 알파벳을 제거합니다.  
  - **숫자** – 모든 숫자를 제거합니다.  
  - **기호** – 수학, 기하학, 기술, 통화 기호와 “?”, “1”, “™” 같은 문자형 기호를 제거합니다.  
  - **구두점** – 모든 구두점을 제거합니다.  
- **하위 문자열 제거** – 선택한 셀에서 지정된 하위 문자열(예: 단어)을 제거합니다.  

### 요청 매개변수

| 매개변수 이름            | 유형  | 위치 | 설명                                                                    |
| ----------------------- | ----- | ---- | ----------------------------------------------------------------------- |
| removeCharactersOptions | 클래스 | 본문 | 제거할 문자, 문자 집합 또는 하위 문자열을 정의하는 옵션입니다.         |

**`removeCharactersOptions` 스키마**

| 속성             | 유형    | 필수 여부 | 설명                                                                                          |
| ---------------- | ------- | --------- | -------------------------------------------------------------------------------------------- |
| Range            | 문자열  | 예        | 처리할 셀을 식별하는 A1 표기법 또는 이름이 지정된 범위(예: `"A1:C10"`)입니다.              |
| CustomCharacters | 문자열  | 아니요    | 삭제할 사용자 정의 문자가 포함된 문자열(예: `"@#$"`)입니다.                                   |
| CharacterSet     | 문자열  | 아니요    | 미리 정의된 집합을 지정하는 열거형 값(`"NonPrinting"`, `"Text"`, `"Numeric"`, `"Symbols"`, `"Punctuation"`) |
| Substring        | 문자열  | 아니요    | 제거할 정확한 하위 문자열(예: `"USD"`)입니다.                                                 |
| IgnoreCase       | 불리언  | 아니요    | `true`인 경우, 문자 제거가 대소문자를 구분하지 않습니다.                                         |

**예제 JSON 요청 본문**

```json
{
  "Range": "A1:B20",
  "CustomCharacters": "@#$",
  "CharacterSet": "NonPrinting",
  "Substring": "USD",
  "IgnoreCase": true
}
```

**샘플 cURL 요청**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/removecharacters" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "Range": "A1:B20",
           "CustomCharacters": "@#$",
           "CharacterSet": "NonPrinting",
           "Substring": "USD",
           "IgnoreCase": true
         }'
```

### **응답**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[병합된 파일 이름]",
    "Filesize" : [파일 크기],
    "FileContent" : "[Base64String]"
}
```

**HTTP 상태 코드**

| 코드 | 의미                     | 설명                                                      |
|------|--------------------------|-----------------------------------------------------------|
| 200  | OK                       | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함       |
| 400  | 잘못된 요청              | 누락되거나 유효하지 않은 매개변수(예: 지원되지 않는 파일 형식) |
| 401  | 인증되지 않음            | 유효하지 않거나 누락된 JWT 토큰                            |
| 413  | 페이로드가 너무 큼       | 업로드된 파일이 크기 제한을 초과함                          |
| 500  | 내부 서버 오류           | 예기치 않은 서버 오류 발생                                 |

## SDK를 사용하여 PostRemoveCharacters API 사용 방법

### PostRemoveCharacters API 사양

<a href="https://reference.aspose.cloud/cells/#/TextProcessingController/PostRemoveCharacters" rel="noopener noreferrer">PostRemoveCharacters 엔드포인트의 전체 OpenAPI 사양</a>은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 개발 속도가 가장 빨라집니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다: