---
title: "Excel 파일에서 메타데이터 가져오기"
second_title: "문서"
linktitle: "스토리지 사용 없이 가져오기"
type: docs
url: /metadata/get/
keywords: "Aspose.Cells, Excel, 메타데이터, REST API, 클라우드 SDK"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크북에서 기본 제공 또는 사용자 정의 메타데이터를 검색합니다. 요청 형식, 매개변수, 샘플 SDK 코드 및 오류 처리가 포함됩니다."
weight: 23
ArticleTitle: "Excel 파일에서 메타데이터 가져오기 - Aspose.Cells Cloud API"
---

이 REST API는 하나 이상의 Excel 파일에서 **메타데이터**를 검색합니다.  
요청에는 OAuth 2.0 클라이언트 자격 증명 흐름을 통해 얻은 `Authorization: Bearer <access_token>` 헤더가 포함되어야 합니다.

**필수 조건**: 이 엔드포인트를 호출하려면 Aspose Cloud OAuth 2.0 토큰 엔드포인트에서 얻은 유효한 액세스 토큰이 필요합니다. 토큰을 획득하는 예시 curl 요청:

```bash
curl -X POST "https://api.aspose.cloud/connect/token" \
     -H "Content-Type: application/x-www-form-urlencoded" \
     -d "grant_type=client_credentials&client_id=<your_client_id>&client_secret=<your_client_secret>"
```

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/metadata/get
```

### 쿼리 매개변수

| 매개변수 이름 | 유형   | 설명                                                               |
| ------------- | ------ | ----------------------------------------------------------------- |
| type          | string | `ALL` / `BuiltIn` / `Custom` – 반환할 메타데이터 그룹을 지정합니다. |

### 요청 본문 매개변수

| 매개변수 이름 | 유형      | 설명                                                         |
| ------------- | --------- | ----------------------------------------------------------- |
| excel file    | data file | 멀티파트 요청의 첫 번째 부분으로 제공되는 Excel 파일입니다. |

### 응답

```json
[
  {
    "Name": "Author",
    "Value": "John Doe",
    "BuiltIn": true,
    "IsReadOnly": false
  },
  {
    "Name": "CustomProp1",
    "Value": "Custom Value",
    "BuiltIn": false,
    "IsReadOnly": false
  }
]
```

| 코드 | 의미                 | 발생 조건                              |
|------|---------------------|-------------------------------------|
| 200  | 성공                 | 메타데이터가 반환되었습니다.                |
| 400  | 잘못된 요청           | 파일 누락 또는 잘못된 쿼리입니다.    |
| 401  | 인증되지 않음         | 잘못되었거나 누락된 토큰입니다.         |
| 404  | 찾을 수 없음          | 지정된 파일을 찾을 수 없습니다.         |
| 500  | 내부 서버 오류        | 예기치 않은 서버 오류입니다.        |

이 API는 해당되는 경우 표준 HTTP 상태 코드와 함께 오류 응답 JSON 객체를 반환합니다.

### 클라우드 SDK 패밀리

SDK를 사용하면 저수준 세부 사항을 처리함으로써 개발 속도가 빨라집니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetMetadata.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetMetadata.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetMetadata.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetMetadata.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetMetadata.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetMetadata.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetMetadata.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetMetadata.go" >}}

{{< /tab >}}

{{< /tabs >}}
---