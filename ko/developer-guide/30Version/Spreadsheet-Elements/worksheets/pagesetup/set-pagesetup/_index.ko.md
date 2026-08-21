---
title: "워크시트에 페이지 설정 설정하기"
second_title: "Document"
linktitle: "페이지 설정 설정하기"
type: docs
url: /ko/set-page-setup/
keywords: "Aspose.Cells, Excel, 페이지 설정, REST API, 워크시트, 클라우드 SDK"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트의 페이지 설정을 설정하는 방법을 배워보세요. 요청 세부 정보, 보안이 강화된 HTTPS cURL 예제, 응답 상태 코드 및 여러 프로그래밍 언어의 SDK 코드 스니펫이 포함되어 있습니다."
weight: 20
ArticleTitle: "워크시트에 페이지 설정 설정하기 – Aspose.Cells Cloud API 가이드"
---

사전 요구 사항: 이 API를 호출하려면 유효한 JWT(OAuth) 토큰이 필요하며, 워크북이 Aspose Cloud 저장소 위치에 있어야 하며, 해당 위치에 대해 읽기/쓰기 권한이 있어야 합니다. 토큰이 **Authorization** 헤더에 포함되어 있고, 계정에 필요한 API 할당량이 있는지 확인하세요.

이 REST API는 Excel 워크시트의 페이지 설정을 설정합니다.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pagesetup
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 강화되어 있으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **요청 매개변수**

| 매개변수 이름 | 유형   | 위치 | 설명                 |
| ------------- | ------ | ---- | --------------------- |
| name          | string | path | 문서 이름.            |
| sheetName     | string | path | 워크시트 이름.        |
| pageSetup     | object | body | 페이지 설정 설명.     |
| folder        | string | query | 문서 폴더.           |
| storageName   | string | query | 저장소 이름.         |

**`pageSetup` 객체의 예제 JSON 페이로드**

```json
{
  "pageSetup": {
    "orientation": "Portrait",
    "paperSize": "A4",
    "fitToPagesTall": 1,
    "fitToPagesWide": 1,
    "centerHorizontally": true,
    "centerVertically": false
  }
}
```

<a href="https://reference.aspose.cloud/cells/#/PageSetup/PostPageSetup" target="_blank" rel="noopener noreferrer">OpenAPI 사양</a>은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API에 호출을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Tasks/pagesetup" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{
  "pageSetup": {
    "orientation": "Portrait",
    "paperSize": "A4",
    "fitToPagesTall": 1,
    "fitToPagesWide": 1,
    "centerHorizontally": true,
    "centerVertically": false
  }
}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

API는 작업 결과를 나타내는 JSON 객체를 반환합니다:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**가능한 응답 상태 코드**

| 코드 | 의미                       | 발생 시기                                         |
|------|----------------------------|--------------------------------------------------|
| 200  | OK                         | 성공적인 페이지 설정 업데이트                      |
| 400  | Bad Request                | 잘못된 JSON 페이로드 또는 필수 필드 누락          |
| 401  | Unauthorized               | 누락되거나 유효하지 않은 JWT 토큰                 |
| 404  | Not Found                  | 워크북 또는 워크시트 이름이 존재하지 않음         |
| 500  | Internal Server Error      | 예기치 않은 서버 오류                             |

## 클라우드 SDK 패밀리

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 호출을 수행하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostPageSetup.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostPageSetup.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostPageSetup.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostPageSetup.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostPageSetup.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostPageSetup.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostPageSetup.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostPageSetup.go" >}}

{{< /tab >}}

{{< /tabs >}}