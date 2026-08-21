---
title: "폴더 생성 – Aspose.Cells Cloud API | Excel 저장소 관리"
second_title: "문서"
ArticleTitle: "폴더 생성 – Aspose.Cells Cloud API"
linktitle: "폴더 생성"
type: docs
url: /ko/create-folder/
keywords: "Aspose.Cells, Cloud API, 폴더 생성, 저장소 관리, Excel"
description: "간단한 PUT 요청을 통해 Aspose.Cells Cloud 저장소에 새 폴더를 생성합니다. 요청 형식, 매개변수, 응답 및 오류 처리 방법을 확인하세요."
weight: 100
---

**createFolder** 작업은 Excel API에서 사용하는 클라우드 저장소의 지정된 위치에 새 폴더를 생성합니다. 이 작업은 파일을 조직화하고 구조화된 디렉터리 계층 구조를 유지하는 데 필수적입니다.

## **Excel API: 폴더 생성**

### 웹 API

```
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 강화되었으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **createFolder** API의 요청 매개변수는 다음과 같습니다

| 매개변수 이름 | 유형   | 위치 | 필수 여부 | 기본값 | 설명                                                                 |
| ------------- | ------ | ---- | -------- | ------ | -------------------------------------------------------------------- |
| `path`        | String | 경로 | 예       | –      | 생성할 폴더 경로 (예: `myFolder/subFolder`)                         |
| `storageName` | String | 쿼리 | 아니요   | –      | 사용할 저장소 이름. 생략 시 기본 저장소가 적용됩니다.              |

### 응답 설명

```json
{}
```

성공 시 이 작업은 콘텐츠를 반환하지 않습니다. 일반적인 HTTP 상태 코드는 다음과 같습니다:

**HTTP 상태 코드**

| HTTP 코드 | HTTP 상태             | 설명                                                               |
| --------- | --------------------- | ------------------------------------------------------------------ |
| 200       | OK                    | 웹 API가 성공적으로 호출됨; 응답에 작업 세부 정보가 포함됨.       |
| 400       | Bad Request           | 누락되었거나 잘못된 매개변수 (예: 지원되지 않는 파일 형식).        |
| 401       | Unauthorized          | 잘못되거나 누락된 JWT 토큰.                                        |
| 413       | Payload Too Large     | 업로드된 파일이 크기 제한을 초과함.                                |
| 500       | Internal Server Error | 예기치 않은 서버 오류.                                             |

## OpenAPI 사양

[OpenAPI 사양](https://reference.aspose.cloud/cells/#/FolderController/CreateFolder)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용해 Cloud API로 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/myFolder/subFolder" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 관리해 주므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스로 요청을 보내는 방법을 보여줍니다:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CreateFolder.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CreateFolder.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CreateFolder.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CreateFolder.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CreateFolder.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CreateFolder.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CreateFolder.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CreateFolder.go" >}}
{{</tab>}}
{{< /tabs >}}