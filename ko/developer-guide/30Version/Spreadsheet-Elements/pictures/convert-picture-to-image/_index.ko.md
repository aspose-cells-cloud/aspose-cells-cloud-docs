---
title: "Aspose.Cells Cloud API – 워크시트에서 그림 가져오기"
second_title: "문서"
linktitle: "가져오기"
type: docs
url: /pictures/get/
aliases: [/convert-picture-to-image/]
keywords: "Aspose.Cells, 그림 가져오기, API, Excel, 클라우드, REST"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트에서 특정 그림을 검색합니다. 엔드포인트, 매개변수, 인증 단계, 응답 코드 및 코드 예제를 포함합니다."
weight: 10
ArticleTitle: "Aspose.Cells Cloud API – 워크시트에서 그림 가져오기"
---

이 REST API는 Excel 워크시트에서 0부터 시작하는 인덱스를 기준으로 그림을 검색합니다.

## REST API

이 엔드포인트를 호출하려면 **Authorization** 헤더에 유효한 JWT 액세스 토큰을 포함해야 합니다. 토큰은 Aspose.Cells Cloud 인증 흐름을 통해 얻을 수 있으며, 파일 접근에 필요한 범위가 필요합니다. 토큰 획득에 대한 자세한 내용은 전역 **인증** 가이드를 참조하십시오.

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/{pictureIndex}
```

### 요청 매개변수

| 매개변수 이름 | 유형    | 위치 | 설명                                                                                                         |
| ------------- | ------- | ---- | ------------------------------------------------------------------------------------------------------------- |
| name          | string  | path | Excel 문서의 이름.                                                                                           |
| sheetName     | string  | path | 워크시트의 이름.                                                                                             |
| pictureIndex  | integer | path | 그림의 0부터 시작하는 인덱스.                                                                                 |
| format        | string  | query | 원하는 내보내기 형식(예: png, jpg, bmp, gif, tiff). 생략 시 그림은 원래 형식으로 반환됩니다.                  |
| folder        | string  | query | 문서가 포함된 폴더.                                                                                          |
| storageName   | string  | query | 저장소 위치의 이름.                                                                                          |

### 오류 응답

| HTTP 코드 | 설명                                                                   |
| --------- | ---------------------------------------------------------------------- |
| 401       | 인증되지 않음 – 누락되거나 유효하지 않은 토큰.                             |
| 404       | 찾을 수 없음 – 지정된 파일, 워크시트 또는 페이지 분할 인덱스가 존재하지 않음. |
| 400       | 잘못된 요청 – 잘못된 요청 구문 또는 유효하지 않은 매개변수.                  |
| 500       | 내부 서버 오류 – 예기치 않은 조건이 발생했습니다.                          |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Pictures/GetWorksheetPicture)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures/1?format=png" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```bash
# 응답 본문에 바이너리 이미지 데이터(PNG)가 반환됩니다.
# 예: base64로 인코딩된 스니펫
iVBORw0KGgoAAAANSUhEUgAA...
```

{{< /tab >}}

{{< /tabs >}}

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 개발 속도를 높이는 가장 빠른 방법입니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

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

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "ExampleGetWorksheetPictureWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "ExampleGetWorksheetPictureWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ExampleGetWorksheetPictureWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "ExampleGetWorksheetPictureWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "ExampleGetWorksheetPictureWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}