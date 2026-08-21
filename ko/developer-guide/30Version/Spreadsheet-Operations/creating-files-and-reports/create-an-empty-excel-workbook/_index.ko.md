---
title: "빈 Excel 워크시트 만들기"
second_title: "문서"
linktitle: "빈 워크시트"
type: docs
url: /ko/create-an-empty-excel-file/
aliases:
  [
    "/create-an-empty-excel-workbook/",
    "/workbook/new/",
    "/workbook/create/empty-workbook/",
  ]
keywords: "Aspose.Cells, 클라우드, Excel, 빈 워크시트, REST API, SDK"
description: "Aspose.Cells Cloud REST API를 사용하여 빈 Excel 워크시트를 만드는 방법을 알아보세요. cURL 및 SDK 예제가 포함되어 있습니다."
weight: 20
ArticleTitle: "Aspose.Cells Cloud API를 사용하여 빈 Excel 워크시트 만들기"
---

이 REST API는 **빈 워크시트**를 생성합니다.

## PutWorkbookCreate API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}
```

### **보안 및 인증**

Aspose.Cells Cloud API는 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 쿼리 매개변수

| 매개변수 이름 | 유형    | 설명                                                  |
| ------------- | ------- | ----------------------------------------------------- |
| templateFile  | string  | 기본으로 사용할 템플릿 워크시트 파일의 경로 (선택 사항).    |
| dataFile      | string  | 워크시트를 채우기 위한 데이터 파일의 경로 (선택 사항).      |
| isWriteOver   | boolean | `true`인 경우 기존 파일을 덮어쓰고, `false`인 경우 덮어쓰지 않습니다. |
| folder        | string  | 생성된 워크시트를 저장할 폴더 경로 (선택 사항).            |
| storageName   | string  | 사용할 스토리지 서비스 이름입니다.                         |

### 요청 본문 매개변수

| 매개변수 이름 | 유형 | 설명                                 |
| ------------- | ---- | ------------------------------------ |
| data          | file | 생성할 워크시트 파일의 이진 콘텐츠입니다. |

### **응답**

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```

**HTTP 상태 코드**

| 코드 | 의미                         | 반환 시점                                  |
|------|------------------------------|-------------------------------------------|
| 200 OK | 워크시트가 성공적으로 생성되었습니다. | 정상적인 흐름                              |
| 201 Created | 워크시트가 생성되었습니다 (대체 응답). | API가 생성 상태를 반환할 때              |
| 400 Bad Request | 잘못된 매개변수 | 클라이언트 측 오류                        |
| 401 Unauthorized | 토큰 누락 또는 잘못된 토큰 | 인증 오류                                 |
| 409 Conflict | 파일이 존재하고 `isWriteOver=false`인 경우 | 기존 파일과 충돌 시                       |

## SDK를 사용하여 PutWorkbookCreate API 사용하기

### PutWorkbookCreate API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookCreate)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

**cURL** 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 액세스할 수 있습니다. 유효한 OAuth2/JWT 액세스 토큰을 포함한 `Authorization` 헤더를 포함해야 합니다. 빈 워크시트의 경우 요청 본문은 선택 사항입니다. 파일을 업로드해야 하는 경우 아래와 같이 `--data-binary @empty.xlsx`를 추가하세요.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
# newworkbook.xlsx라는 빈 워크시트 생성
curl -X PUT "https://api.aspose.cloud/v3.0/cells/newworkbook.xlsx?isWriteOver=false" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>" \
     --data-binary @empty.xlsx   # 완전히 빈 워크시트의 경우 이 줄을 생략하세요
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

### Aspose.Cells Cloud SDK 사용하기

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 작업에 집중할 수 있게 해줍니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookCreateEmpty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookCreateEmpty.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookCreateEmpty.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookCreateEmpty.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookCreateEmpty.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookCreateEmpty.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookCreateEmpty.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookCreateEmpty.go" >}}

{{< /tab >}}

{{< /tabs >}}