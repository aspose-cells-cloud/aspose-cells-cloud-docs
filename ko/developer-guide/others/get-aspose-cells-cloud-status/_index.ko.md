---
title: "Aspose.Cells Cloud Web API - Aspose.Cells Cloud 상태 확인"
second_title: "문서"
ArticleTitle: "Aspose.Cells Cloud 상태 확인"
linktype: "docs"
url: /ko/get-aspose-cells-cloud-status/
keywords: "Aspose.Cells, 클라우드 API, 헬스 체크, Excel, REST"
description: "Aspose.Cells Cloud 서비스의 헬스 상태를 실시간으로 모니터링합니다."
weight: 100
---

Aspose.Cells Cloud 서비스의 헬스 상태를 실시간으로 확인합니다.

**필수 조건:** 이 API를 호출하려면 Aspose Cloud 클라이언트 자격 증명을 사용해 Bearer 액세스 토큰을 획득해야 합니다. 획득한 토큰을 `Authorization` 헤더에 `Bearer {access_token}` 형식으로 포함시켜 전송해야 합니다.

## **Aspose.Cells Cloud 상태 확인**

### **Web API**

이 엔드포인트는 HTTP **GET** 메서드를 사용하며 요청 본문이 필요하지 않습니다.

```
GET https://api.aspose.cloud/v4.0/cells
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 위해 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>을 요구합니다.

### **요청 매개변수:**

| 매개변수 이름 | 유형   | 경로/쿼리 문자열/HTTP 본문 | 설명                                  |
| ------------- | ------ | ------------------------- | ------------------------------------- |
| Authorization | String | 헤더                      | 인증용 Bearer 토큰 (필수)             |
| format        | String | 쿼리                      | 원하는 응답 형식, 예: `json`          |

### **응답**

```json
{
  "status": "OK",
  "service": "Aspose.Cells Cloud",
  "timestamp": "2026-07-06T12:34:56Z"
}
```

**응답 스키마**

| 필드       | 유형              | 설명                             |
| --------- | ----------------- | -------------------------------- |
| status    | string            | 서비스 헬스 상태 (`OK`, `Degraded` 등) |
| service   | string            | 서비스 이름                      |
| timestamp | string (ISO‑8601) | 상태 확인 시간                   |

이 API는 Aspose.Cells Cloud 서비스의 현재 헬스 **상태**를 포함하는 표준 JSON 페이로드를 반환합니다.

**HTTP 상태 코드**

- **200 OK** – 서비스가 정상이며 응답에 상태 정보가 포함되어 있습니다.
- **401 Unauthorized** – 인증 토큰이 누락되었거나 유효하지 않습니다.
- **503 Service Unavailable** – 현재 서비스가 점검 중이거나 장애가 발생한 상태입니다.

## SDK를 사용하여 Aspose.Cells Cloud 상태 확인 API 사용하기

### OpenAPI 명세서

[OpenAPI 명세서](https://reference.aspose.cloud/cells/#/CellsStatusController/GetAsposeCellsCloudStatus)는 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 공개적으로 제공되는 프로그래밍 인터페이스를 정의합니다.

### Aspose.Cells Cloud SDK 사용하기

SDK를 사용하면 통합이 간편해지고 보일러플레이트 코드가 줄어듭니다. SDK는 내부 세부 사항을 처리해 주므로 최소한의 노력으로 Aspose.Cells Cloud의 실행 상태를 조회할 수 있습니다. Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.