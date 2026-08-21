---
title: "Excel 파일 내 텍스트 콘텐츠 검색 및 바꾸기"
second_title: "문서"
linktitle: "검색 및 바꾸기"
type: docs
url: /search-and-replace/
aliases: [/working-with-text/, /text/]
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크북 및 워크시트에서 텍스트를 검색하고 바꾸는 방법을 배워보세요. 요청 형식, .NET, Java, Python용 샘플 코드, 오류 처리를 포함합니다."
keywords: "Aspose.Cells Cloud, Excel, 검색 및 바꾸기, REST API, .NET, Java, Python"
weight: 20
ArticleTitle: "Aspose.Cells Cloud API를 사용하여 Excel 파일에서 텍스트 검색 및 바꾸기"
---

텍스트 작업은 Excel 파일에 대해 복잡한 처리 과정입니다. 이러한 복잡성에는 여러 요인이 관련되며, 처리 과정 중에 반드시 고려해야 합니다. Aspose.Cells Cloud는 다양한 스프레드시트 형식에서 텍스트를 검색하고 바꾸는 데 신뢰할 수 있는 방법을 제공합니다.

Excel 워크북에서 텍스트를 다루는 경우, 특정 문자열을 찾아 여러 시트에 걸쳐 업데이트해야 할 필요가 종종 있습니다. Aspose.Cells Cloud API는 지원되는 모든 스프레드시트 형식에서 작동하는 통합 **검색 및 바꾸기** 작업을 제공하여 이 작업을 간소화합니다.

## 개요

검색 및 바꾸기 기능을 사용하면 워크북 또는 특정 워크시트에서 특정 문자열을 찾아 새로운 값으로 대체할 수 있습니다. 이 작업은 **XLS, XLSX, XLSM, XLSB, ODS, CSV** 등 Aspose.Cells Cloud에서 지원하는 모든 형식에서 작동합니다. **검색 및 바꾸기** 기능을 활용하면 전체 워크북에서 데이터를 빠르게 정리하거나 반복되는 오타를 수정하거나 일관된 명명 규칙을 적용할 수 있습니다.

## 사전 요구 사항

- 유효한 **Client‑Id** 및 **Client‑Secret**이 있는 활성화된 Aspose.Cloud 계정
- OAuth 2.0 인증 흐름을 통해 얻은 액세스 토큰
- 대상 워크북은 Aspose Cloud 스토리지에 저장되어 있거나 공용 URL을 통해 접근 가능해야 함
- 필요한 SDK 설치 (예: Aspose.Cells‑Cloud for .NET, Java, Python)

## API 참조

**메서드:** `POST`  
**엔드포인트**

```
POST https://api.aspose.cloud/v3.0/cells/{fileName}/searchreplace
```

| 매개변수           | 유형      | 필수 여부 | 설명                                                                          |
| ------------------ | --------- | --------- | ----------------------------------------------------------------------------- |
| `fileName`         | string    | 예        | 워크북 이름 (확장자 포함)                                                        |
| `folder`           | string    | 아니요    | 클라우드 스토리지 폴더 경로                                                      |
| `storage`          | string    | 아니요    | 기본값이 아닌 경우 스토리지 이름                                                   |
| `sheetName`        | string    | 아니요    | 특정 워크시트 이름; 생략 시 전체 워크북에 작업 적용                                |
| `searchString`     | string    | 예        | 검색할 텍스트                                                                   |
| `replaceString`    | string    | 예        | 검색된 항목을 대체할 텍스트                                                      |
| `ignoreCase`       | boolean   | 아니요    | 대소문자 구분 없이 검색하려면 `true`로 설정                                      |
| `matchWholeCell`   | boolean   | 아니요    | 전체 셀 일치 항목만 대체하려면 `true`로 설정                                      |

**헤더**

- `Authorization: Bearer {access_token}`
- `Content-Type: application/json`

**요청 본문 (JSON)**

```json
{
  "searchString": "OldValue",
  "replaceString": "NewValue",
  "ignoreCase": false,
  "matchWholeCell": false,
  "sheetName": "Sheet1"
}
```

**성공 응답 (JSON)**

```json
{
  "status": "OK",
  "replacedCount": 3,
  "updatedFileUrl": "https://api.aspose.cloud/v3.0/storage/file/updatedWorkbook.xlsx"
}
```

## 지원되는 형식

| 형식                                  | 확장자                    |
| ------------------------------------- | ------------------------- |
| Excel 워크북                          | .xls, .xlsx, .xlsm, .xlsb |
| OpenDocument 스프레드시트             | .ods                      |
| CSV                                   | .csv                      |
| 기타 (Aspose.Cells에서 지원하는 경우) | —                         |

## 코드 샘플

아래는 세 가지 인기 있는 SDK에 대한 최소 예제입니다. `{clientId}`, `{clientSecret}` 등 모든 플레이스홀더를 실제 값으로 바꾸세요. 이 샘플은 프로그래밍 방식으로 **검색 및 바꾸기** 작업을 수행하는 방법을 보여줍니다.

## 오류 처리 및 예외 상황

| HTTP 코드 | 의미                                            | 권장 조치                                                                |
| --------- | ----------------------------------------------- | ------------------------------------------------------------------------ |
| 400       | 잘못된 요청 – 누락 또는 잘못된 매개변수          | 필수 필드 및 데이터 유형 확인                                            |
| 401       | 인증되지 않음 – 잘못 또는 만료된 토큰            | 액세스 토큰 새로 고침                                                    |
| 404       | 없음 – 워크북 또는 워크시트가 존재하지 않음      | 파일 이름, 폴더 경로, `sheetName` 확인                                  |
| 415       | 지원되지 않는 미디어 유형 – 잘못된 파일 형식     | 업로드된 파일이 지원되는 Excel 또는 CSV 형식인지 확인                   |
| 202       | 수락됨 – 처리를 위해 요청 수락됨                | 비동기 처리 사용 시 작업 상태 폴링                                       |
| 204       | 콘텐츠 없음 – 본문 없이 작업 성공                | 대체가 적용되었으며 추가 데이터는 반환되지 않음                          |
| 500       | 내부 서버 오류 – 예기치 않은 실패                 | 짧은 대기 후 재시도; 문제가 지속되면 Aspose 지원팀에 문의               |

**참고:**  
- 대규모 워크북은 요청 크기 제한을 초과할 수 있으므로, 먼저 파일을 클라우드 스토리지에 업로드하는 것을 고려하세요.  
- `ignoreCase`를 `true`로 설정하면 로케일에 따른 대소문자 매핑으로 인해 결과가 영향을 받을 수 있습니다.  
- `matchWholeCell`을 수식과 함께 사용하면 수식 텍스트 내 일부 일치 항목이 대체되지 않습니다.

## Excel 파일에서 검색 및 바꾸기

- [Excel 워크북에서 텍스트 항목 가져오기](/cells/workbook/get-text-items/)
- [Excel 워크시트에서 텍스트 항목 가져오기](/cells/worksheets/get-text-items/)
- [Excel 워크북에서 텍스트 찾기](/cells/workbook/find-text/)
- [Excel 워크시트에서 텍스트 찾기](/cells/worksheets/find-text/)
- [파일 업로드 없이 Excel 파일에서 텍스트 찾기](/cells/search/)
- [Excel 워크북에서 텍스트 바꾸기](/cells/workbook/replace-text/)
- [Excel 워크시트에서 텍스트 바꾸기](/cells/worksheets/replace-text/)
- [파일 업로드 없이 Excel 파일에서 텍스트 바꾸기](/cells/replace/)

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Aspose.Cells Cloud API를 사용하여 Excel 파일에서 텍스트 검색 및 바꾸기",
  "description": "Aspose.Cells Cloud의 검색 및 바꾸기 엔드포인트에 대한 문서로, 요청 형식, 매개변수, 예제, 오류 처리를 포함합니다.",
  "url": "https://docs.aspose.cloud/cells/search-and-replace/",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "publisher": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2026-07-30",
  "keywords": "Aspose.Cells Cloud, Excel, 검색 및 바꾸기, API, REST"
}
</script>