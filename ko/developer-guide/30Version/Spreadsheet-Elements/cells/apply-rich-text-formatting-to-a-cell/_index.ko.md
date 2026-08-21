---
title: "셀에 서식 있는 텍스트(Rich Text) 적용하기"
type: docs
url: /ko/apply-rich-text-formatting-to-a-cell/
weight: 40
keywords: "Aspose.Cells, Excel, 서식 있는 텍스트, 셀 서식, REST API, Aspose.Cells Cloud"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 셀에 서식 있는 텍스트(Rich Text) 서식을 적용하는 방법을 알아보세요. 요청 구문, 매개변수 세부 정보, cURL 예제, SDK 스니펫 포함."
ArticleTitle: "Aspose.Cells Cloud API를 사용하여 셀에 서식 있는 텍스트 적용하기"
---

이 REST API는 Excel 파일 내 셀에 **서식 있는 텍스트(Rich Text)** 서식을 적용합니다.

**필수 조건:** 이 작업을 호출하기 전에 유효한 JWT 토큰이 필요하며, 대상 Excel 파일이 이미 지정된 저장소 폴더에 존재해 있어야 합니다.

**배경 정보:** 서식 있는 텍스트(Rich Text) 서식을 사용하면 단일 셀 내에서 여러 글꼴 스타일을 적용할 수 있어 Excel 워크시트에서 더 풍부하고 표현력 있는 데이터를 제공할 수 있습니다.

## PostCellCharacters API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/characters
```

### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름 | 유형   | 위치     | 설명                                                                 |
|---------------|--------|----------|----------------------------------------------------------------------|
| name          | string | path     | Excel 파일 이름(예: `Book1.xlsx`)                                  |
| sheetName     | string | path     | 대상 셀이 포함된 워크시트 이름                                      |
| cellName      | string | path     | 서식을 적용할 셀의 주소(예: `A1`)                                   |
| options       | object | body     | 셀에 대한 서식 있는 텍스트 서식 설정을 정의하는 JSON 객체            |
| folder        | string | query    | Excel 파일이 위치한 저장소 폴더                                     |
| storageName   | string | query    | 사용자 정의 저장소를 사용할 경우 저장소 서비스 이름                |

### **응답**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP 상태 코드**

| 코드 | 의미           | 설명                                                   |
|------|----------------|--------------------------------------------------------|
| 200  | OK             | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함   |
| 400  | Bad Request    | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형) |
| 401  | Unauthorized   | 유효하지 않거나 누락된 JWT 토큰                         |
| 413  | Payload Too Large | 업로드된 파일이 크기 제한을 초과함                    |
| 500  | Internal Server Error | 예기치 않은 서버 오류                              |

## SDK를 사용한 PostCellCharacters API 사용 방법

### PostCellCharacters API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Cells/PostCellCharacters)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청(Request)" tabName12="응답(Response)" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/cells/A1/characters" \
-X POST \
-d "{ \"FontSetting\": [ { \"Font\": { \"IsBold\": \"true\", \"Size\": \"24\" }, \"Length\": \"5\", \"StartIndex\": \"0\" }, { \"Font\": { \"IsItalic\": \"true\", \"Size\": \"15\" }, \"Length\": \"4\", \"StartIndex\": \"5\" } ] }" \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
*C# SDK 예제*  

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCellCharacters.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
*Java SDK 예제*  

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCellCharacters.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
*PHP SDK 예제*  

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCellCharacters.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
*Ruby SDK 예제*  

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCellCharacters.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
*Node.js SDK 예제*  

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCellCharacters.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
*Python SDK 예제*  

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCellCharacters.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
*Perl SDK 예제*  

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCellCharacters.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
*Go SDK 예제*  

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCellCharacters.go" >}}
{{< /tab >}}

{{< /tabs >}}
---