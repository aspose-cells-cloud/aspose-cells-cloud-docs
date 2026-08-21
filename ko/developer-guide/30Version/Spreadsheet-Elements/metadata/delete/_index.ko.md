---
title: "Excel 파일에서 메타데이터 삭제하기"
second_title: "문서"
linktitle: "스토리지 사용 없이 삭제"
type: docs
url: /metadata/delete/
keywords: "Aspose.Cells, 메타데이터 삭제, Excel API, 워크북 속성"
description: "Aspose.Cells Cloud API를 통해 워크북 메타데이터(작성자, 제목, 사용자 정의 등)를 삭제합니다. 엔드포인트, 인증, 매개변수, cURL 및 SDK 샘플 포함."
weight: 55
ArticleTitle: "Excel 파일에서 메타데이터 삭제하기 – Aspose.Cells Cloud 문서"
---

**개요**  
메타데이터 삭제 작업은 업로드된 Excel 파일에서 모든 워크북 속성(표준 및 사용자 정의)을 영구적으로 제거한 후, 처리된 파일을 응답으로 반환합니다.

**사전 조건**  
- 유효한 Aspose.Cells Cloud JWT 토큰 (OAuth 2.0 인증 흐름을 통해 획득 가능).  
- API 버전 **v3.0** (이 예제에서 사용된 엔드포인트).  
- SDK 사용 시, 사용 중인 언어에 맞는 Aspose.Cells Cloud SDK를 설치해야 합니다(예: NuGet, Maven, npm, pip, CPAN, 또는 Go 모듈을 통해).

이 REST API는 하나 이상의 Excel 파일에서 **메타데이터**를 삭제합니다. 작성자, 제목, 사용자 정의 데이터 등 워크북 속성을 제거하고, 정제된 파일을 반환합니다.

## API

```http
POST https://api.aspose.cloud/v3.0/cells/metadata/delete
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 위해 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>을 요구합니다.

### **요청 매개변수**

| 매개변수 이름 | 유형   | 위치 | 설명                                         |
| ------------- | ------ | ---- | --------------------------------------------- |
| file          | 파일   | formData | **메타데이터** 삭제를 위해 업로드할 Excel 파일 |
| type          | 문자열 | 쿼리 | 작업 유형; 모든 **메타데이터**를 삭제하려면 **all**로 설정 |

<a href="https://apireference.aspose.cloud/cells/#/DeleteMetadata" target="_blank" rel="noopener noreferrer">OpenAPI 스펙</a>은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 요청을 수행할 수 있도록 지원합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예제는 cURL을 사용해 Cloud API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/metadata/delete?type=all" \
  -X POST \
  -H "Authorization: Bearer <jwt 토큰>" \
  -F "file=@file1.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "file1.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

**오류 응답**은 다음과 같은 내용을 포함할 수 있습니다:

- **400 Bad Request** – 파일 누락 또는 `type` 값이 유효하지 않음.  
- **401 Unauthorized** – JWT 토큰이 유효하지 않거나 누락됨.  
- **500 Internal Server Error** – 서버 측 처리 오류.

API는 각 경우에 대한 세부 정보를 담은 `Error` 필드를 포함하는 JSON 객체를 반환합니다.

| 코드 | 의미 | 설명 |
|------|------|------|
| 200 | OK | 메타데이터 삭제 완료, 파일 반환됨 |
| 400 | Bad Request | 파일 누락 또는 `type`이 유효하지 않음 |
| 401 | Unauthorized | JWT 토큰이 유효하지 않거나 누락됨 |
| 500 | Internal Server Error | 서버 처리 실패 |

## Cloud SDK Family

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 저수준 세부 사항을 처리하므로, 개발자는 프로젝트 핵심 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteMetadata.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteMetadata.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteMetadata.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteMetadata.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteMetadata.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteMetadata.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteMetadata.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteMetadata.go" >}}

{{< /tab >}}

{{< /tabs >}}