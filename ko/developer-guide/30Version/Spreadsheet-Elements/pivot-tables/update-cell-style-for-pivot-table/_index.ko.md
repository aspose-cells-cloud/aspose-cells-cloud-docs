---
title: "피벗 테이블 셀 스타일 업데이트"
second_title: "문서"
linktype: "형식"
type: docs
url: /ko/pivot-tables/format/
aliases: [  /ko/update-cell-style-for-pivot-table/ ]
keywords: "Aspose.Cells Cloud, 피벗 테이블 스타일, 셀 스타일 업데이트 API, REST API, Excel API, 스프레드시트 서식, 클라우드 SDK, 셀 스타일, 피벗 테이블"
description: "Aspose.Cells Cloud REST API를 사용하여 피벗 테이블의 특정 셀 스타일을 업데이트하는 방법을 알아보세요. 엔드포인트, 매개변수, 인증, cURL 예제, Go SDK 코드 스니펫, SEO 최적화 가이드 포함."
weight: 90
ArticleTitle: "피벗 테이블 셀 스타일 업데이트 - Aspose.Cells Cloud API 문서"
---

이 REST API는 피벗 테이블 내 셀의 **스타일**을 업데이트합니다.

**필수 조건 / 인증**  
이 엔드포인트를 호출하려면 유효한 Aspose Cloud JWT 액세스 토큰이 필요합니다. [인증 가이드](/authentication/)에 설명된 OAuth 2.0 흐름을 통해 토큰을 획득하세요. 요청 헤더에 토큰을 포함하세요:

```http
Authorization: Bearer <jwt token>
```

JWT 토큰은 모든 Aspose.Cells Cloud API 호출에 필요합니다.

## PostPivotTableCellStyle API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/Format
```

### **보안 및 인증**

Aspose.Cells Cloud API는 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요하며 보안이 강화되어 있습니다.

### **요청 매개변수**

| 매개변수 이름   | 유형    | 위치 | 설명                                                                                          |
| --------------- | ------- | ---- | ----------------------------------------------------------------------------------------------- |
| name            | string  | path | 문서 이름(필수).                                                                                |
| sheetName       | string  | path | 워크시트 이름(필수).                                                                            |
| pivotTableIndex | integer | path | 피벗 테이블 인덱스(필수).                                                                       |
| column          | integer | query | 서식을 지정할 셀의 0부터 시작하는 열 인덱스(필수).                                              |
| row             | integer | query | 서식을 지정할 셀의 0부터 시작하는 행 인덱스(필수).                                              |
| style           | object  | body | 새 셀 스타일을 정의하는 Style DTO(Data-Transfer Object).                                        |
| needReCalculate | boolean | query | 스타일 적용 후 피벗 테이블을 다시 계산할지 여부를 나타냅니다. 기본값은 **false**입니다.         |
| folder          | string  | query | 문서가 저장된 폴더(선택 사항).                                                                   |
| storageName     | string  | query | 스토리지 이름(선택 사항).                                                                        |
| Method          | string  | N/A  | 요청에 사용된 HTTP 메서드(**POST**).                                                             |

<a href="https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableCellStyle" target="_blank" rel="noopener noreferrer">OpenAPI 사양</a>은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

**cURL** 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 클라우드 API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/Format?column=1&row=1" \
  -X POST \
  -d '{"Font":{"Name":"Arial","Size":10}}' \
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

**응답**  
성공 시 서비스는 HTTP 200 상태를 반환하며 빈 본문으로 스타일이 적용되었음을 나타냅니다. 오류 발생 시 오류 코드와 메시지가 포함된 JSON 페이로드가 반환됩니다.

| HTTP 상태 코드 | 설명                                                                 |
|--------------|----------------------------------------------------------------------|
| 200          | 스타일이 성공적으로 적용됨.                                          |
| 400          | 잘못된 요청 – 예: 잘못된 열/행 인덱스.                               |
| 401          | 인증되지 않음 – 누락되거나 잘못된 JWT 토큰.                          |
| 404          | 찾을 수 없음 – 지정된 문서, 워크시트 또는 피벗 테이블이 존재하지 않음. |
| 500          | 내부 서버 오류 – 예기치 않은 조건.                                   |

성공 시 응답 본문은 비어 있습니다.

자세한 내용은 **Get Pivot Table** API 문서를 참조하세요.

## 클라우드 SDK 패밀리

SDK를 사용하면 개발 속도가 가장 빩니다. SDK는 저수준 세부 사항을 추상화하여 비즈니스 로직에 집중할 수 있도록 합니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예제는 **Go** SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "3236805d26482f06f4656b14f2d00d79" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "피벗 테이블 셀 스타일 업데이트",
  "description": "REST API를 사용하여 Aspose.Cells Cloud 피벗 테이블의 특정 셀 스타일을 업데이트하는 가이드.",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2026-07-30",
  "keywords": "Aspose.Cells Cloud, 피벗 테이블, 셀 스타일, REST API, Go SDK",
  "url": "https://docs.aspose.cloud/cells/pivot-tables/format/",
  "publisher": {
    "@type": "Organization",
    "name": "Aspose"
  }
}
</script>
---