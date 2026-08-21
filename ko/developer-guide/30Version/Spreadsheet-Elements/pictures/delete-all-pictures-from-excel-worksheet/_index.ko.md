---
title: "Excel 워크시트에서 모든 그림 삭제하기"
second_title: "문서"
linktype: "지우기"
type: docs
url: /ko/pictures/clear/
aliases: [  /ko/delete-all-pictures-from-excel-worksheet/ ]
keywords: "Aspose.Cells Cloud, Excel, 모든 그림 삭제, 워크시트, REST API, 그림 지우기"
description: "Aspose.Cells Cloud REST API를 사용하여 cURL 및 SDK 예제로 Excel 워크시트에서 모든 그림을 삭제하는 방법을 알아보세요."
weight: 60
ArticleTitle: "Aspose.Cells Cloud로 Excel 워크시트에서 모든 그림을 삭제하는 방법"
---

이 REST API는 워크시트의 **모든** 그림을 삭제합니다.

**필수 조건**  
- 유효한 OAuth 2.0 액세스 토큰이 있는 활성화된 Aspose.Cells Cloud 계정  
- API 버전 3.0 이상이 필요합니다. 이전 버전은 사용 중단되었습니다.  
- 대상 Excel 파일은 지원되는 저장소 위치(기본 또는 사용자 정의)에 저장되어 있어야 합니다.

**버전 호환성**  
이 엔드포인트는 Cells Cloud 3.0 API 사양을 따릅니다. 클라이언트 라이브러리 및 요청 URL이 `api.aspose.cloud/v3.0`을 대상으로 하는지 확인하세요.

## DeleteWorksheetPictures API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 위해 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>을 요구합니다.

### **요청 매개변수**

| 매개변수 이름 | 유형   | 위치 | 설명                                    |
| ------------- | ------ | ---- | --------------------------------------- |
| name          | string | Path | Excel 파일 이름입니다.                  |
| sheetName     | string | Path | 그림이 포함된 워크시트 이름입니다.      |
| folder        | string | Query | 파일이 저장된 폴더입니다.               |
| storageName   | string | Query | 저장소 서비스 이름입니다.               |

### 오류 응답

| HTTP 코드 | 설명                                                         |
| --------- | ------------------------------------------------------------ |
| 401       | 인증되지 않음 – 토큰이 누락되었거나 유효하지 않습니다.        |
| 404       | 찾을 수 없음 – 지정된 파일, 워크시트 또는 페이지 분할 인덱스가 존재하지 않습니다. |
| 400       | 잘못된 요청 – 요청 구문이 잘못되었거나 매개변수가 유효하지 않습니다. |
| 500       | 내부 서버 오류 – 예기치 않은 조건이 발생했습니다.           |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Pictures/DeleteWorksheetPictures)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/pictures" \
  -X DELETE \
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

SDK를 사용하는 것이 개발 속도를 높이는 가장 빠른 방법입니다. SDK가 저수준 세부 사항을 처리해주므로 비즈니스 로직에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetPictures.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetPictures.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetPictures.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetPictures.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetPictures.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetPictures.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetPictures.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetPictures.go" >}}

{{< /tab >}}

{{< /tabs >}}

**참고:** DELETE 작업은 페이징을 지원하지 않으며, 표준 Aspose.Cells Cloud API 속도 제한(기본값: 분당 100 요청)의 적용을 받습니다. 클라이언트 로직을 적절히 조정하세요.

**참고 자료**:  
- [/pictures/delete/](../delete/) – 워크시트에서 특정 그림 삭제  
- [/pictures/add/](../add/) – 워크시트에 그림 추가  
---