---
title: "Aspose.Cells Cloud 데이터 가져오기 API – Excel 스프레드시트에 CSV, JSON, XML 데이터를 자동으로 가져오는 클라우드 솔루션"
second_title: "문서"
ArticleTitle: "다중 소스 데이터 통합 Excel 플랫폼 – Aspose.Cells Cloud 자동 데이터 가져오기 및 변환 API"
linktype: "스프레드시트에 데이터 가져오기"
type: docs
url: /ko/import-data-into-spreadsheet/
keywords: "Aspose Cells, 데이터 가져오기 API, CSV를 Excel로, JSON을 Excel로, XML을 Excel로, 클라우드 스프레드시트, REST API"
description: "Aspose.Cells Cloud REST API를 사용해 CSV, JSON 또는 XML 데이터를 Excel 스프레드시트에 가져오세요. 요청 형식, 매개변수, 샘플 SDK 코드, 오류 처리 방법을 알아보세요."
weight: 100
---

## 핵심 기능

### 다중 포맷 데이터 지원

- **<a href="https://docs.fileformat.com/spreadsheet/csv/" rel="noopener noreferrer">CSV</a> 데이터 가져오기**: 다양한 구분자를 지원하며 인코딩을 자동으로 감지합니다.
- **<a href="https://docs.fileformat.com/web/json/" rel="noopener noreferrer">JSON</a> 데이터 처리**: 복잡한 JSON 구조를 Excel 테이블로 평면화합니다.
- **<a href="https://docs.fileformat.com/web/xml/" rel="noopener noreferrer">XML</a> 파일 변환**: 노드 데이터를 Excel 행 및 열 구조에 매핑합니다.

## **스프레드시트에 데이터 가져오기 API 설명**

### 웹 API

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data
```

### **보안 및 인증**

Aspose.Cells Cloud API는 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름     | 유형   | 위치             | 설명                                                              |
| ------------------ | ------ | ---------------- | ------------------------------------------------------------------------ |
| datafile           | File   | FormData         | 가져올 데이터 파일(CSV, JSON 또는 XML).                        |
| spreadsheet        | File   | FormData         | 가져온 데이터를 수신할 대상 워크북.                 |
| worksheet          | string | Query            | 데이터가 삽입될 워크시트 이름.                         |
| startCell          | string | Query            | 가져오기 시작 위치를 나타내는 좌상단 셀(예: `A1`). |
| insert             | bool   | Query            | `true`이면 행을 삽입하고, `false`이면 기존 데이터를 덮어씁니다.               |
| convertNumericData | bool   | Query            | `true`이면 숫자로 변환 가능한 문자열을 가져오는 동안 숫자로 변환합니다.              |
| splitter           | string | Query            | 단일 문자 CSV 구분자(기본값은 `,`).                         |
| outPath            | string | Query (선택 사항) | 업데이트된 워크북이 저장될 폴더 경로.                   |
| outStorageName     | string | Query (선택 사항) | 출력 파일을 저장할 저장소 위치 이름.                        |
| fontsLocation      | string | Query (선택 사항) | 필요한 경우 사용자 정의 폰트 폴더 경로.                              |
| region             | string | Query (선택 사항) | 스프레드시트 지역 설정(예: `en-US`).                        |
| password           | string | Query (선택 사항) | 보호된 워크북을 열기 위한 비밀번호.                               |

### 응답

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**HTTP 상태 코드**

| 코드 | 의미               | 설명                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK (성공)                    | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보 포함. |
| 400  | Bad Request (잘못된 요청)           | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식).      |
| 401  | Unauthorized (인증되지 않음)          | 잘못되거나 누락된 JWT 토큰.                                     |
| 413  | Payload Too Large (페이로드 너무 큼)     | 업로드된 파일이 크기 제한을 초과함.                                 |
| 500  | Internal Server Error (내부 서버 오류) | 예기치 않은 서버 오류.                                          |

## 이 API를 사용해야 하는 이유

- **효율적인 데이터 로딩** – 중간 파일을 생성하지 않고 대용량 데이터셋을 워크북으로 한 번에 가져올 수 있습니다.
- **광범위한 SDK 지원** – .NET, Java, PHP, Ruby, Node.js, Python, Go, Perl용 클라이언트 라이브러리를 제공하여 통합을 간편하게 합니다.
- **메모리 내 처리** – 임시 저장소 요구 사항을 줄이기 위해 메모리에서 변환을 수행합니다.

## SDK를 사용하여 스프레드시트에 데이터 가져오기 API 사용 방법

**참고 / 제한 사항:** 이 API는 한 번의 가져오기당 최대 1,000,000개의 행을 지원합니다. 기본 CSV 구분자는 쉼표(,)만 허용되며, 다른 단일 문자 구분자는 `splitter` 매개변수를 통해 지정할 수 있습니다. 대용량 XML 파일은 처리 시간을 늘릴 수 있습니다.

데이터 내보내기 또는 워크북 형식 변환과 관련된 작업은 **데이터 내보내기** 및 **워크북 변환** 문서를 참조하세요.

### 스프레드시트에 데이터 가져오기 API 사양

<a href="https://reference.aspose.cloud/cells/#/DataProcessingController/ImportDataIntoSpreadsheet" rel="noopener noreferrer">스프레드시트에 데이터 가져오기 API 사양</a>은 공개적으로 접근 가능한 프로그래밍 인터페이스를 제공하여 웹 브라우저에서 직접 REST 요청을 수행할 수 있습니다.
cURL 명령줄 도구를 사용해 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예시는 cURL을 사용해 클라우드 API에 호출을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/import/data?worksheet=Sheet1&startCell=A1&insert=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "datafile=@/path/to/data.csv" \
  -F "spreadsheet=@/path/to/workbook.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 인코딩됨)",
  "contentType": "MIME 유형",
  "fileDownloadName": "선택적 파일 이름"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 저수준 세부 정보를 추상화하여 스프레드시트 워크시트에 데이터를 간단한 코드로 빠르게 가져올 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.