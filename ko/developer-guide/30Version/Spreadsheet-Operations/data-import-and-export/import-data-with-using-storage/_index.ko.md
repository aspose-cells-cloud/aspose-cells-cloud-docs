---
title: "스토리지를 사용하여 데이터 가져오기"
second_title: "문서"
linktype: "docs"
url: /ko/import-data-with-using-storage/
aliases:
  - /import-data-into-excel-worksheet/
  - /import-data-into-worksheet/
  - /import-data-in-excel-worksheet/
  - /import-data/
  - /import/with-using-storage/
description: "스토리지를 사용하여 데이터 가져오기: Aspose.Cells Cloud API를 사용하여 다양한 스토리지 소스에서 Excel 워크시트로 데이터를 가져옵니다. JSON, CSV 등 다양한 형식을 HTTPS를 통해 지원합니다."
keywords: "Aspose.Cells Cloud, Excel, 데이터 가져오기, REST API, 클라우드 스토리지, JSON, CSV, PDF, Markdown, HTTPS"
weight: 10
ArticleTitle: "스토리지를 사용하여 데이터 가져오기 - Aspose.Cells Cloud API 문서"
---

이 REST API는 Excel 파일로 데이터를 가져옵니다.

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 적용되며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 파라미터

| 파라미터 이름 | 유형   | 위치 | 설명                                             |
| ------------- | ------ | ---- | ------------------------------------------------ |
| name          | string | path | Excel 파일 이름.                                |
| folder        | string | query | 파일이 위치한 스토리지 내 폴더 경로.            |
| storageName   | string | query | 스토리지 서비스 이름.                           |
| importData    | object | body | 가져올 데이터를 포함하는 JSON 객체.              |

**데이터 가져오기 옵션 파라미터**는 [레퍼런스 링크](/cells/import/#import-data-option-parameter)에서 설명합니다.

**필수 조건:** `Authorization` 헤더에 유효한 JWT 토큰을 제공해야 하며, 대상 워크북이 지정된 스토리지 위치에 이미 존재해야 합니다.

### 응답

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP 상태 코드**

| 코드 | 의미                  | 설명                                              |
|------|-----------------------|---------------------------------------------------|
| 200  | OK (성공)             | 필터가 성공적으로 적용되었으며, 응답에는 작업 세부 정보가 포함됩니다. |
| 400  | Bad Request (잘못된 요청) | 누락되거나 잘못된 파라미터(예: 지원되지 않는 파일 형식)가 있습니다. |
| 401  | Unauthorized (인증되지 않음) | 유효하지 않거나 누락된 JWT 토큰입니다.             |
| 413  | Payload Too Large (페이로드가 너무 큼) | 업로드된 파일이 크기 제한을 초과했습니다.         |
| 500  | Internal Server Error (내부 서버 오류) | 예기치 않은 서버 오류가 발생했습니다.             |

## SDK를 사용한 PostImportData API 사용 방법

### PostImportData API 사양

<a href="https://apireference.aspose.cloud/cells/#/Workbook/PostImportData" rel="noopener noreferrer">OpenAPI 사양</a>은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예제는 cURL을 사용하여 클라우드 API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/importdata" \
     -X POST \
     -d '{"Data":[1,2,4],"DestinationWorksheet":"Sheet1","FirstRow":1,"FirstColumn":2,"IsVertical":true,"IsInsert":true,"importDataType":"IntArray"}' \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 최적화할 수 있습니다. SDK는 저수준 세부 사항을 추상화하여 비즈니스 로직에 집중할 수 있게 해줍니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하십시오.

다음 코드 예제는 PHP SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다.