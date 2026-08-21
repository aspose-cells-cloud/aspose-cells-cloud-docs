---
title: "Excel 워크북에서 이름 가져오기"
second_title: "문서"
linktitle: "이름"
type: docs
url: /get-names-from-an-excel-file/
aliases:
  [
    /get-names-count-from-excel-workbooks/,
    /workbook/names/,
    /workbook/get/names/,
  ]
keywords: "Aspose.Cells, 클라우드, Excel, 워크북, 이름, REST API, SDK"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크북에서 정의된 모든 이름을 검색합니다. 인증 가이던스, cURL 예제, 응답 스키마, 오류 처리 및 SDK 샘플이 포함됩니다."
weight: 120
ArticleTitle: "Excel 워크북에서 이름 가져오기 – Aspose.Cells Cloud API"
---

이 REST API는 Excel 워크북에서 정의된 이름을 검색합니다.

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 위해 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

## GetWorkbookNames API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/names
```

요청 매개변수는 다음과 같습니다:

| 매개변수 이름 | 유형   | 위치 | 설명                                      |
| ------------- | ------ | ---- | ----------------------------------------- |
| name          | string | path | 워크북 파일 이름입니다.                   |
| folder        | string | query| 워크북이 포함된 폴더입니다.              |
| storageName   | string | query| 사용할 저장소 이름입니다.                |

요청에는 다음 HTTP 헤더가 포함되어야 합니다:

| 헤더          | 유형   | 설명                                        |
|---------------|--------|---------------------------------------------|
| Authorization | string | Bearer JWT 토큰 (필수)                      |
| Accept        | string | `application/json`                          |
| Content-Type  | string | `application/json` (본문이 있는 요청의 경우) |

**인증** – 이 API는 OAuth2/JWT 베어러 토큰을 요구합니다. 클라이언트 ID와 클라이언트 시크릿을 사용하여 `https://api.aspose.cloud/connect/token`에서 토큰을 획득한 후, 모든 요청에 `Authorization: Bearer <jwt token>` 헤더를 포함해야 합니다.

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkbookNames)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 액세스할 수 있습니다. 아래 예제는 cURL을 사용하여 Aspose.Cells Cloud API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/names" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "Names": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "Count": 0,
    "NameList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        }
      }
    ]
  }
}
```

_응답 필드_

- **Status** _(string)_ – 작업 상태 메시지입니다.
- **Names.link** _(object)_ – 컬렉션의 하이퍼링크 정보입니다.
- **Names.Count** _(integer)_ – 반환된 정의된 이름의 총 개수입니다.
- **Names.NameList** _(array)_ – 이름 객체의 목록입니다. 각 객체는 탐색 세부 정보를 포함하는 **link** 객체를 포함합니다.

**오류 처리** – 서비스는 다음 HTTP 상태 코드를 반환할 수 있습니다:

| 코드 | 의미                  | 권장 조치                                                    |
| ---- | --------------------- | ------------------------------------------------------------ |
| 401  | 인증되지 않음         | 유효한 JWT 토큰이 제공되었는지 확인하세요.                     |
| 404  | 찾을 수 없음          | 워크북 이름, 폴더, 저장소가 올바른지 확인하세요.             |
| 500  | 내부 서버 오류        | 문제가 지속될 경우 나중에 다시 시도하거나 Aspose 지원팀에 문의하세요. |

{{< /tab >}}

{{< /tabs >}}

## 클라우드 SDK 패밀리

SDK를 사용하면 개발 속도가 가장 빠릅니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbookNames.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbookNames.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbookNames.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbookNames.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbookNames.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbookNames.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbookNames.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbookNames.go" >}}

{{< /tab >}}

{{< /tabs >}}
---