---
title: "GetSpreadsheetStructure"
ArticleTitle: "GetSpreadsheetStructure – Aspose.Cells Cloud"
second_title: "문서"
linktype: "docs"
url: /cells/spreadsheet/structure
aliases: []
keywords: "Aspose.Cells, 스프레드시트 구조, API"
description: "Excel 워크북의 핵심 메타데이터, 워크시트, 테이블, 피벗 테이블, 차트, 도형 및 기타 정보를 JObject 유형의 JSON 객체로 구조적으로 변환합니다."
weight: 1000
---

## Aspose.Cells Cloud 웹 서비스의 GetSpreadsheetStructure

Excel 워크북의 핵심 메타데이터, 워크시트, 테이블, 피벗 테이블, 차트, 도형 및 기타 정보를 JObject 유형의 JSON 객체로 구조적으로 변환하여 데이터 내보내기, API 응답 및 로그 기록 등의 시나리오에 활용합니다.

### 웹 API 엔드포인트

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/structure
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 유지되며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름 | 유형   | 경로/쿼리 문자열/HTTP 본문 | 설명 |
|---------------|--------|-----------------------------|------|
| Spreadsheet   | 파일   | FormData (본문)             | 업로드할 스프레드시트 파일입니다. |
| region        | 문자열 | 쿼리                        | 스프레드시트 지역/언어 설정(예: `en-US`, `fr-FR`). 숫자 서식, 날짜 파싱 및 로케일 관련 동작에 영향을 미칩니다. |
| password      | 문자열 | 쿼리                        | 스프레드시트 파일을 열기 위한 비밀번호입니다. |

### 요청 본문 매개변수

| 매개변수 이름 | 유형 | 설명 |
|---------------|------|------|
| Spreadsheet   | 파일 | 업로드할 스프레드시트 파일입니다. |

### **응답**

```json
{
  "Worksheets": [
    {
      "Name": "Sheet1",
      "Tables": [],
      "PivotTables": [],
      "Charts": [],
      "Shapes": []
    }
  ],
  "DocumentProperties": {
    "Author": "John Doe",
    "Created": "2023-01-01T12:00:00Z"
  }
}
```

**응답 상태 코드**

| 코드 | 의미 | 설명 |
|------|------|------|
| 200 | 성공 | 스프레드시트 구조를 성공적으로 가져왔습니다. |
| 400 | 잘못된 요청 | 요청 매개변수 또는 파일 형식이 유효하지 않습니다. |
| 401 | 인증 실패 | 인증에 실패했거나 JWT 토큰이 누락되었습니다. |
| 413 | 페이로드가 너무 큼 | 업로드된 파일이 허용된 크기 제한을 초과했습니다. |
| 500 | 내부 서버 오류 | 서버에서 예기치 않은 오류가 발생했습니다. |

## SDK를 사용하여 GetSpreadsheetStructure 사용 방법

### GetSpreadsheetStructure 사양

[GetSpreadsheetStructure API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetSpreadsheetStructure)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose Cells Cloud 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
# 보안 연결을 위해 HTTPS 사용
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/structure?region=en-US&password=yourPassword" \
  -X PUT \
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
      "Tables": [],
      "PivotTables": [],
      "Charts": [],
      "Shapes": []
    }
  ],
  "DocumentProperties": {
    "Author": "John Doe",
    "Created": "2023-01-01T12:00:00Z"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 가장 빠르게 높일 수 있습니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 작업에 집중할 수 있게 해줍니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose Cells Cloud 웹 서비스를 호출하는 방법을 보여줍니다:
`[TBD]`
---