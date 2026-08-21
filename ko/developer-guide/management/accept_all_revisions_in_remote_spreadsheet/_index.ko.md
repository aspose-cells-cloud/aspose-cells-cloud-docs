---
title: "원격 스프레드시트에서 모든 수정사항 수락하기"
ArticleTitle: "원격 스프레드시트에서 모든 수정사항 수락하기 – Aspose.Cells Cloud"
second_title: "문서"
linktitle: "원격 스프레드시트에서 모든 수정사항 수락하기"
type: docs
url: /ko/cells/accept-all-revisions
aliases: [  /ko/cells/accept-all-revisions ]
keywords: "Aspose.Cells, AcceptAllRevisions, 원격 스프레드시트"
description: "원격 스프레드시트에서 모든 수정사항을 수락하고 업데이트된 워크북 파일을 반환합니다."
weight: 1000
---

## Aspose.Cells Cloud 웹 서비스의 원격 스프레드시트에서 모든 수정사항 수락하기 기능

원격 저장소에 저장된 지정된 워크북에서 추적된 모든 변경사항(수정사항)을 수락합니다. 이 작업은 선택적으로 결과 워크북을 다른 위치 또는 저장소에 저장하고 업데이트된 파일을 바이너리 스트림으로 반환합니다.

### 웹 API 엔드포인트

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/accept-all-revisions
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 보장되며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 파라미터

| 파라미터 이름 | 타입 | 경로/쿼리 문자열/HTTP 본문 | 설명 |
|----------------|------|-----------------------------|-------------|
| name | string | Path | 원격 저장소에 저장된 워크북 파일 이름 |
| folder | string | Query | (선택 사항) 워크북이 위치한 저장소 내 폴더 |
| storageName | string | Query | (선택 사항) 사용자 정의 클라우드 저장소를 사용할 경우 저장소 이름. 생략 시 기본 저장소 사용 |
| outPath | string | Query | (선택 사항) 업데이트된 워크북을 저장할 폴더 경로. 기본값은 null |
| outStorageName | string | Query | (선택 사항) 출력 파일을 저장할 저장소 이름 |
| fontsLocation | string | Query | (선택 사항) 사용자 정의 글꼴 위치 경로 |
| region | string | Query | (선택 사항) 스프레드시트 지역/언어 설정(예: `en-US`, `fr-FR`). 숫자 형식, 날짜 파싱, 지역별 동작에 영향을 줌 |
| password | string | Query | (선택 사항) 스프레드시트 파일을 열기 위한 비밀번호 |

### 요청 본문 파라미터

| 파라미터 이름 | 타입 | 설명 |
| -------------- | ---- | ----------- |
| *없음* | *없음* | 이 작업은 요청 본문이 필요하지 않습니다. |

### **응답**

```json
{
  "File": "업데이트된 워크북의 바이너리 스트림(예: .xlsx)이 응답 본문으로 반환됩니다."
}
```

**응답 상태 코드**

| 코드 | 의미 | 설명 |
|------|------|-------------|
| 200 | OK | 모든 수정사항이 수락된 워크북이 바이너리 파일 스트림으로 반환됩니다. |
| 400 | Bad Request | 필수 파라미터 누락 또는 잘못된 요청 형식 |
| 401 | Unauthorized | 잘못되거나 누락된 JWT 토큰 |
| 413 | Payload Too Large | 요청 크기가 허용된 제한을 초과함 |
| 500 | Internal Server Error | 서버에서 예기치 않은 오류 발생 |

## SDK를 사용하여 원격 스프레드시트에서 모든 수정사항 수락하기 사용 방법

### 원격 스프레드시트에서 모든 수정사항 수락하기 사양

[원격 스프레드시트에서 모든 수정사항 수락하기 API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/AcceptAllRevisionsInRemoteSpreadsheet)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose Cells Cloud 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예제는 cURL을 사용해 클라우드 API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
# 안전한 연결을 위해 HTTPS 사용
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/accept-all-revisions?folder=myFolder&storageName=MyStorage&outPath=output%2Fupdated.xlsx&outStorageName=OutStorage&fontsLocation=%2Fcustom%2Ffonts&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "File": "업데이트된 워크북의 바이너리 스트림(예: .xlsx)."
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 가장 빠르게 향상시킬 수 있습니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 작업에 집중할 수 있게 해줍니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose Cells Cloud 웹 서비스를 호출하는 방법을 보여줍니다:
 `[TBD]`
---