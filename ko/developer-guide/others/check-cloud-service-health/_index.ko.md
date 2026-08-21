---
title: "Aspose.Cells Cloud – 서비스 건강 상태 확인 (API)"
second_title: "문서"
ArticleTitle: "Aspose.Cells Cloud 건강 상태 점검"
linktype: "서비스 건강 상태 확인"
type: docs
url: /ko/check-cloud-service-health/
keywords: "Aspose.Cells Cloud, API 건강 상태 점검, REST 상태, 클라우드 서비스 모니터링"
description: "Aspose.Cells Cloud 서비스 건강 상태를 실시간으로 모니터링하세요. GET /v4.0/cells/status/check 엔드포인트, 매개변수, 응답 형식 및 SDK 예제를 알아보세요."
weight: 100
---

Aspose.Cells Cloud 서비스의 건강 상태를 확인하세요.

**필수 조건**  
이 엔드포인트를 호출하려면 유효한 Aspose Cloud 액세스 토큰이 필요합니다. Aspose Cloud 대시보드에서 애플리케이션을 등록한 후 클라이언트 ID(client-id)와 클라이언트 시크릿(client-secret)을 사용해 OAuth2 토큰 엔드포인트에서 베어러 토큰(Bearer token)을 발급받으세요. 아래와 같이 토큰을 `Authorization` 헤더에 포함하세요.

## **클라우드 서비스 건강 상태 확인**

### **웹 API**

```http
GET https://api.aspose.cloud/v4.0/cells/status/check
```

### **보안 및 인증**

Aspose.Cells Cloud API는 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>을 요구하는 보안 서비스입니다.

### **요청 매개변수**

| 매개변수        | 유형   | 필수 여부 | 설명                                                       |
| --------------- | ------ | --------- | ---------------------------------------------------------- |
| Authorization   | header | 예        | 인증용 베어러 토큰 (`Authorization: Bearer <token>`).      |
| detail          | query  | 아니요    | 세부 구성 요소 정보를 포함하려면 `true`로 설정하세요.       |
| Accept          | header | 아니요    | 원하는 응답 형식이며, 기본값은 `application/json`입니다.   |

### **응답**

요청이 성공하면 서비스는 JSON 페이로드를 반환합니다.

```json
{
  "status": "OK",
  "service": "Cells",
  "timestamp": "{{timestamp}}",
  "components": {
    "api": "정상 작동 중",
    "storage": "정상 작동 중",
    "database": "정상 작동 중"
  }
}
```

**HTTP 상태 코드**

| 코드 | 의미                 | 설명                                                       |
| ---- | -------------------- | ---------------------------------------------------------- |
| 200  | OK                   | 서비스가 정상입니다. 위의 JSON 예제를 참조하세요.          |
| 401  | 인증되지 않음        | 유효하지 않거나 누락된 인증 토큰입니다.                    |
| 503  | 서비스 사용 불가능     | 현재 서비스가 비정상적이거나 유지보수 중입니다.            |
| 4xx  | 클라이언트 오류       | 요청 매개변수가 잘못되었거나 요청 형식이 잘못되었습니다.    |
| 5xx  | 서버 오류             | 예기치 않은 서버 오류입니다. 나중에 다시 시도하세요.        |

## Aspose.Cells Cloud 상태 API를 SDK와 함께 사용하는 방법

### OpenAPI 사양

<a href="https://reference.aspose.cloud/cells/#/CellsStatusController/CheckCloudServiceHealth" target="_blank" rel="noopener noreferrer">OpenAPI 사양</a>은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 내부 세부 사항을 처리하므로 최소한의 코드로 Cells 클라우드 건강 상태 점검 기능을 구현할 수 있습니다.  
사용 가능한 Aspose.Cells Cloud SDK 전체 목록은 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

아래는 가장 일반적인 SDK를 사용해 건강 상태 점검 엔드포인트를 호출하는 방법을 보여주는 샘플 코드 스니펫입니다.

---