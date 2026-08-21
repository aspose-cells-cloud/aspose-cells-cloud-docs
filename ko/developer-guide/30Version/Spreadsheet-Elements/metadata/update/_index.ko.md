---
title: "메타데이터 업데이트"
second_title: "문서"
linktitle: "스토리지 사용 없이 업데이트"
type: docs
url: /metadata/update/
keywords: "메타데이터, Excel, Aspose.Cells Cloud, REST API, 업데이트, 스프레드시트"
description: "Aspose.Cells Cloud REST API는 Excel 파일의 메타데이터를 업데이트할 수 있도록 지원합니다. 다양한 프로그래밍 언어(C#, Java, Python, Ruby, Go 등)를 위한 여러 SDK를 지원하여 원활한 통합이 가능합니다."
weight: 35
ArticleTitle: "메타데이터 업데이트 – Aspose.Cells Cloud API 문서"
---

이 REST API는 여러 Excel 파일에서 **메타데이터**를 업데이트합니다.

**필수 조건:** 활성화된 Aspose Cloud 계정, 유효한 JWT 액세스 토큰, 업로드할 Excel 파일.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/metadata/update
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 강화되어 있으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름        | 유형     | 위치            | 설명                                     |
| ------------------- | -------- | --------------- | ---------------------------------------- |
| file                | 파일     | formData        | 업로드할 Excel 파일.                      |
| DocumentProperties  | 객체     | HTTP 본문 (JSON)| Excel 파일에 설정할 문서 속성.            |

**참고:** 단일 요청당 최대 10개의 파일을 업로드할 수 있습니다. 지원되는 형식은 `.xlsx`, `.xls`, `.csv`입니다. 전체 요청 크기는 100MB를 초과할 수 없습니다.

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/PostMetadata)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예시는 cURL을 사용하여 Cloud API에 호출을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/metadata/update" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'xxxxx1=@xxxx1.xlsx' \
  -F 'xxxxx2=@xxxx2.xlsx' \
  -d '[{ "name": "test", "value": "test" }]'
```

요청에는 Bearer JWT 토큰이 포함된 **Authorization** 헤더가 필요합니다. 토큰은 Aspose Cloud 클라이언트 자격 증명을 사용하여 생성되어야 합니다.

{{< /tab >}}

{{< tab tabNum="12" >}}

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

## 클라우드 SDK 패밀리

SDK를 사용하면 개발 속도를 최대한 빠르게 할 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostMetadata.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostMetadata.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostMetadata.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostMetadata.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostMetadata.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostMetadata.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostMetadata.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostMetadata.go" >}}

{{< /tab >}}

{{< /tabs >}}

**참고:**  
- [메타데이터 조회](/metadata/get/)  
- [메타데이터 삭제](/metadata/delete/)  
---