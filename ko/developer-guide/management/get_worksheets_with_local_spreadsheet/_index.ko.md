---
title: "로컬 스프레드시트로 워크시트 가져오기"
ArticleTitle: "로컬 스프레드시트로 워크시트 가져오기 – Aspose.Cells Cloud"
second_title: "문서"
linktitle: "로컬 스프레드시트로 워크시트 가져오기"
type: docs
url: /ko/cells/spreadsheet/worksheets
aliases: []
keywords: "Aspose.Cells, 워크시트, 로컬 스프레드시트, API"
description: "현재 활성화된 로컬 스프레드시트에서 워크시트의 전체 목록을 가져옵니다."
weight: 1000
---

## Aspose.Cells Cloud 웹 서비스의 로컬 스프레드시트로 워크시트 가져오기 기능

이 엔드포인트는 인터롭 또는 로컬 API를 통해 로컬 스프레드시트 애플리케이션(예: Excel)에 액세스하여 각 워크시트의 이름과 유형(예: 표준, 차트, 매크로)을 수집하고, 이를 구조화된 JSON 배열로 반환합니다. 일반적으로 워크시트 선택 UI를 채우거나 스프레드시트 콘텐츠를 감사할 때 사용됩니다.

### 웹 API 엔드포인트

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/worksheets
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 강화되었으며 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름 | 유형   | 경로/쿼리 문자열/HTTP 본문 | 설명 |
|---------------|--------|-----------------------------|-------------|
| Spreadsheet   | 파일   | FormData (HTTP 본문)        | 스프레드시트 파일 업로드 |
| region        | 문자열 | 쿼리                        | 스프레드시트 지역/언어 설정(예: `en-US`, `fr-FR`). 숫자 서식, 날짜 파싱 및 로케일별 동작에 영향을 줍니다. *(선택 사항)* |
| password      | 문자열 | 쿼리                        | 스프레드시트 파일을 열기 위한 암호. *(선택 사항)* |

### 요청 본문 매개변수

| 매개변수 이름 | 유형 | 설명 |
|---------------|------|-------------|
| Spreadsheet   | 파일 | 스프레드시트 파일 업로드 |

### **응답**

```json
{
  "Worksheets": [
    {
      "Name": "Sheet1",
      "Id": 0,
      "Type": "Standard"
    },
    {
      "Name": "Chart1",
      "Id": 1,
      "Type": "Chart"
    }
    // ... 추가 워크시트
  ]
}
```

**응답 상태 코드**

| 코드 | 의미 | 설명 |
|------|------|------|
| 200 | OK | 워크시트 목록이 성공적으로 조회되었습니다. |
| 400 | Bad Request | 잘못된 요청(예: 잘못된 URL 또는 필수 데이터 누락) |
| 401 | Unauthorized | 인증 실패 또는 자격 증명이 제공되지 않았습니다. |
| 404 | Not Found | 소스 파일에 액세스할 수 없습니다. |
| 413 | Payload Too Large | 업로드된 파일이 허용된 크기 제한을 초과했습니다. |
| 500 | Internal Server Error | 데이터를 가져오는 동안 스프레드시트에 문제가 발생했습니다. |

## SDK를 사용하여 로컬 스프레드시트로 워크시트 가져오기 사용 방법

### 로컬 스프레드시트로 워크시트 가져오기 API 사양

[로컬 스프레드시트로 워크시트 가져오기 API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetWorksheetsWithLocalSpreadsheet)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells Cloud 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예시는 cURL을 사용하여 Cloud API에 호출을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
# 보안 연결을 위해 HTTPS 사용
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/worksheets?region=en-US&password=yourPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@example.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Worksheets": [
    {
      "Name": "Sheet1",
      "Id": 0,
      "Type": "Standard"
    },
    {
      "Name": "Chart1",
      "Id": 1,
      "Type": "Chart"
    }
    // ... 추가 워크시트
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose Cells Cloud SDK 사용

SDK를 사용하는 것이 개발을 가장 빠르게 가속화하는 방법입니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 작업에 집중할 수 있도록 합니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하십시오.

다음 코드 예시는 다양한 SDK를 사용하여 Aspose.Cells Cloud 웹 서비스를 호출하는 방법을 보여줍니다:
`[TBD]`
---