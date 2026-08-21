---
title: "Aspose.Cells Cloud 폴더 이동 API – 클라우드에서 폴더를 빠르게 이동하기"
second_title: "문서"
ArticleTitle: "클라우드 기반 Excel 파일 관리 – 클라우드에서 폴더를 빠르게 이동하기"
linktitle: "폴더 이동"
type: docs
url: /ko/move-folder/
keywords: "Aspose.Cells, 폴더 이동, 클라우드 저장소, Excel API"
description: "RESTful 폴더 이동 API를 통해 Aspose.Cells Cloud 저장소에서 폴더를 이동하는 방법을 알아보세요. 엔드포인트, 매개변수, 샘플 cURL 요청, 오류 코드, C#, Java, Python 등 다양한 SDK 예제를 포함합니다."
weight: 100
---

이 API는 Aspose.Cells Cloud 저장소 내에서 한 위치에서 다른 위치로 폴더를 이동합니다. 파일을 정리하고 클라우드 저장소를 효율적으로 관리하는 데 도움이 됩니다.

## **Excel API: 폴더 이동**

### 웹 API

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/move/{srcPath}
```

**예시 cURL 요청**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/move/FolderA?destPath=FolderB" \
     -H "Authorization: Bearer {access_token}"
```

### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **moveFolder** API 요청 매개변수

| 매개변수 이름     | 유형   | 위치  | 설명                                                                |
| ----------------- | ------ | ----- | ------------------------------------------------------------------- |
| srcPath           | string | Path  | 이동할 폴더의 전체 경로 (예: `FolderA/`)                            |
| destPath          | string | Query | 폴더를 이동할 대상 경로 (예: `FolderB/`)                            |
| srcStorageName    | string | Query | (선택 사항) 소스 저장소 이름                                        |
| destStorageName   | string | Query | (선택 사항) 대상 저장소 이름                                        |

**매개변수 상세 설명**

- **srcPath** – 필수. 소스 폴더 경로.
- **destPath** – 필수. 대상 폴더 경로.
- **srcStorageName** – 선택 사항. 소스 저장소 식별자.
- **destStorageName** – 선택 사항. 대상 저장소 식별자.

### **응답**

성공 시 API는 빈 응답 본문과 HTTP 상태 코드 **200 OK**를 반환합니다. 오류는 `error` 필드를 포함하는 JSON 객체 형태로 반환됩니다.

**HTTP 상태 코드**

| HTTP 코드 | HTTP 상태               | 설명                                                             |
| --------- | ----------------------- | ---------------------------------------------------------------- |
| 200       | OK                      | 웹 API 호출 성공; 응답에는 작업 세부 정보가 포함됩니다.          |
| 400       | Bad Request             | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형).         |
| 401       | Unauthorized            | 잘못되거나 누락된 JWT 토큰.                                      |
| 413       | Payload Too Large       | 업로드된 파일이 크기 제한을 초과했습니다.                        |
| 500       | Internal Server Error   | 예기치 않은 서버 오류.                                           |

## OpenAPI 사양

[OpenAPI 사양](https://reference.aspose.cloud/cells/#/FolderController/MoveFolder)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API로 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/move/{srcPath}?destPath={destPath}" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{}
```

{{< /tab >}}

{{< /tabs >}}

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 처리해 주므로, 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스로 요청을 보내는 방법을 보여줍니다:

---