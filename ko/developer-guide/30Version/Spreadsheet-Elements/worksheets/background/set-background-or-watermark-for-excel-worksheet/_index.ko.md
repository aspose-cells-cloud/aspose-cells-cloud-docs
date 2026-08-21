---
title: "Excel 워크시트에 배경 설정"
ArticleTitle: "Excel 워크시트에 배경 설정 – Aspose.Cells Cloud API 가이드"
second_title: "문서"
linktype: "docs"
url: /ko/worksheets/background/add/
aliases: [  /ko/set-background-or-watermark-for-excel-worksheet/ ]
keywords: "Aspose.Cells, Excel, 워크시트, 배경, REST API, SDK, 이미지 추가"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트에 배경 이미지(PNG, JPEG, BMP)를 추가하는 방법을 알아보세요. 엔드포인트, 필요한 매개변수, 인증 단계, cURL 예제 및 SDK 코드 샘플을 포함합니다."
weight: 180
---

이 REST API는 워크시트에 배경 이미지를 추가합니다.

## 보안 및 인증
Aspose.Cells Cloud API는 보안이 강화되었으며 [JWT 토큰 기반 인증](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)이 필요합니다.

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/background
```

### **요청 매개변수**

| 매개변수 이름 | 유형   | 위치 | 설명                                                    |
| -------------- | ------ | -------- | -------------------------------------------------------------- |
| name           | string | path     | Excel 워크북의 이름입니다.                                    |
| sheetName      | string | path     | 이미지를 적용할 워크시트의 이름입니다.           |
| imageFile      | file   | body     | 배경으로 설정할 이진 이미지 파일(PNG, JPEG, BMP 등)입니다. |
| folder         | string | query    | 워크북이 위치한 저장소 폴더입니다.               |
| storageName    | string | query    | Aspose Cloud 저장소의 이름입니다.                              |

**지원되는 형식 및 제한 사항**

- 허용되는 이미지 확장자: **PNG, JPEG, BMP, GIF**.
- 최대 파일 크기: **5MB**.
- 이미지는 워크시트 배경 전체를 채우도록 타일링됩니다.

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Worksheets/PutWorksheetBackground)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/background" \
  -X PUT \
  -F "imageFile=@Creative.jpg" \
  -H "Content-Type: multipart/form-data" \
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

_가능한 오류 응답_

| HTTP 코드 | 설명                                                 |
| --------- | ----------------------------------------------------------- |
| 400       | 잘못된 요청 – 누락되었거나 유효하지 않은 매개변수입니다.                |
| 401       | 인증되지 않음 – 유효하지 않거나 만료된 JWT 토큰입니다.                |
| 404       | 없음 – 워크북 또는 워크시트가 존재하지 않습니다.           |
| 500       | 내부 서버 오류 – 서버에서 예기치 않은 조건이 발생했습니다. |

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리해주므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}
---