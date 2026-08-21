---
title: "Excel 워크시트에서 모든 그림 가져오기"
second_title: "문서"
linktitle: "모두 가져오기"
type: docs
url: /pictures/get-all/
aliases: [/get-picture-from-a-worksheet/]
keywords: "Aspose.Cells Cloud, Excel 워크시트, 그림 API, 모든 그림 가져오기, REST API, SDK"
description: "Aspose.Cells Cloud REST API를 통해 Excel 워크시트에서 모든 그림 객체를 검색합니다."
ArticleTitle: "Excel 워크시트에서 모든 그림 가져오기 - Aspose.Cells Cloud API"
weight: 10
---

이 REST API는 Excel 워크시트에서 모든 그림 정보를 검색합니다.

**사전 요구 사항**  
이 엔드포인트를 호출하기 전에 다음 사항을 확인하세요:

- 유효한 Aspose Cloud JWT 액세스 토큰이 있어야 합니다.  
- 대상 Excel 파일이 선택한 스토리지에 업로드되어 있어야 합니다.  
- 사용자 정의 스토리지를 사용하는 경우 올바른 스토리지 이름이 필요합니다.  
- 그림이 포함된 워크시트 이름이 필요합니다.

## GetWorksheetPictures API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures
```

**참고:** API를 호출할 때 HTTPS(TLS 1.2 이상)를 사용하고, `Authorization` 헤더에 유효한 JWT 토큰을 포함해야 합니다.

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 강화되어 있으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **요청 매개변수**

| 매개변수 이름 | 유형   | 위치 | 설명                                      |
| ------------- | ------ | ---- | ----------------------------------------- |
| name          | string | path | Excel 파일의 이름입니다.                   |
| sheetName     | string | path | 그림이 포함된 워크시트의 이름입니다.      |
| folder        | string | query | 파일이 저장된 폴더 경로입니다.           |
| storageName   | string | query | 스토리지 서비스의 이름입니다.             |

### 오류 응답

| HTTP 코드 | 설명                                                                      |
| --------- | ------------------------------------------------------------------------- |
| 401       | 인증되지 않음 – 토큰이 누락되었거나 유효하지 않습니다.                      |
| 404       | 찾을 수 없음 – 지정된 파일, 워크시트 또는 페이지 나누기 인덱스가 존재하지 않습니다. |
| 400       | 잘못된 요청 – 요청 구문이 잘못되었거나 매개변수가 유효하지 않습니다.        |
| 500       | 내부 서버 오류 – 예기치 않은 조건이 발생했습니다.                         |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Pictures/GetWorksheetPictures)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예시는 cURL을 사용해 Cloud API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Pictures": {
    "PictureList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/1",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/2",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      }
    ],
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet2/pictures",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**성공 응답** – 성공적인 호출은 HTTP 200 상태 코드와 각 그림의 리소스 링크 목록을 포함하는 `Pictures` 객체를 포함한 JSON 페이로드를 반환합니다.

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예시는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스에 요청을 보내는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetPictureWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetPictureWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetPictureWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetPictureWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetPictureWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetPictureWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetPictureWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetPictureWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}

SDK는 각각의 패키지 관리자(NuGet(.NET), Maven Central(Java), Composer(PHP), npm(Node.js), PyPI(Python), CPAN(Perl), Go modules(Go))에서 직접 다운로드할 수 있습니다.

*참고:* 그림 추가, 그림 삭제, 그림 속성 업데이트.