---
title: "Excel 파일에서 이미지 업데이트하기"
second_title: "문서"
linktype: "업데이트"
type: docs
url: /pictures/update/
aliases: [/update-a-specific-picture-from-excel-workshee/]
keywords: "Aspose.Cells Cloud, Excel, 이미지 업데이트, REST API, SDK"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트의 이미지를 업데이트하는 방법을 알아보세요. 요청 세부 정보, cURL 예제, 여러 언어의 SDK 스니펫이 포함되어 있습니다."
ArticleTitle: "Aspose.Cells Cloud REST API를 사용하여 Excel 파일의 이미지 업데이트하기"
weight: 70
---

이 REST API는 지정된 인덱스로 식별되는 Excel 워크시트의 이미지를 업데이트합니다.

**필수 조건:** 유효한 Aspose Cloud JWT 토큰, Aspose Cloud 저장소에 저장된 대상 Excel 파일, API 버전 3.0 이상을 사용해야 합니다.

## PostWorksheetPicture API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/{pictureIndex}
```

### **보안 및 인증**

Aspose.Cells Cloud API는 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **요청 파라미터**

| 파라미터 이름 | 유형    | 위치 | 설명                                                      |
| ------------- | ------- | ---- | --------------------------------------------------------- |
| name          | string  | path | Excel 문서의 이름입니다.                                  |
| sheetName     | string  | path | 이미지를 포함하는 워크시트의 이름입니다.                  |
| pictureIndex  | integer | path | 업데이트할 이미지의 0부터 시작하는 인덱스입니다.          |
| picture       | object  | body | 업데이트할 이미지 속성을 설명하는 JSON 객체입니다.        |
| folder        | string  | query | 문서가 저장된 폴더입니다.                                |
| storageName   | string  | query | 저장소 서비스의 이름입니다.                              |

**참고:** 이미지 인덱스는 0부터 시작합니다. 지원되는 이미지 형식은 JPEG, PNG, BMP, GIF입니다. 최대 이미지 크기는 10MB입니다.

### 오류 응답

| HTTP 코드 | 설명                                                   |
| --------- | ------------------------------------------------------ |
| 401       | 인증되지 않음 – 토큰이 누락되었거나 유효하지 않습니다.   |
| 404       | 찾을 수 없음 – 지정된 파일, 워크시트 또는 이미지 인덱스가 존재하지 않습니다. |
| 400       | 잘못된 요청 – 요청 문법이 잘못되었거나 파라미터가 유효하지 않습니다. |
| 500       | 내부 서버 오류 – 예기치 않은 조건이 발생했습니다.      |

<a href="https://apireference.aspose.cloud/cells/#/Pictures/PostWorksheetPicture" rel="noopener noreferrer">OpenAPI 사양</a>은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API에 요청하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures/1" \
-X POST \
-d "{ \"UpperLeftRow\": 10, \"Top\": 0, \"UpperLeftColumn\": 1, \"Left\": 0, \"LowerRightRow\": 0, \"Bottom\": 0, \"LowerRightColumn\": 3, \"ImageFormat\": \"jpg\", \"SourceFullName\": \"download.jpg\"}" \
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

{{< /tab >}}

{{< /tabs >}}

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 가장 빠른 개발 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetPicture.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetPicture.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetPicture.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetPicture.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetPicture.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetPicture.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetPicture.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetPicture.go" >}}

{{< /tab >}}

{{< /tabs >}}

*참고:* 이미지 추가, 이미지 삭제, 이미지 가져오기, 이미지 지우기 – Aspose.Cells Cloud API의 다른 이미지 관련 작업.