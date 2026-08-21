---
title: "Excel ListObject에 슬라이서 삽입하기 – Aspose.Cells Cloud API"
second_title: "문서"
linktitle: "슬라이서 삽입"
type: docs
keywords: "Aspose.Cells, Excel 슬라이서, ListObject, REST API, 클라우드 SDK"
description: "Aspose.Cells Cloud REST API(v3.0)를 사용하여 Excel ListObject에 슬라이서를 추가하는 방법을 알아보세요. 엔드포인트, 파라미터, 인증, 샘플 cURL 요청 및 응답 JSON이 포함됩니다."
weight: 20
ArticleTitle: "Excel ListObject에 슬라이서 삽입하기 – Aspose.Cells Cloud API"
---

이 REST API는 Excel 워크시트의 목록 개체(list object)에 슬라이서를 삽입합니다.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/InsertSlicer
```

### 요청 파라미터

| 파라미터 이름     | 타입     | 위치   | 설명                                                               |
| ---------------- | ------- | ------ | ------------------------------------------------------------------ |
| name             | String  | Path   | Excel 파일의 이름.                                                 |
| sheetName        | String  | Path   | 목록 개체가 포함된 워크시트의 이름.                                |
| listObjectIndex  | Integer | Path   | 슬라이서를 추가할 목록 개체의 0부터 시작하는 인덱스.               |
| columnIndex      | Integer | Query  | 슬라이서 기준이 되는 열의 0부터 시작하는 인덱스.                   |
| destCellName     | String  | Query  | 슬라이서를 배치할 셀 참조(예: **A1**).                             |
| folder           | String  | Query  | Excel 파일이 저장된 스토리지 폴더.                                 |
| storageName      | String  | Query  | Aspose Cloud 스토리지 서비스의 이름.                               |

cURL 명령줄 도구를 사용하여 API를 호출할 수 있습니다:

{{< tabs tabTotal="2" tabID="1" tabName1="요청(Request)" tabName2="응답(Response)" >}}
{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/InsertSlicer" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **참고:** 요청에는 Aspose Cloud 인증 서비스에서 얻은 유효한 JWT 베어러 토큰이 필요합니다. 이 엔드포인트는 요청 본문이 필요하지 않으며, 클라이언트 라이브러리가 페이로드를 요구할 경우 빈 JSON 객체 `{}`를 전송합니다.

{{< /tab >}}
{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Slicer": {
    "Name": "Slicer1",
    "ColumnIndex": 2,
    "Position": "A1"
  }
}
```

> **응답 헤더:** `Content-Type: application/json`

{{< /tab >}}
{{< /tabs >}}

**HTTP 상태 코드**

| 코드 | 의미                    | 설명                                                  |
| ---- | ----------------------- | ----------------------------------------------------- |
| 200  | OK                      | 필터가 성공적으로 적용되었으며, 응답에 작업 세부 정보가 포함됩니다. |
| 400  | Bad Request             | 누락되거나 잘못된 파라미터(예: 지원되지 않는 파일 형식).   |
| 401  | Unauthorized            | 잘못되거나 누락된 JWT 토큰.                             |
| 413  | Payload Too Large       | 업로드된 파일이 크기 제한을 초과했습니다.               |
| 500  | Internal Server Error   | 예기치 않은 서버 오류.                                  |

### 오류 처리

오류가 발생하면 API는 `ErrorMessage` 필드를 포함한 JSON 객체를 반환하며, 여기에는 문제에 대한 설명이 기술되어 있습니다. HTTP 상태 코드와 `ErrorMessage`를 검사하여 적절한 조치를 취할 수 있습니다.

## 클라우드 SDK 패밀리

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 처리해주므로, 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 GitHub 저장소를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectInsertSlicer.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectInsertSlicer.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectInsertSlicer.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectInsertSlicer.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectInsertSlicer.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectInsertSlicer.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectInsertSlicer.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectInsertSlicer.go" >}}
{{< /tab >}}

{{< /tabs >}}