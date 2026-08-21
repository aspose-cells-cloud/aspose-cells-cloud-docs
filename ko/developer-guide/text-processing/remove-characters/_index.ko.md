---
title: "Aspose.Cells Cloud Remove Characters Web API – Excel에서 사용자 정의 문자 및 부분 문자열 삭제(온라인 단축 코드)"
second_title: "문서"
ArticleTitle: "Excel 텍스트 클리너 – 선택한 범위에서 문자 및 부분 문자열 삭제"
linktitle: "문자 제거"
type: docs
url: /ko/remove-characters/
keywords: "Aspose.Cells, 문자 제거, Excel API, 텍스트 정리, 스프레드시트"
description: "선택한 범위 내 Excel 셀에서 사용자 정의 문자, 문자 집합 및 부분 문자열을 제거합니다. Aspose.Cells API를 사용해 특정 위치의 텍스트를 정확하게 삭제하여 데이터 정리를 수행합니다."
weight: 100
---

선택한 셀 범위에서 사용자 정의 문자, 문자 집합 또는 부분 문자열을 삭제하여 Excel 데이터를 정리합니다. Aspose.Cells API를 사용해 특정 위치의 텍스트를 정확하게 제거하여 데이터 서식을 최적화하세요.

## 소개

특정하고 불필요한 문자를 제거하여 Excel 데이터를 간편하게 정리하고 표준화하세요. 이 애드인은 셀을 효과적으로 정화할 수 있는 여러 가지 목표 지향적 방법을 제공합니다:

- **사용자 정의 문자 제거**  
  정의한 특정 기호를 모두 삭제합니다. 필드에 각 문자를 입력하기만 하면 애드인이 선택한 셀에서 해당 문자의 모든 인스턴스를 즉시 제거합니다. 고유한 구분자, 오타, 특수 기호 제거에 이상적입니다.

- **문자 집합 제거 (대량 정리)**
  - **인쇄 불가능 문자** – 분석 및 서식 오류를 유발하는 보이지 않는 문자(개행, 캐리지 리턴, 탭, 그리고 ASCII 0-31, 127, 129, 141, 143, 144, 157 등 제어 문자)를 데이터에서 정리합니다.
  - **텍스트 문자 (모든 알파벳)** – 선택한 범위에서 모든字母(A-Z, a-z)를 제거하여 숫자와 기호만 남깁니다.
  - **숫자 문자 (모든 숫자)** – 모든 숫자(0-9)를 삭제하여 순수 텍스트만 추출합니다. 제품 이름이나 텍스트 설명 정리에 적합합니다.
  - **기호** – 수학(예: ±, √), 기하(예: ∆, °), 기술, 통화(예: £, ¢), 그리고 문자 모양 기호(예: ™, ®, ©) 등 다양한 기호를 제거하여 정리합니다.
  - **구두점 기호** – 마침표, 쉼표, 따옴표, 하이픈 등 모든 구두점 기호를 삭제하여 깔끔하고 구두점 없는 텍스트를 만듭니다.

- **특정 부분 문자열 제거**  
  단일 문자를 넘어서 단어 전체 또는 특정 문자 시퀀스를 삭제합니다. 데이터 세트에서 흔히 쓰이는 접두사, 접미사 또는 불필요한 텍스트 문구를 손쉽게 제거하세요.

**버전 4.0 – 업데이트일 2024-11-15**

## RemoveCharacters API

### 웹 API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/characters
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 보장되며 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

```bash
-H "Authorization: Bearer {access_token}"
```

### 요청 매개변수

| 매개변수 이름     | 유형   | 위치               | 설명                                                                                                                                                                                                                      |
| ----------------- | ------ | ------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet       | File   | FormData           | 처리할 스프레드시트 파일입니다. 지원되는 형식은 XLSX, XLS, ODS, CSV 등이 포함됩니다.                                                                                                                                        |
| removeTextMethod  | String | Query              | 텍스트 제거 방법을 지정합니다. 옵션: `None`, `RemoveCustomCharacter`, `RemoveCharacterSets`, `RemoveSubString`. 기본값은 `None`입니다.                                                                                        |
| characterSets     | String | Query              | `RemoveCharacterSets`가 선택되었을 때 제거할 사전 정의된 문자 집합입니다. 옵션: `NonPrintingCharacters`, `TextCharacters`, `NumericCharacters`, `Symbols`, `PunctuationMarks`. 여러 집합은 쉼표로 결합 가능합니다. |
| removeCustomValue | String | Query              | `RemoveCustomCharacter` 또는 `RemoveSubString`를 사용할 때 제거할 사용자 정의 문자 또는 부분 문자열입니다.                                                                                                                           |
| worksheet         | String | Query _(optional)_ | 텍스트 제거를 적용할 워크시트 이름입니다. **생략 시 워크북의 첫 번째 워크시트가 처리됩니다.**                                                                                           |
| range             | String | Query _(optional)_ | 텍스트 제거를 적용할 셀 범위입니다(예: `"A1:C10"`). **생략 시 지정된 워크시트 내 사용된 모든 셀에 작업이 적용됩니다.**                                                                      |
| outPath           | String | Query _(optional)_ | 처리된 워크북이 저장될 클라우드 스토리지 폴더 경로입니다. 생략 시 파일은 원본 폴더에 저장됩니다.                                                                                                        |
| outStorageName    | String | Query _(optional)_ | 출력 파일이 저장될 클라우드 스토리지 이름입니다.                                                                                                                                                              |
| region            | String | Query _(optional)_ | 문자 집합 정의를 위한 로케일을 설정합니다(예: `"en-US"`, `"ja-JP"`).                                                                                                                                                      |
| password          | String | Query _(optional)_ | 필요 시 보호된 워크북의 비밀번호입니다.                                                                                                                                                                                  |

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

### 오류 코드

- **400 Bad Request** – 잘못된 Aspose.Cells Cloud API URI입니다.
- **401 Unauthorized** – 잘못된 액세스 토큰, 또는 잘못된 클라이언트 ID 및 비밀번호입니다.
- **404 Not Found** – 스프레드시트 파일에 접근할 수 없습니다.
- **500 Server Error** – 스프레드시트가 계산 데이터를 가져오는 중 예외가 발생했습니다.

## Remove Characters API를 어디에 사용해야 하나요?

- **데이터 가져오기/내보내기** – 보이지 않는 문자 및 서식 오류를 제거하여 가져온 CSV/데이터를 정리합니다.
- **데이터베이스 관리** – 불필요한 기호나 구두점을 제거하여 제품 코드, ID, 이름을 표준화합니다.
- **재무 분석** – 통화 기호와 텍스트 문자를 제거하여 순수 숫자만 추출합니다.
- **텍스트 처리** – 분석 및 보고를 위해 개행 및 탭을 제거하여 깔끔한 텍스트를 만듭니다.
- **재고 관리** – 불필요한 접두사나 접미사를 제거하여 제품 이름을 정리합니다.

## Remove Characters API를 사용해야 하는 이유

- **시간 절약** – 수동 정리에 비해 여러 유형의 문자를 한 번에 대량 제거하여 시간을 절약하세요.
- **정확성 보장** – 분석 오류 및 서식 문제를 유발하는 숨은 문자를 제거하세요.
- **데이터 표준화** – 데이터 세트와 시스템 전체에서 일관된 서식을 달성합니다.
- **분석 향상** – 숫자 또는 텍스트를 필요에 따라 분리하여 깔끔하고 분석 준비가 완료된 데이터를 확보하세요.
- **가져오기 오류 수정** – 데이터베이스와 수식을 깨트리는 문제 있는 문자를 제거합니다.
- **개발자 친화적** – Aspose.Cells Cloud는 여러 언어의 SDK 라이브러리를 제공하며, 체계적인 문서와 함께 빠른 개발을 가능하게 합니다. 사용자 정의 솔루션 구축에 비해 개발 작업량을 크게 줄입니다.
- **비용 효율적** – 워크북을 먼저 업로드하지 않고도 문자를 제거할 수 있어 저장 공간을 절약하고 비용을 줄입니다.

## OpenAPI 사양

[OpenAPI 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveCharacters)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있게 합니다.

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 가장 효과적으로 높일 수 있습니다. SDK는 기본 세부 사항을 처리하므로 **문자 제거** 기능을 최소한의 코드로 Cells에 구현할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

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