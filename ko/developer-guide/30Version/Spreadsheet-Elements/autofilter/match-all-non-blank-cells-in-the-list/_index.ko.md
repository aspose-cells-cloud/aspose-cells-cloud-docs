---
title: "Excel 워크시트에서 비어 있지 않은 모든 셀 일치시키기"
second_title: "문서"
linktitle: "비어 있지 않은 모든 셀 일치시키기"
type: docs
url: /autofilter/match-all-non-blank/
aliases: [/match-all-non-blank-cells-in-the-list/]
keywords: "Aspose.Cells Cloud, 비어 있지 않은 셀 일치, AutoFilter, Excel API"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트의 AutoFilter 목록에서 비어 있지 않은 모든 셀을 일치시키는 방법을 알아보세요. 엔드포인트, 매개변수, 인증, 응답 스키마, 오류 코드 및 SDK 예제를 포함합니다."
ArticleTitle: "Aspose.Cells Cloud API를 사용하여 Excel 워크시트에서 비어 있지 않은 모든 셀 일치시키기"
weight: 100
---

**개요**  
*비어 있지 않은 모든 셀 일치시키기* 작업은 워크시트에 AutoFilter를 적용하고, 지정된 열에 데이터가 포함된 행만 반환하며, 빈 셀은 무시합니다. 이 기능은 데이터 세트 정리, 리포트 생성, 추가 분석을 위한 데이터 준비 등에 유용합니다.

**사전 요구 사항**  
- Aspose.Cells Cloud 인증을 위한 유효한 JWT 토큰.  
- 워크북이 Aspose Cloud 스토리지에 업로드되어 있어야 합니다.  
- 필터를 적용하려는 파일 이름, 워크시트 이름 및 0부터 시작하는 열 인덱스(`fieldIndex`)가 필요합니다.

이 REST API는 Excel 워크시트의 AutoFilter 목록에서 비어 있지 않은 모든 셀을 일치시킵니다.

## PostWorksheetMatchNonBlanks API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/matchNonBlanks
```

### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름 | 유형    | 위치 | 설명                                                    |
| -------------- | ------- | -------- | -------------------------------------------------------------- |
| name           | string  | path     | Excel 파일의 이름.                                    |
| sheetName      | string  | path     | AutoFilter가 포함된 워크시트 이름.        |
| fieldIndex     | integer | query    | 필터를 적용할 열의 0부터 시작하는 인덱스. |
| folder         | string  | query    | _(선택 사항)_ 파일이 저장된 폴더 경로.             |
| storageName    | string  | query    | _(선택 사항)_ 사용할 스토리지 서비스 이름.               |

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
| 200  | OK                          | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보가 포함됨. |
| 400  | 잘못된 요청                 | 누락되었거나 잘못된 매개변수(예: 지원되지 않는 파일 형식). |
| 401  | 인증되지 않음                | 잘못되었거나 누락된 JWT 토큰. |
| 413  | 페이로드가 너무 큼           | 업로드된 파일이 크기 제한을 초과함. |
| 500  | 내부 서버 오류       | 예기치 않은 서버 오류. |

*예시 오류 응답 (400)*  

```json
{
  "Code": 400,
  "Message": "잘못된 매개변수: fieldIndex는 음이 아닌 정수여야 합니다."
}
```

## SDK를 사용하여 PostWorksheetMatchNonBlanks API 사용하는 방법

### PostWorksheetMatchNonBlanks API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/AutoFilter/PostWorksheetMatchNonBlanks)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API에 호출을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/matchNonBlanks?fieldIndex=0" \
  -X POST \
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

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 호출을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetMatchNonBlanks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetMatchNonBlanks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetMatchNonBlanks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetMatchNonBlanks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetMatchNonBlanks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetMatchNonBlanks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetMatchNonBlanks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetMatchNonBlanks.go" >}}

{{< /tab >}}

{{< /tabs >}}
---