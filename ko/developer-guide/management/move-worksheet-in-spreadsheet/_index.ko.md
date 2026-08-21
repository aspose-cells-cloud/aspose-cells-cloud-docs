---
title: "Aspose.Cells Cloud Excel: 워크시트 이동 Web API – 프로그래밍 방식으로 시트 순서 변경"
second_title: "문서"
ArticleTitle: "Excel에서 워크시트 이동하는 방법 – 시트 순서 및 위치 재배열"
linktitle: "스프레드시트에서 워크시트 이동"
type: docs
url: /move-worksheet-in-spreadsheet/
keywords: "워크시트 이동 API, 시트 재배열 API, 시트 순서 변경 API, Excel 탭 관리 API, Aspose Cells REST API, 시트 위치 자동화, 워크북 구성 API, 스프레드시트 구조 API, 클라우드 Excel 자동화, 대량 시트 재배열"
description: "Excel 워크북 내에서 워크시트를 이동하여 시트 순서를 재조정하고 워크북 구조를 최적화하는 방법을 알아보세요. 워크시트 위치를 변경하고 탭을 재배열해 워크플로우를 개선하며 전문적인 스프레드시트 관리를 위해 시트 구성 작업을 자동화하세요."
weight: 100
---

Aspose.Cells Cloud API를 사용하여 Excel 워크북 내에서 프로그래밍 방식으로 워크시트를 이동하세요. RESTful API 호출을 통해 시트 순서를 변경하고, 탭을 재배열하며, 워크북 구조를 최적화하세요. 스프레드시트 구성 자동화 및 표준화된 워크북 레이아웃 생성에 이상적입니다.

## **스프레드시트에서 워크시트 이동 API**

### Web API

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/move/worksheet?sheetName={sheetName}&position={position}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}
```

### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

```bash
-H "Authorization: Bearer {access_token}"
```

### **요청 매개변수:**

| 매개변수 이름 | 유형     | 경로/쿼리 스트링/HTTP 본문 | 설명                                                                                                                                                   |
| :------------ | :------- | :------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet   | 파일     | FormData                   | **필수**. 재배열할 워크시트가 포함된 소스 Excel 워크북 파일(.xlsx, .xls 등).                                                                          |
| worksheet     | 문자열   | 쿼리                       | **필수**. 이동할 워크시트의 정확한 이름(예: `Summary`, `RawData_2024`).                                                                               |
| position      | 정수     | 쿼리                       | **필수**. 워크시트의 새 0부터 시작하는 인덱스 위치. 예: `0`은 첫 번째 위치로 이동, `2`는 세 번째 시트로 이동.                                             |
| outPath       | 문자열   | 쿼리                       | **선택 사항**. 재배열된 워크북을 저장할 클라우드 스토리지의 대상 폴더 경로. `null`이거나 생략 시 소스 파일 디렉터리가 기본값으로 사용됩니다.             |
| outStorageName| 문자열   | 쿼리                       | **필수**. 출력 파일을 저장할 구성된 클라우드 스토리지 서비스의 이름 식별자(예: `TeamDrive`).                                                            |
| region        | 문자열   | 쿼리                       | **선택 사항**. 적용할 로케일 설정(예: `es-MX`). 저장 작업 중 일부 포맷팅 규칙에 영향을 미칠 수 있습니다.                                                 |
| password      | 문자열   | 쿼리                       | **선택 사항**. 암호 보호 워크북을 열고 수정하는 데 필요한 복호화 암호. 파일이 암호화되지 않았다면 생략 가능합니다.                                      |

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

**HTTP 상태 코드**

| 코드 | 의미                  | 설명                                                       |
| ---- | --------------------- | ---------------------------------------------------------- |
| 200  | OK(성공)              | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함.     |
| 400  | Bad Request(잘못된 요청) | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형).  |
| 401  | Unauthorized(인증되지 않음) | 잘못되거나 누락된 JWT 토큰.                             |
| 413  | Payload Too Large(페이로드 크기 초과) | 업로드한 파일이 크기 제한을 초과함.                 |
| 500  | Internal Server Error(내부 서버 오류) | 예기치 않은 서버 오류.                                 |

## 어디에서 스프레드시트의 워크시트 이동 API를 사용해야 할까요?

- **표준화된 보고서 생성**: 월간 또는 분기 보고서가 자동 생성된 후 `요약` 또는 `임원 개요` 워크시트를 워크북 상단으로 이동해 파일을 열었을 때 핵심 결론이 먼저 표시되도록 합니다.
- **데이터 처리 파이프라인**: ETL 프로세스에서 다양한 데이터 소스의 원본 워크시트를 처리한 후, `Processed_Data` 워크시트를 워크북 내 논리적인 위치(예: 중간)로 이동시켜 원본 데이터와 분석 결과와 함께 명확한 프로세스 구조를 만듭니다.
- **사용자 맞춤형 파일 배포**: 사용자가 구성 인터페이스(예: 차트 페이지를 상단에 배치)를 통해 선호하는 레이아웃을 선택하면, 시스템이 선택에 따라 워크북 내 워크시트 순서를 자동으로 재배열하고 맞춤형 파일을 배포합니다.

## 왜 스프레드시트의 워크시트 이동 API를 사용해야 할까요?

- **개발자 친화적**: Aspose.Cells Cloud는 다양한 언어 SDK 라이브러리를 제공해 빠른 개발을 지원하며, 체계적인 문서도 제공됩니다. 맞춤 솔루션 구축에 비해 개발 작업량을 크게 줄여줍니다.
- **인력 비용 절감**: 문서 통합 전담 인력을 줄일 수 있습니다.
- **사용량 기준 과금**: 사전 투자 없이 실제로 사용한 API 호출만 비용을 지불합니다.
- **유지보수 비용 없음**: 서버 유지보수, 소프트웨어 업데이트, 호환성 문제 해결이 필요 없습니다.

## SDK를 사용해 스프레드시트의 워크시트 이동 API를 사용하는 방법

### 스프레드시트의 워크시트 이동 API 사양

[스프레드시트의 워크시트 이동 API 사양](https://reference.aspose.cloud/cells/#/ManagementController/MoveWorksheetInSpreadsheet)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 제공하여 웹 브라우저에서 직접 REST 상호작용을 용이하게 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예제는 cURL로 클라우드 API에 호출을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/worksheet/move?sheetName=Sheet1&destIndex=0" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -F "Spreadsheet=@/path/to/input.xlsx"
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

SDK를 사용하면 낮은 수준의 세부 사항을 추상화해 간결한 코드로 스프레드시트의 워크시트를 이동할 수 있어 개발 속도가 가장 빠릅니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.  
다음 코드 예제는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MoveWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MoveWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MoveWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MoveWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MoveWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MoveWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MoveWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MoveWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}