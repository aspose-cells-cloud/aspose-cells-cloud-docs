---
title: "Excel 워크시트에서 셀 병합 해제하기"
type: docs
url: /ko/unmerge-cells-in-excel-worksheet/
weight: 120
keywords: "Aspose.Cells, Excel, 셀 병합 해제, REST API, 클라우드 SDK"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트에서 셀 병합을 해제하는 방법에 대해 알아보세요. 요청 예시, 응답 형식 및 여러 프로그래밍 언어의 SDK 코드 샘플을 제공합니다."
ArticleTitle: "Excel 워크시트에서 셀 병합 해제하기"
---

이 REST API는 Excel 파일 내 셀의 병합을 해제합니다.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/unmerge
```

## 보안 및 인증

Aspose.Cells Cloud API는 안전하며 [JWT 토큰 기반 인증](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)이 필요합니다.


**요청 매개변수**

| 매개변수 이름 | 유형    | 위치 | 설명                                             |
|---------------|---------|------|--------------------------------------------------|
| name          | string  | path | 워크북 파일 이름.                                |
| sheetName     | string  | path | 워크시트 이름.                                   |
| startRow      | integer | query| 병합 해제를 시작할 첫 번째 행의 0 기반 인덱스.     |
| startColumn   | integer | query| 병합 해제를 시작할 첫 번째 열의 0 기반 인덱스.    |
| totalRows     | integer | query| 병합 해제 작업에 포함할 행 수.                    |
| totalColumns  | integer | query| 병합 해제 작업에 포함할 열 수.                    |
| folder        | string  | query| 워크북이 저장된 폴더 경로.                        |
| storageName   | string  | query| 스토리지 서비스 이름.                             |

## **응답**

CellCloudResponse를 반환합니다.

- **응답 필드 개요**

| 필드           | 유형    | 설명                                           |
| --------------- | ------- | ----------------------------------------------------- |
| `Status`          | string  |                                                    |
| `Code`           | integer | 200, 400, 401, 500,...                              |


```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP 상태 코드**

| 코드 | 의미                     | 설명                                      |
|------|--------------------------|-------------------------------------------|
| 200  | OK                       | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함. |
| 400  | Bad Request              | 누락되었거나 유효하지 않은 매개변수(예: 지원되지 않는 파일 유형). |
| 401  | Unauthorized             | 유효하지 않거나 누락된 JWT 토큰. |
| 413  | Payload Too Large        | 업로드된 파일이 크기 제한을 초과함. |
| 500  | Internal Server Error    | 예기치 않은 서버 오류. |
## SDK를 사용하여 PostWorksheetUnmerge API 사용하는 방법

### PostWorksheetUnmerge API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetUnmerge)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예시는 cURL을 사용하여 클라우드 API에 호출을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/unmerge?startRow=10&startColumn=10&totalRows=10&totalColumns=10" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt 토큰>"
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

### Aspose.Cells Cloud SDK 사용하기

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 처리해주므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예시는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 호출을 수행하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetUnmerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetUnmerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetUnmerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetUnmerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetUnmerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetUnmerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetUnmerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetUnmerge.go" >}}

{{< /tab >}}

{{< /tabs >}}