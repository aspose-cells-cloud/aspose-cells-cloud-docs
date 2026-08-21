---
title: "GetMergedCellsInRemotedWorksheet"
ArticleTitle: "원격 워크시트의 병합 셀 가져오기 – Aspose.Cells Cloud API"
second_title: "문서"
linktitle: "원격 워크시트의 병합 셀 가져오기"
type: docs
url: /ko/cells/mergedcells/get
aliases: []
keywords: "Aspose Cells, 병합 셀 가져오기, 원격 워크시트, API"
description: "스프레드시트의 원격 워크시트에서 모든 병합 셀 영역을 검색합니다."
weight: 10
---

## Aspose.Cells Cloud 웹 서비스의 GetMergedCellsInRemotedWorksheet

원격 스프레드시트 워크시트에서 모든 병합 셀 영역을 가져옵니다.

### 웹 API 엔드포인트

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/mergedcells
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 위해 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름 | 유형 | 경로/쿼리 문자열/HTTP 본문 | 설명 |
|----------------|--------|-----------------------------|-------------|
| name | string | 경로 | 스프레드시트 이름 |
| worksheet | string | 경로 | 워크시트 이름 |
| folder | string | 쿼리 | 스프레드시트의 클라우드 스토리지 경로 |
| storageName | string | 쿼리 | (선택 사항) 사용자 지정 클라우드 스토리지를 사용할 경우 스토리지 이름. 생략 시 기본 스토리지를 사용합니다. |
| region | string | 쿼리 | 스프레드시트의 지역/언어 설정(예: `en-US`, `fr-FR`). 숫자 서식, 날짜 파싱 및 로케일 관련 동작에 영향을 줍니다. |
| password | string | 쿼리 | 스프레드시트 파일을 열기 위한 비밀번호 |

### 요청 본문 매개변수

| 매개변수 이름 | 유형 | 설명 |
| -------------- | ---- | ----------- |
| — | — | *없음* |

### **응답**

```json
[
  {
    "FirstRow": 0,
    "FirstColumn": 0,
    "TotalRows": 2,
    "TotalColumns": 3
  },
  {
    "FirstRow": 5,
    "FirstColumn": 1,
    "TotalRows": 1,
    "TotalColumns": 4
  }
]
```

**응답 상태 코드**

| 코드 | 의미 | 설명 |
|------|---------|-------------|
| 200 | OK | 요청이 성공했으며 병합 셀 영역 목록이 반환되었습니다. |
| 400 | Bad Request | 잘못된 URL이거나 요청 매개변수가 잘못되었습니다. |
| 401 | Unauthorized | 인증에 실패했거나 자격 증명이 제공되지 않았습니다. |
| 413 | Payload Too Large | 요청 페이로드가 허용된 크기를 초과했습니다. |
| 500 | Internal Server Error | 데이터를 가져오는 중 스프레드시트에 문제가 발생했습니다. |

## SDK를 사용하여 GetMergedCellsInRemotedWorksheet 사용하는 방법

### GetMergedCellsInRemotedWorksheet 사양

[GetMergedCellsInRemotedWorksheet API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetMergedCellsInRemotedWorksheet)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
# 보안 연결을 위해 HTTPS 사용
curl -v "https://api.aspose.cloud/v4.0/cells/Sample.xlsx/worksheets/Sheet1/mergedcells?folder=MyFolder&storageName=MyStorage&region=en-US&password=1234" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
[
  {
    "FirstRow": 0,
    "FirstColumn": 0,
    "TotalRows": 2,
    "TotalColumns": 3
  },
  {
    "FirstRow": 5,
    "FirstColumn": 1,
    "TotalRows": 1,
    "TotalColumns": 4
  }
]
```

{{< /tab >}}

{{< /tabs >}}

### Aspose Cells Cloud SDK 사용

SDK를 사용하면 개발 속도가 가장 빠르게 향상됩니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 작업에 집중할 수 있도록 해줍니다. Aspose.Cells Cloud SDK 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose Cells Cloud 웹 서비스를 호출하는 방법을 보여줍니다:
`[TBD]`
---