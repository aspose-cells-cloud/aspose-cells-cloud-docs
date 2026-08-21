---
title: "Aspose.Cells Cloud 웹 API - Excel에서 텍스트를 숫자로 변환 및 특수 문자 정리"
secondtitle: "문서"
articletitle: "Excel 데이터 클리너 - 텍스트를 숫자로 변환 및 불필요한 문자 제거"
linktitle: "텍스트 변환"
type: docs
url: /convert-text/
keywords: "Aspose.Cells 텍스트 변환, Excel 텍스트를 숫자로, Excel 특수 문자 제거, Excel 줄 바꿈 바꾸기, 악센트 문자 정규화, Excel 데이터 정리 API"
description: "Aspose.Cells Cloud API를 사용하여 Excel 파일의 텍스트 형식 숫자를 숫자 값으로 변환하고, 불필요한 문자 및 줄 바꿈을 교체하며, 악센트 문자를 표준 문자로 정규화합니다."
weight: 100
---

Aspose.Cells API를 사용하여 Excel 데이터를 정리합니다. 텍스트 형식 숫자를 숫자 값으로 변환하고, 불필요한 문자 및 줄 바꿈을 제거하며, 악센트 문자를 일반 알파벳으로 정규화합니다.

## 개요

**텍스트로 저장된 숫자를 숫자로 변환, 불필요한 데이터 제거, 악센트 치환—한 번의 호출로 모든 작업 수행, 수식은 전혀 사용하지 않습니다.**

- **텍스트로 저장된 숫자를 숫자로 변환**: 텍스트로 저장된 숫자 데이터를 진정한 숫자로 변환하여 정확한 계산과 적절한 데이터 표현을 보장합니다.
- **특정 문자 치환**: 선택한 셀 범위에서 지정된 문자를 한 번에 모두 치환하여 데이터를 표준화합니다.
- **줄 바꿈을 공백, 쉼표 또는 세미콜론으로 변환**: 줄 바꿈을 공백, 쉼표 또는 세미콜론으로 바꿔 가독성을 높이고, 더 체계적이고 시각적으로 깔끔한 결과를 만듭니다.
- **악센트 문자 치환**: 데이터가 여러 언어로 구성된 경우, “é”, “ü”와 같은 악센트가 붙은 문자를 해당 악센트 없는 문자로 바꿔 일관성과 명확성을 높입니다.

## **ConvertText API**

### 웹 API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/convert/text
```

### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

```bash
-H "Authorization: Bearer {access_token}"
```

### **convertText** API의 요청 매개변수는 다음과 같습니다:

| 매개변수 이름     | 유형   | 경로/쿼리 스트링/HTTP 본문 | 설명                                                                                                                                                 |
| ---------------- | ------ | -------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | 파일   | FormData                   | 처리할 스프레드시트 파일입니다. 지원되는 형식은 XLSX, XLS, ODS, CSV 등입니다.                                                                         |
| convertTextType  | 문자열 | 쿼리                       | 텍스트 변환 유형을 지정합니다(예: 텍스트 형식 숫자를 숫자 값으로 변환하거나, 악센트가 붙은 문자를 일반 문자로 변환).                                   |
| sourceCharacters | 문자열 | 쿼리                       | 텍스트에서 치환하거나 제거할 문자, 문자열 또는 패턴을 지정합니다(예: `"é,è,ê"`, `"#N/A"`, `"\\n"`은 줄 바꿈을 의미).                                 |
| targetCharacters | 문자열 | 쿼리                       | 소스 문자를 치환할 대체 문자 또는 문자열을 지정합니다(예: 악센트 문자는 `"e"`로, 제거는 `""`, 줄 바꿈은 `" "`로).                                     |
| worksheet        | 문자열 | 쿼리                       | _(선택 사항)_ 텍스트 변환이 적용될 워크시트 이름입니다. 생략 시 첫 번째 워크시트에 적용됩니다.                                                        |
| range            | 문자열 | 쿼리                       | _(선택 사항)_ 텍스트 변환이 적용될 셀 범위입니다(예: `"A1:C10"`). 생략 시 지정된 워크시트 내 사용된 모든 셀에 적용됩니다.                              |
| outPath          | 문자열 | 쿼리                       | _(선택 사항)_ 처리된 워크북이 저장될 클라우드 저장소 폴더 경로입니다. 생략 시 원본 폴더에 저장됩니다.                                                  |
| outStorageName   | 문자열 | 쿼리                       | 출력 파일이 저장될 클라우드 저장소 이름입니다.                                                                                                       |
| region           | 문자열 | 쿼리                       | _(선택 사항)_ 텍스트 변환 규칙에 사용할 로케일을 설정합니다. 특히 언어별 문자 처리 시 중요합니다(예: `"en-US"`, `"fr-FR"`).                            |
| password         | 문자열 | 쿼리                       | _(선택 사항)_ 업로드된 스프레드시트가 암호로 보호된 경우, 파일을 열고 처리하기 위해 암호를 입력합니다.                                                |

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

### 오류 코드

- **400 Bad Request**: 잘못된 Aspose.Cells Cloud API URI입니다.
- **401 Unauthorized**: 잘못된 액세스 토큰, 또는 잘못된 클라이언트 ID 및 비밀번호입니다.
- **404 Not Found**: 스프레드시트 파일에 접근할 수 없습니다.
- **500 Server Error**: 스프레드시트가 계산 데이터를 가져오는 동안 예외가 발생했습니다.

## Convert Text API를 어디에 사용해야 하나요?

- **숫자 형식 수정**: 텍스트로 저장된 숫자(예: “123.45”)를 계산에 적합한 숫자 형식으로 변환합니다.
- **특수 문자 정리**: 데이터에서 불필요한 특수 기호, 여분의 공백 또는 보이지 않는 문자를 제거합니다.
- **줄 바꿈 처리**: 셀 내 줄 바꿈을 공백 또는 다른 구분자로 치환합니다.
- **악센트 문자 정규화**: 악센트가 붙은 문자(예: “é”, “ñ”)를 일반 알파벳(“e”, “n”)으로 변환합니다.
- **CSV 파일 전처리**: CSV 파일을 Excel로 가져오기 전에 텍스트 형식을 표준화합니다.

## Convert Text API를 사용해야 하는 이유는 무엇인가요?

- **자동 형식 변환**: 단일 요청으로 텍스트 형식 숫자를 계산 가능한 값으로 대량 변환합니다.
- **문자 표준화**: 특수 문자, 악센트 문자, 인코딩 문제를 일관되게 처리합니다.
- **데이터 일관성**: 전체 데이터 세트에서 텍스트 형식을 완전히 통일합니다.
- **개발자 친화적**: Aspose.Cells Cloud는 다양한 언어 SDK 라이브러리를 제공하여 빠른 개발을 가능하게 하며, 포괄적인 문서를 제공합니다. 사용자 지정 텍스트 처리 솔루션을 구축하는 것에 비해 개발 부담을 크게 줄여줍니다.
- **비용 효율성**: 워크북을 먼저 업로드하지 않고도 텍스트를 변환할 수 있어 저장 공간을 절약하고 비용을 줄입니다.

## OpenAPI 사양

[OpenAPI 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/ConvertText)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

### Aspose.Cells Cloud SDK 사용

SDK를 사용하는 것이 개발 속도를 최대한 높이는 최선의 방법입니다. SDK는 내부 세부 사항을 처리하므로, 최소한의 코드로 셀에 대한 텍스트 변환 기능을 쉽게 구현할 수 있습니다.  
Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)에서 확인하세요.

다음 코드 예제는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertText.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertText.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertText.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertText.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertText.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertText.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertText.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertText.go" >}}
{{</tab>}}
{{< /tabs >}}
---