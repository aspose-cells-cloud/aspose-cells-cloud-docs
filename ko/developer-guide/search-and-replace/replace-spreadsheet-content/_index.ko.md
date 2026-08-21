---
title: "Aspose.Cells Cloud – 로컬 엑셀 파일에서 텍스트 바꾸기 (찾기 및 바꾸기 API)"
second_title: "문서"
ArticleTitle: "로컬 엑셀 파일에서 대량 텍스트 바꾸기 – 찾기 및 바꾸기 API"
linktitle: "스프레드시트 콘텐츠 바꾸기"
type: docs
url: /ko/replace-spreadsheet-content/
keywords: "엑셀에서 텍스트 바꾸기, Aspose.Cells 찾기 및 바꾸기, 로컬 스프레드시트 API, 엑셀 파일 바꾸기, API로 콘텐츠 바꾸기"
description: "클라우드에 업로드하지 않고 로컬 엑셀 워크북에서 텍스트를 바꿉니다. Aspose.Cells Cloud 찾기 및 바꾸기 API를 사용하여 특정 범위, 워크시트 또는 전체 파일을 단일 호출로 업데이트합니다."
weight: 100
---

클라우드에 업로드하지 않고 로컬 엑셀 스프레드시트 파일 내에 지정된 텍스트를 바꿉니다. Aspose.Cells Cloud 찾기 및 바꾸기 API를 사용하여 오프라인 편집을 수행하여 워크북 콘텐츠를 효율적으로 업데이트합니다.

## **스프레드시트 콘텐츠 바꾸기 API**

### **웹 API**

```http
PUT https://api.aspose.cloud/v4.0/cells/replace/content
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 강화되었으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

```bash
-H "Authorization: Bearer {access_token}"
```

### **요청 매개변수:**

| 매개변수 이름 | 유형   | 경로/쿼리 문자열/HTTP 본문 | 설명                                                                                                                                                                                                 |
| :------------ | :----- | :------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet   | 파일   | FormData                   | 처리할 로컬 스프레드시트 파일입니다. 지원되는 형식은 XLSX, XLS, ODS, CSV 등이 포함됩니다.                                                                                                          |
| searchText    | 문자열 | 쿼리                       | 지정된 워크시트 및 셀 영역 내에서 검색할 텍스트 문자열입니다.                                                                                                                                      |
| replaceText   | 문자열 | 쿼리                       | 지정된 범위 내에서 `searchText`의 모든 발생 항목을 대체할 텍스트 문자열입니다.                                                                                                                    |
| worksheet     | 문자열 | 쿼리                       | _(선택 사항)_ 찾기 및 바꾸기 작업을 수행할 워크시트 이름입니다. 생략 시 첫 번째 워크시트에 작업이 적용됩니다.                                                                                      |
| cellArea      | 문자열 | 쿼리                       | _(선택 사항)_ 텍스트 검색 및 바꾸기 작업이 수행될 특정 셀 범위(예: `"A1:D20"`, `"B5:F15"`)입니다. 생략 시 지정된 워크시트 내의 모든 사용 중인 셀에 작업이 적용됩니다.                              |
| region        | 문자열 | 쿼리                       | _(선택 사항)_ 텍스트 처리를 위한 로케일을 설정합니다. 이는 검색 작업에서 대소문자 구분 및 문자 인코딩에 영향을 줄 수 있습니다(예: `"en-US"`, `"fr-FR"`).                                            |
| password      | 문자열 | 쿼리                       | _(선택 사항)_ 업로드된 스프레드시트가 비밀번호로 보호되어 있는 경우, 파일을 열고 처리하기 위해 비밀번호를 제공합니다.                                                                              |

### **응답**

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

응답은 업데이트된 워크북을 포함하는 이진 스트림입니다. 적절한 파일 확장자(예: `.xlsx`)로 저장하세요.

### **오류 코드**

- **400 Bad Request** – 잘못된 Aspose.Cells Cloud API URI 또는 잘못된 형식의 매개변수.
- **401 Unauthorized** – 잘못되거나 누락된 액세스 토큰; 새 토큰을 발급받으세요.
- **404 Not Found** – 스프레드시트 파일에 접근할 수 없거나 지정된 워크시트가 존재하지 않습니다.
- **500 Server Error** – 스프레드시트 처리 중 내부 오류가 발생했습니다. 문제가 지속되면 지원팀에 문의하세요.

## 스프레드시트 콘텐츠 바꾸기 API는 어디에 사용해야 하나요?

- **로컬 엑셀 파일의 배치 처리** – 온프레미스에 저장된 여러 워크북에서 찾기 및 바꾸기를 자동화합니다.
- **온프레미스 데이터 파이프라인** – 보고서를 보관하거나 배포하기 전에 수정하는 예약 작업에 API를 통합합니다.
- **로컬 보고서 생성** – 클라우드에 업로드하지 않고 템플릿 워크북에 값을 동적으로 삽입합니다.

## 왜 스프레드시트 콘텐츠 바꾸기 API를 사용해야 하나요?

- **개발자 친화적** – Aspose.Cells Cloud는 다양한 언어로 SDK 라이브러리를 제공하여 빠른 개발과 체계적인 문서화를 가능하게 합니다. 사용자 정의 솔루션 구축에 비해 개발 작업량을 크게 줄여줍니다.
- **인력 비용 절감** – 수동 문서 통합 작업을 수행하는 전담 인력을 줄일 수 있습니다.
- **사용량 과금** – 사전 투자가 필요 없으며, 실제로 사용한 API 호출만 요금이 부과됩니다.
- **유지보수 비용 없음** – 유지보수할 서버가 없고, 소프트웨어 업데이트도 필요 없으며, 호환성 문제도 없습니다.
- **복잡한 엑셀 서식 보존** – 바꾸기 작업 후에도 원래 워크북의 서식, 수식 및 차트가 그대로 유지됩니다.

## SDK를 사용하여 스프레드시트 콘텐츠 바꾸기 API를 사용하는 방법

### OpenAPI 사양

[OpenAPI 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceSpreadsheetContent)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 요청을 수행할 수 있도록 합니다.

### Aspose.Cells Cloud SDK 사용

SDK를 사용하는 것이 개발 속도를 가장 빠르게 향상시킬 수 있는 방법입니다. SDK는 하위 수준의 세부 사항을 처리해 주므로, 최소한의 코드로 콘텐츠 바꾸기 작업을 구현할 수 있습니다. 지원되는 언어 전체 목록은 공식 **Aspose.Cells Cloud SDK GitHub 저장소**를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스와 상호 작용하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ReplaceTextInLocalFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ReplaceTextInLocalFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ReplaceTextInLocalFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ReplaceTextInLocalFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ReplaceTextInLocalFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ReplaceTextInLocalFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ReplaceTextInLocalFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ReplaceTextInLocalFile.go" >}}
{{</tab>}}
{{< /tabs >}}