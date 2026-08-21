---
title: "Object Exists API – Aspose.Cells Cloud에서 파일/폴더 존재 여부 확인"
second_title: "문서"
ArticleTitle: "Object Exists API – Aspose.Cells Cloud에서 파일 또는 폴더 존재 여부 확인"
linktitle: "Object Exists"
type: docs
url: /ko/object-exists/
keywords: "Aspose.Cells, 클라우드 스토리지, 오브젝트 존재 여부, 파일 존재 여부, 폴더 존재 여부, API"
description: "Object Exists API를 사용하여 Aspose.Cells Cloud 스토리지 내에 파일 또는 폴더가 존재하는지 빠르게 확인합니다. 선택적으로 스토리지 이름과 버전 ID를 지원하며, 버전 관리가 적용된 오브젝트와도 호환됩니다."
weight: 100
---

**Object Exists API**는 개발자가 Aspose.Cells Cloud 스토리지 내에 특정 파일 또는 폴더가 존재하는지 확인할 수 있도록 해줍니다. 이 API는 존재 여부와 경로가 폴더를 가리키는지 여부를 간단한 부울(Boolean) 값으로 반환합니다.

## **Excel API: Object Exists**

### 웹 API

```http
GET https://api.aspose.cloud/v5.0/cells/storage/exist/{path}
```

_`{path}`_는 스토리지 내 파일 또는 폴더의 전체 경로입니다.

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 확보되었으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름   | 유형   | 위치   | 필수 여부 | 설명                                                              |
| --------------- | ------ | ------ | --------- | ----------------------------------------------------------------- |
| `path`          | string | Path   | 예        | 파일 또는 폴더의 전체 경로입니다.                                |
| `storageName`   | string | Query  | 아니요    | 스토리지 이름이며, 생략 시 기본 스토리지가 사용됩니다.           |
| `versionId`     | string | Query  | 아니요    | 파일의 특정 버전 식별자입니다(버전 관리가 활성화된 경우에 해당). |

**HTTP 상태 코드**

| HTTP 코드 | HTTP 상태             | 설명                                                        |
| --------- | --------------------- | ----------------------------------------------------------- |
| 200       | OK(성공)              | 웹 API가 성공적으로 호출됨; 응답에 작업 세부 정보 포함.    |
| 400       | Bad Request(잘못된 요청) | 누락되었거나 잘못된 매개변수(예: 지원되지 않는 파일 유형). |
| 401       | Unauthorized(인증되지 않음) | 잘못되었거나 누락된 JWT 토큰.                            |
| 413       | Payload Too Large(ペイロードが大きすぎます) | 업로드된 파일이 크기 제한을 초과했습니다.              |
| 500       | Internal Server Error(내부 서버 오류) | 예기치 않은 서버 오류입니다.                            |

### **응답**

성공적인 호출은 두 속성을 포함하는 JSON 페이로드를 반환합니다:

```json
{
  "Exists": true,
  "IsFolder": false
}
```

- **Exists** – 파일 또는 폴더가 존재하면 `true`, 그렇지 않으면 `false`.
- **IsFolder** – 경로가 폴더를 가리키면 `true`, 파일이면 `false`.

## OpenAPI 사양

[OpenAPI 사양](https://reference.aspose.cloud/cells/#/StorageController/ObjectExists)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API에 호출을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/exist/myFolder/subFolder" \
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

SDK를 사용하는 것이 개발 속도를 높이는 가장 좋은 방법입니다. SDK는 저수준 세부 사항을 처리해주므로, 개발자는 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 호출을 수행하는 방법을 보여줍니다. Gist가 로드되지 않으면 각 탭 아래에 정적 예제가 제공됩니다.