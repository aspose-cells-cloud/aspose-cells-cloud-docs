---
title: "범위를 CSV로 변환"
ArticleTitle: "범위를 CSV로 변환 – Aspose.Cells Cloud API"
second_title: "문서"
linktitle: "범위를 CSV로 변환"
type: docs
url: /ko/cells/convert/range/csv
aliases: []
keywords: "변환, csv, 범위, Aspose.Cells"
description: "로컬 드라이브의 스프레드시트 범위를 CSV 파일로 변환합니다."
weight: 1
---

## Aspose.Cells Cloud 웹 서비스의 범위를 CSV로 변환

이 작업은 로컬 파일 시스템에서 스프레드시트 파일을 읽어 지정된 범위를 CSV 형식으로 변환한 후 변환 결과를 직접 반환합니다. 이 작업은 클라우드 서버에서 완전히 처리되므로 클라우드 저장소로 중간 업로드가 필요하지 않습니다. 이 API는 사용자 정의 폰트, 행/열 자동 맞춤, 로케일 설정, 암호 보호 워크북 등의 선택적 매개변수를 지원합니다.

### 웹 API 엔드포인트

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/csv
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 위해 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>을 요구합니다.

### 요청 매개변수

| 매개변수 이름    | 유형    | 경로/쿼리 문자열/HTTP 본문 | 설명                                                                                                                            |
|------------------|---------|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | 파일    | FormData                    | 스프레드시트 파일 업로드.                                                                                                               |
| worksheet        | 문자열  | 쿼리                        | 스프레드시트의 워크시트 이름. **필수**.                                                                                           |
| range            | 문자열  | 쿼리                        | 셀 영역. 예: `A1:C10`. **필수**.                                                                                                 |
| outPath          | 문자열  | 쿼리                        | (선택 사항) 워크북이 저장될 폴더 경로. 기본값은 null입니다.                                                          |
| outStorageName   | 문자열  | 쿼리                        | 출력 파일 저장소 이름.                                                                                                              |
| fontsLocation    | 문자열  | 쿼리                        | 사용자 정의 폰트 사용.                                                                                                                      |
| AutoRowsFit      | 불리언  | 쿼리                        | (선택 사항) 워크시트의 모든 행을 자동으로 맞춥니다.                                                                                            |
| AutoColumnsFit   | 불리언  | 쿼리                        | (선택 사항) 워크시트의 모든 열을 자동으로 맞춥니다.                                                                                         |
| region           | 문자열  | 쿼리                        | 스프레드시트 지역/언어 설정(예: `en-US`, `fr-FR`). 숫자 서식, 날짜 파싱 및 로케일 관련 동작에 영향을 줍니다. |
| password         | 문자열  | 쿼리                        | 스프레드시트 파일을 열기 위한 암호.                                                                                             |

### 요청 본문 매개변수

| 매개변수 이름 | 유형 | 설명 |
| -------------- | ---- | ----------- |
| 없음 | N/A | 요청 본문 매개변수가 없습니다. |

### **응답**

```json
{
  "ResponseFile": "바이너리 파일 스트림 (CSV 콘텐츠)"
}
```

**응답 상태 코드**

| 코드 | 의미 | 설명 |
|------|---------|-------------|
| 200 | 성공 | 범위가 성공적으로 변환되었으며, CSV 파일이 응답 본문에 반환됩니다. |
| 400 | 잘못된 요청 | 잘못된 URL이거나 필수 매개변수가 누락되었습니다. |
| 401 | 인증 실패 | 인증에 실패했거나 자격 증명이 제공되지 않았습니다. |
| 413 | 요청 페이로드가 너무 큼 | 요청 페이로드가 허용된 크기 제한을 초과했습니다. |
| 500 | 내부 서버 오류 | 스프레드시트가 변환 데이터를 가져오는 도중 오류가 발생했습니다. |

## SDK를 사용하여 범위를 CSV로 변환하는 방법

### 범위를 CSV로 변환 사양

[범위를 CSV로 변환 API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToCsv)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
# 보안 연결을 위해 HTTPS 사용
curl -v "https://api.aspose.cloud/v4.0/cells/convert/range/csv?worksheet=Sheet1&range=A1:C10&outPath=outputFolder&outStorageName=MyStorage&fontsLocation=/custom/fonts&AutoRowsFit=true&AutoColumnsFit=true&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@sample.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "ResponseFile": "Base64로 인코딩된 CSV 콘텐츠"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 최대한 빠르게 향상시킬 수 있습니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 작업에 집중할 수 있도록 해줍니다. Aspose.Cells Cloud SDK 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose Cells Cloud 웹 서비스를 호출하는 방법을 보여줍니다:
`[TBD]`
---