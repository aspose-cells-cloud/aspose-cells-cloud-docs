---
title: "Aspose.Cells Cloud 교체 웹 API – 원격 스프레드시트 범위 내 텍스트 업데이트"
second_title: "문서"
ArticleTitle: "클라우드 Excel 파일의 범위 텍스트 일괄 교체 – 찾기 및 교체 API"
linktitle: "원격 범위 콘텐츠 교체"
type: docs
url: /ko/replace-content-in-remote-range/
keywords: "원격 Excel 범위 텍스트 교체, Aspose.Cells Cloud API, Excel 찾기 및 교체, 클라우드 스프레드시트 편집, 원격 Excel 파일 업데이트"
description: "Aspose.Cells Cloud를 사용하여 원격 Excel 파일의 특정 범위에서 텍스트를 찾고 교체합니다. 인증, 오류 처리 및 다중 언어 SDK를 지원합니다."
weight: 100
---

클라우드에 저장된 원격 Excel 파일에서 일괄 텍스트 교체를 수행합니다. Aspose.Cells 찾기 및 교체 API를 사용하여 지정된 범위 내에서 특정 텍스트 문자열을 효율적으로 찾아 업데이트합니다.

## **원격 범위 콘텐츠 교체 API**

### 웹 API

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/replace/content
```

### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

```bash
-H "Authorization: Bearer {access_token}"
```

### **요청 매개변수**

| 매개변수 이름 | 유형   | 경로/쿼리 문자열/HTTP 본문 | 설명                                                                                                                                                 |
| :------------ | :----- | :-------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name          | String | 경로                        | 수정할 클라우드 스토리지에 저장된 워크북 파일 이름(예: `"report.xlsx"`).                                                               |
| searchText    | String | 쿼리                        | 지정된 워크시트 및 셀 범위에서 검색할 텍스트 문자열입니다. 정확한 텍스트 일치를 지원합니다.                                                   |
| replaceText   | String | 쿼리                        | 지정된 범위 내에서 `searchText`의 모든Occurrences를 대체할 텍스트 문자열입니다.                                                           |
| worksheet     | String | 경로                        | 찾기 및 교체 작업을 수행할 워크시트 이름입니다.                                                                           |
| cellArea      | String | 경로                        | 텍스트 검색 및 교체가 수행될 특정 셀 범위(예: `"A1:D20"`)입니다.                                                                |
| folder        | String | 쿼리                        | 소스 워크북이 위치한 클라우드 스토리지 폴더 경로입니다.                                                                                         |
| storageName   | String | 쿼리                        | _(선택 사항)_ 워크북이 있는 클라우드 스토리지 이름입니다. 생략 시 기본 클라우드 스토리지가 사용됩니다.                                       |
| region        | String | 쿼리                        | _(선택 사항)_ 텍스트 처리를 위한 로케일을 설정하며, 검색 작업에서 대소문자 구분 및 문자 인코딩에 영향을 줄 수 있습니다(예: `"en-US"`, `"tr-TR"`). |
| password      | String | 쿼리                        | _(선택 사항)_ 워크북이 암호 보호되어 있는 경우, 파일을 열고 수정하기 위해 암호를 제공합니다.                                                       |

### **응답**

```json
{
  "Name": "CellsCloudResponse",
  "Type": "Class",
  "Properties": [
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer"
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String"
      }
    }
  ]
}
```

성공적인 호출은 다음 구체적인 JSON 페이로드를 반환합니다:

```json
{
  "Code": 200,
  "Status": "OK"
}
```


### 오류 코드

| 코드 | 메시지      | 발생 시점                                          |
| ---- | ----------- | ------------------------------------------------- |
| 400  | 잘못된 요청 | 요청 URI 또는 매개변수가 잘못된 형식인 경우.            |
| 401  | 인증되지 않음 | 인증 토큰이 누락되었거나 유효하지 않은 경우.                |
| 404  | 찾을 수 없음 | 지정된 워크북을 찾을 수 없거나 접근할 수 없는 경우.     |
| 500  | 서버 오류   | 워크북 처리 중 내부 서버 오류가 발생한 경우. |

## 원격 스프레드시트 범위 콘텐츠 교체 API는 어디에 사용해야 하나요?

- **일괄 클라우드 파일 업데이트**: AWS S3 및 Azure Blob과 같은 클라우드 스토리지에 저장된 여러 Excel 파일의 콘텐츠를 수정합니다.
- **동적 클라우드 템플릿 채우기**: 클라우드에 저장된 보고서 템플릿에 일괄적으로 동적 데이터를 채웁니다.
- **지역 간 파일 동기화**: 서로 다른 지리적 영역에 있는 클라우드 스토리지의 Excel 파일 콘텐츠 일관성을 동기화합니다.

## 원격 스프레드시트 범위 콘텐츠 교체 API를 사용해야 하는 이유는 무엇인가요?

- **개발자 친화적**: Aspose.Cells Cloud는 다중 언어 SDK 라이브러리를 제공하여 빠른 개발과 포괄적인 문서화를 가능하게 합니다. 맞춤 솔루션 구축에 비해 개발 작업량을 크게 줄여줍니다.
- **인건비 절감**: 문서 통합을 처리하는 전담 인력의 필요성을 줄입니다.
- **사용량 기준 과금**: 선급 투자가 필요 없으며, 실제로 사용한 API 호출에 대해서만 요금이 부과됩니다.
- **유지보수 비용 없음**: 서버 유지보수, 소프트웨어 업데이트, 호환성 문제 해결이 필요 없습니다.
- **복잡한 Excel 서식 보존**: 보편적으로 접근 가능한 PDF 형식으로 복잡한 Excel 서식을 보존합니다.

## SDK를 사용하여 원격 스프레드시트 범위 콘텐츠 교체 API 사용 방법

### OpenAPI 사양

[OpenAPI 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceContentInRemoteRange)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

### Aspose.Cells Cloud SDK 사용

SDK를 사용하는 것이 개발 속도를 극대화하는 최선의 방법입니다. SDK는 기본 세부 사항을 처리하므로, 최소한의 코드로 스프레드시트의 셀 콘텐츠 교체를 간편하게 구현할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}

```csharp
```

{{</tab>}}
{{<tab tabNum="2" >}}

```java
```

{{</tab>}}
{{<tab tabNum="3" >}}

```php
```

{{</tab>}}
{{<tab tabNum="4" >}}

```ruby
```

{{</tab>}}
{{<tab tabNum="5" >}}

```javascript
```

{{</tab>}}
{{<tab tabNum="6" >}}

```python
```

{{</tab>}}
{{<tab tabNum="7" >}}

```perl
```

{{</tab>}}
{{<tab tabNum="8" >}}

```go
```

{{</tab>}}
{{< /tabs >}}