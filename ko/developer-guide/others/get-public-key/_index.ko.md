---
title: "Aspose.Cells Cloud API – 공개 키 가져오기(v4.0) | REST 문서"
second_title: "문서"
ArticleTitle: "공개 키 가져오기"
linktype: "공개 키 가져오기"
type: docs
url: /ko/get-public-key/
keywords: "Aspose.Cells, 공개 키, RSA, API, 클라우드"
description: "Aspose.Cells Cloud에서 데이터 암호화에 사용되는 RSA 공개 키를 검색합니다. 엔드포인트, 매개변수, 샘플 요청/응답, 상태 코드 및 SDK 사용 예제가 포함되어 있습니다."
weight: 100
---

이 API는 비대칭 암호화 알고리즘에서 공개 키를 검색합니다.

**간단 요약:** Aspose.Cells 공개 키 가져오기 API를 사용하여 클라우드에서 엑셀 파일을 작업할 때 데이터를 암호화하는 데 필요한 RSA 공개 키(2048비트)를 가져옵니다. 이 엔드포인트는 JSON 형식으로 키를 반환하며, OAuth 2.0으로 보호됩니다.

## **공개 키 가져오기 API**

**필수 조건:**  
이 엔드포인트를 호출하기 전에 `Cells.Read` 범위를 포함하는 유효한 OAuth 2.0 액세스 토큰을 획득해야 합니다.

### **웹 API**

```
GET https://api.aspose.cloud/v4.0/cells/publickey
```

**샘플 요청(cURL)**

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/publickey" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 강화되어 있으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **요청 매개변수:**

| 매개변수 이름 | 유형   | 위치   | 설명                                                                       |
| ------------- | ------ | ------ | -------------------------------------------------------------------------- |
| Authorization | string | 헤더   | OAuth2 인증용 베어러 토큰(필수).                                             |
| Accept        | string | 헤더   | 원하는 응답 형식(예: `application/json`, 선택 사항이며 기본값은 JSON).      |

### **응답**

```json
{
  "Code": 200,
  "Status": "OK",
  "CellsCloudPublicKey": {
    "PublicKey": "MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAr...",
    "Algorithm": "RSA",
    "KeySize": 2048
  }
}
```

**HTTP 상태 코드**

| 코드 | 의미                  | 설명                                                            |
| ---- | --------------------- | --------------------------------------------------------------- |
| 200  | OK                    | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함.          |
| 400  | 잘못된 요청           | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식).        |
| 401  | 인증되지 않음         | 잘못되거나 누락된 JWT 토큰.                                      |
| 413  | 페이로드 너무 큼      | 업로드된 파일이 크기 제한을 초과함.                             |
| 500  | 내부 서버 오류        | 예기치 않은 서버 오류.                                           |

## SDK를 사용하여 공개 키 가져오기 API 사용 방법

### OpenAPI 사양

[OpenAPI 사양](https://reference.aspose.cloud/cells/#/KeyController/GetPublicKey)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하여 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

### Aspose.Cells Cloud SDK 사용

SDK를 사용하는 것이 개발 속도를 높이는 최선의 방법입니다. SDK는 기본 세부 사항을 처리하므로 최소한의 코드로.cells 공개 키 가져오기를 간단히 구현할 수 있습니다.  
Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

아래는 가장 일반적인 언어에 대한 구체적인 예제입니다:

---