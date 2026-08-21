---
title: "Excel 워크시트에서 행 그룹화"
second_title: "문서"
linktype: "그룹"
type: docs
url: /rows/group/
aliases: [/group-rows-in-excel-worksheet/]
keywords: "행 그룹화, Excel, Aspose.Cells Cloud, REST API, SDK, 워크시트, Excel API"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트에서 행을 그룹화합니다. 다양한 SDK(C#, Java, PHP, Ruby, Node.js, Python, Perl, Go)를 지원하여 손쉽게 통합할 수 있습니다."
weight: 60
ArticleTitle: "Aspose.Cells Cloud API를 사용하여 Excel 워크시트에서 행 그룹화하기"
---

이 REST API는 Excel 워크시트의 행을 그룹화합니다.

**필수 조건:**  
- `Authorization` 헤더에 유효한 OAuth 2.0 액세스 토큰(Bearer JWT)을 제공해야 합니다.  
- 요청을 보내기 전에 워크북이 선택된 `storageName`(또는 기본 저장소)의 지정된 `folder`에 이미 존재해야 합니다.

## PostGroupWorksheetRows API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/group
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 강화되어 있으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **요청 매개변수**

| 매개변수 이름 | 유형    | 위치 | 설명                                                         |
| ------------- | ------- | ---- | ------------------------------------------------------------ |
| name          | string  | path | 워크북 파일 이름입니다.                                      |
| sheetName     | string  | path | 워크시트 이름입니다.                                         |
| firstIndex    | integer | query | 그룹화할 첫 번째 행의 0부터 시작하는 인덱스입니다.          |
| lastIndex     | integer | query | 그룹화할 마지막 행의 0부터 시작하는 인덱스입니다.           |
| hide          | boolean | query | 그룹화된 행을 숨길지 여부를 나타냅니다(`true` 또는 `false`). |
| folder        | string  | query | 워크북이 포함된 폴더 경로입니다.                            |
| storageName   | string  | query | 워크북이 위치한 저장소 이름입니다.                          |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Cells/PostGroupWorksheetRows)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 아래 예제는 cURL을 사용하여 클라우드 API로 요청하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/group?firstIndex=1&lastIndex=2&hide=true" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**HTTP 상태 코드**

| 코드 | 의미              | 설명                                                           |
|------|-------------------|----------------------------------------------------------------|
| 200  | OK                | 필터가 성공적으로 적용되었으며, 응답에 작업 세부 정보가 포함됩니다. |
| 400  | Bad Request       | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식).        |
| 401  | Unauthorized      | 잘못되거나 누락된 JWT 토큰.                                     |
| 413  | Payload Too Large | 업로드된 파일이 크기 제한을 초과했습니다.                      |
| 500  | Internal Server Error | 예기치 않은 서버 오류입니다.                                   |

일반적인 오류 응답:

- **400 Bad Request** – `firstIndex`와 `lastIndex`가 유효한 정수인지, 그리고 `firstIndex` ≤ `lastIndex`인지 확인하세요.  
- **401 Unauthorized** – `Authorization` 헤더에 유효한 JWT 토큰이 포함되어 있는지 확인하세요.  
- **404 Not Found** – 지정된 `folder`/`storageName`에 워크북(`name`)과 워크시트(`sheetName`)가 존재하는지 확인하세요.

{{< /tab >}}

{{< /tabs >}}

**참조:** [Excel 워크시트에서 행 그룹 해제](../rows/ungroup/ "Excel 워크시트에서 행 그룹 해제"), [Excel 워크시트에서 행 숨기기](../rows/hide/ "Excel 워크시트에서 행 숨기기"), [Excel 워크시트에서 행 숨김 해제](../rows/unhide/ "Excel 워크시트에서 행 숨김 해제").

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostGroupWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostGroupWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostGroupWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostGroupWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostGroupWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostGroupWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostGroupWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostGroupWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}