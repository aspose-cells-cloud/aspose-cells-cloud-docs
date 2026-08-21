---
title: "Aspose.Cells Cloud – 테이블을 HTML로 변환"
description: "Aspose.Cells Cloud API를 사용하여 Excel 테이블을 빠르게 HTML로 변환하세요 – 보안이 강화되고 서식을 보존하며 통합이 간편합니다."
keywords: "Aspose.Cells, Excel을 HTML로, 테이블을 HTML로 변환, 클라우드 API, 스프레드시트 변환"
weight: 100
date: 2026-07-30
last_updated: 2026-07-30
version: "v4.0"
url: /ko/convert-table-to-html/
type: docs
---

**간단 요약** – 이 엔드포인트는 로컬 Excel 워크북을 읽어 지정된 **테이블**을 추출한 후 **HTML** 파일로 변환하고 결과를 다운로드 가능한 스트림으로 반환합니다. 중간으로 Aspose Cloud 저장소에 업로드할 필요가 없습니다.

## ConvertTableToHTML API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/html
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 강화되었으며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 이름                 | 위치       | 유형        | 필수 여부 | 설명                                                                      |
| -------------------- | ---------- | ----------- | --------- | ------------------------------------------------------------------------- |
| **Spreadsheet**      | Form‑Data  | `File`      | **예**     | 변환할 테이블이 포함된 Excel 워크북 파일입니다.                            |
| **worksheet**        | Query      | `String`    | **예**     | 테이블이 포함된 워크시트 이름입니다.                                        |
| **tableName**        | Query      | `String`    | **예**     | 변환할 테이블의 정확한 이름입니다.                                          |
| **outPath**          | Query      | `String`    | 아니요     | HTML 파일을 저장할 Aspose Cloud 저장소의 폴더 경로입니다(선택 사항).          |
| **outStorageName**   | Query      | `String`    | 아니요     | 출력 파일을 저장할 저장소 이름입니다(선택 사항).                            |
| **fontsLocation**    | Query      | `String`    | 아니요     | 변환에 필요한 사용자 정의 글꼴이 포함된 폴더 경로입니다.                     |
| **region**           | Query      | `String`    | 아니요     | 로케일 식별자(예: `en-US`, `fr-FR`). 숫자/날짜 서식에 영향을 줍니다.         |
| **password**         | Query      | `String`    | 아니요     | 보호된 워크북을 열기 위한 비밀번호입니다.                                   |
| **AutoRowsFit**      | Query      | `Boolean`   | 아니요     | 워크시트의 모든 행을 자동으로 조정할지 여부(`true`/`false`).                  |
| **AutoColumnsFit**   | Query      | `Boolean`   | 아니요     | 워크시트의 모든 열을 자동으로 조정할지 여부(`true`/`false`).                 |

### **응답**

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

| 코드 | 의미                  | 설명                                                              |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | 성공(OK)              | 필터가 성공적으로 적용됨; 응답에는 작업 세부 정보가 포함됨.        |
| 400  | 잘못된 요청(Bad Request) | 누락되었거나 잘못된 매개변수(예: 지원되지 않는 파일 유형)가 있음.   |
| 401  | 인증되지 않음(Unauthorized) | 잘못되었거나 누락된 JWT 토큰입니다.                               |
| 413  | 요청 페이로드가 너무 큼(Payload Too Large) | 업로드된 파일이 크기 제한을 초과함.                              |
| 500  | 내부 서버 오류(Internal Server Error) | 예기치 않은 서버 오류입니다.                                      |

## 테이블을 HTML로 변환하는 API를 언제 사용하나요?

- **동적 웹 콘텐츠** – 가격표, 일정, 제품 목록 등을 웹 페이지 또는 CMS에 직접 포함합니다.
- **이메일 템플릿** – 이메일 클라이언트에서 일관되게 렌더링되는 주문 요약 또는 보고서용 HTML 스니펫을 생성합니다.
- **대시보드 및 보고 도구** – 전체 워크북을 로드하거나 무거운 그리드 구성 요소를 사용하지 않고 실시간 스프레드시트 데이터를 표시합니다.
- **문서 미리 보기** – 특정 스프레드시트 섹션의 빠르고 서식을 보존한 미리 보기를 제공합니다.

## SDK를 사용하여 테이블을 HTML로 변환하는 API를 사용하는 방법은?

### Convert Table to HTML API 사양

[Convert Table to HTML API 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToHTML)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 제공하며, 웹 브라우저에서 직접 REST 요청을 수행할 수 있습니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API에 호출을 수행하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/html?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.html
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

SDK를 사용하면 저수준 세부 사항을 추상화하여 최소한의 코드로 스프레드시트 테이블 데이터를 CSV 파일로 변환할 수 있어 개발 속도가 가장 빠릅니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 참조하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 호출을 수행하는 방법을 보여줍니다.

---