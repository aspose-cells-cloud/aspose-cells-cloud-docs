---
title: "Aspose.Cells Cloud – 파일 삭제 API"
second_title: "문서"
ArticleTitle: "Aspose.Cells Cloud – 파일 삭제 API"
linktype: "Delete File"
type: docs
url: /ko/delete-file/
keywords: "Aspose Cells, 파일 삭제 API, Excel 클라우드 스토리지, REST API, 파일 관리"
description: "RESTful 파일 삭제 API를 사용하여 Aspose.Cells Cloud 스토리지에서 Excel 파일을 삭제합니다. 엔드포인트, 매개변수, 인증 및 샘플 코드 포함."
weight: 100
---

**deleteFile** API는 클라우드 스토리지에서 지정된 파일을 삭제하여 리소스와 데이터를 효율적으로 관리할 수 있도록 도와줍니다.

## **Excel API: 파일 삭제**

### 웹 API

```http
DELETE https://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 적용되며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

```bash
-H "Authorization: Bearer {access_token}"
```

### 요청 매개변수

| 매개변수 이름 | 유형   | 위치 | 설명                                                                 |
| :------------ | :----- | :--- | :------------------------------------------------------------------- |
| `path`        | string | 경로 | 삭제할 파일의 URL 인코딩된 경로입니다.                               |
| `storageName` | string | 쿼리 | 파일이 위치한 스토리지 이름입니다. 기본 스토리지를 사용하는 경우 생략 가능합니다. |
| `versionId`   | string | 쿼리 | 삭제할 특정 파일 버전의 식별자입니다. 생략 시 최신 버전이 삭제됩니다. |

### 응답 설명

성공적인 요청은 빈 응답 본문과 함께 **HTTP 200**을 반환합니다. JSON 페이로드는 반환되지 않습니다.

```json
{}
```

**HTTP 상태 코드**

| 코드 | 의미                  | 설명                                                  |
| ---- | --------------------- | ----------------------------------------------------- |
| 200  | OK (성공)             | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함. |
| 400  | Bad Request (잘못된 요청) | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형). |
| 401  | Unauthorized (인증되지 않음) | 잘못되거나 누락된 JWT 토큰.                            |
| 413  | Payload Too Large (페이로드 너무 큼) | 업로드된 파일이 크기 제한을 초과함.                    |
| 500  | Internal Server Error (내부 서버 오류) | 예기치 않은 서버 오류.                                 |

## OpenAPI 사양

[OpenAPI 사양](https://reference.aspose.cloud/cells/#/FileController/DeleteFile)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예시는 cURL을 사용하여 Cloud API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v4.0/cells/storage/file/Example.xlsx?storageName=MyStorage" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
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

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 관리해 주므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예시는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 요청을 보내는 방법을 보여줍니다.

---