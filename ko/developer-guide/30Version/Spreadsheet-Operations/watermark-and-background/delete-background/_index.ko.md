---
title: "Excel 워크북에서 배경 제거하기"
second_title: "문서"
linktitle: "삭제"
type: docs
url: /ko/delete-background-in-excel-file/
aliases:
  - /delete-background-in-workbook/
  - /workbook/delete-background/
  - /workbook/background/delete/
keywords: "Aspose Cells 배경 삭제, Excel API 배경 삭제, Aspose.Cells Cloud, DELETE /cells background"
description: "Aspose.Cells Cloud API를 사용하여 Excel 워크북에서 배경 이미지를 제거합니다. DELETE 엔드포인트, 필요한 매개변수, cURL 예제, C#, Java, Python 등 다양한 언어의 SDK 코드를 알아보세요."
weight: 170
ArticleTitle: "Aspose.Cells Cloud API를 사용하여 Excel 워크북에서 배경 이미지 삭제하기"
---

이 REST API는 Excel 워크북의 배경 이미지를 삭제합니다.

## DeleteWorkbookBackground API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/background
```

### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **쿼리 매개변수**

| 매개변수 이름 | 유형   | 설명                                      | 필수 여부 |
| ------------- | ------ | ----------------------------------------- | -------- |
| folder        | string | 원본 워크북이 포함된 폴더입니다.          | 아니요     |
| storageName   | string | 사용할 스토리지 서비스의 이름입니다.      | 아니요     |

### **응답**

```json
{
    "Status" : "OK",
    "Code" : 200
}
```

**HTTP 상태 코드**

| 코드 | 의미                      | 설명                                                |
|------|---------------------------|-----------------------------------------------------|
| 200  | OK                        | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함 |
| 400  | Bad Request               | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형) |
| 401  | Unauthorized              | 잘못되거나 누락된 JWT 토큰                            |
| 413  | Payload Too Large         | 업로드된 파일이 크기 제한을 초과함                    |
| 500  | Internal Server Error     | 예기치 않은 서버 오류                                 |

## SDK를 사용하여 DeleteWorkbookBackground API 사용하는 방법

### DeleteWorkbookBackground API 사양

<a href="https://apireference.aspose.cloud/cells/#/Workbook/DeleteWorkbookBackground" target="_blank" rel="noopener noreferrer">OpenAPI 사양</a>은 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의합니다.

**cURL** 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 필요한 인증 헤더를 포함한 전체 DELETE 요청을 보여주며, 요청 본문은 필요하지 않습니다.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/{name}/background?folder=DotnetFiles" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -H "x-aspose-client: Containerize.Swagger"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4"
   tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby"
   tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}