---
title: "엑셀 파일 잠금 해제"
second_title: "문서"
linktitle: "엑셀 파일 잠금 해제"
type: docs
url: /unlock-excel-files/
aliases: [/unlock/without-storage/, /unlock/, /unlock/without-using-storage/]
keywords: "엑셀 잠금 해제, Aspose.Cells Cloud, REST API, 엑셀 잠금 해제, 비밀번호 보호 워크북, SDK, C#, Java, Python, Node.js, Go, PHP, Ruby, Swift"
description: "Aspose.Cells Cloud REST API는 비밀번호로 보호된 엑셀 파일의 잠금을 해제할 수 있는 엔드포인트를 제공합니다. Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby, Swift 등 다양한 프로그래밍 언어용 SDK를 제공합니다."
ArticleTitle: "Aspose.Cells Cloud REST API를 사용하여 엑셀 파일 잠금 해제"
weight: 70
---

이 REST API는 엑셀 파일의 잠금을 해제합니다.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/unlock
```

### 보안 및 인증

Aspose.Cells Cloud API는 보안이 강화되어 있으며, [JWT 토큰 기반 인증](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)이 필요합니다.

### 요청 파라미터

| 파라미터 이름 | 타입   | 위치             | 설명                                |
| ------------- | ------ | ---------------- | ----------------------------------- |
| file          | file   | formData (HTTP 본문) | 업로드할 파일                         |
| password      | string | query string     | 파일 잠금 해제용 비밀번호 (보호된 경우) |

### 응답

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP 상태 코드**

| 코드 | 의미                     | 설명                                      |
|----|-------------------------|-----------------------------------------|
| 200 | OK                      | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함 |
| 400 | Bad Request             | 누락되었거나 유효하지 않은 파라미터 (예: 지원되지 않는 파일 형식) |
| 401 | Unauthorized            | 유효하지 않거나 누락된 JWT 토큰 |
| 413 | Payload Too Large       | 업로드된 파일이 크기 제한을 초과함 |
| 500 | Internal Server Error   | 예기치 않은 서버 오류 |

## SDK를 사용한 PostUnlock API 사용 방법

### PostUnlock API 사양

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/LightCells/PostUnlock)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 요청을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/unlock?password=123456" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "xxxxx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "xxxxx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 처리해주므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

**참고**  
- 이 API는 단일 요청으로 여러 엑셀 파일의 잠금을 해제할 수 있으며, 각 파일은 응답의 `Files` 배열에 반환됩니다.  
- 호환성 문제를 방지하려면 SDK 버전이 API 버전(`v3.0`)과 일치하는지 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 요청을 보내는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnlock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnlock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnlock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnlock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnlock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnlock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnlock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnlock.go" >}}

{{< /tab >}}

{{< /tabs >}}