---
title: "Aspose.Cells Cloud Excel 워크시트 삭제 웹 API - 워크북에서 시트를 프로그래밍 방식으로 제거하기"
second_title: "문서"
ArticleTitle: "Excel에서 워크시트를 삭제하는 방법 - 워크북에서 시트 제거하기"
linktype: "워크시트 삭제"
type: docs
url: /delete-worksheet-from-spreadsheet/
keywords: "Aspose Cells, 워크시트 삭제 API, Excel 시트 제거, 클라우드 스프레드시트, REST API"
description: "Aspose.Cells Cloud API를 사용하여 Excel 파일에서 워크시트를 삭제하는 방법을 알아보세요. 엔드포인트, 매개변수, 샘플 cURL 및 SDK 예제가 포함됩니다."
weight: 100
---

Aspose.Cells Cloud API를 사용하여 Excel 워크북에서 워크시트를 프로그래밍 방식으로 삭제합니다. 단일 또는 여러 시트를 안전하게 제거하고, 워크북 구조를 정리하며, 스프레드시트 최적화를 자동화하세요. 엔터프라이즈급 Excel 관리 및 문서 처리 워크플로우를 위한 RESTful API입니다.

## 스프레드시트에서 워크시트 삭제 API

### 웹 API

```http
PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/delete/worksheet?sheetName={sheetName}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}"
```

### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수:

| 매개변수 이름     | 유형     | 위치     | 설명                                                                                                                                                                                                 |
| :---------------- | :------- | :------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet       | 파일     | FormData | **필수.** 워크시트를 제거할 원본 Excel 워크북 파일(.xlsx, .xls 등).                                                                                                                                |
| sheetName         | 문자열   | 쿼리     | **필수.** 삭제할 워크시트의 정확한 이름(예: `Sheet1`, `TemporaryData`).                                                                                                                             |
| outPath           | 문자열   | 쿼리     | **선택 사항.** 수정된 워크북을 저장할 클라우드 스토리지의 대상 폴더 경로. 생략하거나 `null`인 경우, 워크북은 원본 파일과 동일한 위치 또는 기본 경로에 저장됩니다.                                 |
| outStorageName    | 문자열   | 쿼리     | **선택 사항.** 출력 파일을 쓸 클라우드 스토리지 서비스의 식별자(예: `ProjectStorage`). 지정하지 않으면 기본 스토리지가 사용됩니다.                                                                      |
| region            | 문자열   | 쿼리     | **선택 사항.** 저장 작업 중 지역별 수식 또는 데이터에 영향을 줄 수 있는 로케일 설정(예: `it-IT`).                                                                                                   |
| password          | 문자열   | 쿼리     | **선택 사항.** 암호 보호 스프레드시트를 열고 수정하는 데 필요한 암호. 파일이 암호화되지 않은 경우 생략하세요.                                                                                       |

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

| 코드 | 의미                  | 설명                                                             |
| ---- | --------------------- | ---------------------------------------------------------------- |
| 200  | OK(성공)              | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보가 포함됨.         |
| 400  | 잘못된 요청           | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식).           |
| 401  | 인증되지 않음         | 잘못되거나 누락된 JWT 토큰.                                        |
| 413  | 페이로드가 너무 큼    | 업로드된 파일이 크기 제한을 초과함.                                |
| 500  | 내부 서버 오류        | 예기치 않은 서버 오류.                                             |

## 스프레드시트에서 워크시트 삭제 API는 어디에 사용해야 하나요?

- **자동 보고서 후처리** – 최종 재무 보고서를 생성한 후, 일시 계산에 사용된 중간 워크시트를 자동으로 삭제하여 최종 파일을 깔끔하고 전문적으로 유지합니다.
- **템플릿 파일의 동적 정리** – 사용자가 템플릿에서 맞춤 문서(예: 견적서)를 생성할 때, 선택되지 않은 옵션 페이지를 삭제합니다.
- **워크플로우 보관 최적화** – 프로젝트 또는 감사가 완료된 후, 초안 또는 협업 워크시트를 제거하고, 보관 및 규정 준수를 위해 최종 버전만 유지합니다.

## 왜 스프레드시트에서 워크시트 삭제 API를 사용해야 하나요?

- **개발자 친화적** – Aspose.Cells Cloud는 여러 언어의 SDK 라이브러리를 제공하여 빠른 개발을 가능하게 하며, 포괄적인 문서를 제공합니다.
- **노력 비용 절감** – 수동으로 문서를 통합할 전담 인력을 배치할 필요가 없습니다.
- **사용량 과금** – 사전 투자 없이 실제로 사용한 API 호출에만 비용을 지불합니다.
- **유지보수 비용 없음** – 유지 관리할 서버 없음, 소프트웨어 업데이트 없음, 호환성 문제 없음.

## SDK를 사용하여 스프레드시트에서 워크시트 삭제 API 사용하기

### 스프레드시트에서 워크시트 삭제 API 사양

<a href="https://reference.aspose.cloud/cells/#/ManagementController/DeleteWorksheetFromSpreadsheet" rel="noopener noreferrer">스프레드시트에서 워크시트 삭제 API 사양</a>은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하여, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API에 호출을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/delete/worksheet?sheetName=Sheet1" \
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

SDK를 사용하면 저수준 세부 정보를 추상화하여 최소한의 코드로 워크시트를 삭제할 수 있으므로 개발 속도가 가장 빠릅니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}