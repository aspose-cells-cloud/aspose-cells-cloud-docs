---
title: "FlipData"
ArticleTitle: "FlipData – Aspose.Cells Cloud"
second_title: "문서"
linktitle: "FlipData"
type: docs
url: /cells/flip
aliases: []
keywords: "FlipData, 변환, Aspose.Cells"
description: "스프레드시트 파일 내 지정된 데이터 범위를 전치합니다."
weight: 100
---

## Aspose.Cells Cloud 웹 서비스의 FlipData

이 API는 주어진 데이터 행렬의 방향을 뒤집습니다. 예를 들어, 3x2 범위(3행 2열)는 출력 시 2x3 범위(2행 3열)로 변환됩니다. 이 기능은 다양한 차트, 보고서 또는 데이터 모델의 입력 요구 사항에 맞춰 데이터를 재구성할 때 일반적으로 사용됩니다.

### 웹 API 엔드포인트

```http
PUT https://api.aspose.cloud/v4.0/cells/flip
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 위해 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 파라미터

| 파라미터 이름 | 타입    | 경로/쿼리 문자열/HTTP 본문 | 설명 |
|---------------|---------|-----------------------------|------|
| Spreadsheet   | 파일    | FormData                    | 스프레드시트 파일 업로드 |
| worksheet     | 문자열  | 쿼리                        | 워크시트 이름 |
| cellArea      | 문자열  | 쿼리                        | 지정된 데이터 범위 |
| Horizontal    | 불리언  | 쿼리                        | 가로/세로 뒤집기. 기본값: true |
| outPath       | 문자열  | 쿼리                        | (선택 사항) 워크북이 저장될 폴더 경로. 기본값은 null입니다. |
| outStorageName| 문자열  | 쿼리                        | 출력 파일의 저장소 이름 |
| region        | 문자열  | 쿼리                        | 스프레드시트 지역/언어 설정(예: `en-US`, `fr-FR`). 숫자 서식, 날짜 파싱 및 지역 고유 동작에 영향을 미칩니다. |
| password      | 문자열  | 쿼리                        | 스프레드시트 파일을 열기 위한 비밀번호 |

### 요청 본문 파라미터

| 파라미터 이름 | 타입 | 설명 |
| -------------- | ---- | ----------- |
| *없음* | *해당 없음* | *추가적인 JSON 본문은 필요하지 않습니다. 파일은 multipart/form-data로 전송됩니다.* |

### **응답**

```json
{
  "File": "<변환된 워크북의 이진 스트림>"
}
```

**응답 상태 코드**

| 코드 | 의미 | 설명 |
|------|------|------|
| 200 | 성공 | 작업이 성공적으로 완료되었으며, 변환된 스프레드시트 파일이 반환됩니다. |
| 400 | 잘못된 요청 | 하나 이상의 필수 파라미터가 누락되었거나 유효하지 않습니다. |
| 401 | 인증 실패 | 인증에 실패했습니다 – JWT 토큰이 누락되었거나 유효하지 않습니다. |
| 413 | 페이로드가 너무 큼 | 업로드된 파일이 허용된 크기 제한을 초과했습니다. |
| 500 | 내부 서버 오류 | 서버에서 예기치 않은 오류가 발생했습니다. |

## SDK를 사용한 FlipData 활용 방법

### FlipData 사양

[FlipData API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TransformController/FlipData)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells Cloud 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용해 클라우드 API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
# 안전한 연결을 위해 HTTPS 사용
curl -v "https://api.aspose.cloud/v4.0/cells/flip?worksheet=Sheet1&cellArea=A1:B3&Horizontal=true&outPath=output%2Ffolder&outStorageName=MyStorage&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "File": "<변환된 워크북의 이진 스트림>"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 가장 빠르게 높일 수 있습니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 작업에 집중할 수 있도록 해줍니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 참조하십시오.

다음 코드 예제는 다양한 SDK를 사용해 Aspose Cells Cloud 웹 서비스를 호출하는 방법을 보여줍니다:
 `[TBD]`
---