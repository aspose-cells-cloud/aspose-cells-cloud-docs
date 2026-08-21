---
title: "Aspose.Cells Cloud API를 사용하여 Excel 워크북 보호"
second_title: "문서"
linktitle: "Excel 파일 보호"
type: docs
url: /ko/protect-excel-file/
aliases: [  /ko/protect-excel-workbooks/ , /ko/workbook/protect/ ]
keywords: "Aspose.Cells, Excel 보호, API, REST, SDK"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크북을 보호하는 방법을 알아보세요. 인증 단계, 쿼리 및 본문 매개변수, cURL 요청 및 C#, Java, PHP, Ruby, Node.js, Python, Perl, Go용 SDK 코드 예제가 포함되어 있습니다."
weight: 30
ArticleTitle: "Aspose.Cells Cloud API를 사용하여 Excel 워크북 보호"
---

이 REST API는 Excel 워크북을 **보호**하며, Aspose.Cells Cloud를 사용하여 암호 및 보호 옵션을 사용하여 Excel 워크북을 안전하게 보호할 수 있습니다.

## PostProtectDocument API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/protection
```

### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 쿼리 매개변수

| 매개변수 이름 | 유형   | 설명                                                     |
| -------------- | ------ | --------------------------------------------------------------- |
| folder         | string | 소스 워크북이 포함된 폴더. _(선택 사항)_          |
| storageName    | string | 저장소 위치의 이름. _(선택 사항; 기본값 = "Default")_ |

### 요청 본문 매개변수

| 매개변수 이름 | 유형                      | 설명                                                   |
| -------------- | ------------------------- | ------------------------------------------------------------- |
| protection     | WorkbookProtectionRequest | 워크북에 대한 보호 설정을 정의하는 객체. |

#### WorkbookProtectionRequest

| 매개변수 이름 | 유형   | 설명                                                                                                                                              |
| -------------- | ------ | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ProtectionType | string | 적용할 보호 유형. 허용되는 값(대/소문자 구분 없음): **ALL**, **CONTENTS**, **NONE**, **OBJECTS**, **SCENARIOS**, **STRUCTURE**, **WINDOWS**. |
| Password       | string | 보호를 위해 설정할 선택적 암호.                                                                                                             |

### 응답

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP 상태 코드**

| 코드 | 의미                     | 설명                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함. |
| 400  | Bad Request                 | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형). |
| 401  | Unauthorized                | 잘못되거나 누락된 JWT 토큰. |
| 413  | Payload Too Large           | 업로드된 파일이 크기 제한을 초과함. |
| 500  | Internal Server Error       | 예기치 않은 서버 오류. |

## SDK를 사용하여 PostProtectDocument API 사용하는 방법

### 사전 요구 사항

API를 호출하기 전에 다음 단계를 완료했는지 확인하세요:

- 보안 섹션에 설명된 인증 플로우를 사용하여 **JWT 액세스 토큰을 획득**하세요.  
- 워크북을 Aspose Cloud 저장소에 **업로드**하거나, 대상 폴더에 이미 존재하는지 확인하세요.  
- 저장소 이름(지정하지 않으면 기본값은 `"Default"`)과 보호하려는 파일의 정확한 파일 이름을 **알고 있어야 합니다**.

### PostProtectDocument API 사양

<a href="https://apireference.aspose.cloud/cells/#/Workbook/PostProtectDocument" target="_blank" rel="noopener noreferrer">OpenAPI 사양</a>은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

### 예제: cURL을 사용하여 워크북 보호

1. **사전 요구 사항 / 인증** 섹션에서 설명한 대로 액세스 토큰을 획득하세요.  
2. 요청 실행:

   ```bash
   curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/protection?folder=MyFolder&storageName=MyStorage" \
        -H "accept: application/json" \
        -H "Content-Type: application/json" \
        -H "Authorization: Bearer <access_token>" \
        -d '{ "ProtectionType": "ALL", "Password": "aspose" }'
   ```

   응답에는 보호가 성공적으로 완료되었음을 확인하는 상태 객체가 포함됩니다.

### Aspose.Cells Cloud SDK 사용

SDK를 사용하는 것이 Aspose.Cells Cloud에 대해 개발하는 가장 빠른 방법입니다. SDK는 저수준 세부 사항을 추상화하여 비즈니스 로직에 집중할 수 있도록 합니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 저장소</a>를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostProtectWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostProtectWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostProtectWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostProtectWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostProtectWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostProtectWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostProtectWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostProtectWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}

### 샘플 전체 응답

```json
{
  "Status": "OK",
  "Code": 200,
  "Workbook": {
    "Name": "test.xlsx",
    "Path": "/MyFolder/test.xlsx",
    "Protection": {
      "ProtectionType": "ALL",
      "Password": true
    }
  }
}
```