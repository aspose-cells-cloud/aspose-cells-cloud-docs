---
title: "Aspose.Cells Cloud 웹 API – 텍스트 추출"
second_title: "Aspose.Cells Cloud – 온라인 샌드박스"
linktitle: "텍스트 추출"
type: docs
url: /ko/extract-text/
keywords: "Aspose.Cells Cloud, 텍스트 추출, Excel API, 셀 텍스트 추출, REST API"
description: "Aspose.Cells Cloud API를 사용하여 Excel 셀에서 하위 문자열, 숫자 또는 문자를 추출합니다. 'before/after 텍스트', 위치 기반 추출 및 새 범위로 직접 출력을 지원합니다."
weight: 100
ArticleTitle: "Aspose.Cells Cloud 텍스트 추출 API 문서"
---

스preadsheet 셀에서 하위 문자열, 문자 또는 숫자를 다른 셀으로 추출하여 복잡한 FIND, MIN, LEFT, RIGHT 수식을 사용할 필요를 제거합니다.

## **ExtractText API**

```http
PUT https://api.aspose.cloud/v4.0/cells/content/extract/text
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 보장되며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

```bash
-H "Authorization: Bearer {access_token}"
```

### **extractText API의 요청 매개변수**

| 매개변수 이름     | 유형     | 위치          | 설명                                                                                                                     |
| ---------------- | ------- | ------------- | ------------------------------------------------------------------------------------------------------------------------ |
| Spreadsheet      | 파일    | FormData      | spreadsheet 파일을 업로드합니다.                                                                                         |
| extractTextType  | 문자열  | Query         | 추출 모드를 나타내는 열거형입니다. 허용되는 값: `Before`, `After`, `BeforePosition`, `AfterPosition`.                   |
| beforeText       | 문자열  | Query         | 추출하려는 하위 문자열 **앞에** 나타나야 하는 텍스트입니다. `extractTextType=Before`인 경우 사용됩니다.                   |
| afterText        | 문자열  | Query         | 추출하려는 하위 문자열 **뒤에** 나타나야 하는 텍스트입니다. `extractTextType=After`인 경우 사용됩니다.                    |
| beforePosition   | 정수    | Query         | 셀의 왼쪽에서부터 반환할 문자 수입니다. `extractTextType=BeforePosition`인 경우 사용됩니다.                               |
| afterPosition    | 정수    | Query         | 셀의 오른쪽에서부터 반환할 문자 수입니다. `extractTextType=AfterPosition`인 경우 사용됩니다.                              |
| outPositionRange | 문자열  | Query         | 추출된 텍스트를 기록할 대상 범위(예: `Sheet1!A1`)입니다.                                                                |
| worksheet        | 문자열  | Query         | 소스 셀을 포함하는 워크시트 이름입니다.                                                                                  |
| range            | 문자열  | Query         | 소스 셀 또는 범위(예: `A1`)입니다.                                                                                       |
| outPath          | 문자열  | Query _(선택 사항)_ | 결과 워크북이 저장될 저장소 내 폴더 경로입니다. 생략 시 결과는 응답 본문에 반환됩니다.                                   |
| outStorageName   | 문자열  | Query         | 출력 파일에 사용할 저장소 이름입니다.                                                                                    |
| region           | 문자열  | Query         | spreadsheet 지역 설정(예: `US`, `EU`)입니다.                                                                            |
| password         | 문자열  | Query         | 보호된 워크북을 열기 위한 비밀번호입니다.                                                                                |

**샘플 cURL 요청**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/content/extract/text?extractTextType=Before&beforeText=Total&outPositionRange=Sheet1!B1&worksheet=Sheet1&range=A1" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Sample.xlsx"
```

### **응답**

요청이 성공하면, API는 추출된 텍스트와 쓰여진 셀의 주소를 포함하는 JSON 페이로드를 반환합니다:

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

`outPath` 매개변수가 제공되면, 응답에는 상태 메시지만 포함되며 워크북은 지정된 위치에 저장됩니다.

**`outPath`를 생략했을 때의 샘플 응답**

```json
{
  "Code": 200,
  "Status":"OK"
}
```

### 오류 코드

- **200 OK** – 추출이 성공적으로 완료되었습니다.  
- **202 Accepted** – 요청이 비동기 처리를 위해 수락되었습니다.  
- **400 Bad Request** – 잘못된 Aspose.Cells Cloud API URI 또는 필수 매개변수가 누락되었습니다.  
- **401 Unauthorized** – 잘못된 액세스 토큰, 클라이언트 ID 또는 클라이언트 비밀번호입니다.  
- **404 Not Found** – 지정된 spreadsheet 파일에 접근할 수 없습니다.  
- **500 Server Error** – 워크북 처리 중 예기치 않은 오류가 발생했습니다.

## OpenAPI 사양

[OpenAPI 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/ExtractText)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

### Aspose.Cells Cloud SDK 사용

SDK를 사용하는 것이 개발 속도를 가장 빠르게 향상시킬 수 있는 방법입니다. SDK는 기본 세부 사항을 처리하므로, 최소한의 코드로 셀에 대해 **텍스트 추출** 기능만 구현하면 됩니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{<tab tabNum="1" >}}

```csharp
// C# 예제 – 텍스트 추출 (간결성을 위해 코드 생략)
```

{{</tab>}}

{{<tab tabNum="2" >}}

```java
// Java 예제 – 텍스트 추출 (간결성을 위해 코드 생략)
```

{{</tab>}}

{{<tab tabNum="3" >}}

```php
// PHP 예제 – 텍스트 추출 (간결성을 위해 코드 생략)
```

{{</tab>}}

{{<tab tabNum="4" >}}

```ruby
# Ruby 예제 – 텍스트 추출 (간결성을 위해 코드 생략)
```

{{</tab>}}

{{<tab tabNum="5" >}}

```javascript
// Node.js 예제 – 텍스트 추출 (간결성을 위해 코드 생략)
```

{{</tab>}}

{{<tab tabNum="6" >}}

```python
# Python 예제 – 텍스트 추출 (간결성을 위해 코드 생략)
```

{{</tab>}}

{{<tab tabNum="7" >}}

```perl
# Perl 예제 – 텍스트 추출 (간결성을 위해 코드 생략)
```

{{</tab>}}

{{<tab tabNum="8" >}}

```go
// Go 예제 – 텍스트 추출 (간결성을 위해 코드 생략)
```

{{</tab>}}

{{< /tabs >}}