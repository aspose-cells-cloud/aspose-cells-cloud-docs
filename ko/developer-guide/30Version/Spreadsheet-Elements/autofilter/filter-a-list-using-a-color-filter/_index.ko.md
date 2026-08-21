---
title: "Excel 워크시트에 색상 필터 추가"
second_title: "문서"
linktitle: "색상 필터 추가"
type: docs
url: /ko/autofilter/add-color-filter/
aliases: [  /ko/filter-a-list-using-a-color-filter/ , /ko/autofilter/add-a-color-filter/ ]
keywords: "Excel, 색상 필터, Aspose.Cells Cloud, REST API, 자동 필터, JWT 인증"
description: "Aspose.Cells Cloud API를 사용하여 Excel 워크시트에 색상 필터를 적용하는 방법을 알아보세요. 엔드포인트, 매개변수, cURL 예제, 오류 처리 및 SDK 샘플이 포함되어 있습니다."
weight: 65
ArticleTitle: "Aspose.Cells Cloud API를 사용하여 Excel 워크시트에 색상 필터 추가하기"
---

Aspose.Cells Cloud API를 사용하여 Excel 워크시트에 색상 필터를 추가하는 방법을 알아보세요. 이 가이드에서는 필요한 엔드포인트, 매개변수, 인증 전제 조건, 샘플 cURL 요청, SDK 예제 및 응답 처리 방법을 다룹니다.

이 REST API는 Excel 워크시트에 **색상 필터**를 추가합니다.

## PutWorksheetColorFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/colorFilter
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 위해 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수:


| 매개변수 이름 | 유형    | 위치 | 설명                                                                 |
|---------------|---------|------|-----------------------------------------------------------------------------|
| name          | string  | path | Excel 파일의 이름.                                                          |
| sheetName     | string  | path | 필터를 적용할 데이터가 포함된 워크시트의 이름.                             |
| range         | string  | query| 필터를 적용할 셀 범위(예: `A1:B10`).                                        |
| fieldIndex    | integer | query| 색상 필터를 적용할 열의 0부터 시작하는 인덱스.                              |
| colorFilter   | object  | body | 필터링할 전경색 및 배경색을 정의하는 JSON 객체.                             |
| matchBlanks   | boolean | query| 빈 셀이 포함된 행을 필터 결과에 포함할지 여부.                              |
| refresh       | boolean | query| 필터 적용 후 워크시트를 새로 고칠지 여부(`true`인 경우 새로 고침).          |
| folder        | string  | query| Excel 파일이 위치한 저장소 폴더.                                            |
| storageName   | string  | query| 저장소 서비스의 이름(예: Aspose Cloud Storage).                             |

**`colorFilter` JSON 스키마**

| 속성              | 유형   | 설명                                                                    | 필수 여부 |
|-------------------|--------|--------------------------------------------------------------------------------|----------|
| Pattern           | string | 필터 패턴(예: `"Solid"`).                                             | 예      |
| ForegroundColor   | object | 전경색을 정의합니다. `Color`, `ColorIndex`, `IsShapeColor`, `ThemeColor`, `Type`와 같은 하위 속성을 포함합니다. | 아니요 |
| BackgroundColor   | object | 배경색을 정의합니다. `ForegroundColor`와 동일한 하위 속성을 가집니다.      | 아니요 |

### **응답**

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
| 400  | 잘못된 요청                 | 누락되거나 유효하지 않은 매개변수(예: 지원되지 않는 파일 유형). |
| 401  | 인증되지 않음                | 잘못되거나 누락된 JWT 토큰. |
| 413  | 페이로드가 너무 큼           | 업로드된 파일이 크기 제한을 초과함. |
| 500  | 내부 서버 오류       | 예기치 않은 서버 오류. |

## SDK를 사용하여 PutWorksheetColorFilter API 사용하는 방법

### PutWorksheetColorFilter API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetColorFilter)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/colorFilter?range=A1%3AB1&fieldIndex=0" \
-X PUT \
-d "{ \"Pattern\": \"Solid\", \"ForegroundColor\": { \"Color\": { \"A\": 255, \"R\": 0, \"G\": 255, \"B\": 255 }, \"ColorIndex\": 0, \"IsShapeColor\": true, \"ThemeColor\": { \"ColorType\": \"Text2\", \"Tint\": 1 }, \"Type\": \"Automatic\" }, \"BackgroundColor\": { \"Color\": { \"A\": 255, \"R\": 0, \"G\": 255, \"B\": 255 }, \"ColorIndex\": 0, \"IsShapeColor\": true, \"ThemeColor\": { \"ColorType\": \"Text2\", \"Tint\": 0 }, \"Type\": \"Automatic\" }}" \
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

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 작업에 집중할 수 있게 해줍니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetColorFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetColorFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetColorFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetColorFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetColorFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetColorFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetColorFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetColorFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}

**참고:** [사용자 지정 필터 추가](https://docs.aspose.cloud/cells/autofilter/add-custom-filter/), [날짜 필터 추가](https://docs.aspose.cloud/cells/autofilter/add-date-filter/), [자동 필터 제거](https://docs.aspose.cloud/cells/autofilter/remove-auto-filter/)도 참조하세요.