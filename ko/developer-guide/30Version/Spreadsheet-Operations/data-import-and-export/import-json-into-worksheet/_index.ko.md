---
title: "JSON 데이터를 Excel로 가져오기"
second_title: "문서"
linktitle: "JSON 가져오기"
type: docs
url: /ko/import-json-data-into-excel/
aliases: [  /ko/import/json/ ]
keywords: "Aspose.Cells Cloud, JSON 가져오기, Excel API, REST JSON 가져오기, SDK 예제"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트에 JSON 데이터를 가져오는 방법을 알아보세요. 엔드포인트 세부 정보, 요청/응답 예제, .NET, Java, Python용 SDK 코드를 포함합니다."
weight: 40
---

이 REST API는 **JSON 데이터를 Excel 워크시트에 가져옵니다**.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/importjson
```
### **보안 및 인증**

Aspose.Cells Cloud API는 보안이며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **요청 매개변수**

| 매개변수 이름         | 위치         | 유형   | 설명                                                                                          |
| --------------------- | ------------ | ------ | ---------------------------------------------------------------------------------------------------- |
| name                  | Path         | string | 워크북 파일의 이름입니다.                                                                       |
| importJsonRequest     | HTTP 본문    | class  | JSON 가져오기 세부 정보를 포함하는 요청 페이로드입니다.                                               |
| password              | 쿼리 문자열  | string | 워크북을 열기 위한 비밀번호(보호된 경우).                                                    |
| folder                | 쿼리 문자열  | string | 원본 워크북이 포함된 폴더입니다.                                                      |
| storageName           | 쿼리 문자열  | string | 워크북이 저장된 저장소의 이름입니다.                                                  |
| outPath               | 쿼리 문자열  | string | 가져오기 후 출력 파일의 경로입니다. 생략 시 업데이트된 워크북이 응답으로 반환됩니다. |
| outStorageName        | 쿼리 문자열  | string | 출력 파일의 저장소 이름입니다.                                                                    |
| checkExcelRestriction | 쿼리 문자열  | string | Excel 고유 제한 사항을 적용할지 여부를 나타내는 플래그(true/false)입니다.                         |

### **요청 본문 예시**

```json
{
  "JsonFileSource": {
    "FilePath": "string"
  },
  "ImportPosition": {
    "SheetName": "string",
    "RowIndex": 0,
    "ColumnIndex": 0
  },
  "JsonContent": "string"
}
```

### 응답

성공적인 요청은 다음과 유사한 JSON 페이로드와 함께 **HTTP 200**을 반환합니다:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

가능한 상태 코드:

| 코드 | 의미                                 |
| ---- | --------------------------------------- |
| 200  | 가져오기 성공                        |
| 400  | 잘못된 요청 – 누락 또는 유효하지 않은 데이터   |
| 401  | 인증되지 않음 – 유효하지 않거나 누락된 토큰 |
| 500  | 내부 서버 오류                   |


## SDK를 사용하여 PostWorkbookImportJson API 사용하는 방법

### PostWorkbookImportJson API 사양

[OpenAPI 사양](https://reference.aspose.cloud/cells/#/DataProcessing/PostWorkbookImportJson)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

### Aspose.Cells Cloud SDK 사용

SDK를 사용하는 것이 개발 속도를 높이는 가장 효율적인 방법입니다. SDK는 저수준 세부 사항을 처리하므로 비즈니스 로직에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하십시오.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

---