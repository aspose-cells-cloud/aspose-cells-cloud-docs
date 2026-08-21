---
title: "워크시트 셀 주석 업데이트"
type: docs
url: /ko/comments/update/
aliases: [  /ko/update-a-comment-in-excel-workbook/ ]
keywords: "Aspose.Cells Cloud, REST API, Excel, 워크시트, 셀 주석, 워크시트 주석 업데이트, comment object"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크북의 셀에 대한 워크시트 주석을 업데이트합니다. 요청 세부 정보, 응답 코드, SDK 예제를 포함합니다."
weight: 30
ArticleTitle: "워크시트 셀 주석 업데이트 – Aspose.Cells Cloud API"
---

이 REST API는 워크시트 셀의 주석을 업데이트합니다. 이 엔드포인트를 사용하여 Excel 파일의 **워크시트 주석을 업데이트**할 수 있습니다.

**사전 조건:**  
- `Authorization` 헤더에 유효한 OAuth/JWT 액세스 토큰을 포함해야 합니다.  
- 워크북은 지원되는 클라우드 스토리지 위치에 저장되어 있어야 합니다(`folder` 및 선택적으로 `storageName` 지정).

## PostWorksheetComment API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 갖춰져 있으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름 | 유형   | 위치 | 설명                                                                 |
| ------------- | ------ | ---- | ------------------------------------------------------------------- |
| name          | string | path | Excel 문서의 이름.                                                  |
| sheetName     | string | path | 셀을 포함하는 워크시트의 이름.                                      |
| cellName      | string | path | 셀의 주소(예: **A1**).                                               |
| comment       | object | body | 추가 또는 업데이트할 주석을 정의하는 **Comment** 객체.              |
| folder        | string | query | 문서가 저장된 폴더.                                                 |
| storageName   | string | query | 스토리지 서비스의 이름.                                             |

[OpenAPI 사양서](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetComment)는 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

**cURL** 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용해 클라우드 API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/a1" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "CellName": "a1",
        "Author": "test",
        "HtmlNote": "string",
        "Note": "this is a comment",
        "AutoSize": true,
        "IsVisible": true,
        "Width": 10,
        "Height": 10
      }'
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

가능한 응답 상태 코드:

| 코드 | 설명                                                         |
|------|--------------------------------------------------------------|
| 200  | 주석이 성공적으로 업데이트되었습니다.                        |
| 400  | 잘못된 요청 – 매개변수 누락 또는 유효하지 않음.              |
| 401  | 인증 실패 – 인증되지 않음.                                   |
| 404  | 찾을 수 없음 – 워크북, 워크시트 또는 주석이 존재하지 않음.   |
| 500  | 내부 서버 오류.                                              |

**참고 / 팁:**  
- 주석 최대 길이는 1024자입니다.  
- 지원되는 문자는 UTF-8이며, 제어 문자는 사용을 피하세요.  

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 Aspose.Cells Cloud와 개발을 진행하는 가장 빠른 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 개발에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetComment.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetComment.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetComment.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetComment.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetComment.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetComment.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetComment.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetComment.go" >}}

{{< /tab >}}

{{< /tabs >}}

관련 작업:  
- [워크시트 주석 조회](/comments/get/)  
- [워크시트 주석 추가](/comments/add/)  
- [워크시트 주석 삭제](/comments/delete/)