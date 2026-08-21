---
title: "원격 폴더의 일치하는 스프레드시트 병합"
description: "Aspose Cloud 저장소에 저장된 스프레드시트 파일을 단일 파일로 결합합니다. PDF, CSV, JSON, XLSX, ODS, XPS 등 30개 이상의 출력 형식을 지원합니다."
keywords: "Aspose.Cells, 스프레드시트 병합, 원격 폴더, API, PDF, CSV, JSON, XLSX, ODS, XPS"
weight: 100
type: docs
url: /ko/merge-spreadsheets-in-remote-folder/
---

원격 Aspose Cloud 저장소 폴더에 있는 여러 스프레드시트 파일을 단일 출력 파일로 결합합니다. 이 작업은 클라우드에서 완전히 실행되므로 소스 파일을 로컬로 다운로드할 필요가 없습니다. 30개 이상의 출력 형식(PDF, CSV, JSON, XLSX, ODS, XPS 등)을 지원합니다.

## MergeSpreadsheetsInRemoteFolder API

```http
PUT https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets
```

### **보안 및 인증**

Aspose.Cells Cloud API는 안전하며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수 <a id="request-parameters"></a>

| 이름                    | 유형    | 위치   | 필수 여부 | 설명                                                                                           |
| ----------------------- | ------- | ------ | --------- | ---------------------------------------------------------------------------------------------- |
| **folder**              | 문자열  | 쿼리   | **예**    | 소스 스프레드시트가 포함된 클라우드 저장소 폴더입니다.                                         |
| **fileMatchExpression** | 문자열  | 쿼리   | **예**    | 파일을 선택하기 위한 패턴(예: `*report*.xlsx`). 와일드카드 `*` 및 `?`를 지원합니다.             |
| **outFormat**           | 문자열  | 쿼리   | **예**    | 원하는 출력 형식(`PDF`, `CSV`, `JSON`, `XLSX`, `ODS`, `XPS`, 등).                              |
| **mergeInOneSheet**     | 불리언  | 쿼리   | **예**    | `true` — 모든 데이터를 단일 워크시트에 병합합니다. `false` — 각 소스 파일을 별도의 워크시트로 저장합니다. |
| **storageName**         | 문자열  | 쿼리   | 아니요    | 사용자 정의 저장소 이름; 생략 시 기본 저장소를 사용합니다.                                     |
| **outPath**             | 문자열  | 쿼리   | 아니요    | 병합된 파일을 저장할 대상 폴더입니다. 생략 시 소스 폴더에 파일이 저장됩니다.                    |
| **outStorageName**      | 문자열  | 쿼리   | 아니요    | 병합된 파일이 저장될 저장소 이름입니다.                                                        |
| **fontsLocation**       | 문자열  | 쿼리   | 아니요    | 사용자 정의 글꼴이 포함된 폴더 경로(PDF/이미지 내보내기에 필요)입니다.                         |
| **region**              | 문자열  | 쿼리   | 아니요    | 숫자, 날짜 및 통화 서식을 위한 로케일(예: `en-US`, `de-DE`)입니다.                             |
| **password**            | 문자열  | 쿼리   | 아니요    | 보호된 소스 스프레드시트를 열기 위한 암호입니다.                                                |

## 요청 예시(cURL) <a id="request-example"></a>

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets?folder=MyFolder&fileMatchExpression=*.xlsx&outFormat=PDF&mergeInOneSheet=true" \
     -H "Authorization: Bearer <access_token>" \
     -H "Accept: application/json"
```

### **응답**

```json
{
  "Name": "ResponseFile",
  "DataType": {
    "Identifier": "File",
    "Reference": "Stream"
  }
}
```

파일은 `FileUrl`에서 직접 다운로드하거나, `outPath`로 지정된 위치에 저장할 수 있습니다.

**성공 응답 세부 정보**

| 상태 코드    | 콘텐츠‑유형                | 설명                                    |
| ------------ | -------------------------- | ----------------------------------------- |
| 200 OK       | `application/octet-stream` | 병합된 워크북 파일의 바이너리 스트림입니다. |
| 202 Accepted | `application/json`         | `FileUrl`, `FileName` 등이 포함된 JSON입니다. |

**HTTP 상태 코드**

| 코드 | 의미                  | 설명                                                      |
| ---- | --------------------- | ---------------------------------------------------------- |
| 200  | OK                    | 필터가 성공적으로 적용되었으며, 응답에 작업 세부 정보가 포함됩니다. |
| 400  | 잘못된 요청           | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식)입니다.      |
| 401  | 인증되지 않음         | 잘못되거나 누락된 JWT 토큰입니다.                             |
| 413  | 페이로드가 너무 큼    | 업로드된 파일이 크기 제한을 초과했습니다.                      |
| 500  | 내부 서버 오류        | 예기치 않은 서버 오류입니다.                                  |

## SDK를 사용하여 스프레드시트 병합 API 사용하는 방법

### OpenAPI 사양

<a href="https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheetsInRemoteFolder" rel="noopener noreferrer">OpenAPI 사양</a>은 API에 대한 기계 가독성 설명을 제공하여 직접 REST 상호 작용을 가능하게 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예시는 cURL을 사용하여 클라우드 API에 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets?folder=MyFolder&fileMatchExpression=*.xlsx&outFormat=PDF&mergeInOneSheet=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/Book1.xlsx" \
  -F "Spreadsheet=@/path/to/Book2.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 인코딩)",
  "contentType": "MIME 유형",
  "fileDownloadName": "선택적 파일 이름"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 저수준 세부 정보를 추상화하여 짧은 코드로 스프레드시트 워크시트에 데이터를 빠르게 가져올 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 참조하세요.