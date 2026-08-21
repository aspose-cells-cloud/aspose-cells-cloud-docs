---
title: "Aspose.Cells Cloud 중복 하위 문자열 제거 웹 API - Excel에서 반복되는 텍스트 정리"
second_title: "문서"
ArticleTitle: "Excel 중복 하위 문자열 제거기 – 셀 내 중복 텍스트 정리"
linktitle: "중복 하위 문자열 제거"
type: docs
url: /ko/remove-duplicate-substrings/
keywords: "Aspose.Cells, 중복 하위 문자열, Excel API, 텍스트 정리, 클라우드"
description: "Aspose.Cells Cloud API를 사용하여 Excel 셀에서 중복 하위 문자열을 제거하면서 서식과 유효성 검사를 그대로 유지합니다."
weight: 100
---

Excel 셀에서 중복 하위 문자열을 지능형로 감지하여 제거합니다. Aspose.Cells 중복 제거 API를 사용하여 불필요한 텍스트를 제거하면서 원본 셀 서식을 그대로 유지합니다.

## **소개**: 정확하게 불필요한 문자 제거하기

반복 하위 문자열 클리너 API는 Excel 범위 내 개별 셀에서 중복 하위 문자열을 제거하면서 셀 서식, 데이터 유효성 검사 및 기타 워크북 구조를 그대로 유지합니다. 각 셀을 독립적으로 처리하며, 중복 하위 문자열의 첫 번째 occurrences만 유지합니다.

### **데이터 소스 옵션**

| 필드         | 유형   | 필수 여부 | 설명                                                    |
| ------------ | ------ | --------- | ------------------------------------------------------- |
| `workbook`   | 파일   | 예        | Excel 워크북 파일(.xlsx, .xlsm)                        |
| `range`      | 문자열 | 예        | 처리할 대상 범위(예: "A1:D100", "Sheet1!A:D")           |

### **구분자 옵션**

| 필드                                | 유형      | 기본값     | 설명                                                                                                                                                          |
| ----------------------------------- | --------- | ---------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `delimiters`                        | 문자열    | `"preset"` | 옵션: `preset`, `custom`, `comma`, `semicolon`, `space`, `tab`, `line-break` 또는 사용자 지정 구분자 문자열(여러 문자는 복합 구분자로 처리됨)                 |
| `treatConsecutiveDelimitersAsOne`  | 불리언    | `false`    | 인접한 구분자를 하나의 구분자로 합칩니다.                                                                                                                     |
| `caseSensitive`                    | 불리언    | `false`    | 비교 시 대/소문자를 구분할지 결정합니다. `false`인 경우 중복 감지 시 대/소문자를 무시합니다.                                                                   |

## **RemoveDuplicateSubstrings API**

### 웹 API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/duplicate-substrings
```

### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

```bash
-H "Authorization: Bearer {access_token}"
```

### **RemoveDuplicateSubstrings** API의 요청 매개변수는 다음과 같습니다.

| 매개변수 이름                   | 유형     | 경로/쿼리 문자열/HTTP 본문 | 설명                                                                                                                                                                           |
| :----------------------------- | :------- | :------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet                    | 파일     | FormData                   | 처리할 스프레드시트 파일입니다. 지원되는 형식은 XLSX, XLS, ODS, CSV 등이 포함됩니다.                                                                                          |
| delimiters                     | 문자열   | 쿼리                       | 셀 콘텐츠를 하위 문자열로 분할하여 중복 감지 및 제거에 사용할 하나 이상의 구분자 문자를 지정합니다. 여러 구분자를 지정할 수 있습니다(예: `",;"`).                             |
| treatConsecutiveDelimitersAsOne | 불리언   | 쿼리                       | `true`로 설정하면 연속된 구분자 문자가 하나의 구분자로 처리됩니다. `false`이면 각 구분자가 개별적으로 처리됩니다.                                                               |
| caseSensitive                   | 불리언   | 쿼리                       | `true`이면 중복 감지 시 대/소문자가 고려됩니다(예: "Text" ≠ "text"). `false`이면 중복 비교 시 대/소문자가 무시됩니다.                                                           |
| worksheet                       | 문자열   | 쿼리                       | _(옵션)_ 중복 하위 문자열 제거 작업을 적용할 워크시트 이름입니다. 생략하면 첫 번째 워크시트에 작업이 적용됩니다.                                                                |
| range                           | 문자열   | 쿼리                       | _(옵션)_ 중복 하위 문자열 제거 작업을 적용할 셀 범위(예: `"A1:C10"`)입니다. 생략하면 지정된 워크시트 내 사용된 모든 셀에 작업이 적용됩니다.                                      |
| outPath                         | 문자열   | 쿼리                       | _(옵션)_ 처리된 워크북이 저장될 클라우드 스토리지 폴더 경로입니다. 생략하면 원본 폴더에 파일이 저장됩니다.                                                                       |
| outStorageName                  | 문자열   | 쿼리                       | 출력 파일이 저장될 클라우드 스토리지 이름입니다.                                                                                                                               |
| region                          | 문자열   | 쿼리                       | _(옵션)_ 텍스트 처리에 사용할 로케일을 설정합니다. 이는 특정 언어(예: `"en-US"`, `"tr-TR"`)에 대한 구분자 해석 및 대/소문자 구분 규칙에 영향을 줄 수 있습니다.                    |
| password                        | 문자열   | 쿼리                       | _(옵션)_ 업로드된 스프레드시트가 암호로 보호되어 있는 경우, 파일을 열고 처리하기 위해 암호를 입력합니다.                                                                         |

**요청 예시(cURL)**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/content/remove/duplicate-substrings?delimiters=comma&caseSensitive=false" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Sample.xlsx" \
     -F "range=A1:D100"
```

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

### **상태 코드**

| 코드 | 의미            | 설명                                                                                      |
|------|-----------------|-------------------------------------------------------------------------------------------|
| 200  | OK              | 요청이 성공적이며 처리된 워크북이 반환됩니다.                                               |
| 202  | Accepted        | 요청이 비동기 처리를 위해 수락되었습니다.                                                  |
| 400  | Bad Request     | 요청이 잘못되었거나 유효하지 않은 매개변수가 포함되어 있습니다.                             |
| 401  | Unauthorized    | 인증에 실패했거나 토큰이 누락되었거나 유효하지 않습니다.                                     |
| 404  | Not Found       | 지정된 워크북이나 리소스를 찾을 수 없습니다.                                               |
| 500  | Internal Server Error | 서버 측에서 예기치 않은 오류가 발생했습니다.                                              |

## 중복 하위 문자열 제거 API는 어디에 사용해야 하나요?

- **데이터 정제 및 표준화 시나리오**: `"VIP,Premium,VIP,Gold"`와 같은 태그를 `"VIP,Premium,Gold"`로 정리합니다.
- **기술 및 운영 데이터**: 반복된 오류 코드가 포함된 로그 항목 정리, 중복된 바이너리/랙 식별자 제거 등
- **콘텐츠 및 미디어 관리**: 기술 태그 중복 제거, 불필요한 자격증 항목 제거 등

## 왜 중복 하위 문자열 제거 API를 사용해야 하나요?

- **수동 작업 자동화**: 반복적인 편집을 제거하고 사람의 오류를 줄입니다.
- **데이터 무결성 유지**: 셀 색상, 글꼴, 테두리 및 조건부 서식은 변경되지 않으며, 드롭다운 목록 및 유효성 검사 규칙도 유지됩니다.
- **유연한 처리**: 구분자에 독립적이며, 선택적 대/소문자 구분 제어와 헤더 보호 기능을 제공합니다.
- **개발자 친화적**: Aspose.Cells Cloud는 여러 언어로 SDK 라이브러리를 제공하며, 체계적인 문서를 통해 빠른 개발이 가능합니다.
- **비용 효율성**: 클라우드에서 작업이 수행되어 중간 파일을 로컬에 저장할 필요가 없습니다.

## OpenAPI 명세서

[OpenAPI 명세서](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveDuplicateSubstrings)는 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

### Aspose.Cells Cloud SDK 사용하기

SDK를 사용하는 것이 개발 속도를 최대한 높이는 방법입니다. SDK는 내부 세부 사항을 처리하므로, 최소한의 코드로 셀의 중복 하위 문자열 제거 기능을 간단히 구현할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예시는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RemoveCharactersWithFirstNCharacters.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RemoveCharactersWithFirstNCharacters.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RemoveCharactersWithFirstNCharacters.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RemoveCharactersWithFirstNCharacters.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RemoveCharactersWithFirstNCharacters.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RemoveCharactersWithFirstNCharacters.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RemoveCharactersWithFirstNCharacters.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RemoveCharactersWithFirstNCharacters.go" >}}
{{</tab>}}
{{< /tabs >}}