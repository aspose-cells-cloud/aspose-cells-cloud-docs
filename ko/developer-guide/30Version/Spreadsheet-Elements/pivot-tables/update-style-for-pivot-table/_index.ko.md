---
title: "피벗 테이블 스타일 업데이트"
second_title: "문서"
linktitle: "모두 서식 지정"
type: docs
url: /ko/pivot-tables/format-all/
aliases: [  /ko/update-style-for-pivot-table/ ]
keywords: "피벗 테이블, 스타일 업데이트, Aspose.Cells Cloud, REST API, Excel, 스프레드시트, API, 피벗 테이블 스타일, 모두 서식 지정"
description: "Aspose.Cells Cloud REST API를 사용하여 전체 피벗 테이블의 스타일을 업데이트하는 방법을 알아보세요. 요청 세부 정보, cURL 예제, 여러 프로그래밍 언어에 대한 SDK 스니펫을 포함합니다."
weight: 100
ArticleTitle: "피벗 테이블 스타일 업데이트 - Aspose.Cells Cloud API"
---

이 REST API는 피벗 테이블의 스타일을 업데이트합니다.

## PostPivotTableStyle API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/FormatAll
```

**필수 조건 / 인증**  
`Authorization` 헤더에 유효한 JWT 액세스 토큰을 제공해야 합니다(예: `Bearer <jwt token>`). 토큰이 지정된 워크북 및 워크시트에 접근할 수 있는 권한을 가지고 있는지 확인하십시오.

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 위해 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### **요청 매개변수**

| 매개변수 이름   | 유형      | 위치   | 설명                                                                                   |
| --------------- | --------- | ------ | -------------------------------------------------------------------------------------- |
| name            | string    | path   | 워크북 파일의 이름.                                                                    |
| sheetName       | string    | path   | 피벗 테이블이 포함된 워크시트.                                                         |
| pivotTableIndex | integer   | path   | 서식을 적용할 피벗 테이블의 0부터 시작하는 인덱스.                                     |
| style           | object    | body   | 적용할 서식을 정의하는 스타일 DTO.                                                     |
| needReCalculate | boolean   | query  | 서식 지정 후 피벗 테이블을 다시 계산하려면 **true**로 설정(기본값은 **false**).       |
| folder          | string    | query  | 워크북이 저장된 폴더.                                                                  |
| storageName     | string    | query  | 스토리지 서비스의 이름.                                                                |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableStyle)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예제는 cURL을 사용하여 클라우드 API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/FormatAll" \
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

**HTTP 상태 코드**

| 코드 | 의미                       | 설명                                           |
|------|----------------------------|------------------------------------------------|
| 200  | OK                         | 필터가 성공적으로 적용되었으며, 응답에 작업 세부 정보가 포함됩니다. |
| 400  | 잘못된 요청                 | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형). |
| 401  | 인증되지 않음               | 잘못되거나 누락된 JWT 토큰. |
| 413  | 요청 페이로드가 너무 큼     | 업로드된 파일이 크기 제한을 초과했습니다. |
| 500  | 내부 서버 오류              | 예기치 않은 서버 오류. |

{{< /tab >}}

{{< /tabs >}}

## 클라우드 SDK 패밀리

SDK를 사용하면 API에 가장 빠르게 개발할 수 있습니다. SDK는 저수준 세부 사항을 추상화하여 비즈니스 로직에 집중할 수 있도록 도와줍니다. Aspose.Cells Cloud SDK 전체 목록은 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 저장소</a>를 참조하십시오.

다음 코드 예제는 Go SDK를 사용하여 API를 호출하는 방법을 보여줍니다:

{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "0b2caae7acfa3e947b856c07b6e8633a" >}}

{{< /tab >}}

{{< /tabs >}}