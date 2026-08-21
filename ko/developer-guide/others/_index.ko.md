---
title: "Aspise.Cells Cloud Web API – 기타 기능: 건강 상태 확인, 공개 키 조회"
linktitle: "기타 기능"
ArticleTitle: "기타 기능: 건강 상태 확인, 공개 키 조회"
second_title: "문서"
type: docs
url: /other-features/
keywords: "Aspose.Cells, 클라우드 API, 건강 상태 확인, 공개 키, 액세스 토큰, Excel, REST"
description: "Aspose.Cells Cloud의 기타 기능 살펴보기: 건강 상태 확인 엔드포인트, 공개 키 조회, 토큰 생성을 통해 Excel API 통합을 보안하세요."
weight: 180
---

**사전 준비 사항** – 아래 나열된 기능을 사용하려면 유효한 Aspose Cloud 구독과 인증을 위한 활성화된 **클라이언트 ID** / **클라이언트 시크릿** 쌍이 필요합니다.

이러한 "기타 기능"은 Aspose.Cells Cloud API에 필수적인 지원 작업을 제공합니다. 예를 들어, 서비스 가용성 확인, 암호화 키 조회, 액세스 토큰 발급 등이 포함됩니다. 일반적으로 워크북 관련 엔드포인트를 사용하기 전에 호출됩니다.

- **[Aspose.Cells Cloud 건강 상태 확인](https://docs.aspose.cloud/cells/check-cloud-service-health/)**  
  Aspose.Cells Cloud 서비스가 연결 가능하고 정상적으로 작동 중인지 확인합니다. 성공적인 호출 시 **HTTP 200** 상태 코드와 JSON `{ "status": "OK" }`가 반환됩니다. 워크플로우 초기 단계에서 이 엔드포인트를 사용하여 불필요한 오류를 방지하세요.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/check-cloud-service-health/">자세히 알아보기</a>

- **[Aspose.Cells Cloud 실행 상태 조회](https://docs.aspose.cloud/cells/get-aspose-cells-cloud-status/)**  
  서비스의 현재 실행 시간 상태를 조회합니다. 응답은 API가 정상 운영 중인지, 유지보수 중인지, 또는 문제가 발생했는지를 나타냅니다.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/get-aspose-cells-cloud-status/">자세히 알아보기</a>

- **[공개 키 조회](https://docs.aspose.cloud/cells/get-public-key/)**  
  Aspose.Cells Cloud에서 발급한 JWT 토큰을 검증하는 데 사용되는 RSA 공개 키(PEM 형식)를 가져옵니다. 서버 측에서 토큰을 검증할 때 이 키가 필요합니다.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/get-public-key/">자세히 알아보기</a>

- **[클라이언트 ID 및 시크릿을 사용해 액세스 토큰 조회](https://docs.aspose.cloud/cells/post-access-token/)**  
  **client_credentials** 부여 유형을 사용하여 OAuth 2.0 액세스 토큰을 생성합니다. 요청 본문에 **클라이언트 ID**와 **클라이언트 시크릿**을 포함하면, 응답에 `access_token`, `token_type`, `expires_in`이 포함됩니다. 이후 모든 API 호출 시 이 토큰을 `Authorization` 헤더에 포함해야 합니다.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/post-access-token/">자세히 알아보기</a>