---
title: "Excel 워크시트에서 배경 삭제"
second_title: "문서"
linktitle: "삭제"
type: docs
url: /ko/worksheets/background/delete/
aliases: [/delete-background-or-watermark-of-excel-worksheet/]
keywords: "Aspose.Cells Cloud, 워크시트 배경 삭제, Excel, REST API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트의 배경 이미지를 삭제합니다. C#, Java, PHP, Ruby, Node.js, Python, Perl, Go용 SDK가 제공됩니다."
weight: 210
ArticleTitle: "Aspose.Cells Cloud API를 사용하여 Excel 워크시트에서 배경 삭제"
---

이 REST API는 워크시트의 배경 이미지를 삭제합니다.

**필수 조건:** 워크시트가 Aspose Cloud 저장소에 저장되어 있어야 하며, 인증을 위한 유효한 JWT 액세스 토큰이 필요합니다.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/background
```

### **요청 매개변수**

| 매개변수 이름 | 유형   | 위치 | 설명                                                   |
| ------------- | ------ | ---- | ------------------------------------------------------ |
| name          | string | path | Excel 파일의 이름입니다.                               |
| sheetName     | string | path | 배경이 삭제될 워크시트의 이름입니다.                   |
| folder        | string | query| 파일이 위치한 저장소의 폴더 경로입니다.                |
| storageName   | string | query| 저장소 이름(기본 저장소가 아닌 경우)입니다.            |

[OpenAPI 사양서](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetBackground)는 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 요청을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 모든 요청에는 유효한 JWT 토큰이 필요합니다. 인증 가이드에 설명된 대로 OAuth2 토큰 엔드포인트를 통해 토큰을 획득하세요.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/WorkSheetBackground_Sample_Test_Book.xls/worksheets/Sheet1/background" \
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

**HTTP 상태 코드**

| 코드 | 의미                  | 설명                                           |
|------|-----------------------|------------------------------------------------|
| 200  | OK (성공)             | 필터가 성공적으로 적용되었으며, 응답에 작업 세부 정보가 포함됩니다. |
| 400  | 잘못된 요청           | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형)입니다. |
| 401  | 인증되지 않음         | 유효하지 않거나 누락된 JWT 토큰입니다.         |
| 413  | 요청 페이로드가 너무 큼 | 업로드된 파일이 크기 제한을 초과합니다.        |
| 500  | 내부 서버 오류        | 예기치 않은 서버 오류가 발생했습니다.          |

{{< /tab >}}

{{< /tabs >}}

## 클라우드 SDK 패밀리

SDK를 사용하면 개발 속도를 극대화할 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

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