---
title: "Aspose.Cells Cloud 평가"
second_title: "문서"
ArticleTitle: "Aspose.Cells Cloud 평가"
LinkTitle: "평가"
type: docs
url: /evaluate-aspose-cells/
description: "Excel 파일 및 기타 스프레드시트 형식을 생성, 변환, 병합, 분할, 보호 및 조작하기 위한 REST API인 Aspose.Cells Cloud를 탐색하세요."
weight: 60
keywords:
  - Aspose.Cells Cloud
  - Excel API
  - REST API
  - 스프레드시트 조작
  - 무료 체험
  - 평가
---

Aspose Cloud 대시보드에서 무료 체험 계정을 생성하여 **Aspose.Cells Cloud** REST API를 평가할 수 있습니다. 등록 후 **클라이언트 ID**(Client Id)와 **클라이언트 시크릿**(Client Secret)을 받아 매월 최대 150회까지 API 호출을 수행할 수 있습니다.

**사전 요구 사항**  
시작하기 전에 활성 인터넷 연결과 지원되는 개발 환경이 준비되어 있는지 확인하세요. API는 HTTP를 통해 직접 호출할 수도 있으며, 보다 쉬운 통합을 위해 Aspose.Cells SDK(.NET, Java, Python, PHP 등)를 사용할 수 있습니다.

**빠른 시작 단계**

1. **무료 체험 계정 생성** – [Aspose Cloud 대시보드](https://dashboard.aspose.cloud)에 접속해 가입한 후 이메일 주소를 확인하세요.  
2. **자격 증명 획득** – 대시보드의 **인증**(Authentication) 섹션에서 *클라이언트 ID*와 *클라이언트 시크릿*을 확인하세요.  
3. **액세스 토큰 생성** – 자격 증명(`grant_type=client_credentials`, `client_id`, `client_secret`을 폼 URL 인코딩 형식으로)을 포함하여 `POST` 요청을 `https://api.aspose.cloud/connect/token`으로 보내세요(정확한 요청 본문 내용은 API 참조를 참고하세요).  
4. **첫 API 호출 수행** – `Authorization: Bearer <token>` 헤더에 토큰을 포함시켜 `GET https://api.aspose.cloud/v3.0/cells/{file}/worksheets`와 같은 간단한 엔드포인트를 호출하세요.  

무료 체험을 통해 서비스의 기능을 실제로 경험해보고, 아무런 비용 없이 초기 개발 및 테스트를 진행할 수 있습니다.

**API 참조 요약**

| 작업 | 메서드 | URL | 필수 파라미터 | 샘플 응답 |
|------|--------|-----|----------------|-----------|
| 액세스 토큰 받기 | POST | `https://api.aspose.cloud/connect/token` | `grant_type=client_credentials`, `client_id`, `client_secret` (폼 URL 인코딩) | `{ "access_token": "eyJ0eXAi...", "expires_in": 3600 }` |
| 워크시트 목록 조회 | GET | `https://api.aspose.cloud/v3.0/cells/{file}/worksheets` | 경로: `{file}` – 업로드된 워크북의 이름; 헤더: `Authorization: Bearer <token>` | `{ "Worksheets": { "WorksheetList": [ { "Name": "Sheet1" }, { "Name": "Sheet2" } ] } }` |

세부 가격 정보, 사용 한도 및 추가 요금제 옵션은 [체험 요금제](https://purchase.aspose.cloud/trial) 페이지를 참고하세요.