---
title: "테이블 언피벗"
ArticleTitle: "테이블 언피벗 – Aspose.Cells Cloud API"
second_title: "문서"
linktype: "docs"
url: /cells/unpivot/table
aliases: []
keywords: "Aspose.Cells, 언피벗, 변환"
description: "스프레드시트에서 행과 열을 전환합니다."
weight: 1
---

## Aspose.Cells Cloud 웹 서비스의 테이블 언피벗

스프레드시트에서 행과 열을 전환합니다.

### 웹 API 엔드포인트

```http
PUT https://api.aspose.cloud/v4.0/cells/unpivot/table
```

### **보안 및 인증**

Aspose.Cells Cloud API는 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요하며, 보안이 확보되어 있습니다.

### 요청 매개변수

| 매개변수 이름     | 유형      | 경로/쿼리 문자열/HTTP 본문 | 설명                                                                                                              |
|------------------|-----------|-----------------------------|-------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | 파일      | FormData                    | 업로드할 스프레드시트 파일.                                                                                        |
| worksheet        | 문자열    | 쿼리                        | 워크시트 이름.                                                                                                     |
| index            | 정수      | 쿼리                        | 지정된 데이터 범위.                                                                                                |
| skipEmptyValue   | 부울값    | 쿼리                        | 빈 값을 건너뜀 (기본값: true).                                                                                     |
| outPath          | 문자열    | 쿼리                        | (선택 사항) 워크북이 저장될 폴더 경로. 기본값은 null입니다.                                                        |
| outStorageName   | 문자열    | 쿼리                        | 출력 파일의 저장소 이름.                                                                                           |
| region           | 문자열    | 쿼리                        | 스프레드시트 지역/언어 설정(예: `en-US`, `fr-FR`). 숫자 포맷팅, 날짜 파싱 및 로케일별 동작에 영향을 줍니다.         |
| password         | 문자열    | 쿼리                        | 스프레드시트 파일을 열기 위한 비밀번호.                                                                            |

### 요청 본문 매개변수

| 매개변수 이름 | 유형 | 설명 |
| -------------- | ---- | ----------- |
| 없음            | 없음  | 요청 본문 매개변수가 없습니다. |

### **응답**

```json
{
  "File": "언피벗된 스프레드시트의 바이너리 스트림"
}
```

**응답 상태 코드**

| 코드 | 의미 | 설명 |
|------|------|------|
| 200 | 성공 | 언피벗된 스프레드시트 파일이 반환됩니다. |
| 400 | 잘못된 요청 | 잘못된 요청 매개변수입니다. |
| 401 | 인증 실패 | 인증에 실패했거나 JWT 토큰이 누락되었거나 유효하지 않습니다. |
| 413 | 페이로드가 너무 큼 | 업로드된 파일이 허용된 크기 제한을 초과했습니다. |
| 500 | 내부 서버 오류 | 예기치 않은 서버 오류가 발생했습니다. |

## SDK를 사용한 테이블 언피벗 사용 방법

### 테이블 언피벗 사양

[테이블 언피벗 API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4# /Transform/UnpivotTable)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API에 요청을 보내는 방법을 보여줍니다.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# 보안 연결을 위해 HTTPS 사용
curl -v "https://api.aspose.cloud/v4.0/cells/unpivot/table?worksheet={worksheet}&index={index}&skipEmptyValue={skipEmptyValue}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "File": "언피벗된 스프레드시트의 바이너리 스트림"
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 가장 빠르게 향상시킬 수 있습니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 작업에 집중할 수 있도록 해줍니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose Cells Cloud 웹 서비스를 호출하는 방법을 보여줍니다:
 `[TBD]`
---