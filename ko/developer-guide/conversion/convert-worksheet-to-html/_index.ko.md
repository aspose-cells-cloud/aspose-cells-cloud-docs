---
title: "Aspose.Cells Cloud 웹 API – 워크시트를 HTML로 변환"
second_title: "문서"
ArticleTitle: "Aspose.Cells Cloud API를 사용하여 워크시트를 HTML로 변환하는 방법"
linktitle: "워크시트를 HTML로 변환"
type: docs
url: /ko/convert-worksheet-to-html/
description: "Aspose.Cells Cloud API를 사용하여 Excel 워크시트를 HTML로 변환하는 방법을 배워보세요. 업로드가 필요 없고, 사용자 정의 글꼴, 지역 설정 지원 및 오류 처리 기능을 제공합니다."
keywords: "Aspose.Cells, Excel을 HTML로, 워크시트 변환, 클라우드 API"
weight: 100
---

**ConvertWorksheetToHtml** 엔드포인트는 로컬 파일 시스템에서 Excel 워크북을 읽어 지정된 워크시트를 추출한 후 HTML 파일로 콘텐츠를 반환합니다. 변환 작업은 완전히 Aspose의 클라우드 서버에서 실행되므로 중간 업로드나 저장이 필요 없습니다. 스프레드시트 데이터를 웹에서 바로 볼 수 있도록 생성하는 데 이상적이며, 선택적 출력 경로, 사용자 정의 글꼴, 지역 설정, 암호로 보호된 워크북도 지원합니다.

## 워크시트를 HTML로 변환하는 API

### 웹 API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/html
```

### **보안 및 인증**

Aspose.Cells Cloud API는 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름     | 유형     | 위치     | 필수/선택적 | 설명                                                                                                                                                                                                                                                                               |
| :---------------- | :------- | :------- | :---------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet       | 파일     | 필수     | FormData    | 처리할 이진 Excel 파일입니다. 유효한 .xlsx, .xls, .xlsb 등이어야 합니다. 예: `myWorkbook.xlsx`. Excel 파일은 요청 본문에서 직접 읽히며, 클라우드 저장소로 사전 업로드할 필요가 없습니다.                                                                                                         |
| worksheet         | 문자열   | 필수     | 쿼리        | 변환할 워크시트의 이름(대소문자 구분). 제공된 워크북에 반드시 존재해야 합니다. 예: `Sheet1`.                                                                                                                                                                                       |
| outPath           | 문자열   | 선택적   | 쿼리        | 생성된 HTML 파일을 저장할 대상 폴더 경로(클라우드 저장소 기준). 생략 시, 파일은 응답에 직접 반환됩니다. 예: `/output/html/`.                                                                                                                                                         |
| outStorageName    | 문자열   | 선택적   | 쿼리        | `outPath`에 사용할 클라우드 저장소 서비스의 이름입니다. `outPath`가 기본 저장소가 아닌 곳을 가리킬 때만 필요합니다.                                                                                                                                                                |
| fontsLocation     | 문자열   | 선택적   | 쿼리        | 변환 시 사용할 사용자 정의 TrueType/OpenType 글꼴이 포함된 폴더의 절대 경로입니다. 비표준 문자의 올바른 렌더링을 가능하게 합니다.                                                                                                                                                 |
| region            | 문자열   | 선택적   | 쿼리        | 숫자/날짜 형식에 영향을 주는 로케일 식별자(예: `en-US`, `fr-FR`). 기본값은 워크북의 내부 지역 설정입니다.                                                                                                                                                                            |
| password          | 문자열   | 선택적   | 쿼리        | 보호된 워크북을 열 때 필요한 암호입니다. 보호되지 않은 파일은 생략하십시오.                                                                                                                                                                                                       |

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

**HTTP 상태 코드**

| 코드 | 의미               | 설명                                                      |
| ---- | ------------------ | --------------------------------------------------------- |
| 200  | OK (성공)          | 필터가 성공적으로 적용되었으며, 응답에 작업 세부 정보가 포함됩니다. |
| 400  | Bad Request (잘못된 요청) | 누락되거나 유효하지 않은 매개변수(예: 지원되지 않는 파일 형식)입니다.  |
| 401  | Unauthorized (인증되지 않음) | 잘못되거나 누락된 JWT 토큰입니다.                         |
| 413  | Payload Too Large (ペイロードが大きすぎます) | 업로드된 파일이 크기 제한을 초과했습니다.                 |
| 500  | Internal Server Error (내부 서버 오류) | 예기치 않은 서버 오류입니다.                              |

## 워크시트를 HTML로 변환하는 API는 어디에 사용하면 좋을까요?

- 웹 포털에 실시간 스프레드시트 데이터를 임베드 – 재무 보고서 워크시트를 HTML로 변환하여 Excel 플러그인 없이 브라우저에서 바로 볼 수 있도록 합니다.
- Excel 템플릿에서 인쇄용 HTML 인보이스 생성 – 미리 정의된 워크시트에서 웹 준비가 완료된 인보이스 페이지를 자동으로 생성합니다.
- 문서 스니펫 생성 – 설계 사양 시트를 HTML 조각으로 변환하여 기술 매뉴얼이나 위키에 삽입합니다.
- 로우코드 BI 대시보드 개발 – 워크시트 데이터를 가져와 HTML로 변환한 뒤, 사용자 정의 대시보드 위젯 내에 표시합니다.

## 왜 워크시트를 HTML로 변환하는 API를 사용해야 할까요?

- **업로드가 필요 없는 워크플로우** – 클라우드에서 로컬 파일을 직접 변환하므로, 먼저 대규모 워크북을 저장소로 전송할 필요가 없습니다.
- **고성능 렌더링** – 서버 측 변환은 Aspose의 최적화된 엔진을 활용하여 빠르고 정확한 HTML 출력을 제공합니다.
- **출력 제어의 완전한 제어** – 선택적 매개변수(사용자 정의 글꼴, 지역, 암호)를 통해 HTML을 로케일 및 브랜딩 요구 사항에 맞게 조정할 수 있습니다.
- **원활한 통합** – multipart/form-data를 사용한 간단한 PUT 요청이 CI/CD 파이프라인, 마이크로서비스, 서버리스 함수에 자연스럽게 통합됩니다.

## SDK를 사용하여 워크시트를 HTML로 변환하는 API 사용 방법

### 워크시트를 HTML로 변환하는 API 사양

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToHtml" target="_blank" rel="noopener noreferrer">워크시트를 HTML로 변환하는 API 사양</a>은 웹 브라우저에서 직접 REST 상호 작용을 실행할 수 있는 공개적으로 접근 가능한 프로그래밍 인터페이스를 제공합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API에 호출을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/html?worksheet=Sheet1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.html
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 인코딩됨)",
  "contentType": "MIME 유형",
  "fileDownloadName": "선택적 파일 이름"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 저수준 세부 정보를 추상화해 간결한 코드로 워크시트를 병합하는 등 개발 속도를 높일 수 있습니다.  
Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud/aspnet-sdk" target="_blank" rel="noopener noreferrer">Aspose.Cells Cloud SDK GitHub 저장소</a>를 참조하십시오.  
다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스와 상호 작용하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertWorksheetToHtml.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertWorksheetToHtml.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertWorksheetToHtml.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertWorksheetToHtml.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertWorksheetToHtml.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertWorksheetToHtml.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertWorksheetToHtml.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertWorksheetToHtml.go" >}}
{{</tab>}}
{{< /tabs >}}