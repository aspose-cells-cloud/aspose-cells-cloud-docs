---
title: "테이블 분할"
ArticleTitle: "테이블 분할 – Aspose.Cells Cloud API"
second_title: "문서"
linktype: "docs"
url: /ko/cells/split/table
aliases: []
keywords: "Aspose.Cells, 테이블 분할, API"
description: "스preadsheet에서 테이블을 열 값별로 분할하는 API입니다."
weight: 1
---

## Aspose.Cells Cloud 웹 서비스의 SplitTable

이 메서드는 지정된 열의 고유한 값에 따라 행을 그룹화하여 소스 테이블을 분할합니다. 각 데이터 그룹(고유 분할 값별)은 별도의 데이터 단위로 처리됩니다. 내보내기 대상은 두 가지 핵심 불리언 매개변수에 의해 제어됩니다:
- 워크북 구조를 결정합니다. `true`인 경우 각 분할 단위가 별도의 워크북 파일로 저장됩니다. `false`인 경우 각 단위가 현재 워크북 내의 새 워크시트가 됩니다.
- 출력 패키징을 결정합니다. `true`로 설정하고 `toNewWorkbook` = `true`와 함께 사용하면 여러 개의 개별 파일이 생성되어 ZIP 아카이브로 반환됩니다. `false`인 경우 모든 데이터가 단일 파일(다중 시트 워크북 또는 기타 설정에 따라 단일 파일)로 통합됩니다.

### 웹 API 엔드포인트

```http
PUT https://api.aspose.cloud/v4.0/cells/split/table
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 확보하며 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름     | 유형      | 경로/쿼리 문자열/HTTP 본문 | 설명                                                                                                                                                      |
|------------------|-----------|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | 파일      | FormData                    | 스프레드시트 파일 업로드.                                                                                                                                  |
| worksheet        | 문자열    | 쿼리                        | 테이블이 포함된 워크시트.                                                                                                                                  |
| tableName        | 문자열    | 쿼리                        | 분할할 데이터 테이블.                                                                                                                                      |
| splitColumnName  | 문자열    | 쿼리                        | 기준이 되는 열 이름.                                                                                                                                       |
| saveSplitColumn  | 불리언    | 쿼리                        | 분할 열의 데이터를 유지할지 여부.                                                                                                                          |
| splitRowNumber   | 정수      | 쿼리                        | [TBD]                                                                                                                                                      |
| toNewWorkbook    | 불리언    | 쿼리                        | 내보내기 대상 제어: true - 분할된 데이터를 포함한 새 워크북 파일 생성; false - 현재 워크북에 새 워크시트 추가.                                            |
| toMultipleFiles  | 불리언    | 쿼리                        | true - 테이블 데이터를 **여러 개별 파일**(ZIP 아카이브로 반환)로 내보내기; false - 다중 시트 워크북 또는 다른 설정에 따라 **단일 파일**로 모든 데이터 저장. 기본값: false. |
| outPath          | 문자열    | 쿼리                        | (선택 사항) 워크북이 저장될 폴더 경로. 기본값은 null입니다.                                                                                               |
| outStorageName   | 문자열    | 쿼리                        | 출력 파일 저장소 이름.                                                                                                                                     |
| fontsLocation    | 문자열    | 쿼리                        | 사용자 정의 글꼴 사용.                                                                                                                                     |
| region           | 문자열    | 쿼리                        | 스프레드시트 지역/언어 설정(예: `en-US`, `fr-FR`). 숫자 서식, 날짜 파싱, 지역별 동작에 영향을 미칩니다.                                                   |
| password         | 문자열    | 쿼리                        | 스프레드시트 파일을 열기 위한 비밀번호.                                                                                                                   |

### 요청 본문 매개변수

| 매개변수 이름 | 유형 | 설명               |
| -------------- | ---- | ------------------- |
| Spreadsheet    | 파일 | 스프레드시트 파일 업로드. |

### **응답**

```json
{
  "file": "이진 스트림 (매개변수에 따라 ZIP 아카이브 또는 워크북)"
}
```

**응답 상태 코드**

| 코드 | 의미            | 설명                                                                                     |
|------|-----------------|------------------------------------------------------------------------------------------|
| 200  | OK              | 분할 작업이 성공적으로 완료되었습니다. 응답에는 생성된 파일(ZIP 아카이브 또는 워크북)이 포함됩니다. |
| 400  | Bad Request     | 잘못된 URL 또는 요청 매개변수입니다.                                                     |
| 401  | Unauthorized    | 인증에 실패했거나 자격 증명이 제공되지 않았습니다.                                        |
| 404  | Not Found       | 소스 파일에 접근할 수 없습니다.                                                          |
| 413  | Payload Too Large | 요청 본문 크기가 허용된 크기를 초과했습니다.                                               |
| 500  | Internal Server Error | 스프레드시트에서 데이터를 가져오는 도중 오류가 발생했습니다.                              |

## SDK를 사용하여 SplitTable 사용하는 방법

### SplitTable 사양

[SplitTable API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/SplitTable)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells Cloud 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 Cloud API에 호출을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
# 안전한 연결을 위해 HTTPS 사용
curl -v "https://api.aspose.cloud/v4.0/cells/split/table?worksheet=Sheet1&tableName=MyTable&splitColumnName=Category&saveSplitColumn=true&splitRowNumber=1&toNewWorkbook=true&toMultipleFiles=true&outPath=output%2Ffolder&outStorageName=MyStorage&fontsLocation=%2Fcustom%2Ffonts&region=en-US&password=SecretPassword" \
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
  "file": "이진 스트림 (매개변수에 따라 ZIP 아카이브 또는 워크북)"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 가장 빠르게 향상시킬 수 있습니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 작업에 집중할 수 있도록 해줍니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 참조하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose Cells Cloud 웹 서비스를 호출하는 방법을 보여줍니다:
`[TBD]`
---