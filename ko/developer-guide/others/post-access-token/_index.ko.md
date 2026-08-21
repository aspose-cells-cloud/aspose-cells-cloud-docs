---
title: "Aspose.Cells Cloud 웹 API - 액세스 토큰 발급"
second_title: "문서"
ArticleTitle: "클라이언트 ID 및 비밀번호로 액세스 토큰 받기"
linktitle: "액세스 토큰 발급"
type: docs
url: /ko/post-access-token/
keywords: "Aspose.Cells, 클라우드, 액세스 토큰, OAuth2, API, 인증, REST, Excel, Office Cloud"
description: "클라이언트 ID 및 비밀번호를 사용하여 POST /cells/connect/token 엔드포인트를 호출함으로써 Aspose.Cells Cloud에 대한 OAuth2 액세스 토큰을 획득합니다."
weight: 100
---

클라이언트 ID 및 비밀번호를 사용하여 Cells Cloud 토큰 가져오기 API로 액세스 토큰을 검색합니다.

## 액세스 토큰 발급 API

엔드포인트를 호출하기 전에 다음 사항을 확인하세요:

* 등록된 Aspose Cloud 계정이 있어야 합니다.  
* Aspose Cloud 포털에서 생성한 **클라이언트 ID** 및 **클라이언트 비밀번호**가 있어야 합니다.  

### 웹 API

```
POST https://api.aspose.cloud/v4.0/cells/connect/token
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 우수하며 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름 | 유형   | 위치                         | 설명                                               |
| ------------- | ------ | ---------------------------- | -------------------------------------------------- |
| grant_type    | string | 본문 (form‑url‑encoded)      | OAuth에 필요한 고정 값 `client_credentials`입니다. |
| client_id     | string | 본문 (form‑url‑encoded)      | 귀하에게 발급된 클라이언트 식별자입니다.           |
| client_secret | string | 본문 (form‑url‑encoded)      | 클라이언트 ID와 관련된 비밀번호입니다.             |

**요청 예시(cURL)**  

```bash
curl -X POST "https://api.aspose.cloud/v4.0/cells/connect/token" \
     -H "Content-Type: application/x-www-form-urlencoded" \
     -d "grant_type=client_credentials&client_id=YOUR_CLIENT_ID&client_secret=YOUR_CLIENT_SECRET"
```

### 응답

```json
{
  "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
  "token_type": "Bearer",
  "expires_in": 3600
}
```

**HTTP 상태 코드**

| 코드 | 의미                 | 설명                                                |
|------|----------------------|-----------------------------------------------------|
| 200  | OK (성공)            | 필터가 성공적으로 적용되었으며, 응답에는 작업 세부 정보가 포함됩니다. |
| 400  | Bad Request (잘못된 요청) | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식)가 있습니다. |
| 401  | Unauthorized (인증되지 않음) | 잘못되거나 누락된 JWT 토큰입니다.                    |
| 413  | Payload Too Large (페이로드 너무 큼) | 업로드된 파일이 크기 제한을 초과했습니다.           |
| 500  | Internal Server Error (내부 서버 오류) | 예기치 않은 서버 오류가 발생했습니다.                |

**오류 처리 예시**

```json
{
  "error": "invalid_client",
  "error_description": "클라이언트 인증에 실패했습니다."
}
```

## SDK를 사용하여 Get public key API 사용하는 방법

### OpenAPI 명세서

[OpenAPI 명세서](https://reference.aspose.cloud/cells/#/CellsAuthorityController/PostAccessToken)는 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하여 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

### Aspose.Cells Cloud SDK 사용

SDK를 사용하는 것이 가장 빠르게 시작할 수 있는 방법입니다. SDK는 기본 HTTP 세부 정보를 추상화하여 최소한의 코드로 Cells의 액세스 토큰을 획득할 수 있게 해줍니다.

Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다.