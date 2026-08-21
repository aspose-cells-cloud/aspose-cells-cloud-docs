---
title: "GetStructureInRemoteSpreadsheet"
ArticleTitle: "원격 스프레드시트에서 구조 가져오기 – Aspose.Cells Cloud API"
second_title: "문서"
linktype: "GetStructureInRemoteSpreadsheet"
type: docs
url: /ko/cells/{name}/structure
aliases: []
keywords: "Aspose.Cells, GetStructure, 스프레드시트, 구조"
description: "원격 엑셀 워크북의 워크시트, 테이블, 피벗테이블, 차트, 도형 등 핵심 정보를 포함한 구조 메타데이터를 조회합니다."
weight: 100
---

## Aspose.Cells Cloud 웹 서비스의 원격 스프레드시트에서 구조 가져오기 기능

엑셀 워크북의 핵심 메타데이터, 워크시트, 테이블, 피벗테이블, 차트, 도형 등의 정보를 JObject 타입의 JSON 객체로 구조화하여, 데이터 내보내기, API 응답, 로그 기록 등에 활용합니다.

### 웹 API 엔드포인트

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/structure
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 보장되며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 파라미터

| 파라미터 이름 | 타입 | 경로/쿼리 문자열/HTTP 본문 | 설명 |
|----------------|------|-----------------------------|-------------|
| name | string | Path | 스프레드시트 파일의 이름입니다. |
| folder | string | Query | 파일이 위치한 폴더입니다. (선택 사항) |
| storageName | string | Query | (선택 사항) 사용자 정의 클라우드 스토리지를 사용할 경우 스토리지 이름입니다. 생략 시 기본 스토리지를 사용합니다. |
| region | string | Query | 스프레드시트 지역/언어 설정(예: `en-US`, `fr-FR`)입니다. 숫자 서식, 날짜 파싱, 지역별 동작에 영향을 줍니다. |
| password | string | Query | 스프레드시트 파일을 열기 위한 비밀번호입니다. |

### 요청 본문 파라미터

| 파라미터 이름 | 타입 | 설명 |
| -------------- | ---- | ----------- |
| [TBD] | [TBD] | [TBD] |

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
  "WorkbookProperties": {
    "Author": "string",
    "Created": "string",
    "Version": "string"
  },
  "DocumentProperties": {
    "Title": "string",
    "Subject": "string",
    "Keywords": "string"
  }
}
```

**응답 상태 코드**

| 코드 | 의미 | 설명 |
|------|------|-------------|
| 200 | OK | 워크북 구조를 성공적으로 조회했습니다. |
| 400 | Bad Request | 요청 파라미터가 유효하지 않습니다. |
| 401 | Unauthorized | 인증에 실패했거나 토큰이 없습니다. |
| 413 | Payload Too Large | 요청 본문 크기가 허용된 크기를 초과했습니다. |
| 500 | Internal Server Error | 예기치 않은 서버 오류가 발생했습니다. |

## SDK를 사용하여 원격 스프레드시트에서 구조 가져오기 사용 방법

### 원격 스프레드시트에서 구조 가져오기 사양

[원격 스프레드시트에서 구조 가져오기 API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetStructureInRemoteSpreadsheet)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용해 클라우드 API에 요청하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
# 보안 연결을 위해 HTTPS 사용
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/structure?folder=myFolder&storageName=MyStorage&region=en-US&password=SecretPwd" \
  -X GET \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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
  "WorkbookProperties": {
    "Author": "John Doe",
    "Created": "2023-01-01T12:00:00Z",
    "Version": "16.0"
  },
  "DocumentProperties": {
    "Title": "SalesReport",
    "Subject": "Quarterly Sales",
    "Keywords": "sales,report,2023"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose Cells Cloud SDK 사용하기

SDK를 사용하면 가장 빠르게 개발을 가속화할 수 있습니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 작업에 집중할 수 있도록 도와줍니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하십시오.

다음 코드 예제는 다양한 SDK를 사용해 Aspose Cells Cloud 웹 서비스를 호출하는 방법을 보여줍니다:
`[TBD]`
---