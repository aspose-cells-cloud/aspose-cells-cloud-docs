---
title: "Excel 파일에서 개체 지우기"
second_title: "문서"
linktitle: "지우기"
type: docs
url: /ko/clear/
aliases: [  /ko/clearobjects/ ]
keywords: "Aspose.Cells, Excel, 개체 지우기, REST API, 클라우드 SDK, 주석 삭제, 차트 삭제"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크북에서 주석, 차트, 도형 및 기타 개체를 삭제합니다. 여러 SDK를 지원하며 정리된 파일을 Base64 형식으로 반환합니다."
weight: 39
---

이 REST API는 Excel 파일의 개체를 지웁니다.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/clearobjects
```

### 요청 매개변수

| 매개변수     | 유형   | 위치      | 필수 여부 | 기본값 | 허용 값                                                                                                                                                                         | 설명                                 |
| ------------ | ------ | --------- | -------- | ------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------- |
| file         | 파일   | form‑data | 예       | —       | —                                                                                                                                                                               | 업로드할 Excel 파일                         |
| objecttype   | 문자열 | query     | 아니요   | —       | `duplicaterows`, `blankcolumns`, `blankrows`, `formula`, `content`, `style`, `chart`, `comment`, `picture`, `shape`, `listobject`, `hyperlink`, `oleobject`, `pivottable`, `validation`, `background` | 지울 개체 유형(쉼표로 구분) |

[OpenAPI 사양서](https://apireference.aspose.cloud/cells/#/LightCells/PostClearObjects)는 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예제는 cURL을 사용해 클라우드 API로 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/clearobjects?objecttype=comment" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt 토큰>" \
  -F 'xxxxx1=@xxxx1.xlsx' \
  -F 'xxxxx2=@xxxx2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "file1",
      "FileSize": 274022,
      "FileContent": "-----Base64문자열--------"
    },
    {
      "Filename": "file2",
      "FileSize": 274022,
      "FileContent": "-----Base64문자열--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## 클라우드 SDK 패밀리

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 작업에 집중할 수 있도록 도와줍니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostClearObjects.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostClearObjects.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostClearObjects.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostClearObjects.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostClearObjects.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostClearObjects.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostClearObjects.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostClearObjects.go" >}}

{{< /tab >}}

{{< /tabs >}}